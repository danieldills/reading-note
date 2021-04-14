## APIs

### Web API design
[source](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

Most modern web applications expose APIs that clients can use to interact with the application. A well-designed web API should aim to support:

- Platform independence. Any client should be able to call the API, regardless of how the API is implemented internally. This requires using standard protocols, and having a mechanism whereby the client and the web service can agree on the format of the data to exchange.

- Service evolution. The web API should be able to evolve and add functionality independently from client applications. As the API evolves, existing client applications should continue to function without modification. All functionality should be discoverable so that client applications can fully use it.

### Introduction to REST
[source](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

REST stands for Representational State Transfer as and architectural approach to desining web services. 

- A primary advantage of REST over HTTP is that it uses open standards, and does not bind the implementation of the API or the client applications to any specific implementation. For example, a REST web service could be written in ASP.NET, and client applications can use any language or toolset that can generate HTTP requests and parse HTTP responses.

1. Organize the API around resources

  - A resource doesn't have to be based on a single physical data item. For example, an order resource might be implemented internally as several tables in a relational database, but presented to the client as a single entity. Avoid creating APIs that simply mirror the internal structure of a database. The purpose of REST is to model entities and the operations that an application can perform on those entities. A client should not be exposed to the internal implementation.

2. Define operations in terms of HTTP methods

The HTTP protocol defines a number of methods that assign semantic meaning to a request. The common HTTP methods used by most RESTful web APIs are:

- GET retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.

- POST creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.

- PUT either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.

- PATCH performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.

- DELETE removes the resource at the specified URI.

[<== Back](README.md)
