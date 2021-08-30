State management is the process by which you maintain state and page information over multiple requests for the same or different pages.

**Client Side State Management:**
To maintain the state of values on the client’s machine, we use the client-side state management techniques.
1.View State:
The view state property provides an object for retaining values between multiple requests for the same page. it can be defined as ViewState[“Viewstate_variable_name”]
2.Control State:
The data that is associated with the server controls is called as control state. You can persist information about a control that is not part of the view state.
3.Hidden fields:
Like view state, hidden fields store data in an HTML form without displaying it in the user's browser. The data is available only when the form is processed.
4.Cookies:
Cookies store a value in the user's browser that the browser sends with every page request to the same server. Cookies are the best way to store state data that must be available for multiple Web pages on a web site.
a.Session cookies:
It is one which is created by default by the web server on the client’s machine during a session. This cookie uses a session id.
b.Persistent cookies:
When we specify the expiration time for a session cookie, it becomes a persistent cookie. This cookie expires as the time outs.
5.Query Strings:
In query strings values are stored at the end of the URL. These values are visible to the user through his or her browser’s address bar. Query strings are not secure. 


Server Side State Management:
To maintain the state of values on the server’s machine, we use the server-side state management techniques
1.Application State:
Application object is used to store information at application level rather than user level. All pages of your application can access the Application object. Application variables are stored on a web server.
syntax: Application [“ApplicationState_VariableName”]
2.Session State:
The session enables the persistence of values across all the pages for a given session.Session state variables are stored on the webserver.Session state variables are cleared when the user session times out. The default time for a session to exist is 20 minutes. This can be changed to another value in the web.config file occurring in the solution explorer.
syntax: Session[“SessionState_VariableName”]