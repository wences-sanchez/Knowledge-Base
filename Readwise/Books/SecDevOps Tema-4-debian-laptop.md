# SecDevOps Tema-4

deck:: [[UNI::SecDevOps Tema-4]]\
author:: [[UNIR]]\
full-title:: "SecDevOps Tema-4"\
category:: #books\
\
tags:: SecDevOps UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/1197c14e-d3d2-4409-856d-0ba0aad04d05.jpg)
## Highlights
- id:: 6363992f-aa13-40ae-9fee-59ca304f92b8
   ¿Cual es la capa superior del modelo TCP/IP? #flashcard 
    La capa de aplicación es la capa superior del modelo TCP/IP.
  
     (Page 5)
-
- id:: 6363992f-9604-44bd-b951-05180b065ac4
   ¿Qué componentes con las que interactuamos en un ordenador se consideran parte de la capa de aplicación? #flashcard 
    independientemente del software que se utilice, el protocolo usado por el software es el agente que se considera parte de la capa de aplicación.
  
     (Page 6)
-
- id:: 6363992f-1657-40fe-a08b-1de8e03564f1
   ¿A qué se considera un servidor en el modelo cliente-servidor? #flashcard 
    En el modelo cliente-servidor, cualquier proceso puede actuar como servidor o cliente. No es el tipo o tamaño de la máquina, ni sus especificaciones de hardware, lo que lo convierten en servidor, sino su capacidad de atender las peticiones de los procesos cliente. Un sistema puede actuar simultáneamente como servidor y cliente. Es decir, uno de sus procesos está actuando como servidor, y otro está actuando como cliente. Tanto cliente como servidor pueden residir en la misma máquina. Dos procesos en el modelo cliente-servidor pueden interactuar de varias maneras:  Llamada a procedimiento remoto (Remote Procedure Calls o RPC).  Sockets.
  
     (Page 6)
-
- id:: 6363992f-0ea5-45c0-8cc6-791fb87be070
   ¿Qué es un socket? #flashcard 
    Un socket es un objeto en la pila de protocolos de red del sistema operativo al que se entregan los paquetes recibidos por el host y dirigidos al socket, identificado por el número de puerto. El segundo proceso, actuando como cliente, también abre un socket, pero, en lugar de esperar una solicitud entrante, envía paquetes a través de dicho socket. Cuando llega la petición al servidor, esta es dirigida al socket y atendida por el proceso.
  
     (Page 6)
-
- id:: 6363992f-aae3-41f8-8f6e-34877385a390
   ¿Cómo se ponen de acuerdo los servidores DNS para preguntarse por los dominios? #flashcard 
    Aunque las peticiones de resolución de nombres usan UDP como protocolo de transporte, los servidores DNS se comunican entre ellos mediante TCP en el puerto 53. Esta comunicación se usa para el intercambio y sincronización de zonas DNS. Este mecanismo permite que una actualización de un registro DNS se pueda replicar a otros servidores sin intervención manual.
  
     (Page 13)
-
- id:: 6363992f-bc90-457d-b6ca-14df5b6d1139
   ¿Qué es SMTP? #flashcard 
    El protocolo de transferencia de correo simple (SMTP) se utiliza para el intercambio de mensajes de correo electrónico entre un cliente y un servidor, o entre servidores (IETF, s. f.). En un cliente de escritorio, un agente de la aplicación se encarga de gestionar el envío al servidor mediante SMTP, mientras que el usuario final utiliza SMTP solo para enviar los correos electrónicos, los servidores normalmente utilizan SMTP tanto para enviar como para recibir correos.
  
     (Page 14)
-
- id:: 6363992f-20f9-4d8e-b666-baade1cb8133
   +++ #flashcard 
    La recepción de correos en los clientes se suele llevar a cabo con POP o IMAP.
  
     (Page 15)
-
- id:: 6363992f-7a56-4f1f-922a-87c4d17d8959
   ¿Qué puertos usa SMTP? #flashcard 
    recepción. Los clientes usan el puerto TCP 587 como destino para el envío de mensajes, mientras que los servidores usan el puerto TCP 25 tanto para el envío como para la
  
     (Page 15)
-
- id:: 6363992f-1b51-4115-847d-3f7f5594aa44
   ¿Para qué se usa el protocolo POP? #flashcard 
    Aunque los clientes de correo usan SMTP para el envío de mensajes, usan POP (Post Office Protocol) para la descarga de mensajes nuevos. IMAP es otro protocolo que también permite el envío y la recepción.
  
     (Page 16)
-
- id:: 6363992f-af20-4d65-9996-f2ba067b0368
   +++ #flashcard 
    El protocolo funciona sobre el puerto TCP 110. En el modo delete, el servidor borra los mensajes una vez descargados por el cliente. En el modo keep, tanto el servidor como el cliente mantienen los mensajes, hasta que el usuario los borra.
  
     (Page 17)
-
- id:: 6363992f-4624-448e-98bf-022326afe271
   ¿Qué es FTP? #flashcard 
    El File Transfer Protocol es el protocolo más utilizado para la transferencia de archivos en la red, o, al menos, lo era antes de la popularización de las redes de intercambio peer-to-peer. FTP utiliza TCP como capa de transporte, y utiliza diferentes puertos en función del modo de funcionamiento:  El cliente siempre inicia una conexión de control al puerto TCP 21.  En modo activo, el cliente abre un socket en un puerto aleatorio e indica al servidor que inicie la transferencia de datos en ese puerto.  En modo pasivo, es el servidor el que abre un socket adicional en un puerto aleatorio y le indica al cliente que lo use para sus transferencias. El modo activo no funcionará en situaciones con firewalls o en las que el cliente está detrás de un NAT, ya que el puerto, en el cliente, no será accesible desde la red del servidor.
  
     (Page 17)
-
- id:: 6363992f-790a-492e-9976-ef073ba92388
  
  El estándar define una lista de códigos de respuesta agrupados en cinco secciones. Al igual que las cabeceras, los códigos son extensibles. El primer dígito del código define la clase de respuesta:  1xx – Información: petición recibida, continuando el procesado.  2xx – Éxito: la petición se recibió y ha sido procesada con éxito.  3xx – Redirección: el cliente debe tomar acción para terminar de completar la petición.  4xx – Error de cliente: la petición no puede completarse por un error en la petición.  5xx – Error de servidor: la petición puede ser válida, pero el servidor no ha podido procesarla por algún otro error. #flashcard 
  
  
     (Page 21)
-
- id:: 6363992f-2dd9-4361-b569-3b5c544e4fc2
   ¿Cuáles son los códigos más comunes de HTTP? #flashcard 
    pu
  
     (Page 21)
-
- id:: 6363992f-0483-44d0-be7c-3507d440bde3
  
  Network Time Protocol (NTP), es un protocolo de sincronización de reloj. Un equipo puede fijar su reloj local tras una petición a un servidor, sin necesidad de intervención del usuario. Funciona a través de redes con una latencia variable. #flashcard 
  
  
     (Page 28)
-
- id:: 6363992f-bd31-4dbb-a077-0c8840b879a7
   ¿Para qué se usa NTP? #flashcard 
    d
  
     (Page 28)
-
- id:: 6363992f-7d6b-4d08-8c95-c491b6d4f3a7
  
  Criptografía asimétrica Estos algoritmos también se conocen como de clave pública. Resuelven el problema del intercambio de claves definiendo un algoritmo que usa dos claves (conocidas como key pair o pareja de claves), cada una de las cuales puede usarse para cifrar un mensaje. Cuando se cifra un mensaje con una de las claves, hay que usar la otra para descifrarlo. Los usuarios ya no tienen que compartir una misma clave, sino que es suficiente que compartan una de las dos claves. Siguiendo con el ejemplo anterior, si el usuario A quiere que solo el usuario B lea el contenido del mensaje, cifrará el mensaje con la clave pública de B. Es decir, B siempre compartirá la misma clave, considerada pública, con cualquier usuario de quien necesite recibir mensajes. Deberá mantener la otra clave, la privada, en secreto. Esta clave privada será la única que permite descifrar los mensajes cifrados con la clave pública de B. No hace falta compartir la clave pública por un canal seguro, hay otras implicaciones a la hora de compartir esta clave. #flashcard 
  
  
     (Page 31)
-
- id:: 6363992f-5fa2-41d8-8f37-84905e273f15
   Explica cómo s utilizan las clavs públicas/privadas. #flashcard 
    e
  
     (Page 31)
-
- id:: 6363992f-15f7-41a3-82ef-f21a87df9b9a
   ¿Qué es SSL? #flashcard 
    Secure Sockets Layer SSL es un protocolo de aplicación que actúa como capa intermedia entre TCP y otro protocolo de aplicación. El ejemplo más conocido es HTTPS, en el que HTTP se transmite sobre SSL y usa el puerto 443 por defecto, pero se usa con otras aplicaciones conocidas, como FTP y SMTP. Ofrece un canal seguro que soporta autenticación, integridad y cifrado mediante certificados, firmas y cifrado. El protocolo usa criptografía asimétrica para la autenticación y el establecimiento de parámetros de la sesión; y criptografía simétrica para el intercambio de los datos. El protocolo es versátil en cuanto a la variedad de algoritmos que soporta. Ambos extremos de la comunicación deben ponerse de acuerdo en un conjunto de algoritmos de firma y cifrado durante el establecimiento.
  
     (Page 39)
-