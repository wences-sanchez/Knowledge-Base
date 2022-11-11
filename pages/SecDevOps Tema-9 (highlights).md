title:: SecDevOps Tema-9 (highlights)
author:: [[UNIR]]
full-title:: "SecDevOps Tema-9"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b3141a2c-9a25-468c-b8b7-792f14c1e626.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- En  este  tipo  de  pipelines  las  pruebas  no  tienen  por  qué  restringirse  a  las funcionalidades de la aplicación. Hay utilidades como OWASP Zed Attack Proxy, o ZAP, que permiten automatizar comprobaciones contra vulnerabilidades típicas de aplicaciones web. #flashcard
		  id:: e2bf6834-c94c-4bd0-81ba-f4a9340ae436
		- (Page 6)
	- -
	- -
		- HTTP soporta, nativamente,  autenticación básica con la cabecera  Authentication, pero  las  aplicaciones  pueden  implementar  sus  propios  mecanismos  mediante cookies  o  cabeceras  personalizadas.  En  estos  casos,  las  pruebas  deben  cubrir elementos como el cifrado no reversible de contraseñas de usuario. #flashcard
		  id:: 9d1da096-e1f1-4f76-a5da-a83b1ef1100c
		- (Page 7)
	- -
	- -
		- Esto lleva a que las aplicaciones no reciban los parches de seguridad que las librerías incorporan en nuevas versiones. Una de las pruebas que se puede incorporar en el pipeline es verificar si las versiones en uso sufren de vulnerabilidades conocidas. Por ejemplo, NodeJS incluye la Node Security Platform en su ecosistema. Mediante npm audit es posible obtener la lista de vulnerabilidades de las versiones en uso. También hay analizadores similares para python, como pyup.io o requires.io. #flashcard
		  id:: 6176406d-9543-46b3-b90a-e9f6226ec262
		- (Page 9)
	- -
	- -
		- Sobre HTTPS y seguridad #flashcard
		  id:: 5c6ab28f-6ebf-422b-ae51-b2ab762bdc9b
			- Las  aplicaciones  que  sirven  sitios  web  o  interfaces  API  REST  deben  proteger  la comunicación  HTTP.  El  protocolo  SSL  y  su  sucesor,  TLS,  añaden  confidencialidad, autenticación  e  integridad  a  HTTP.  Habilitar  HTTPS  no  asegura  que  el  tráfico  sea seguro por sí solo. Las pruebas deberán evaluar aspectos como:   La aplicación solo es accesible por HTTPS, no por HTTP. Como mucho, cualquier petición por HTTP deberá redirigir a la misma ruta con prefijo https://.   Los  certificados  se  han  generado  con  la  longitud  de  clave  suficiente,  no  han caducado y no han sido revocados.
		- (Page 9)
	- -
	- -
		-   El  servidor  solo  soportará  las  suites  de  cifrado  más  modernas  o,  al  menos,  no soportará  suites  con  vulnerabilidades  conocidas.  La  adopción  de  algoritmos modernos  no  tiene  por  qué  ser  rápida  en  todos  los  clientes,  así  que  las organizaciones deben encontrar un equilibrio entre los clientes que soportan y los algoritmos que quieren dejar de soportar. Por  ejemplo,  testssl.sh  es  una  herramienta  de  línea  de  comandos  que  genera informes sobre los certificados y las suites de cifrado ofrecidas por el servidor. #flashcard
		  id:: 59065442-2f52-4bb4-a365-07b19aea5373
		- (Page 10)
	- -
	- -
		- Ya  se  trate  de  una  aplicación  con  una  interfaz  HTTPS  o  un  servidor  interno  que analice  un  data  lake  periódicamente,  las  instancias  en  las  que  se  ejecutan  los procesos deben estar protegidas a nivel de red. En un entorno de nube, además, hay que tener en cuenta no solo las instancias de cómputo, sino otros objetos nativos del proveedor, como balanceadores de carga y redes virtuales. #flashcard
		  id:: 1ddd4e8f-3ac8-47ad-8da0-d72f22c2bf08
		- (Page 10)
	- -
	- -
		- Este  tipo  de  despliegues  son  ideales  para  las  pruebas  de  esta  fase.  Se  puede desplegar un entorno que simule lo más posible el de producción, aunque a menor escala, y ejecutar pruebas de acceso sobre él. En este caso, no se trata de comprobar vulnerabilidades a nivel de aplicación, sino de verificar que las reglas de firewall (o el objeto equivalente, como un grupo de seguridad) está configurado correctamente. Como estos entornos son privados, se pueden llevar a cabo escaneos de puertos sin afectar el funcionamiento del entorno de producción. #flashcard
		  id:: 00a0e54a-c09e-448d-9ccd-50b18545f20b
		- (Page 10)
	- -
	- -
		- Las aplicaciones harán uso de algún tipo de persistencia, ya sea una base de datos desplegada ad hoc, una base de datos como servicio (por ejemplo, RDS en Amazon o MongoDB  Atlas)  o  un  almacenamiento  de  bloque  o  de  objeto  como  Amazon  S3  o Backblaze B2. Estos elementos deben ser también protegidos, por lo que las pruebas comprobarán que no se permite acceso sin credenciales, o que los puertos de la base de datos solo están abiertos a los servidores de la aplicación. #flashcard
		  id:: 69c9b64f-0dc5-4f3a-95ae-84bbb8f6a47a
		- (Page 11)
	- -
	- -
		- Si un atacante consigue acceder a una de las herramientas del  pipeline de CI/CD, cualquier otra medida que se haya implementado no servirá de nada. Da igual que todos  los  elementos  de  la  aplicación  estén  protegidos  y  las  pruebas  finalicen satisfactoriamente:  quien  tenga  acceso  completo  al  pipeline  puede  modificar  a  su gusto cualquier elemento de la aplicación o de la infraestructura. #flashcard
		  id:: a1f7f6c5-e7be-4eea-85f2-f0e0eea1cef2
		- (Page 11)
	- -
	- -
		- puntos en lo que habrá que prestar atención, por ejemplo:   En  todas  las  herramientas  habrá  que  configurar  el  acceso  basado  en  roles,  de manera que cada usuario reciba el mínimo conjunto de permisos necesarios.   Los  commits  deben  estar  firmados  para  evitar  que  se  incorporen  a  la  rama principal si son de un individuo ajeno a la organización o, en caso de que se lleguen a aceptar, tener la posibilidad de auditar su origen. #flashcard
		  id:: 2fad9fd3-9fa4-4cdc-a3d4-275ea1afdc26
		- (Page 12)
	- -
	- -
		- Algunas  de  las  buenas  prácticas  de  control  de  acceso,  no  solo  en  aplicaciones  de control de versiones, sino en cualquier sistema, son las siguientes:   Mantener la lista de usuarios con acceso ilimitado al repositorio lo más pequeña posible. Siempre es necesario que haya uno o varios administradores principales, pero no se debe caer en la tentación de dar acceso indiscriminado a los usuarios solo para facilitar la asignación de permisos. #flashcard
		  id:: d904c223-0876-48e2-9710-3b4e823bbb99
		- (Page 12)
	- -
	- -
		-   Requerir autenticación multifactor (MFA). Cada vez más servicios de control de versiones  soportan  autenticación  de  doble  factor,  lo  que  ofrece  una  capa  de seguridad adicional. #flashcard
		  id:: 88f59daf-43f4-43f3-b068-e4fc49f721b2
		- (Page 13)
	- -
	- -
		-   Auditar  regularmente  los  miembros  de  los  grupos #flashcard
		  id:: b196ed3c-20fd-444f-afbd-7b0d166f97d3
		- (Page 13)
	- -
	- -
		- Sistemas como GitHub ofrecen características de seguridad, como la protección de ramas para evitar operaciones sensibles, como añadir commits directamente a la rama máster. Si el acceso basado en roles está bien configurado, este tipo de restricciones proporcionan una buena capa de seguridad. #flashcard
		  id:: d0de4f88-fcf0-4c5f-a710-1450ae1c0148
		- (Page 13)
	- -
	- -
		- Pero un atacante sería capaz de deshabilitar estas protecciones si consigue acceso al repositorio. La firma de commits con git proporciona una capa adicional. Git soporta la firma de commits y etiquetas con PGP. Esta funcionalidad consiste en aplicar firmas criptográficas  a  cada  parche,  commit  y  etiqueta,  utilizando  claves  que  los desarrolladores mantienen en secreto. #flashcard
		  id:: 5ebb69da-d0d0-448b-86d6-f730e30ffc5e
		- (Page 13)
	- -
	- -
		- Los algoritmos que se usan no son diferentes a los que se usan en HTTPS, aunque las herramientas no son las mismas. Si los commits se firman con una clave válida dentro de la organización, se pueden considerar confiables. #flashcard
		  id:: 6dec0b2e-d607-459b-a8da-73ebe900cf6d
		- (Page 14)
	- -