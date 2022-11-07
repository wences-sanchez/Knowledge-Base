title:: Java EE 7 Essentials (highlights)
deck:: [[Other-Books::Java EE 7 Essentials]]
author:: [[Arun Gupta]]
full-title:: "Java EE 7 Essentials"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/51jiR4AW%2BAL._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Java EE application components never interact directly with other Java EE application components. They use the protocols and methods of the container #flashcard
		  id:: be6406ba-c76d-4f78-a248-128a31fb2568
		- ([Location 222](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=222))
	- -
	- -
		- POJOs (plain old Java objects), #flashcard
		  id:: 26394583-0932-4c15-8313-3e82ca8ee611
		- tags:: [[pink]] [[rosa]]
		- ([Location 251](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=251))
	- -
	- -
		- A servlet is a web component hosted in a servlet container and generates dynamic content. The web clients interact with a servlet using a request/response pattern. #flashcard
		  id:: 09dac69f-4f9c-46a3-9c76-54e104c1345a
		- tags:: [[pink]] [[rosa]]
		- ([Location 416](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=416))
	- -
	- -
		- A servlet is defined using the @WebServlet annotation on a POJO, and must extend the javax.servlet.http.HttpServlet class. #flashcard
		  id:: b5140532-0587-4e6d-978d-86319a6c3119
		- tags:: [[naranja]]
		- ([Location 420](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=420))
	- -
	- -
		- Crear un servlet a partir de un POJO #flashcard
		  id:: 41b22671-8ca1-49ca-b1e4-63b8536eba7d
			- A servlet is defined using the @WebServlet annotation on a POJO, and must extend the javax.servlet.http.HttpServlet class.
		- ([Location 420](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=420))
	- -
	- -
		- The HttpServlet interface has one doXXX method to handle each of HTTP GET, POST, PUT, DELETE, HEAD, OPTIONS, and TRACE requests. #flashcard
		  id:: 22c54bce-a53a-48f1-8e53-4061bb359cd1
		- ([Location 450](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=450))
	- -
	- -
		- The HttpServlet interface has one doXXX method to handle each of HTTP GET, POST, PUT, DELETE, HEAD, OPTIONS, and TRACE requests. #flashcard
		  id:: e1da1446-b67f-4c42-a9d0-71d9d392c0cc
		- ([Location 450](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=450))
	- -
	- -
		- (PrintWriter out = response.getWriter()) #flashcard
		  id:: e7bea88f-5f80-4a28-9b8f-6dc7bbe8f23e
		- tags:: [[orange]] [[naranja]]
		- ([Location 479](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=479))
	- -
	- -
		- Request parameters may be passed in GET and POST requests. In a GET request, these parameters are passed in the query string as name/value pairs. #flashcard
		  id:: ad00014b-a060-4db8-a16e-fa139ea3e169
		- ([Location 495](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=495))
	- -
	- -
		- Probar con variables en la dirección web en el browser (doGET) #flashcard
		  id:: af3a31cf-0d8c-4461-a9bf-8ef4ae7350d2
			- In a GET request, these parameters are passed in the query string as name/value pairs.
		- ([Location 495](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=495))
	- -
	- -
		- . . ./account?tx=10 #flashcard
		  id:: 203abc07-3ffd-49d7-a9b7-6dfaca0e3214
		- tags:: [[orange]] [[naranja]]
		- ([Location 498](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=498))
	- -
	- -
		- In both GET and POST requests, these parameters can be obtained from HttpServletRequest: #flashcard
		  id:: 44e69bd5-3f87-45b9-9077-564f8ce6b562
		- ([Location 501](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=501))
	- -
	- -
		- A servlet is packaged in a web application in a .war file. #flashcard
		  id:: d458650a-f543-4492-b903-24bb2d65c8df
		- ([Location 552](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=552))
	- -
	- -
		- config.setHttpOnly(true); #flashcard
		  id:: 36490c18-8219-45e7-9cda-57ce5a69f917
		- tags:: [[orange]] [[naranja]]
		- ([Location 572](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=572))
	- -
	- -
		- HttpSession session = request.getSession(true); #flashcard
		  id:: a65f70b7-f6f9-4290-bb0d-65efb630cdc1
		- tags:: [[orange]] [[naranja]]
		- ([Location 583](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=583))
	- -
	- -
		- HttpSession session = request.getSession(true); #flashcard
		  id:: b72d79d8-4e0e-4bc1-a5a8-30e21d4428fe
		- tags:: [[naranja]]
		- ([Location 583](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=583))
	- -
	- -
		- request.getRequestDispatcher("bank").forward(request, response); #flashcard
		  id:: 9bde0275-a273-41fe-b579-dc6888f0aae9
		- tags:: [[orange]] [[naranja]]
		- ([Location 597](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=597))
	- -
	- -
		- request.getRequestDispatcher("bank").forward(request, response); #flashcard
		  id:: e2f02929-5bb1-4481-96bc-03b7f54dceb2
		- tags:: [[naranja]]
		- ([Location 597](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=597))
	- -
	- -
		- in this case, the original request object is not available to the redirected URL. The redirect may also be marginally slower because it entails two requests from the client, whereas forward is performed within the container: #flashcard
		  id:: 7bda894f-f8a0-4507-8b53-8fee2338d16b
		- ([Location 606](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=606))
	- -
	- -
		- The asynchronous behavior needs to be explicitly enabled on a servlet. You achieve this by adding the asyncSupported attribute on @WebServlet: @WebServlet(urlPatterns="/async", asyncSupported=true) #flashcard
		  id:: bb9bdd7a-978e-4675-ab31-3eafc65d15d0
		- tags:: [[blue]] [[azul]]
		- ([Location 831](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=831))
	- -
	- -
		- the <deny-uncovered-http-methods> element ensures that HTTP GET is called with the required security credentials, #flashcard
		  id:: 4daadd2d-f0ee-4e64-9aec-3be72d8afbdd
		- ([Location 1105](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1105))
	- -
	- -
		- @RolesAllowed, @DenyAll, @PermitAll, and @TransportProtected provide an alternative set of annotations to specify security roles on a particular resource or a method of the resource: #flashcard
		  id:: 26bec1c8-54ce-4b2d-b9e7-3208ca60128c
		- ([Location 1108](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1108))
	- -
	- -
		- JSF allows you to: Create a web page with a set of reusable UI components following the Model-View-Controller (MVC) #flashcard
		  id:: 22342251-8a3d-4fd3-ac5a-1c60a644bcad
		- ([Location 1292](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1292))
	- -
	- -
		- JavaServer Faces is a server-side user interface (UI) framework for Java-based web applications. #flashcard
		  id:: b4ac2816-8b8e-47db-950c-3b3126a63882
		- ([Location 1292](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1292))
	- -
	- -
		- Facelets is the view declaration language (aka view handler) for JSF. #flashcard
		  id:: 4fe979ef-98ce-43eb-a1d0-c5c95ca13cae
		- ([Location 1304](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1304))
	- -
	- -
		- Table 3-1. Standard tag libraries supported by Facelets #flashcard
		  id:: 8cf64274-1b77-4caf-81ef-574320892df1
		- tags:: [[blue]] [[azul]]
		- ([Location 1324](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1324))
	- -
	- -
		- Usar EL para mostrar una variable de una clase ejemplo. #flashcard
		  id:: 7760a0c9-7e29-4350-ba56-c555b31ee802
			- Facelets provides Expression Language (EL) integration. This allows two-way data binding between the backing beans and the UI:
		- ([Location 1339](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1339))
	- -
	- -
		- Para usar EL tenemos que estar en una página de tipo .jsp, .jsf, por supuesto. O decirle a Eclipse que tenga la página en cuenta. #flashcard
		  id:: bb049892-6ee4-4eea-8b43-9613e6235a73
			- web pages built with XHTML have a .xhtml extension.
		- ([Location 1339](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1339))
	- -
	- -
		- Para las EL, hay que poner el nombre de la clase en minúscula. #flashcard
		  id:: 4d24d9fd-e240-47b1-b218-aef4e8b3e862
			- @Named @RequestScoped
		- tags:: [[pink]] [[rosa]]
		- ([Location 1347](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1347))
	- -
	- -
		- It’s important to add @Named on a CDI bean to enable its injection in an EL. #flashcard
		  id:: 6a9b3ce7-9f8c-4455-94e9-7b41e1116bc4
		- tags:: [[blue]] [[azul]]
		- ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1351))
	- -
	- -
		- <h:dataTable value="#{customerSessionBean.customerNames}" var="c">   <h:column>#{c.value}</h:column> </h:dataTable> #flashcard
		  id:: 726b2cf2-f815-4674-8642-7a929fd4cc5c
		- tags:: [[orange]] [[naranja]]
		- ([Location 1366](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1366))
	- -
	- -
		- Crear una página plantilla JSF. #flashcard
		  id:: 6ed48bf8-401d-4f22-8c1b-70439eeada66
			- A template page looks like:
		- ([Location 1397](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1397))
	- -
	- -
		- Crear una página cliente JSF #flashcard
		  id:: ae48b635-253e-4312-a57b-a0efeb7953ec
			- A template client page looks like:
		- ([Location 1427](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1427))
	- -
	- -
		- There is a ui:define element with a name matching the ui:insert element in the template, so the contents are replaced. #flashcard
		  id:: 3c0f9678-d0c5-4230-acf6-a58440cf8cbc
		- ([Location 1444](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1444))
	- -
	- -
		- <a href="#{resource['header.jpg']}">click here</a> #flashcard
		  id:: f19fb87a-70ad-475c-8128-88d028d5a49f
		- tags:: [[orange]] [[naranja]]
		- ([Location 1452](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1452))
	- -
	- -
		- JSF defines a composite component as a component that consists of one or more JSF components defined in a Facelets markup file. #flashcard
		  id:: b9811bc4-4d91-4c93-b997-86d8720943da
		- ([Location 1474](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1474))
	- -
	- -
		- allows you to create a reusable component from an arbitrary region of a page. #flashcard
		  id:: c02066a7-7e97-4369-bb12-9d09c058daca
		- ([Location 1475](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1475))
	- -
	- -
		- The composite component is defined in the defining page and used in the using page. #flashcard
		  id:: 94bca0ca-ba19-4226-af2c-74d60d7df884
		- ([Location 1476](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1476))
	- -
	- -
		- instead of repeating this code everywhere, it is beneficial to convert this fragment into a composite component. #flashcard
		  id:: 1be1ef4f-bbad-42c2-8a15-688385a55787
		- ([Location 1521](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1521))
	- -
	- -
		- convention-over-configuration, #flashcard
		  id:: 155a2e31-9364-4153-80bd-a7b27d18b153
		- tags:: [[blue]] [[azul]]
		- ([Location 1523](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1523))
	- -
	- -
		- The defining page can then pass the values: #flashcard
		  id:: 31962026-9116-4ce9-9bdc-32d6bd61ab11
		- ([Location 1553](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1553))
	- -
	- -
		- h:inputText is now using #{cc.attrs.xxx} instead of #{user.xxx}. #{cc.attrs} is a default EL expression that is available for composite component authors and provides access to attributes of the current composite component. In this case, #{cc.attrs} has name and password defined as attributes. #flashcard
		  id:: 5fd0f8db-0205-4c59-9685-58b336c8961a
		- ([Location 1603](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1603))
	- -
	- -
		- life-cycle phases: #flashcard
		  id:: 619d3254-1b90-49f9-a4c3-d40f285a2213
		- ([Location 1632](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1632))
	- -
	- -
		- <f:viewParam name="name" value="#{user.name}"/> #flashcard
		  id:: a3b481b5-6f2e-4a11-920e-be6ea9478811
		- tags:: [[orange]] [[naranja]]
		- ([Location 1810](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1810))
	- -
	- -
		- <h:link value="Login" outcome="login"/> #flashcard
		  id:: 5d796b08-5ac1-4d5c-8088-8d5a960b720c
		- tags:: [[orange]] [[naranja]]
		- ([Location 1848](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1848))
	- -
	- -
		- <f:param name="name" value="#{user.name}"/> #flashcard
		  id:: e3696e84-b227-44ee-9224-dab7e12f47fa
		- tags:: [[orange]] [[naranja]]
		- ([Location 1858](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1858))
	- -
	- -
		- JSF provides several built-in validators such as f:validateLength and f:validateDoubleRange. #flashcard
		  id:: b788e3b7-f61b-421f-b892-82f77aaa433c
		- ([Location 1925](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1925))
	- -
	- -
		- <h:commandButton action="login" value="Login"/> #flashcard
		  id:: 820a8453-1b2e-4d43-b4bb-75ea0f4c5724
		- tags:: [[orange]] [[naranja]]
		- ([Location 2048](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2048))
	- -
	- -
		- Faces Flow #flashcard
		  id:: c0415c8d-654d-43ce-8bdc-1721b31f2297
		- ([Location 2065](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2065))
	- -
	- -
		- REST is an architectural style of services that utilizes web standards. Web services designed using REST are called RESTful web services, #flashcard
		  id:: b1233d12-f194-4b96-842c-ede385ad6259
		- tags:: [[blue]] [[azul]]
		- ([Location 2916](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2916))
	- -
	- -
		- Use standard HTTP methods to interact with the resource: #flashcard
		  id:: b5a90798-779f-4a9f-8aee-a2962286d1b1
		- ([Location 2921](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2921))
	- -
	- -
		- Communication between the client and the endpoint is stateless. #flashcard
		  id:: 57bb5737-5472-41a4-bb9e-3cb97f185a43
		- ([Location 2923](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2923))
	- -
	- -
		- Java API for RESTful web services (JAX-RS) defines a standard annotation-driven API that helps developers build a RESTful web service in Java and invoke it. #flashcard
		  id:: 829603c6-3564-462b-b9f2-74310bec8385
		- tags:: [[blue]] [[azul]]
		- ([Location 2924](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2924))
	- -
	- -
		- @Path("orders") public class OrderResource { #flashcard
		  id:: bfafe3c3-5bd5-45b4-85db-f776c1419b42
		- tags:: [[orange]] [[naranja]]
		- ([Location 2930](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2930))
	- -
	- -
		- @GET   public List<Order> getAll() { #flashcard
		  id:: 6b833fdf-4e3c-421b-952c-d834641bed6e
		- tags:: [[orange]] [[naranja]]
		- ([Location 2933](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2933))
	- -
	- -
		- @GET   @Path("{oid}")   public Order getOrder(@PathParam("oid")int id) { #flashcard
		  id:: 29ceb6eb-bdb1-446f-b3ef-bc25ccda4899
		- tags:: [[orange]] [[naranja]]
		- ([Location 2936](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2936))
	- -
	- -
		- @XmlRootElement public class Order { #flashcard
		  id:: 824e748f-52f0-47f8-b393-6931928c4bbc
		- tags:: [[orange]] [[naranja]]
		- ([Location 2942](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2942))
	- -
	- -
		- The @Path annotation on the getOrder resource method marks it as a subresource that is accessible at orders/{oid}. #flashcard
		  id:: a1ecd7e9-026f-4ec7-9551-40320a7246f1
		- ([Location 2952](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2952))
	- -
	- -
		- The curly braces around oid identify it as a template parameter and bind its value at runtime to the id parameter of the getOrder resource method. #flashcard
		  id:: 2e2cbf5e-7f47-4670-b2a5-091846a0ffe3
		- ([Location 2954](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2954))
	- -
	- -
		- The @PathParam can also be used to bind template parameters to a resource class field. #flashcard
		  id:: 86f58021-1502-4082-ae52-7d47a721da81
		- ([Location 2955](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2955))
	- -
	- -
		- Typically, a RESTful resource is bundled in a .war file along with other classes and resources. #flashcard
		  id:: e5f73579-ba39-4d9a-99fd-4657cd6ab756
		- ([Location 2957](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2957))
	- -
	- -
		- The name attribute in the HTML form and the value of the @FormParam annotation are exactly the same to ensure the binding. #flashcard
		  id:: de640365-f1a6-4f8b-9d32-9a806459d445
		- ([Location 3097](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=3097))
	- -
	- -
		- The HTTP HEAD method is identical to GET except that no response body is returned. #flashcard
		  id:: b36d223f-3cd7-4afb-831e-698aa50aa9cb
		- ([Location 3140](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=3140))
	- -