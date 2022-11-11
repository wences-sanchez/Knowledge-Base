# Java EE 7 Essentials

deck:: [[Other-Books::Java EE 7 Essentials]]\
author:: [[Arun Gupta]]\
full-title:: "Java EE 7 Essentials"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/51jiR4AW%2BAL._SL200_.jpg)

## Highlights
- 

Java EE application components never interact directly with other Java EE application components. They use the protocols and methods of the container #flashcard 


    ([Location 222](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=222))
-
- 

POJOs (plain old Java objects), #flashcard  #pink #rosa 


    ([Location 251](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=251))
-
- 

A servlet is a web component hosted in a servlet container and generates dynamic content. The web clients interact with a servlet using a request/response pattern. #flashcard  #pink #rosa 


    ([Location 416](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=416))
-
- 

A servlet is defined using the @WebServlet annotation on a POJO, and must extend the javax.servlet.http.HttpServlet class. #flashcard  #naranja 


    ([Location 420](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=420))
-
- 
 Crear un servlet a partir de un POJO #flashcard 
    A servlet is defined using the @WebServlet annotation on a POJO, and must extend the javax.servlet.http.HttpServlet class.

    ([Location 420](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=420))
-
- 

The HttpServlet interface has one doXXX method to handle each of HTTP GET, POST, PUT, DELETE, HEAD, OPTIONS, and TRACE requests. #flashcard 


    ([Location 450](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=450))
-
- 

The HttpServlet interface has one doXXX method to handle each of HTTP GET, POST, PUT, DELETE, HEAD, OPTIONS, and TRACE requests. #flashcard 


    ([Location 450](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=450))
-
- 

(PrintWriter out = response.getWriter()) #flashcard  #orange #naranja 


    ([Location 479](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=479))
-
- 

Request parameters may be passed in GET and POST requests. In a GET request, these parameters are passed in the query string as name/value pairs. #flashcard 


    ([Location 495](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=495))
-
- 
 Probar con variables en la dirección web en el browser (doGET) #flashcard 
    In a GET request, these parameters are passed in the query string as name/value pairs.

    ([Location 495](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=495))
-
- 

. . ./account?tx=10 #flashcard  #orange #naranja 


    ([Location 498](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=498))
-
- 

In both GET and POST requests, these parameters can be obtained from HttpServletRequest: #flashcard 


    ([Location 501](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=501))
-
- 

A servlet is packaged in a web application in a .war file. #flashcard 


    ([Location 552](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=552))
-
- 

config.setHttpOnly(true); #flashcard  #orange #naranja 


    ([Location 572](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=572))
-
- 

HttpSession session = request.getSession(true); #flashcard  #orange #naranja 


    ([Location 583](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=583))
-
- 

HttpSession session = request.getSession(true); #flashcard  #naranja 


    ([Location 583](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=583))
-
- 

request.getRequestDispatcher("bank").forward(request, response); #flashcard  #orange #naranja 


    ([Location 597](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=597))
-
- 

request.getRequestDispatcher("bank").forward(request, response); #flashcard  #naranja 


    ([Location 597](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=597))
-
- 

in this case, the original request object is not available to the redirected URL. The redirect may also be marginally slower because it entails two requests from the client, whereas forward is performed within the container: #flashcard 


    ([Location 606](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=606))
-
- 

The asynchronous behavior needs to be explicitly enabled on a servlet. You achieve this by adding the asyncSupported attribute on @WebServlet: @WebServlet(urlPatterns="/async", asyncSupported=true) #flashcard  #blue #azul 


    ([Location 831](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=831))
-
- 

the <deny-uncovered-http-methods> element ensures that HTTP GET is called with the required security credentials, #flashcard 


    ([Location 1105](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1105))
-
- 

@RolesAllowed, @DenyAll, @PermitAll, and @TransportProtected provide an alternative set of annotations to specify security roles on a particular resource or a method of the resource: #flashcard 


    ([Location 1108](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1108))
-
- 

JSF allows you to: Create a web page with a set of reusable UI components following the Model-View-Controller (MVC) #flashcard 


    ([Location 1292](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1292))
-
- 

JavaServer Faces is a server-side user interface (UI) framework for Java-based web applications. #flashcard 


    ([Location 1292](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1292))
-
- 

Facelets is the view declaration language (aka view handler) for JSF. #flashcard 


    ([Location 1304](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1304))
-
- 

Table 3-1. Standard tag libraries supported by Facelets #flashcard  #blue #azul 


    ([Location 1324](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1324))
-
- 
 Usar EL para mostrar una variable de una clase ejemplo. #flashcard 
    Facelets provides Expression Language (EL) integration. This allows two-way data binding between the backing beans and the UI:

    ([Location 1339](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1339))
-
- 
 Para usar EL tenemos que estar en una página de tipo .jsp, .jsf, por supuesto. O decirle a Eclipse que tenga la página en cuenta. #flashcard 
    web pages built with XHTML have a .xhtml extension.

    ([Location 1339](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1339))
-
- 
 Para las EL, hay que poner el nombre de la clase en minúscula. #flashcard  #pink #rosa 
    @Named @RequestScoped

    ([Location 1347](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1347))
-
- 

It’s important to add @Named on a CDI bean to enable its injection in an EL. #flashcard  #blue #azul 


    ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1351))
-
- 

<h:dataTable value="#{customerSessionBean.customerNames}" var="c">   <h:column>#{c.value}</h:column> </h:dataTable> #flashcard  #orange #naranja 


    ([Location 1366](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1366))
-
- 
 Crear una página plantilla JSF. #flashcard 
    A template page looks like:

    ([Location 1397](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1397))
-
- 
 Crear una página cliente JSF #flashcard 
    A template client page looks like:

    ([Location 1427](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1427))
-
- 

There is a ui:define element with a name matching the ui:insert element in the template, so the contents are replaced. #flashcard 


    ([Location 1444](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1444))
-
- 

<a href="#{resource['header.jpg']}">click here</a> #flashcard  #orange #naranja 


    ([Location 1452](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1452))
-
- 

JSF defines a composite component as a component that consists of one or more JSF components defined in a Facelets markup file. #flashcard 


    ([Location 1474](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1474))
-
- 

allows you to create a reusable component from an arbitrary region of a page. #flashcard 


    ([Location 1475](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1475))
-
- 

The composite component is defined in the defining page and used in the using page. #flashcard 


    ([Location 1476](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1476))
-
- 

instead of repeating this code everywhere, it is beneficial to convert this fragment into a composite component. #flashcard 


    ([Location 1521](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1521))
-
- 

convention-over-configuration, #flashcard  #blue #azul 


    ([Location 1523](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1523))
-
- 

The defining page can then pass the values: #flashcard 


    ([Location 1553](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1553))
-
- 

h:inputText is now using #{cc.attrs.xxx} instead of #{user.xxx}. #{cc.attrs} is a default EL expression that is available for composite component authors and provides access to attributes of the current composite component. In this case, #{cc.attrs} has name and password defined as attributes. #flashcard 


    ([Location 1603](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1603))
-
- 

life-cycle phases: #flashcard 


    ([Location 1632](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1632))
-
- 

<f:viewParam name="name" value="#{user.name}"/> #flashcard  #orange #naranja 


    ([Location 1810](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1810))
-
- 

<h:link value="Login" outcome="login"/> #flashcard  #orange #naranja 


    ([Location 1848](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1848))
-
- 

<f:param name="name" value="#{user.name}"/> #flashcard  #orange #naranja 


    ([Location 1858](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1858))
-
- 

JSF provides several built-in validators such as f:validateLength and f:validateDoubleRange. #flashcard 


    ([Location 1925](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=1925))
-
- 

<h:commandButton action="login" value="Login"/> #flashcard  #orange #naranja 


    ([Location 2048](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2048))
-
- 

Faces Flow #flashcard 


    ([Location 2065](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2065))
-
- 

REST is an architectural style of services that utilizes web standards. Web services designed using REST are called RESTful web services, #flashcard  #blue #azul 


    ([Location 2916](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2916))
-
- 

Use standard HTTP methods to interact with the resource: #flashcard 


    ([Location 2921](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2921))
-
- 

Communication between the client and the endpoint is stateless. #flashcard 


    ([Location 2923](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2923))
-
- 

Java API for RESTful web services (JAX-RS) defines a standard annotation-driven API that helps developers build a RESTful web service in Java and invoke it. #flashcard  #blue #azul 


    ([Location 2924](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2924))
-
- 

@Path("orders") public class OrderResource { #flashcard  #orange #naranja 


    ([Location 2930](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2930))
-
- 

@GET   public List<Order> getAll() { #flashcard  #orange #naranja 


    ([Location 2933](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2933))
-
- 

@GET   @Path("{oid}")   public Order getOrder(@PathParam("oid")int id) { #flashcard  #orange #naranja 


    ([Location 2936](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2936))
-
- 

@XmlRootElement public class Order { #flashcard  #orange #naranja 


    ([Location 2942](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2942))
-
- 

The @Path annotation on the getOrder resource method marks it as a subresource that is accessible at orders/{oid}. #flashcard 


    ([Location 2952](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2952))
-
- 

The curly braces around oid identify it as a template parameter and bind its value at runtime to the id parameter of the getOrder resource method. #flashcard 


    ([Location 2954](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2954))
-
- 

The @PathParam can also be used to bind template parameters to a resource class field. #flashcard 


    ([Location 2955](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2955))
-
- 

Typically, a RESTful resource is bundled in a .war file along with other classes and resources. #flashcard 


    ([Location 2957](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=2957))
-
- 

The name attribute in the HTML form and the value of the @FormParam annotation are exactly the same to ensure the binding. #flashcard 


    ([Location 3097](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=3097))
-
- 

The HTTP HEAD method is identical to GET except that no response body is returned. #flashcard 


    ([Location 3140](https://readwise.io/to_kindle?action=open&asin=B00EJX7WEQ&location=3140))
-