# JavaServer Pages

deck:: [[Other-Books::JavaServer Pages]]\
author:: [[Hans Bergsten]]\
full-title:: "JavaServer Pages"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/514oOAgmIlL._SL200_.jpg)

## Highlights
- 

the Java Enterprise APIs have expanded to encompass a number of areas: #flashcard 


    ([Location 308](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=308))
-
- 

a JSP page can change its content based on any number of variable items, including the identity of the user, the user’s browser type, information provided by the user, and selections made by the user. #flashcard 


    ([Location 320](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=320))
-
- 

Instead of embedding HTML in programming code, JSP lets you embed special active elements into HTML pages. #flashcard 


    ([Location 346](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=346))
-
- 

a JSP page is always compiled before it’s processed by the server. #flashcard  #blue #azul 


    ([Location 376](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=376))
-
- 

ASP.NET, the latest version of ASP, #flashcard 


    ([Location 410](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=410))
-
- 

the same simple client program must be able to talk to many different server applications, and the applications must be able to work with many different types of clients. To satisfy this need, the protocol of how a client and a server talk to each other must be defined in detail. That’s exactly what the HyperText Transport Protocol (HTTP) is for. #flashcard  #blue #azul 


    ([Location 485](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=485))
-
- 

A resource can be a number of things, such as a simple HTML file returned verbatim to the browser or a program that generates the response dynamically. #flashcard  #blue #azul 


    ([Location 499](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=499))
-
- 

HTTP is a stateless protocol. This means that the server doesn’t keep any information about the client after it sends its response, #flashcard  #blue #azul 


    ([Location 504](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=504))
-
- 

http://www.weather.com/forecast?city=Hermosa+Beach #flashcard  #blue #azul 


    ([Location 606](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=606))
-
- 

The query string starts with a question mark (?) and consists of name/value pairs separated by ampersands (&). #flashcard  #blue #azul 


    ([Location 607](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=607))
-
- 

A GET request always uses a query string to send parameter values, while a POST request always sends them as part of the body #flashcard  #blue #azul 


    ([Location 620](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=620))
-
- 

a servlet is a piece of code that adds new functionality to a server #flashcard  #blue #azul 


    ([Location 666](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=666))
-
- 

The deployment descriptor and all the other web application files are arranged in a well-defined hierarchy within an archive file, called a web application archive (WAR). #flashcard 


    ([Location 719](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=719))
-
- 

Everything in the page that isn’t a JSP element is called template text #flashcard 


    ([Location 800](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=800))
-
- 

Why use this design with JSP? #flashcard 


    ([Location 927](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=927))
-
- 

Without this clue, the server is unable to distinguish a JSP page from any other type of file and sends it unprocessed to the browser. #flashcard  #blue #azul 


    ([Location 1190](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1190))
-
- 

If the application is installed with the context path ora (more about this later), you use a URL such as http://localhost:8080/ora/ch5/easy.jsp to access the JSP page. #flashcard  #blue #azul 


    ([Location 1232](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1232))
-
- 

A browser doesn’t have access to the files under this directory, so it’s a safe place for files you don’t want public. #flashcard 


    ([Location 1235](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1235))
-
- 

lib and classes. All application class files (such as servlet and custom tag library classes) must be stored in these two directories. #flashcard 


    ([Location 1239](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1239))
-
- 

Class files that aren’t packaged in JAR files must be stored in the classes directory, #flashcard 


    ([Location 1242](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1242))
-
- 

There are three different directives that you can use in a JSP page: page, include, and taglib #flashcard 


    ([Location 1282](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1282))
-
- 

If you omit the contentType attribute, the container sets the header to text/html. #flashcard 


    ([Location 1298](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1298))
-
- 

<%-- and --% #flashcard  #orange #naranja 


    ([Location 1314](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1314))
-
- 

JSP action elements represent dynamic actions that take place at runtime, as opposed to JSP directives #flashcard  #blue #azul 


    ([Location 1338](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1338))
-
- 

<prefix:action_name                 attr1="value1" attr2="value2">   action_body </prefix:action_name> #flashcard  #orange #naranja 


    ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1351))
-
- 

<prefix:action_name                 attr1="value1" attr2="value2" / #flashcard  #orange #naranja 


    ([Location 1358](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1358))
-
- 

Action elements, or tags as they are often called, #flashcard 


    ([Location 1369](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1369))
-
- 

Actions can be grouped into three categories: standard, custom, and JSP Standard Tag Library. #flashcard  #blue #azul 


    ([Location 1380](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1380))
-
- 

The JSP standard actions use the prefix jsp. Since the prefix is fixed, and the behavior for all standard actions is defined #flashcard  #blue #azul 


    ([Location 1383](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1383))
-
- 

a bean is simply a Java class that follows certain coding conventions, so it can be used by tools as a component in a larger application. #flashcard  #blue #azul 


    ([Location 1588](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1588))
-
- 

<jsp:useBean id="cartoon"       class="com.ora.jsp.beans.motd.CartoonBean" / #flashcard  #orange #naranja 


    ([Location 1711](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=1711))
-
- 

Cookies, as you probably remember, are small pieces of text a server sends to the browser. #flashcard  #blue #azul 


    ([Location 5921](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=5921))
-
- 

Java Servlet Programming #flashcard  #pink #rosa 


    ([Location 9853](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=9853))
-
- 

A servlet is a Java class that extends a server with functionality for processing a request and producing a response. #flashcard  #blue #azul 


    ([Location 9856](https://readwise.io/to_kindle?action=open&asin=B0093T4LXG&location=9856))
-
