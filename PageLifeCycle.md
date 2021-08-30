__Page Life Cycle__

![image](https://user-images.githubusercontent.com/86051093/131300673-bfdd7373-a6b9-4a5c-a782-faffbe229495.png)


**PreInit :**	This event is raised after the start stage is complete and before the initialization stage.<br/><br/>
**Init    :**	This event occurs after all controls have been initialized. We can use this event to read or initialize control properties.<br/><br/>
**InitComplete :**	This event occurs at the end of the page's initialization stage. We can use this event to make changes to view state that we want to make sure are persisted after the next postback.<br/><br/>
__PreLoad__	:This event is occurs before the post back data is loaded in the controls.<br/><br/>
__Load__ :This event is raised for the page first time and then recursively for all child controls.<br/><br/>
__Control events__:This event is used to handle specific control events such as Button control' Click event.<br/><br/>
__LoadComplete__:This event occurs at the end of the event-handling stage. We can use this event for tasks that require all other controls on the page be loaded.<br/><br/>
__PreRender__:This event occurs after the page object has created all controls that are required in order to render the page.<br/><br/>
__PreRenderComplete__:This event occurs after each data bound control whose DataSourceID property is set calls its DataBind method.<br/><br/>
__SaveStateComplete__:	It is raised after view state and control state have been saved for the page and for all controls.<br/><br/>
__Render__:This is not an event; instead, at this stage of processing, the Page object calls this method on each control.<br/><br/>
__Unload__:This event raised for each control and then for the page.
