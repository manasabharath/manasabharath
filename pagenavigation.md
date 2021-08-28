__Page navigation is the process of moving from one page to another page in your website. There are many ways to navigate from one page to another in ASP.NET.__

1.Client-side navigation<br/>
2.Cross-page posting<br/>
3.Client-side browser redirect<br/>
4.Server-side transfer<br/>

__1.Client-side navigation__:
control used to navigate user to anther page or on the same page.
The main property  of hyperlink control is NavigateUrl. The NavigateUrl property of hyperlink control store the address of destination page.<br/>
<asp:HyperLink ID="HyperLink1" runat="server" NavigateUrl="~/Welcome.aspx"><br/>
         Goto Welcome Page<br/>
</asp:HyperLink>

__2.Cross-page posting:__
It is used to send values from the source page to the target page. It posts current page information to the target page and that information is available in the target page.By default, when you click a button,the webform posts to itself. if you want to post to another webform on a button click,set the postback url of the button,to the page that you want to post to.<br/>
protected void Page_Load(object sender, EventArgs e)<br/>
    {<br/>
        if (Page.PreviousPage != null)<br/>
        {<br/>
            TextBox MyTextBox = (TextBox)Page.PreviousPage.FindControl("TextBox1");<br/>
            if (MyTextBox != null)<br/>
            {<br/>
                Label1.Text = MyTextBox.Text;<br/>
            }
        }
    }
    
__3.Client-side browser redirect:__
Response.Redirect() will send you to a new page, update the address bar and add it to the Browser History. On your browser you can click back.It redirects the request to some plain HTML pages on our server or to some other web server.It causes additional roundtrips to the server on each request..<br/>
protected void Button1_Click(object sender, EventArgs e)<br/>
    {<br/>
        Response.Redirect("TutorialRide.aspx");<br/>
    }
    
__4.Server-side transfer:__
User can redirect programmatically to a target page on the server by calling the Transfer method. The source and target pages must be in the same application.it Enables you to read values and public properties from source page and It does not update the browser information with the target page data. User cannot use refresh or back buttons in an application.<br/>
protected void Button1_Click(object sender, EventArgs e)<br/>
    {<br/>
        Server.Transfer("TutorialRide.aspx");<br/>
    }
