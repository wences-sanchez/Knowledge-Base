title:: SecDevOps Tema-4 (highlights)
author:: [[UNIR]]
full-title:: "SecDevOps Tema-4"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/1197c14e-d3d2-4409-856d-0ba0aad04d05.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Cual es la capa superior del modelo TCP/IP? #flashcard
		  id:: 0597ef4c-fb62-4e13-aa6f-272bd54d3f3b
			- La capa de aplicación es la capa superior del modelo TCP/IP.
		- (Page 5)
	- -
	- -
		- ¿Qué componentes con las que interactuamos en un ordenador se consideran parte de la capa de aplicación? #flashcard
		  id:: 3f8c9046-6771-4320-82a6-a4d0d7efbc69
			- independientemente del software que se utilice, el protocolo usado por el software es el agente que se considera parte de la capa de aplicación.
		- (Page 6)
	- -
	- -
		- ¿A qué se considera un servidor en el modelo cliente-servidor? #flashcard
		  id:: 02190cb2-bcfc-4a99-a6ff-8522a1296252
			- En  el  modelo  cliente-servidor,  cualquier  proceso  puede  actuar  como  servidor  o cliente. No es el tipo o tamaño de la máquina, ni sus especificaciones de hardware, lo que lo convierten en servidor, sino su capacidad de atender las peticiones de los procesos cliente. Un sistema puede actuar simultáneamente como servidor y cliente. Es decir, uno de sus procesos está actuando como servidor, y otro está actuando como cliente. Tanto cliente como servidor pueden residir en la misma máquina. Dos procesos en el modelo cliente-servidor pueden interactuar de varias maneras:   Llamada a procedimiento remoto (Remote Procedure Calls o RPC).   Sockets.
		- (Page 6)
	- -
	- -
		- ¿Qué es un socket? #flashcard
		  id:: b4ae6eb4-8522-44f0-90ba-ca84be593438
			- Un socket es un objeto en la pila de protocolos de red del sistema operativo al que se entregan los paquetes recibidos por el host y dirigidos al socket, identificado por el número de puerto. El segundo proceso, actuando como cliente, también abre un socket, pero, en lugar de esperar una solicitud entrante, envía paquetes a través de dicho socket. Cuando llega la petición al servidor, esta es dirigida al socket y atendida por el proceso.
		- (Page 6)
	- -
	- -
		- ¿Cómo se ponen de acuerdo los servidores DNS para preguntarse por los dominios? #flashcard
		  id:: 6123df82-e309-4294-bcea-0cc1a71bf13f
			- Aunque  las  peticiones  de  resolución  de  nombres  usan  UDP  como  protocolo  de transporte,  los  servidores  DNS  se  comunican  entre  ellos  mediante  TCP  en  el puerto 53. Esta comunicación se usa para el intercambio y sincronización de zonas DNS.  Este  mecanismo permite  que una  actualización  de  un  registro  DNS  se  pueda replicar a otros servidores sin intervención manual.
		- (Page 13)
	- -
	- -
		- ¿Qué es SMTP? #flashcard
		  id:: 0856933b-2b67-474e-885d-2811919f8829
			- El protocolo de transferencia de correo simple (SMTP) se utiliza para el intercambio de mensajes de correo electrónico entre un cliente y un servidor, o entre servidores (IETF,  s.  f.).  En  un  cliente  de  escritorio,  un  agente  de  la  aplicación  se  encarga  de gestionar el envío al servidor mediante SMTP, mientras que el usuario final utiliza SMTP solo para enviar los correos electrónicos, los servidores normalmente utilizan SMTP tanto para enviar como para recibir correos.
		- (Page 14)
	- -
	- -
		- +++ #flashcard
		  id:: 6ff5c1e5-6058-4c75-a724-c95f5d60bd22
			- La recepción de correos en los clientes se suele llevar a cabo con POP o IMAP.
		- (Page 15)
	- -
	- -
		- ¿Qué puertos usa SMTP? #flashcard
		  id:: c8e8f49e-a24f-49cd-9ae5-d37ce6ddc5d4
			- recepción. Los  clientes  usan  el  puerto  TCP  587  como  destino  para  el  envío  de  mensajes, mientras que los servidores usan el puerto TCP 25 tanto para el envío como para la
		- (Page 15)
	- -
	- -
		- ¿Para qué se usa el protocolo POP? #flashcard
		  id:: 52768ab9-1a97-4791-a85a-28b47c0aa3de
			- Aunque los clientes de correo usan SMTP para el envío de mensajes, usan POP (Post Office Protocol) para la descarga de mensajes nuevos. IMAP es otro protocolo que también permite el envío y la recepción.
		- (Page 16)
	- -
	- -
		- +++ #flashcard
		  id:: 64018c1e-3b31-4580-8429-6a8bffdfc25d
			- El protocolo funciona sobre el puerto TCP 110. En el modo delete, el servidor borra los mensajes una vez descargados por el cliente. En el modo keep, tanto el servidor como el cliente mantienen los mensajes, hasta que el usuario los borra.
		- (Page 17)
	- -
	- -
		- ¿Qué es FTP? #flashcard
		  id:: e56c00d5-f50a-4910-9da3-8e2ec4075854
			- El  File  Transfer  Protocol  es  el  protocolo  más  utilizado  para  la  transferencia  de archivos  en  la  red,  o,  al  menos,  lo  era  antes  de  la  popularización  de  las  redes  de intercambio  peer-to-peer.  FTP  utiliza  TCP  como  capa  de  transporte,  y  utiliza diferentes puertos en función del modo de funcionamiento:   El cliente siempre inicia una conexión de control al puerto TCP 21.   En modo activo, el cliente abre un socket en un puerto aleatorio e indica al servidor que inicie la transferencia de datos en ese puerto.   En  modo  pasivo,  es  el  servidor  el  que  abre  un  socket  adicional  en  un  puerto aleatorio y le indica al cliente que lo use para sus transferencias. El modo activo no funcionará en situaciones con firewalls o en las que el cliente está detrás de un NAT, ya que el puerto, en el cliente, no será accesible desde la red del servidor.
		- (Page 17)
	- -
	- -
		- El estándar define una lista de códigos de respuesta agrupados en cinco secciones. Al  igual  que  las  cabeceras,  los  códigos  son  extensibles.  El  primer  dígito del  código define la clase de respuesta:   1xx – Información: petición recibida, continuando el procesado.   2xx – Éxito: la petición se recibió y ha sido procesada con éxito.   3xx  –  Redirección:  el  cliente  debe  tomar  acción  para  terminar  de  completar  la petición.   4xx – Error de cliente: la petición no puede completarse por un error en la petición.   5xx – Error de servidor: la petición puede ser válida, pero el servidor no ha podido procesarla por algún otro error. #flashcard
		  id:: a9d01c44-818f-4288-9c26-33c9b7a475c9
		- (Page 21)
	- -
	- -
		- ¿Cuáles son los códigos más comunes de HTTP? #flashcard
		  id:: 6e20c10c-cedf-4cc2-80ad-aebbde6bd419
			- pu
		- (Page 21)
	- -
	- -
		- Network Time Protocol (NTP), es un protocolo de sincronización de reloj. Un equipo puede fijar su reloj local tras una petición a un servidor, sin necesidad de intervención del usuario. Funciona a través de redes con una latencia variable. #flashcard
		  id:: 7d3044e7-cc8a-4d98-990d-f94bfa2b1ca6
		- (Page 28)
	- -
	- -
		- ¿Para qué se usa NTP? #flashcard
		  id:: 2affde5d-3777-45f5-909b-72e36d573c87
			- d
		- (Page 28)
	- -
	- -
		- Criptografía asimétrica Estos algoritmos también se conocen como de clave pública. Resuelven el problema del  intercambio  de  claves  definiendo  un  algoritmo  que  usa  dos  claves  (conocidas como key pair o pareja de claves), cada una de las cuales puede usarse para cifrar un mensaje. Cuando  se  cifra  un  mensaje  con  una  de  las  claves,  hay  que  usar  la  otra  para descifrarlo. Los usuarios ya no tienen  que compartir una misma clave, sino que es suficiente que compartan una de las dos claves. Siguiendo con el ejemplo anterior, si el  usuario  A  quiere  que  solo  el  usuario  B  lea  el  contenido  del  mensaje,  cifrará  el mensaje  con  la  clave  pública  de  B.  Es  decir,  B  siempre  compartirá  la  misma  clave, considerada pública, con cualquier usuario de quien necesite recibir mensajes. Deberá mantener la otra clave, la privada, en secreto. Esta clave privada será la única que permite descifrar los mensajes cifrados con la clave pública de B. No hace falta compartir la clave pública por un canal seguro, hay otras implicaciones a la hora de compartir esta clave. #flashcard
		  id:: fa03ee8e-a70b-4d86-aece-d4cfe10331c0
		- (Page 31)
	- -
	- -
		- Explica cómo s utilizan las clavs públicas/privadas. #flashcard
		  id:: e3372af0-27a2-4fcc-856b-d8e63c83b1dc
			- e
		- (Page 31)
	- -
	- -
		- ¿Qué es SSL? #flashcard
		  id:: efade22a-036b-44be-9b26-142936650a17
			- Secure Sockets Layer SSL es un protocolo de aplicación que actúa como capa intermedia entre TCP y otro protocolo  de  aplicación.  El  ejemplo  más  conocido  es  HTTPS,  en  el  que  HTTP  se transmite  sobre  SSL  y  usa  el  puerto  443  por  defecto,  pero  se  usa  con  otras aplicaciones conocidas, como FTP y SMTP. Ofrece  un  canal  seguro  que  soporta  autenticación,  integridad  y  cifrado  mediante certificados,  firmas  y  cifrado.  El  protocolo  usa  criptografía  asimétrica  para  la autenticación  y  el  establecimiento  de  parámetros  de  la  sesión;  y  criptografía simétrica para el intercambio de los datos. El protocolo es versátil en cuanto a la variedad de algoritmos que soporta. Ambos extremos de la comunicación deben ponerse de acuerdo en un conjunto de algoritmos de firma y cifrado durante el establecimiento.
		- (Page 39)
	- -