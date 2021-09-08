**Both View Data and view Bag are used to pass data from a controller to a view and Both it is does not provide compile time error checking**<br/>
## ViewData
* ViewData is derived from the ViewDataDictionary class and is basically a Dictionary object
* Data is stored as Object in ViewData.
* ViewData is used for passing value from Controller to View.
* ViewData is available only for Current Request. It will be destroyed on redirection.

## ViewBag
* ViewBag is a Wrapper built around ViewData.
* ViewBag is a dynamic property and it makes use of the C# 4.0 dynamic features.
* ViewBag is used for passing value from Controller to View.
* While retrieving, there is no need for Type Casting data.

## **Routing in MVC**<br/>
In MVC, routing is a process of mapping the browser request to the controller action and return response back. Each MVC application has default routing for the default HomeController. We can set custom routing for newly created controller.<br/><br/>
**Every MVC application must configure (register) at least one route configured by the MVC framework by default. You can register a route in RouteConfig class, which is in RouteConfig.cs under App_Start folder.**<br/>
![image](https://user-images.githubusercontent.com/86051093/132459480-6f72b1e8-d02f-415c-8ae1-4bb6c98d921e.png)

* If the URL doesn't contain anything after the domain name, then the default controller and action method will handle the request.
* For example, http://localhost:1234 would be handled by the HomeController and the Index() method as configured in the default parameter.

## Route Constraints
* We can also apply restrictions on the value of the parameter by configuring route constraints. 
* For example, the following route applies a limitation on the id parameter that the id's value must be numeric.<br/><br/>
   routes.MapRoute(<br/>
        name: "Student",<br/>
        url: "student/{id}/{name}/{standardId}",<br/>
        defaults: new { controller = "Student", action = "Index", id = UrlParameter.Optional, name = UrlParameter.Optional, standardId = UrlParameter.Optional },<br/>
        constraints: new { id = @"\d+" }<br/>
    );<br/>

