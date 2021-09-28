## Data Binding
Data binding deals with how to bind your data from component to HTML DOM elements (Templates).

__One-way data binding__<br/>
One-way data binding is a one-way interaction between component and its template. If you perform any changes in your component, then it will reflect the HTML elements. It supports the following types −

String interpolation
In general, String interpolation is the process of formatting or manipulating strings. In Angular, Interpolation is used to display data from component to view (DOM). It is denoted by the expression of {{ }} and also known as mustache syntax.


__Event binding__<br/>
Events are actions like mouse click, double click, hover or any keyboard and mouse actions. If a user interacts with an application and performs some actions, then event will be raised. It is denoted by either parenthesis () or on-. We have different ways to bind an event to DOM element.

__Property binding__<br/>
Property binding is a one-way mechanism that lets you set the property of a view element. It involves updating the value of a property in the component and binding it to an element in the view template. Property binding uses the [] syntax for data binding. 

__Two-way data binding__<br/>
is a two-way interaction, data flows in both ways (from component to views and views to component). Simple example is ngModel. If you do any changes in your property (or model) then, it reflects in your view and vice versa. It is the combination of property and event binding.
