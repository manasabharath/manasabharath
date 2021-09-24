## Service lifetimes
* Singleton: this lifetime creates one instance of the service. The service instance may be created at the registration time by using the Add() method, as you saw in the example above. Alternatively, the service instance can be created the first time it is requested by using the AddSingleton() method.
* Transient: by using this lifetime, your service will be created each time it will be requested. This means, for example, that a service injected in the constructor of a class will last as long as that class instance exists. To create a service with the transient lifetime, you have to use the AddTransient() method.
* Scoped: the scoped lifetime allows you to create an instance of a service for each client request. This is particularly useful in the ASP.NET context since it allows you to share the same service instance for the duration of an HTTP request processing. To enable the scoped lifetime, you need to use the AddScoped() method.

![image](https://user-images.githubusercontent.com/86051093/134641454-fba0d3a4-144f-479d-81bc-5f147dc40c68.png)
