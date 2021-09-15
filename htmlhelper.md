## HTML Helpers in ASP.NET MVC
It is a method that is used to render html content in a view. Html helpers are implemented as extension methods.

**There are three types of built-in HTML helpers offered by ASP.NET.**
* Standard HTML Helper 
* Strongly-Typed HTML Helper 
* Templated HTML Helper 

## Standard HTML Helper
The HTML helpers that are mainly used to render HTML elements like text boxes, checkboxes, Radio Buttons, and Dropdown lists, etc. are called Standard HTML helpers. 

**List of Standard HTML Helpers** :<br/>
@Html.ActionLink() - Used to create link on html page<br/>
@Html.TextBox() - Used to create text box<br/>
@Html.CheckBox() - Used to create check box<br/>
@Html.RadioButton() - Used to create Radio Button<br/>
@Html.BeginFrom() - Used to start a form<br/>
@Html.EndFrom() - Used to end a form<br/>
@Html.DropDownList() - Used to create drop down list<br/>
@Html.Hidden() - Used to create hidden fields<br/>
@Html.label() - Used for creating HTML label is on the browser<br/>
@Html.TextArea() - The TextArea Method renders textarea element on browser<br/>
@Html.Password() - This method is responsible for creating password input field on browser<br/>
@Html.ListBox() - The ListBox helper method creates html ListBox with scrollbar on browser<br/>

## Strongly-Typed HTML Helper 
The Strongly-Typed HTML helper takes a lambda as a parameter that tells the helper, which element of the model to be utilized in the typed view. The Strongly typed views are used for rendering specific sorts of model objects, rather than using the overall View-Data structure.

**List of strongly-Typed HTML Helper **
@Html.HiddenFor()<br/>
@Html.LabelFor()<br/>
@Html.TextBoxFor()<br/>
@Html.RadioButtonFor()<br/>
@Html.DropDownListFor()<br/>
@Html.CheckBoxFor()<br/>
@Html.TextAreaFor()<br/>
@Html.PasswordFor()<br/>
@Html.ListBoxFor()<br/>

##  Templated HTML Helper
The templated HTML Helper is used for data display and input. It generates HTML automatically as per model property and it can generate HTML for a complete model with a single tag. These are divided into two categories 
* Display Template
* Editor Template

**List of Templated HTML Helpers**
Display

@Html.Display()
@Html.DisplayFor()
@Html.DisplayName()
@Html.DisplayNameFor()
@Html.DisplayText()
@Html.DisplayTextFor()
@Html.DisplayModelFor()

Edit / Input

@Html.Editor()
@Html.EditorFor()
@Html.EditorForModel()
