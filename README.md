# JSP-Servlets
Introduction to servlets
How does servlets work?
Client -server interaction on static pages: Let’s say client sends request to a server asking for a web page . In the context of static, the server already has that page, and it sends response.
But let’s say we are asking for a page which will be built at runtime. Server has to build that page. That request goes to a help application also called web container in this we have servlets.
Servlet is  a java file which can take the request from the client on the internet and process that request and provide you response in the form of html page. 
It goes to web container like tomcat, glassfish…
When request goes to tomcat , since we don’t have the page client is asking , that request goes to servlet. Inside your container we have a file named Deployment Descriptor in which we mention for which request which servlet has to called (everything is mapped) The file name is web.xml.
Web.xml has two tags servlet tag for class and servlet-mapping tag for URL.
Server-takes the request, processes the information and sends the response. That response will be in html. The dynamic page goes to the client in the form of a response object.
Instead of web.xml files we can also use annotations (@WebServlet(“/abc.html”))
HTTPServletRequest (request object)& Response(response object)
Lets say client wants to add two numbers(not only values any form of data) we have to pass those values how do we do that Request object is the answer its an object to hold the value. When you send the Response it can be text, image, video, html etc.
In the webservices world we return json value. With the help of the response object we can send what kind of data we need to send to the client. In the service method we have to give request and response object to the tomcat server.
How to call servlet from a servlet?
RequestDispatcher is a special feature to call a servlet from a servlet.
Client(Browser) doesn’t know from which servlet the response is getting from (this is because same objects are passed between servlets).

 

RequestDispatcher
SendRedirect- URLRewriting
Drawback can’t pass multiple values or pass it in multiple serv
HttpSession- Cookie
Session Management. 

Practical implementation of ServletConfig and ServletContext: 

They both are interface. ServletConfig and ServletContext both are used to get initial value of servlet or an application. The values are stored in key value pair. context-param and context-name tags are used to store the values. In ServletContext values are shared by all the servlets Whereas in ServletConfig values each servlet can have independent values.

JSP: JAVA SERVER PAGE

Declaration <%! %>
Directive <%@ %>
Scriptlet <% %>
Expression <%= %>


JSP  Directive: Directives are elements that relay messages to the JSP container and affect how it compiles the JSP page. The directives themselves do not appear in the XML output.
There are three directives: include, page, and taglib.

@page
<%@ page attribute=”value” attribute=”value” … %>  
Some of the attributes are: 
language="scripting language"		java
extends="className"
import="importList"
session="true| false"
autoFlush="true | false"
contentType="ctinfo"
errorPage="error_url"
isErrorPage="true| false"
info="information"
isELIgnored="true|false"
isThreadSafe="true| false"


Model-View-Controller (MVC) Architecture Using Servlets and JSP:
The MVC (Model-View-Controller) architecture is a design pattern used to separate an application into three main logical components: the model, the view, and the controller. Each of these components handles specific aspects of the application.
Model
•	Role: Represents the application's data and the business logic.
•	Responsibility: Manages data and enforces rules, maintains data integrity, and performs data operations.
•	Example: Java Beans, POJOs (Plain Old Java Objects) that hold data and business logic.
View
•	Role: Represents the presentation layer.
•	Responsibility: Displays data to the user and sends user commands to the controller.
•	Example: JSP (JavaServer Pages) that create the user interface
Controller
•	Role: Manages the flow of the application.
•	Responsibility: Acts as an intermediary between Model and View, processes user input, and updates the model and the view accordingly.
•	Example: Servlets that handle user requests, process input, and determine the response view.
Model: Represents the data and the business logic of the application.
View: Represents the presentation layer (JSP files) where data is displayed to the user.
Controller: Manages the flow between the Model and the View (Servlets).

 
