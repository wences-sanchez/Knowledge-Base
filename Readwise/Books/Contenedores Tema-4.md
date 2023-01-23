# Contenedores Tema-4

deck:: [[UNI::Contenedores Tema-4]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-4"\
category:: #books\
\
tags:: Contenedores UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b65ef07b-020f-4fec-8edf-b02e6b2c6ae7.jpg)
## Highlights
- id:: 63c669ee-577c-4298-850e-f08efb746134
   ¿Qué es **Docker Compose**? #flashcard 
    Docker Compose es una herramienta que nos permite simplificar el despliegue de aplicaciones multicontenedor como un único servicio, permitiéndonos gestionar fácilmente todo el ciclo de vida de los contenedores y otros objetos de la aplicación como volúmenes y redes. En lugar de crear nuestros propios scripts con llamadas al cliente de Docker para configurar y desplegar todos los objetos de nuestra aplicación (contenedores, redes, volúmenes, etc.), Docker Compose nos permite definir en ficheros YAML toda nuestra aplicación, su configuración y cómo se relacionan los objetos y sus dependencias. Será la propia herramienta Docker Compose la encargada de enviar las tareas necesarias a Docker Engine para crear los objetos y ejecutar los contenedores.
  
     (Page 5)
-
- id:: 63c669ee-7b08-4da3-855a-cd4dda5b64fe
   Menciona tres ventajas de *Docker Compose* #flashcard 
    Algunas de las ventajas de los servicios de Docker Compose son:  Permite el despliegue en el mismo host de múltiples entornos aislados de nuestra aplicación multi contenedor. Cada uno de estos entornos será un servicio en Docker Compose con un nombre de proyecto asociado.  Al iniciar un servicio de Docker Compose se buscan ejecuciones anteriores de los contenedores manteniendo sus volúmenes de datos, de manera que no perdamos información.  Al reiniciar un servicio de Docker Compose, se reutilizan aquellos contenedores cuya configuración no ha sido modificada, recreando únicamente aquellos que han sido modificados, acelerando así el reinicio.
  
     (Page 5)
-
- id:: 63c669ee-b49d-49b5-9bbb-29774ebf00dd
   Nombra las secciones que tiene un fichero de Docker Compose #flashcard 
    Un fichero de Compose puede incluir las siguientes secciones a nivel raíz:  version. Indica la versión de Compose utilizada en el fichero.  services. Lista de servicios que componen nuestra aplicación.  volumes. Permite crear volúmenes que serán utilizados por los servicios.  networks. Permite crear volúmenes que serán utilizados por los servicios.
  
     (Page 7)
-
- id:: 63c669ee-c51e-465d-b374-ed6b361c3350
  
  En el siguiente ejemplo se muestra el contenido de un sencillo fichero de Compose en el que se definen dos servicios: version: '3' services: web: build: . ports: - "5000:5000" redis: image: "redis:alpine" #flashcard 
  
  
     (Page 7)
-
- id:: 63c669ee-7609-4070-b145-2a18e25b17d8
   Sobre la opción expose de Docker Compose #flashcard 
    La opción expose permite exponer puertos sin publicarlos en el host. Solamente serían accesibles por los servicios enlazados. Veamos un par de formas de definirlos: expose: ["3000"] expose: - "3000" - "8000"
  
     (Page 9)
-
- id:: 63c669ee-6dda-4802-bb02-a4262bfeb351
  
  sobrescribe a command. Las opciones command y entrypoint de Compose son equivalentes a las instrucciones CMD y ENTRYPOINT de los Dockerfiles que ya vimos. Recordemos que entrypoint #flashcard 
  
  
     (Page 9)
-
- id:: 63c669ee-ddd4-4148-b5b2-58f21fd742ca
   JUNTAR CON LO DE ARRIBA #flashcard 
    Veamos algún ejemplo de uso: command: /app/entrypoint.sh command: ["php", "-d", "vendor/bin/phpunit"] entrypoint: /app/start-service.sh entrypoint: [php, -d, vendor/bin/phpunit]
  
     (Page 10)
-
- id:: 63c669ee-d1ae-4915-a7d6-25789df3e672
   ¿Cómo se pueden definir variables de entorno en Docker Compose? #flashcard 
    Existen varias formas de pasar variables de entorno a los contenedores de los servicios. Podemos utilizar la configuración environment para indicar una lista de variables o bien la configuración env_file para múltiples variables de entorno definidas en un fichero externo: $ cat ./Docker/api/api.env $ cat docker-compose.yml NODE_ENV=test version: '3' services: api: image: 'node:6-alpine' env_file: - ./Docker/api/api.env environment: - NODE_ENV=production
  
     (Page 10)
-
- id:: 63c669ee-51a3-4c22-ad8d-244071819a64
   Orden de las variables de entorno en Docker Compose #flashcard 
    En caso de tener varias definiciones de la misma variable de entorno, Compose utilizará el siguiente orden para elegir qué valor utilizar:  Fichero de Compose.  Variables de entorno del Shell.  Fichero de variables de entorno.  Variables definidas en el Dockerfile.
  
     (Page 10)
-
- id:: 63c669ee-a3de-4142-a3ec-5c283f2069f7
   ¿Cómo puedo establecer **dependencias** entre servicios en **Docker Compose**? #flashcard 
    Para establecer dependencias entre servicios utilizaremos la opción depends_on, permitiendo que un servicio espere a que otros estén arrancados antes de empezar su ejecución. Veamos un ejemplo: services: web: build: . depends_on: - db - redis redis: image: redis db: image: postgres
  
     (Page 11)
-
- id:: 63c669ee-f535-4710-ba70-ed968f1c4051
   Acerca de montar volúmenes en un servicio con Docker Compose #flashcard 
    La opción volumes, dentro de la definición de un servicio, nos permite montar rutas del host en el contenedor o bien volúmenes a partir de su nombre. La sintaxis corta de esta opción nos permite utilizar el formato [ruta_host:]ruta_contenedor[:modo], mientras que la sintaxis larga permite configuraciones adicionales como por ejemplo el tipo de montaje.
  
     (Page 11)
-
- id:: 63c669ee-f0dc-4339-a5df-b1405478f40b
   ¿Cómo puedo llamar a un volumen para un servicio en **Docker Compose**? #flashcard 
    Cuando referenciamos por nombre un volumen en la sección de los servicios, estos deben estar definidos en la sección volumes a nivel raíz del fichero de Compose. Esta sección nos permite la creación y definición de volúmenes asignado un nombre para poder ser referenciado en los servicios definidos. - datavolume:/var/lib/postgresql/data services: db: image: postgres volumes: volumes: datavolume: external:true
  
     (Page 12)
-
- id:: 63c669ee-2c31-4bb6-839f-a753b12af32c
  
  Tabla 1. Comandos de Docker Compose para la gestión de servicios. Fuente: elaboración propia. #flashcard 
  
  
     (Page 14)
-
- id:: 63c669ee-b9fc-4656-be38-b0d785338ca7
  
  Veamos un extracto del fichero Compose de la aplicación: - ./nginx/nginx.conf:/tmp/nginx.conf version: "3.7" services: web: image: nginx volumes: ... ports: - 80:80 depends_on: - backend backend: build: flask ... volumes: - ./flask:/src depends_on: - mongo mongo: #flashcard 
  
  
     (Page 15)
-
- id:: 63c669ee-5f08-4917-9221-8b9aceaa0529
   <<<<<< #flashcard 
    image: mongo
  
     (Page 16)
-
- id:: 63c669ee-c862-4e30-ab21-4fa74855b43c
   INCLUIR IMAGEN #flashcard 
    La siguiente tabla describe las entradas y salidas de los comandos mencionados.
  
     (Page 23)
-