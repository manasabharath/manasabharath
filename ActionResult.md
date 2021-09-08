## Action Results in ASP.NET MVC
All the public methods inside a Controller which respond to the URL are known as Action Methods. When creating an Action Method, we must follow the below rules.
* The action method must be public.
* It cannot be overloaded
* It cannot be a static method
* ActionResult is the base class of all the result types that an action method returns.

## Types of Action Results:
* ViewResult – Represents HTML and markup.
* PartialViewResult – Represents HTML and markup.
* EmptyResult – Represents no result.
* RedirectResult – Represents a redirection to a new URL.
* RedirectToActionResult – It is returning the result to a specified controller and action method
* JsonResult – Represents a JavaScript Object Notation result that can be used in an AJAX application.
* JavaScriptResult – Represents a JavaScript script.
* ContentResult – Represents a text result.
* FileContentResult – Represents a downloadable file (with the binary content).
* FilePathResult – Represents a downloadable file (with a path).
* FileStreamResult – Represents a downloadable file (with a file stream).
