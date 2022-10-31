title:: SecDevOps Tema-9 (highlights)
deck:: [[UNI::SecDevOps Tema-9]]
author:: [[UNIR]]
full-title:: "SecDevOps Tema-9"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b3141a2c-9a25-468c-b8b7-792f14c1e626.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- En  este  tipo  de  pipelines  las  pruebas  no  tienen  por  qué  restringirse  a  las funcionalidades de la aplicación. Hay utilidades como OWASP Zed Attack Proxy, o ZAP, que permiten automatizar comprobaciones contra vulnerabilidades típicas de aplicaciones web. #flashcard
		- (Page 6)
	- -
	- -
		- HTTP soporta, nativamente,  autenticación básica con la cabecera  Authentication, pero  las  aplicaciones  pueden  implementar  sus  propios  mecanismos  mediante cookies  o  cabeceras  personalizadas.  En  estos  casos,  las  pruebas  deben  cubrir elementos como el cifrado no reversible de contraseñas de usuario. #flashcard
		- (Page 7)
	- -
	- -
		- Esto lleva a que las aplicaciones no reciban los parches de seguridad que las librerías incorporan en nuevas versiones. Una de las pruebas que se puede incorporar en el pipeline es verificar si las versiones en uso sufren de vulnerabilidades conocidas. Por ejemplo, NodeJS incluye la Node Security Platform en su ecosistema. Mediante npm audit es posible obtener la lista de vulnerabilidades de las versiones en uso. También hay analizadores similares para python, como pyup.io o requires.io. #flashcard
		- (Page 9)
	- -
	- -
		- Sobre HTTPS y seguridad #flashcard
			- Las  aplicaciones  que  sirven  sitios  web  o  interfaces  API  REST  deben  proteger  la comunicación  HTTP.  El  protocolo  SSL  y  su  sucesor,  TLS,  añaden  confidencialidad, autenticación  e  integridad  a  HTTP.  Habilitar  HTTPS  no  asegura  que  el  tráfico  sea seguro por sí solo. Las pruebas deberán evaluar aspectos como:   La aplicación solo es accesible por HTTPS, no por HTTP. Como mucho, cualquier petición por HTTP deberá redirigir a la misma ruta con prefijo https://.   Los  certificados  se  han  generado  con  la  longitud  de  clave  suficiente,  no  han caducado y no han sido revocados.
		- (Page 9)
	- -
	- -
		-   El  servidor  solo  soportará  las  suites  de  cifrado  más  modernas  o,  al  menos,  no soportará  suites  con  vulnerabilidades  conocidas.  La  adopción  de  algoritmos modernos  no  tiene  por  qué  ser  rápida  en  todos  los  clientes,  así  que  las organizaciones deben encontrar un equilibrio entre los clientes que soportan y los algoritmos que quieren dejar de soportar. Por  ejemplo,  testssl.sh  es  una  herramienta  de  línea  de  comandos  que  genera informes sobre los certificados y las suites de cifrado ofrecidas por el servidor. #flashcard
		- (Page 10)
	- -
	- -
		- Ya  se  trate  de  una  aplicación  con  una  interfaz  HTTPS  o  un  servidor  interno  que analice  un  data  lake  periódicamente,  las  instancias  en  las  que  se  ejecutan  los procesos deben estar protegidas a nivel de red. En un entorno de nube, además, hay que tener en cuenta no solo las instancias de cómputo, sino otros objetos nativos del proveedor, como balanceadores de carga y redes virtuales. #flashcard
		- (Page 10)
	- -
	- -
		- Este  tipo  de  despliegues  son  ideales  para  las  pruebas  de  esta  fase.  Se  puede desplegar un entorno que simule lo más posible el de producción, aunque a menor escala, y ejecutar pruebas de acceso sobre él. En este caso, no se trata de comprobar vulnerabilidades a nivel de aplicación, sino de verificar que las reglas de firewall (o el objeto equivalente, como un grupo de seguridad) está configurado correctamente. Como estos entornos son privados, se pueden llevar a cabo escaneos de puertos sin afectar el funcionamiento del entorno de producción. #flashcard
		- (Page 10)
	- -
	- -
		- Las aplicaciones harán uso de algún tipo de persistencia, ya sea una base de datos desplegada ad hoc, una base de datos como servicio (por ejemplo, RDS en Amazon o MongoDB  Atlas)  o  un  almacenamiento  de  bloque  o  de  objeto  como  Amazon  S3  o Backblaze B2. Estos elementos deben ser también protegidos, por lo que las pruebas comprobarán que no se permite acceso sin credenciales, o que los puertos de la base de datos solo están abiertos a los servidores de la aplicación. #flashcard
		- (Page 11)
	- -
	- -
		- Si un atacante consigue acceder a una de las herramientas del  pipeline de CI/CD, cualquier otra medida que se haya implementado no servirá de nada. Da igual que todos  los  elementos  de  la  aplicación  estén  protegidos  y  las  pruebas  finalicen satisfactoriamente:  quien  tenga  acceso  completo  al  pipeline  puede  modificar  a  su gusto cualquier elemento de la aplicación o de la infraestructura. #flashcard
		  id:: a1f7f6c5-e7be-4eea-85f2-f0e0eea1cef2
		- (Page 11)
	- -
	- -
		- puntos en lo que habrá que prestar atención, por ejemplo:   En  todas  las  herramientas  habrá  que  configurar  el  acceso  basado  en  roles,  de manera que cada usuario reciba el mínimo conjunto de permisos necesarios.   Los  commits  deben  estar  firmados  para  evitar  que  se  incorporen  a  la  rama principal si son de un individuo ajeno a la organización o, en caso de que se lleguen a aceptar, tener la posibilidad de auditar su origen. #flashcard
		- (Page 12)
	- -
	- -
		- Algunas  de  las  buenas  prácticas  de  control  de  acceso,  no  solo  en  aplicaciones  de control de versiones, sino en cualquier sistema, son las siguientes:   Mantener la lista de usuarios con acceso ilimitado al repositorio lo más pequeña posible. Siempre es necesario que haya uno o varios administradores principales, pero no se debe caer en la tentación de dar acceso indiscriminado a los usuarios solo para facilitar la asignación de permisos. #flashcard
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
		- (Page 13)
	- -
	- -
		- Pero un atacante sería capaz de deshabilitar estas protecciones si consigue acceso al repositorio. La firma de commits con git proporciona una capa adicional. Git soporta la firma de commits y etiquetas con PGP. Esta funcionalidad consiste en aplicar firmas criptográficas  a  cada  parche,  commit  y  etiqueta,  utilizando  claves  que  los desarrolladores mantienen en secreto. #flashcard
		- (Page 13)
	- -
	- -
		- Los algoritmos que se usan no son diferentes a los que se usan en HTTPS, aunque las herramientas no son las mismas. Si los commits se firman con una clave válida dentro de la organización, se pueden considerar confiables. #flashcard
		- (Page 14)
	- -