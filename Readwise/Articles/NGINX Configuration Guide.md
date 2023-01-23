# NGINX Configuration Guide

deck:: [[Across-the-Net]]\
author:: [[[email protected]]]\
full-title:: "NGINX Configuration Guide"\
category:: #articles\
url:: https://www.plesk.com/blog/various/nginx-configuration-guide/\

![](https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png)
## Highlights
- id:: 63c669d3-5714-45eb-b640-5285b6d4bb2b
  
  What are Listening Ports?
     The listen directive informs NGINX of the hostname/IP and TCP port, so it recognizes where it must listen for HTTP connections.
     The argument default_server means that this virtual host will be answering requests on port 80 which don’t match the listen statement of a separate virtual host. When it comes to the second statement, this will listen over IPv6 and demonstrate similar behavior. #flashcard 
  
  
    ([View Highlight](https://instapaper.com/read/1475675408/18542195))
-
- id:: 63c669d3-bf15-42e3-b2cb-6363c92df92f
  
  What is Name-based Virtual Hosting?
     The server_name directive enables a number of domains to be served from just one IP address, and the server will determine which domain it will serve according to the request header received.
     Generally, you should create one file for each site or domain you wish to host on your server. #flashcard 
  
  
    ([View Highlight](https://instapaper.com/read/1475675408/18542220))
-
- id:: 63c669d3-29d7-46d8-adb7-95d412214c47
  
  What are Location Blocks?
     NGINX’s location setting helps you set up the way in which NGINX responds to requests for resources inside the server. As the server_name directive informs NGINX how it should process requests for the domain, location directives apply to requests for certain folders and files (e.g. http://example.com/blog/.) .
     Let’s consider a few examples:
     File: /etc/nginx/sites-available/example.com
     location / { }
     location /images/ { }
     location /blog/ { } #flashcard 
  
  
    ([View Highlight](https://instapaper.com/read/1475675408/18542242))
-
- id:: 63c669d3-379c-478b-8a01-8c308b71138b
  
  location / {
     root html;
     index index.html index.htm;
     }
     We can see, in this example, that the document root is based in the html/ directory. Under the NGINX default installation prefix, the location’s full path is /etc/nginx/html/.
     Request: http://example.com/blog/includes/style.css
     Returns: NGINX will try to serve the file found at /etc/nginx/html/blog/includes/style.css
     Please note:
     Absolute paths for the root directive can be used if you wish. The index variable informs NGINX which file it should serve #flashcard 
  
  
    ([View Highlight](https://instapaper.com/read/1475675408/18542310))
-