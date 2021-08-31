State management is the process by which you maintain state and page information over multiple requests for the same or different pages.

**Client Side State Management:**<br/>
To maintain the state of values on the client’s machine, we use the client-side state management techniques.<br/>
**1.View State**:<br/>
The view state property provides an object for retaining values between multiple requests for the same page. it can be defined as ViewState[“Viewstate_variable_name”]<br/>
**2.Control State:**<br/>
The data that is associated with the server controls is called as control state. You can persist information about a control that is not part of the view state.<br/>
**3.Hidden fields:**<br/>
Like view state, hidden fields store data in an HTML form without displaying it in the user's browser. The data is available only when the form is processed.<br/>
**4.Cookies:**<br/>
Cookies store a value in the user's browser that the browser sends with every page request to the same server. Cookies are the best way to store state data that must be available for multiple Web pages on a web site.
**a.Session cookies:**<br/>
It is one which is created by default by the web server on the client’s machine during a session. This cookie uses a session id.<br/>
**b.Persistent cookies:**<br/>
When we specify the expiration time for a session cookie, it becomes a persistent cookie. This cookie expires as the time outs.<br/>
**5.Query Strings:**<br/>
In query strings values are stored at the end of the URL. These values are visible to the user through his or her browser’s address bar. Query strings are not secure. <br/>


**Server Side State Management:**<br/>
To maintain the state of values on the server’s machine, we use the server-side state management techniques<br/>
**1.Application State:**<br/>
Application object is used to store information at application level rather than user level. All pages of your application can access the Application object. Application variables are stored on a web server.<br/>
syntax: Application [“ApplicationState_VariableName”]<br/>
**2.Session State:**<br/>
The session enables the persistence of values across all the pages for a given session.Session state variables are stored on the webserver.Session state variables are cleared when the user session times out. The default time for a session to exist is 20 minutes. This can be changed to another value in the web.config file occurring in the solution explorer.
syntax: Session[“SessionState_VariableName”]


View state:<br/>
Storage: client<br/>
Size:as per when you consider that ViewState is not only sent out to the client but also gets sent back to the server with each request.<br/>
Security:Not very secure<br/>
handling:ViewState is enabled on four levels: machine, application, page, and control. <br/>
Timeout Period :Single WebForm<br/>
performance:It helps preserve page and control values between complete round trips for client requests. <br/>

Session State:<br/>
Storage: server<br/>
Size:as It depends of course on the size of the tables, storing a few kB is usually acceptable.<br/>
Security:secured	<br/>
Timeout Period :session object is limited to the TimeOut setting, default is 20 min.<br/>
performance:can be increased by adding a <sessionState timeout="" /> node under <system.web> in the web.config file, with the timeout value in minutes.<br/>

Application State:<br/>
Storage: server<br/>
Size:an be any size-it will only be stored once.<br/>
Security:secured	<br/>
Timeout Period :Untill the application close.<br/>




