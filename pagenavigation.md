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
It is similar to hyperlink but the target page is invoked using HTTP POST command. It is used to send values from the source page to the target page. It posts current page information to the target page. The post information is available in the target page.Redirects to any page, not just pages in the same Web application.<br/>
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
The Page.Response object has redirect method. The Response.Redirect method redirects a request to a new URL. It instructs the browser to initiate a request for another Web page. The browser issues new request to the target server in the form of HTTP GET request. The redirection can be achieved by changing the client script or the server code. In the client script, add form.submit method for redirecting the data.In the server code. User can redirect by adding Redirect method. It is equivalent to the hyperlink control in the application.<br/>
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
