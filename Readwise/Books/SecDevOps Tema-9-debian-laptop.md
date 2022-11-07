# SecDevOps Tema-9

deck:: [[UNI::SecDevOps Tema-9]]\
author:: [[UNIR]]\
full-title:: "SecDevOps Tema-9"\
category:: #books\
\
tags:: UNI SecDevOps  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b3141a2c-9a25-468c-b8b7-792f14c1e626.jpg)
## Highlights
- id:: 63639930-4ff9-4669-a24e-b28bd48212a9
  
  En este tipo de pipelines las pruebas no tienen por qué restringirse a las funcionalidades de la aplicación. Hay utilidades como OWASP Zed Attack Proxy, o ZAP, que permiten automatizar comprobaciones contra vulnerabilidades típicas de aplicaciones web. #flashcard 
  
  
     (Page 6)
-
- id:: 63639930-9096-4fe3-8747-153483f88484
  
  HTTP soporta, nativamente, autenticación básica con la cabecera Authentication, pero las aplicaciones pueden implementar sus propios mecanismos mediante cookies o cabeceras personalizadas. En estos casos, las pruebas deben cubrir elementos como el cifrado no reversible de contraseñas de usuario. #flashcard 
  
  
     (Page 7)
-
- id:: 63639930-6242-46af-bb6b-ec1d24bf6134
  
  Esto lleva a que las aplicaciones no reciban los parches de seguridad que las librerías incorporan en nuevas versiones. Una de las pruebas que se puede incorporar en el pipeline es verificar si las versiones en uso sufren de vulnerabilidades conocidas. Por ejemplo, NodeJS incluye la Node Security Platform en su ecosistema. Mediante npm audit es posible obtener la lista de vulnerabilidades de las versiones en uso. También hay analizadores similares para python, como pyup.io o requires.io. #flashcard 
  
  
     (Page 9)
-
- id:: 63639930-d16d-41c9-93e0-f9a92862857a
   Sobre HTTPS y seguridad #flashcard 
    Las aplicaciones que sirven sitios web o interfaces API REST deben proteger la comunicación HTTP. El protocolo SSL y su sucesor, TLS, añaden confidencialidad, autenticación e integridad a HTTP. Habilitar HTTPS no asegura que el tráfico sea seguro por sí solo. Las pruebas deberán evaluar aspectos como:  La aplicación solo es accesible por HTTPS, no por HTTP. Como mucho, cualquier petición por HTTP deberá redirigir a la misma ruta con prefijo https://.  Los certificados se han generado con la longitud de clave suficiente, no han caducado y no han sido revocados.
  
     (Page 9)
-
- id:: 63639930-0414-4f17-80c5-98d8e50d5e97
  
   El servidor solo soportará las suites de cifrado más modernas o, al menos, no soportará suites con vulnerabilidades conocidas. La adopción de algoritmos modernos no tiene por qué ser rápida en todos los clientes, así que las organizaciones deben encontrar un equilibrio entre los clientes que soportan y los algoritmos que quieren dejar de soportar. Por ejemplo, testssl.sh es una herramienta de línea de comandos que genera informes sobre los certificados y las suites de cifrado ofrecidas por el servidor. #flashcard 
  
  
     (Page 10)
-
- id:: 63639930-645f-46f1-a1e7-67cceb1dd265
  
  Ya se trate de una aplicación con una interfaz HTTPS o un servidor interno que analice un data lake periódicamente, las instancias en las que se ejecutan los procesos deben estar protegidas a nivel de red. En un entorno de nube, además, hay que tener en cuenta no solo las instancias de cómputo, sino otros objetos nativos del proveedor, como balanceadores de carga y redes virtuales. #flashcard 
  
  
     (Page 10)
-
- id:: 63639930-6652-41b1-9ad6-bb6e8d293f8f
  
  Este tipo de despliegues son ideales para las pruebas de esta fase. Se puede desplegar un entorno que simule lo más posible el de producción, aunque a menor escala, y ejecutar pruebas de acceso sobre él. En este caso, no se trata de comprobar vulnerabilidades a nivel de aplicación, sino de verificar que las reglas de firewall (o el objeto equivalente, como un grupo de seguridad) está configurado correctamente. Como estos entornos son privados, se pueden llevar a cabo escaneos de puertos sin afectar el funcionamiento del entorno de producción. #flashcard 
  
  
     (Page 10)
-
- id:: 63639930-76c8-4b75-afad-49114a210a3d
  
  Las aplicaciones harán uso de algún tipo de persistencia, ya sea una base de datos desplegada ad hoc, una base de datos como servicio (por ejemplo, RDS en Amazon o MongoDB Atlas) o un almacenamiento de bloque o de objeto como Amazon S3 o Backblaze B2. Estos elementos deben ser también protegidos, por lo que las pruebas comprobarán que no se permite acceso sin credenciales, o que los puertos de la base de datos solo están abiertos a los servidores de la aplicación. #flashcard 
  
  
     (Page 11)
-
- id:: 63639930-30dc-4750-a1f1-76b96183d40f
  
  Si un atacante consigue acceder a una de las herramientas del pipeline de CI/CD, cualquier otra medida que se haya implementado no servirá de nada. Da igual que todos los elementos de la aplicación estén protegidos y las pruebas finalicen satisfactoriamente: quien tenga acceso completo al pipeline puede modificar a su gusto cualquier elemento de la aplicación o de la infraestructura. #flashcard 
  
  
     (Page 11)
-
- id:: 63639930-8a9c-4586-b7d9-2f207a4e372d
  
  puntos en lo que habrá que prestar atención, por ejemplo:  En todas las herramientas habrá que configurar el acceso basado en roles, de manera que cada usuario reciba el mínimo conjunto de permisos necesarios.  Los commits deben estar firmados para evitar que se incorporen a la rama principal si son de un individuo ajeno a la organización o, en caso de que se lleguen a aceptar, tener la posibilidad de auditar su origen. #flashcard 
  
  
     (Page 12)
-
- id:: 63639930-e12c-46d4-a8c8-f16631866a3a
  
  Algunas de las buenas prácticas de control de acceso, no solo en aplicaciones de control de versiones, sino en cualquier sistema, son las siguientes:  Mantener la lista de usuarios con acceso ilimitado al repositorio lo más pequeña posible. Siempre es necesario que haya uno o varios administradores principales, pero no se debe caer en la tentación de dar acceso indiscriminado a los usuarios solo para facilitar la asignación de permisos. #flashcard 
  
  
     (Page 12)
-
- id:: 63639930-1784-4791-941f-dfaf7962dd29
  
   Requerir autenticación multifactor (MFA). Cada vez más servicios de control de versiones soportan autenticación de doble factor, lo que ofrece una capa de seguridad adicional. #flashcard 
  
  
     (Page 13)
-
- id:: 63639930-fec0-427b-8142-23015a7e52ec
  
   Auditar regularmente los miembros de los grupos #flashcard 
  
  
     (Page 13)
-
- id:: 63639930-165b-4f08-b794-5f864b9dfc6e
  
  Sistemas como GitHub ofrecen características de seguridad, como la protección de ramas para evitar operaciones sensibles, como añadir commits directamente a la rama máster. Si el acceso basado en roles está bien configurado, este tipo de restricciones proporcionan una buena capa de seguridad. #flashcard 
  
  
     (Page 13)
-
- id:: 63639930-f6b8-4c84-9e82-d8c97676a44d
  
  Pero un atacante sería capaz de deshabilitar estas protecciones si consigue acceso al repositorio. La firma de commits con git proporciona una capa adicional. Git soporta la firma de commits y etiquetas con PGP. Esta funcionalidad consiste en aplicar firmas criptográficas a cada parche, commit y etiqueta, utilizando claves que los desarrolladores mantienen en secreto. #flashcard 
  
  
     (Page 13)
-
- id:: 63639930-d5e7-4b60-9450-309e09c7a225
  
  Los algoritmos que se usan no son diferentes a los que se usan en HTTPS, aunque las herramientas no son las mismas. Si los commits se firman con una clave válida dentro de la organización, se pueden considerar confiables. #flashcard 
  
  
     (Page 14)
-