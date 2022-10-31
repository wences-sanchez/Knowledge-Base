title:: Contenedores Tema-4 (highlights)
deck:: [[UNI::Contenedores Tema-4]]
author:: [[UNIR]]
full-title:: "Contenedores Tema-4"
category:: #books

tags:: Contenedores UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b65ef07b-020f-4fec-8edf-b02e6b2c6ae7.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Qué es **Docker Compose**? #flashcard
		  id:: 19316aa7-a68d-484d-a479-c907b7ae53c4
			- Docker Compose es una herramienta que nos permite simplificar el despliegue de aplicaciones  multicontenedor  como  un  único  servicio,  permitiéndonos  gestionar fácilmente todo el ciclo de vida de los contenedores y otros objetos de la aplicación como volúmenes y redes. En  lugar  de  crear  nuestros  propios  scripts  con  llamadas  al  cliente  de  Docker  para configurar y desplegar todos los objetos de nuestra aplicación (contenedores, redes, volúmenes,  etc.),  Docker  Compose  nos  permite  definir  en  ficheros  YAML  toda nuestra  aplicación,  su  configuración  y  cómo  se  relacionan  los  objetos  y  sus dependencias. Será la propia herramienta Docker Compose la encargada de enviar las  tareas  necesarias  a  Docker  Engine  para  crear  los  objetos  y  ejecutar  los contenedores.
		- (Page 5)
	- -
	- -
		- Menciona tres ventajas de *Docker Compose* #flashcard
		  id:: deda0fc7-e2a4-46c7-83a0-3aee68bcbe58
			- Algunas de las ventajas de los servicios de Docker Compose son:   Permite el despliegue en el mismo host de múltiples entornos aislados de nuestra aplicación  multi  contenedor.  Cada  uno  de  estos  entornos  será  un  servicio  en Docker Compose con un nombre de proyecto asociado.   Al iniciar un servicio de Docker Compose se buscan ejecuciones anteriores de los contenedores manteniendo sus volúmenes de datos, de manera que no perdamos información.   Al reiniciar un servicio de Docker Compose, se reutilizan aquellos contenedores cuya  configuración  no  ha  sido  modificada,  recreando  únicamente  aquellos  que han sido modificados, acelerando así el reinicio.
		- (Page 5)
	- -
	- -
		- Nombra las secciones que tiene un fichero de Docker Compose #flashcard
		  id:: 159ad1ab-69b8-4ba6-8d80-2a3ae09d3995
			- Un fichero de Compose puede incluir las siguientes secciones a nivel raíz:   version. Indica la versión de Compose utilizada en el fichero.   services. Lista de servicios que componen nuestra aplicación.   volumes. Permite crear volúmenes que serán utilizados por los servicios.   networks. Permite crear volúmenes que serán utilizados por los servicios.
		- (Page 7)
	- -
	- -
		- En el siguiente ejemplo se muestra el contenido de un sencillo fichero de Compose en el que se definen dos servicios: version: '3' services: web: build: . ports: - "5000:5000" redis: image: "redis:alpine" #flashcard
		  id:: 7a9f0b86-cc2c-446b-88f6-36695c12081d
		- (Page 7)
	- -
	- -
		- Sobre la opción expose de Docker Compose #flashcard
		  id:: a18d968d-c77e-4127-8327-46c8fcc2737f
			- La  opción  expose  permite  exponer  puertos  sin  publicarlos  en  el  host.  Solamente serían accesibles por los servicios enlazados. Veamos un par de formas de definirlos: expose: ["3000"] expose: - "3000" - "8000"
		- (Page 9)
	- -
	- -
		- sobrescribe a command. Las opciones command y entrypoint de Compose son equivalentes a las instrucciones CMD  y  ENTRYPOINT  de  los  Dockerfiles  que  ya  vimos.  Recordemos  que  entrypoint #flashcard
		  id:: 8a293e8f-7487-4b01-80d8-aa799f3ea7db
		- (Page 9)
	- -
	- -
		- JUNTAR CON LO DE ARRIBA #flashcard
		  id:: d670f9e1-e61a-4b7c-a69c-815bfaf6f630
			- Veamos algún ejemplo de uso: command: /app/entrypoint.sh command: ["php", "-d", "vendor/bin/phpunit"] entrypoint: /app/start-service.sh entrypoint: [php, -d, vendor/bin/phpunit]
		- (Page 10)
	- -
	- -
		- ¿Cómo se pueden definir variables de entorno en Docker Compose? #flashcard
		  id:: 062cb10e-d5f1-4bef-9beb-26c052b2b404
			- Existen  varias  formas  de  pasar  variables  de  entorno  a  los  contenedores  de  los servicios.  Podemos  utilizar  la  configuración  environment  para  indicar  una  lista  de variables  o  bien  la  configuración  env_file  para  múltiples  variables  de  entorno definidas en un fichero externo: $ cat ./Docker/api/api.env $ cat docker-compose.yml NODE_ENV=test version: '3' services: api: image: 'node:6-alpine' env_file: - ./Docker/api/api.env environment: - NODE_ENV=production
		- (Page 10)
	- -
	- -
		- Orden de las variables de entorno en Docker Compose #flashcard
		  id:: 32925311-2220-44e1-b60a-71d8fb5655e0
			- En  caso  de  tener  varias  definiciones  de  la  misma  variable  de  entorno,  Compose utilizará el siguiente orden para elegir qué valor utilizar:   Fichero de Compose.   Variables de entorno del Shell.   Fichero de variables de entorno.   Variables definidas en el Dockerfile.
		- (Page 10)
	- -
	- -
		- ¿Cómo puedo establecer **dependencias** entre servicios en **Docker Compose**? #flashcard
		  id:: 47f8371e-6437-4dfc-b249-ee2918013962
			- Para  establecer  dependencias  entre  servicios  utilizaremos  la  opción  depends_on, permitiendo que un servicio espere a que otros estén arrancados antes de empezar su ejecución. Veamos un ejemplo: services: web: build: . depends_on: - db - redis redis: image: redis db: image: postgres
		- (Page 11)
	- -
	- -
		- Acerca de montar volúmenes en un servicio con Docker Compose #flashcard
		  id:: ad711eae-8f7a-42d0-b120-8ded46bc7cb3
			- La opción volumes, dentro de la definición de un servicio, nos permite montar rutas del host en el contenedor o bien volúmenes a partir de su nombre. La sintaxis corta de esta opción nos permite utilizar el formato [ruta_host:]ruta_contenedor[:modo], mientras que la sintaxis larga permite configuraciones adicionales como por ejemplo el tipo de montaje.
		- (Page 11)
	- -
	- -
		- ¿Cómo puedo llamar a un volumen para un servicio en **Docker Compose**? #flashcard
		  id:: 32324ca3-3fb4-4f77-ba5d-0cc4ed042f8b
			- Cuando referenciamos por nombre un volumen en la sección de los servicios, estos deben estar definidos en la sección volumes a nivel raíz del fichero de Compose. Esta sección nos permite la creación y definición de volúmenes asignado un nombre para poder ser referenciado en los servicios definidos. - datavolume:/var/lib/postgresql/data services: db: image: postgres volumes: volumes: datavolume: external:true
		- (Page 12)
	- -
	- -
		- Tabla 1. Comandos de Docker Compose para la gestión de servicios. Fuente: elaboración propia. #flashcard
		  id:: c6f12c4c-10ba-46cc-8c2c-93a761034b18
		- (Page 14)
	- -
	- -
		- Veamos un extracto del fichero Compose de la aplicación: - ./nginx/nginx.conf:/tmp/nginx.conf version: "3.7" services: web: image: nginx volumes: ... ports: - 80:80 depends_on: - backend backend: build: flask ... volumes: - ./flask:/src depends_on: -  mongo mongo: #flashcard
		  id:: 340a1433-885a-4778-9bf1-8316fbcd9b75
		- (Page 15)
	- -
	- -
		- <<<<<< #flashcard
		  id:: e9e97855-d371-40bc-9eee-1bae6b45f7f8
			- image: mongo
		- (Page 16)
	- -
	- -
		- INCLUIR IMAGEN #flashcard
		  id:: 11f905b6-d66d-4a7d-906a-fbbca1cadde1
			- La siguiente tabla describe las entradas y salidas de los comandos mencionados.
		- (Page 23)
	- -