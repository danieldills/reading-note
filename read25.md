# Permissions & Postgresql

## Permissions

[source](https://www.django-rest-framework.org/api-guide/permissions/)

Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the ```request.user``` and ```request.auth``` properties to determine if the incoming request should be permitted.

Permissions are used to grant or deny access for different classes of users to different parts of the API.

The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the ```IsAuthenticated``` class in REST framework.

A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the ```IsAuthenticatedOrReadOnly``` class in REST framework.

## How permissions are determined

Permissions in REST framework are always defined as a list of permission classes.

Before running the main body of the view each permission in the list is checked. If any permission check fails an ```exceptions.PermissionDenied``` or ```exceptions.NotAuthenticated``` exception will be raised, and the main body of the view will not run.

When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

- The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does not use ```WWW-Authenticate``` headers. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does use ```WWW-Authenticate``` headers. — An HTTP 401 Unauthorized response, with an appropriate ```WWW-Authenticate``` header will be returned.

## Object level permissions

REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

Object level permissions are run by REST framework's generic views when ```.get_object()``` is called. As with view level permissions, an ```exceptions.PermissionDenied``` exception will be raised if the user is not allowed to act on the given object.

If you're writing your own views and want to enforce object level permissions, or if you override the ```get_object``` method on a generic view, then you'll need to explicitly call the ```.check_object_permissions(request, obj)``` method on the view at the point at which you've retrieved the object.

This will either raise a ```PermissionDenied``` or ```NotAuthenticated``` exception, or simply return if the view has the appropriate permissions.

For example:

```py
def get_object(self):
    obj = get_object_or_404(self.get_queryset(), pk=self.kwargs["pk"])
    self.check_object_permissions(self.request, obj)
    return obj
```

Note: With the exception of ```DjangoObjectPermissions```, the provided permission classes in ```rest_framework.permissions``` do not implement the methods necessary to check object permissions.

If you wish to use the provided permission classes in order to check object permissions, you must subclass them and implement the ```has_object_permission()``` method described in the Custom permissions section (below).

## Setting the permission policy

The default permission policy may be set globally, using the ```DEFAULT_PERMISSION_CLASSES``` setting. For example.

```py
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```

If not specified, this setting defaults to allowing unrestricted access:

```py
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```

You can also set the authentication policy on a per-view, or per-viewset basis, using the APIView class-based views.

```py
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response
from rest_framework.views import APIView

class ExampleView(APIView):
    permission_classes = [IsAuthenticated]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```

Or, if you're using the @api_view decorator with function based views.

```py
from rest_framework.decorators import api_view, permission_classes
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response

@api_view(['GET'])
@permission_classes([IsAuthenticated])
def example_view(request, format=None):
    content = {
        'status': 'request was permitted'
    }
    return Response(content)
```

Note: when you set new permission classes via the class attribute or decorators you're telling the view to ignore the default list set in the settings.py file.

Provided they inherit from ```rest_framework.permissions.BasePermission```, permissions can be composed using standard Python bitwise operators. For example, ```IsAuthenticatedOrReadOnly``` could be written:

```py
from rest_framework.permissions import BasePermission, IsAuthenticated, SAFE_METHODS
from rest_framework.response import Response
from rest_framework.views import APIView

class ReadOnly(BasePermission):
    def has_permission(self, request, view):
        return request.method in SAFE_METHODS

class ExampleView(APIView):
    permission_classes = [IsAuthenticated|ReadOnly]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```
