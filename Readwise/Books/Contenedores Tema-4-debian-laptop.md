# Contenedores Tema-4

deck:: [[UNI::Contenedores Tema-4]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-4"\
category:: #books\
\
tags:: UNI Contenedores  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b65ef07b-020f-4fec-8edf-b02e6b2c6ae7.jpg)
## Highlights
- id:: 63639915-aced-4cff-9a3a-362ed4b473e4
   ¿Qué es **Docker Compose**? #flashcard 
    Docker Compose es una herramienta que nos permite simplificar el despliegue de aplicaciones multicontenedor como un único servicio, permitiéndonos gestionar fácilmente todo el ciclo de vida de los contenedores y otros objetos de la aplicación como volúmenes y redes. En lugar de crear nuestros propios scripts con llamadas al cliente de Docker para configurar y desplegar todos los objetos de nuestra aplicación (contenedores, redes, volúmenes, etc.), Docker Compose nos permite definir en ficheros YAML toda nuestra aplicación, su configuración y cómo se relacionan los objetos y sus dependencias. Será la propia herramienta Docker Compose la encargada de enviar las tareas necesarias a Docker Engine para crear los objetos y ejecutar los contenedores.
  
     (Page 5)
-
- id:: 63639915-50e9-4d27-a6d7-d7c8b93a1546
   Menciona tres ventajas de *Docker Compose* #flashcard 
    Algunas de las ventajas de los servicios de Docker Compose son:  Permite el despliegue en el mismo host de múltiples entornos aislados de nuestra aplicación multi contenedor. Cada uno de estos entornos será un servicio en Docker Compose con un nombre de proyecto asociado.  Al iniciar un servicio de Docker Compose se buscan ejecuciones anteriores de los contenedores manteniendo sus volúmenes de datos, de manera que no perdamos información.  Al reiniciar un servicio de Docker Compose, se reutilizan aquellos contenedores cuya configuración no ha sido modificada, recreando únicamente aquellos que han sido modificados, acelerando así el reinicio.
  
     (Page 5)
-
- id:: 63639915-32a7-42de-bc0e-e28eef45875e
   Nombra las secciones que tiene un fichero de Docker Compose #flashcard 
    Un fichero de Compose puede incluir las siguientes secciones a nivel raíz:  version. Indica la versión de Compose utilizada en el fichero.  services. Lista de servicios que componen nuestra aplicación.  volumes. Permite crear volúmenes que serán utilizados por los servicios.  networks. Permite crear volúmenes que serán utilizados por los servicios.
  
     (Page 7)
-
- id:: 63639915-a3e6-434f-8341-b6030c1f639f
  
  En el siguiente ejemplo se muestra el contenido de un sencillo fichero de Compose en el que se definen dos servicios: version: '3' services: web: build: . ports: - "5000:5000" redis: image: "redis:alpine" #flashcard 
  
  
     (Page 7)
-
- id:: 63639915-b1d0-4ac3-b00f-b0bcbcc070e2
   Sobre la opción expose de Docker Compose #flashcard 
    La opción expose permite exponer puertos sin publicarlos en el host. Solamente serían accesibles por los servicios enlazados. Veamos un par de formas de definirlos: expose: ["3000"] expose: - "3000" - "8000"
  
     (Page 9)
-
- id:: 63639915-e935-4a7e-810c-433ce193ca81
  
  sobrescribe a command. Las opciones command y entrypoint de Compose son equivalentes a las instrucciones CMD y ENTRYPOINT de los Dockerfiles que ya vimos. Recordemos que entrypoint #flashcard 
  
  
     (Page 9)
-
- id:: 63639915-ae3b-4b1f-895f-a7db8404fab1
   JUNTAR CON LO DE ARRIBA #flashcard 
    Veamos algún ejemplo de uso: command: /app/entrypoint.sh command: ["php", "-d", "vendor/bin/phpunit"] entrypoint: /app/start-service.sh entrypoint: [php, -d, vendor/bin/phpunit]
  
     (Page 10)
-
- id:: 63639915-ddc0-429c-88e3-37e5bb177699
   ¿Cómo se pueden definir variables de entorno en Docker Compose? #flashcard 
    Existen varias formas de pasar variables de entorno a los contenedores de los servicios. Podemos utilizar la configuración environment para indicar una lista de variables o bien la configuración env_file para múltiples variables de entorno definidas en un fichero externo: $ cat ./Docker/api/api.env $ cat docker-compose.yml NODE_ENV=test version: '3' services: api: image: 'node:6-alpine' env_file: - ./Docker/api/api.env environment: - NODE_ENV=production
  
     (Page 10)
-
- id:: 63639915-c961-42bb-81dd-edb3983590a0
   Orden de las variables de entorno en Docker Compose #flashcard 
    En caso de tener varias definiciones de la misma variable de entorno, Compose utilizará el siguiente orden para elegir qué valor utilizar:  Fichero de Compose.  Variables de entorno del Shell.  Fichero de variables de entorno.  Variables definidas en el Dockerfile.
  
     (Page 10)
-
- id:: 63639915-3edb-49be-8155-07287a37a3cf
   ¿Cómo puedo establecer **dependencias** entre servicios en **Docker Compose**? #flashcard 
    Para establecer dependencias entre servicios utilizaremos la opción depends_on, permitiendo que un servicio espere a que otros estén arrancados antes de empezar su ejecución. Veamos un ejemplo: services: web: build: . depends_on: - db - redis redis: image: redis db: image: postgres
  
     (Page 11)
-
- id:: 63639915-1d2f-429d-945e-16c371bc5396
   Acerca de montar volúmenes en un servicio con Docker Compose #flashcard 
    La opción volumes, dentro de la definición de un servicio, nos permite montar rutas del host en el contenedor o bien volúmenes a partir de su nombre. La sintaxis corta de esta opción nos permite utilizar el formato [ruta_host:]ruta_contenedor[:modo], mientras que la sintaxis larga permite configuraciones adicionales como por ejemplo el tipo de montaje.
  
     (Page 11)
-
- id:: 63639915-ce5b-4a8c-b4fc-80ad910d3488
   ¿Cómo puedo llamar a un volumen para un servicio en **Docker Compose**? #flashcard 
    Cuando referenciamos por nombre un volumen en la sección de los servicios, estos deben estar definidos en la sección volumes a nivel raíz del fichero de Compose. Esta sección nos permite la creación y definición de volúmenes asignado un nombre para poder ser referenciado en los servicios definidos. - datavolume:/var/lib/postgresql/data services: db: image: postgres volumes: volumes: datavolume: external:true
  
     (Page 12)
-
- id:: 63639915-c602-43b7-9793-3f22a2d59e94
  
  Tabla 1. Comandos de Docker Compose para la gestión de servicios. Fuente: elaboración propia. #flashcard 
  
  
     (Page 14)
-
- id:: 63639915-b42e-4684-9d4c-194d7013f28f
  
  Veamos un extracto del fichero Compose de la aplicación: - ./nginx/nginx.conf:/tmp/nginx.conf version: "3.7" services: web: image: nginx volumes: ... ports: - 80:80 depends_on: - backend backend: build: flask ... volumes: - ./flask:/src depends_on: - mongo mongo: #flashcard 
  
  
     (Page 15)
-
- id:: 63639915-b7fc-4ab2-9e49-8295150ad4a3
   <<<<<< #flashcard 
    image: mongo
  
     (Page 16)
-
- id:: 63639915-162a-4924-8709-7948535ce6d9
   INCLUIR IMAGEN #flashcard 
    La siguiente tabla describe las entradas y salidas de los comandos mencionados.
  
     (Page 23)
-