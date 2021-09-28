# API Deployment

[source](https://djangostars.com/blog/configuring-django-settings-best-practices/)

Managing Django Settings: Issues

- Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.

- Sensitive data. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

- Sharing settings between team members. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.

- Django settings are a Python code. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.

settings_local.py

This is the oldest method. I used it when I was configuring a Django project on a production server for the first time. I saw a lot of people use it back in the day, and I still see it now.

The basic idea of this method is to extend all environment-specific settings in the settings_local.py file, which is ignored by VCS. 

Pros:

- Secrets not in VCS.

Cons:

- settings_local.py is not in VCS, so you can lose some of your Django environment settings.
- The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
- You need to have settings_local.example (in VCS) to share the default configurations for developers.

Separate settings file for each environment

This is an extension of the previous approach. It allows you to keep all configurations in VCS and to share default settings between developers.

Pros:

- All environments are in VCS.
- It’s easy to share settings between developers.
Cons:

- You need to find a way to handle secret passwords and tokens.
- “Inheritance” of settings can be hard to trace and maintain.
