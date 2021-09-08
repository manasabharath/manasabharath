**Both View Data and view Bag are used to pass data from a controller to a view and Both View data and viewbag does not provide compile time error checking**<br/>
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
**The RouteConfig.cs file is used to set routing for the application. Initially it contains the following code.**<br/>
![image](https://user-images.githubusercontent.com/86051093/132459480-6f72b1e8-d02f-415c-8ae1-4bb6c98d921e.png)


