__AJAX__ stands for Asynchronous JavaScript and XML.<br/>
It is a new technique for creating better,faster and more interactive web applicatios with the help of xml,html,css,javascript.<br/>


**Advantages:**<br/>
* Reduces the traffic travels between the client and the server. <br/>
* Update a web page without reloading the page.<br/>
* Better interactivity and responsiveness.<br/>

**Disadvantages:**<br/>
* Search engines like Google would not be able to index an AJAX application. <br/>
* It is totally built-in JavaScript code. If any user disables JS in the browser, it won't work.<br/>
* Security is less in AJAX applications as all the files are downloaded at client side.<br/><br/>

**Script Manager:**<br/>
The script manager control is a key control in the asp.net ajax framework.<br/>
* Required in all asp.net ajax enabled pages.<br/>
* manages all framework and custom scripts used by a page.<br/>
* Generates Client-side Web Service Proxy objects.<br/>
* Coordinates Asynchronous operations.<br/>
**Syntax:**<br/>
<asp:ScriptManager ID="ScriptManager1" runat="server">
</asp:ScriptManager><br/><br/>

**Update Panel Control**:<br/>
* The UpdatePanel control is a container control and derives from the Control class.<br/>
* Ajax enables portion for the page.<br/>
* can handle actions triggered by html elements.<br/>
* Supports nested UpdatePanel Controls.<br/>
* Provides template named ContentTemplate.<br/>

Example:<br/>
 <asp:UpdatePanel ID="UpdatePanel1" runat="server">:<br/>
                < ContentTemplate>:<br/>
              <asp:Timer ID="Timer1" runat="server" Interval="1000" OnTick="Timer1_Tick"></asp:Timer>:<br/>
              <asp:Label ID="Label1" runat="server" ></asp:Label>  :<br/>
            </ ContentTemplate>:<br/>
            </asp:UpdatePanel>:<br/>
