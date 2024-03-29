title:: Contenedores Tema-2 (highlights)
deck:: [[UNI::Contenedores Tema-2]]
author:: [[UNIR]]
full-title:: "Contenedores Tema-2"
category:: #books

tags:: Contenedores UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/68232f67-c7d9-423d-bccf-79f4a9e5a0f8.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Los contenedores de Docker están basados en imágenes previamente generadas que contienen  todas  las  dependencias  necesarias  para  nuestra  aplicación  o  servicio. Aunque existen de manera pública multitud de imágenes listas para ser utilizadas, la mayoría de las veces necesitaremos crear nuestras propias imágenes, habitualmente basada en alguna ya disponible. A lo largo del tema se presentarán las principales opciones que tenemos para generar nuestras propias imágenes según nuestras necesidades y las buenas prácticas que deberemos  seguir  para  generar  unas  imágenes  ligeras  y  fácilmente  mantenibles. También veremos los diferentes tipos de capas y sus características que nos podemos encontrar en las imágenes y contenedores. #flashcard
		  id:: d49611d0-ce7d-43c8-9531-53c626a6a67c
		- (Page 4)
	- -
	- -
		- Para  poder  ejecutar  contenedores  con  nuestras  aplicaciones  primero  deberemos crear la imagen Docker de nuestra aplicación, la cual contendrá tanto el código de nuestra  aplicación,  como  todas  las  dependencias  necesarias  para  su  ejecución.  En Docker existen varias formas de crear imágenes:   A partir de una imagen vacía: copiando directamente el sistema de ficheros en ella.  Docker  nos  permite  crear  nuestras  imágenes  desde  cero,  utilizando  como base una imagen oficial de Docker llamada scratch publicada expresamente para   Usando comandos de Docker: a partir de un contenedor en ejecución podemos configurar todo lo necesario en él y crear una imagen de su estado actual con el este propósito. comando docker commit.   A partir de ficheros Dockerfile: los ficheros Dockerfile nos permiten definir una lista de acciones ordenadas para construir una imagen de Docker con el comando docker build. Este será el método más habitual y deseable.   Con  herramientas  de  gestión  de  configuración:  a  veces  necesitaremos  generar imágenes  de  cierta  complejidad,  en  estos  casos  es  posible  utilizar  alguna herramienta de gestión de configuración como, por ejemplo, Puppet, combinada con ficheros Dockerfile. #flashcard
		  id:: b1dc90a6-be57-46e3-8496-02084b06c242
		- (Page 5)
	- -
	- -
		- ¿Qué es una *imágen* en Docker? #flashcard
		  id:: 0e378652-4bc8-4063-9af2-3f9840ad7e3e
			- Las imágenes de Docker están formadas por un conjunto de capas de imagen. Estas capas forman una serie de imágenes intermedias, apiladas una encima de otra, donde cada  capa  depende de  la  capa  inmediatamente debajo  de ella.  Cada  una  de  estas capas de la imagen solamente incluyen los cambios respecto a la anterior, es decir lo que modificamos, añadimos o eliminamos. Docker utiliza sistemas de archivos Union (UnionFS) para combinar todas las capas de la imagen. La  jerarquía  de  las  capas  es  clave  para  una  gestión  eficiente  del  ciclo  de  vida  las imágenes,  ya  que  siempre  deberemos  intentar  situar  las  capas  que  cambian  con mayor frecuencia lo más alto posible en la pila. Esto se debe a que, cuando hacemos cambios en una determinada capa, Docker no solo reconstruye esa, sino todas las capas creadas a partir de ella.
		- (Page 6)
	- -
	- -
		- Cada vez que Docker crea un contenedor a partir de una imagen, se añade una capa de escritura o de contenedor que almacena todos los cambios que se realizan en el contenedor durante su ejecución. Esta capa de contenedor o escritura es la única diferencia entre un contenedor en ejecución  y  la  imagen  de  Docker.  Todos  los  contenedores  similares  que  se  lancen compartirán  el  acceso  a  las  mismas  capas  de  imagen  subyacentes  mientras  se mantiene su propio estado individual con su propia capa de escritura. #flashcard
		  id:: 27d701e7-14f3-4896-9eeb-4466ae7223c8
		- (Page 6)
	- -
	- -
		- AÑADIR IMAGEN #flashcard
		  id:: 056a7d05-c2bf-476c-8cfa-48341bd75e15
			- t
		- (Page 6)
	- -
	- -
		- Las  capas  de  imagen de  Docker  son de  solo lectura  e  inmutables,  lo  cual  permite gestionar el problema de almacenamiento que tendríamos al usar contenedores a gran escala si cada uno de ellos necesitara tener una copia de la imagen. Docker  usa  internamente  un  mecanismo  de  copia  en  escritura  o  copy-on-write (CoW) para reducir la cantidad de espacio en disco requerido. De manera que si un fichero  existe  en  una  capa  inferior  de  la  imagen  y  otra  capa  (ya  sea  durante  la construcción de la imagen o la ejecución del contenedor) necesita leer dicho fichero, simplemente utilizará el ya existente en la capa inferior. Pero en caso de necesitar realizar cambios en el fichero, este se copiará primero en la capa actual y después será modificado. Esto explica (en parte) cómo los contenedores pueden iniciarse tan rápido. No tienen nada que copiar porque toda la información inicial ya está almacenada en la imagen y es accesible por el contenedor, y solamente haría falta crear la capa de contenedor o escritura. #flashcard
		  id:: 1a87950e-7865-4ef6-98a9-be807d15f3fc
		- (Page 7)
	- -
	- -
		- ¿Cómo construirías una imágen de Docker a través de la línea de comandos? #flashcard
		  id:: caa4e844-1694-4189-b906-635529504fc4
			- $ docker build -t nombre-imagen .
		- (Page 8)
	- -
	- -
		- Imaginemos  que  tenemos  un  contenedor  ejecutándose  en  nuestro  entorno  de desarrollo  y  queremos  guardar  su  estado  antes de  realizar algunos  cambios  por  si queremos volver a dicho estado. Para ello utilizaremos el comando  docker  commit que  guardará  el  estado  actual  del  contenedor  en  una  imagen,  devolviendo  el identificador de esta. #flashcard
		  id:: 852c2f36-d687-44ed-99e7-039c72873214
		- (Page 9)
	- -
	- -
		- cómo  podemos  crear  un  contenedor  interactivo  de  manera sencilla. Si ejecutamos el siguiente comando, se nos descargará una imagen Docker de Ubuntu y nos dejará abierto un terminal dentro del contenedor: $ docker run -it ubuntu:bionic /bin/bash root@0ef5d5b9795d:/# #flashcard
		  id:: f6bc220f-b16f-431d-85dc-4808c46ae889
		- (Page 9)
	- -
	- -
		- ¿Cómo podrías guardar el estado actual de un contendor en *Docker* a través de la línea de comandos? #flashcard
		  id:: 35716445-28e9-48f0-bffd-b014490ab7c2
			- Si quisiéramos guardar el estado del contenedor que acabamos de crear, podríamos ejecutar desde un nuevo terminal de nuestra maquina el comando  docker  commit para  persistir  el  estado  actual  del  contenedor.  Será  necesario indicarle  el identificador o nombre del contenedor y, opcionalmente, el nombre que queremos darle a nueva imagen: $ docker commit 0ef5d5b9795d myapp:version1 sha256:cd6827d1d4f348ea41fcafa55c49cd76354706f8860f244852329df16008e86a
		- (Page 10)
	- -
	- -
		- ¿Cómo podrías nombrar (o etiquetar) una *imagen* en Docker? #flashcard
		  id:: 43b395fd-2d9c-4366-8850-d8de99592461
			- $ docker tag ca76b45144f2cb3 nombreimagen Si miramos la ayuda del comando docker  tag y revisamos su sintaxis, veremos que además podemos indicar una etiqueta: $ docker tag --help Usage: docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG] Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
		- (Page 11)
	- -
	- -
		- debemos  conocer  la  terminología  utilizada  por  Docker  en  las imágenes:   Identificador de imagen: se refiere a una capa específica de la imagen, que es de solo lectura y tiene asociado un identificador único.   Etiqueta: se trata de un modificador del nombre de la imagen. Podemos utilizar las  etiquetas  para  indicar  la  versión,  la  distribución  del  sistema  operativo  que utiliza, etc. Ejemplos: latest, stable, 4.1-bionic, 4.0-windowsservercore-1809   Repositorio:  colección  de  imágenes  etiquetadas.  Por  ejemplo,  el  repositorio ubuntu del registro Docker Hub estaría formado por las imágenes ubuntu:latest, ubuntu:18.04, ubuntu:trusty, etc. #flashcard
		  id:: 5b8f09b5-6b83-4284-8cd8-cf56c0da8b4c
		- (Page 11)
	- -
	- -
		- <<<<< #flashcard
		  id:: 0c80aab1-ffcc-4824-8668-6dd19e805fc1
			-   Imagen  o  nombre  de  imagen:  al  referenciar  una  imagen  podemos  utilizar  su identificador único o bien un nombre de imagen que estará compuesto por varios componentes: [<host-registro>/][<usuario>/]<repositorio>[:<etiqueta>] •  El registro es opcional y por defecto tendremos configurado Docker Hub. •  El usuario también es opcional y sería un usuario del registro. •  El nombre del repositorio es obligatorio. •  Si omitimos la etiqueta de la imagen se asumirá latest por defecto.
		- (Page 12)
	- -
	- -
		- ¿Cómo puedes mostrar las imágenes que hay, en Docker? #flashcard
		  id:: 00746424-12ec-4577-a00c-1e783012380c
			- $ docker images nginx REPOSITORY     TAGIMAGE ID       CREATED        SIZE nginx          alpine7d0cdcc60a96   4 weeks ago    21.3MB
		- (Page 13)
	- -
	- -
		- ¿Con qué comando borrarías una *imagen* en Docker? #flashcard
		  id:: b879141c-433a-4857-99ec-6d51445b0877
			- $ docker rmi nginx:alpine Untagged: nginx:alpine
		- (Page 13)
	- -
	- -
		- ¿Cómo podemos eliminar las imágenes en Docker que *estén en desuso*? #flashcard
		  id:: fa5026e3-9715-49ab-8e8d-2cd1a81352c4
			- Con  el  comando  docker  image  prune  podemos  eliminar  todas  las  imágenes consideradas  colgantes  o  dangling.  Si  además  indicamos  la  opción  -a  también  se eliminarán aquellas imágenes que no estén siendo utilizadas por ningún contenedor. $ docker image prune -a
		- (Page 14)
	- -
	- -
		- <<<<<<<< #flashcard
		  id:: 63df2980-8b76-4cd9-ae06-529cf0f3a39b
			- Debemos tener en cuenta que no es posible eliminar una imagen si todavía la está usando  alguno  de  nuestros  contenedores.  El  comando  docker  rmi  devolvería  un mensaje de error indicando qué contenedor está basado en la imagen que queremos eliminar.
		- (Page 14)
	- -
	- -
		- ¿Cómo podemos listar las imágenes de Docker *en desuso*? #flashcard
		  id:: ff3e9900-a64f-4f5f-a881-16fe87077a53
			- Las imágenes colgantes o dangling son aquellas capas que no tienen relación con ninguna imagen etiquetada. Es decir, capas que ya no tienen un propósito y, sin embargo, consumen espacio en disco. Podemos listar las imágenes consideradas como dangling usando el filtro correspondiente: $ docker images -f dangling=true REPOSITORY    TAG           IMAGE ID       CREATED       SIZE <none>        <none>        6c74ebae8348   11 days ago   121MB <none>        <none>        9add3a1309ff   11 days ago   220MB <none>        <none>        68c326a1ee8e   11 days ago   108MB
		- (Page 14)
	- -
	- -
		- AÑADIR IMAGEN #flashcard
		  id:: 14b0663d-2e80-46f5-a82d-55f902d1e30e
			- La siguiente tabla resume las instrucciones más comúnmente utilizadas en nuestros ficheros Dockerfile:
		- (Page 16)
	- -
	- -
		- ¿Cómo podemos ver las diferentes capas de una *imagen* en **Docker**? #flashcard
		  id:: 5a4657b8-9cf0-42ba-a35e-67adb9f49531
			- $ docker image history python_app:latest IMAGE                              CREATED                          CREATED  BY podemos  ver  las diferentes capas que componen una imagen utilizando el comando docker history: SIZE 0B 0B 0B ... 859fb1db4a90        3 minutes ago       /bin/sh -c #(nop)  CMD ["python" "./server.p…   0B 867e1b296ff9        3 minutes ago       /bin/sh -c #(nop)  EXPOSE 5000:5000 2cf8552ed9ca                3  minutes  ago              /bin/sh  -c  #(nop)  COPY 45dd0cfd49a7                3  minutes  ago              /bin/sh  -c  pip  install  -r 9c7c03f19b8a                3  minutes  ago              /bin/sh  -c  #(nop)  COPY dir:9b3e3bb266ad8957c…   164B requirements.txt      9.63MB file:dcf08683799a1e65…   13B 5a3811ed82ae        3 minutes ago          /bin/sh  -c #(nop) WORKDIR /code 79cc46abd78d        5 days ago          /bin/sh -c #(nop)  CMD ["python3"] <missing>           5 days ago          /bin/sh -c set -ex;   wget -O get pip.py "$P…   7.24MB
		- (Page 19)
	- -
	- -
		- La mayoría de las veces, la caché nos será muy útil y nos ahorrará mucho tiempo al generar imágenes. Sin embargo, hay ocasiones en las que el comportamiento de la caché puede no actuar como nosotros deseamos, por lo que es bueno saber cómo invalidar selectivamente la caché en nuestro Dockerfile. La solución más radical sería utilizar el argumento  --no-cache, el cual invalidaría la cache para todos los pasos de nuestro Dockerfile: $ docker build -t python_app --no-cache . Una manera de forzar que se invalide la caché en una instrucción que está utilizando la cache, sería añadiendo un comentario al final de la instrucción para así modificar la línea e invalidarla. Por ejemplo: RUN ["pip", "install", "-r", "requirements.txt"] # Invalidar cache #flashcard
		  id:: 192a46b1-6033-4368-89fe-9a346006534f
		- (Page 20)
	- -
	- -
		- Explica las etapas en los **Dockerfile**. #flashcard
		  id:: 5f3519e0-0bb2-4e0e-b85f-9f494d5d90f9
			- La construcción en múltiples etapas o multi-stage builds es una nueva funcionalidad de introducida en la versión 17.05 que nos permite optimizar y reducir la complejidad de nuestros Dockerfiles. Para  definir las  etapas  utilizaremos  múltiples  sentencias  FROM en  el  mismo  fichero Dockerfile. Cada sentencia FROM iniciará un nuevo proceso de construcción y puede utilizar una imagen base distinta. Además, podremos copiar ficheros de una etapa anterior a la actual con la instrucción COPY, referenciando la etapa origen con --from. Las  etapas  se  numeran  partiendo  desde  cero,  pero  podemos  darles  un  nombre añadiendo AS name al final de la instrucción FROM. En el siguiente Dockerfile de ejemplo podemos ver cómo se utiliza una primera etapa para compilar una aplicación en Go, utilizando la imagen golang como base. En una segunda etapa simplemente copiamos el ejecutable sobre la imagen base alpine. Esto nos  permite  quedarnos solamente  con  los  artefactos  que queramos  de la  primera etapa, reduciendo así el tamaño final de la imagen. FROM golang:1.7.3 AS builder WORKDIR /go/src/github.com/alexellis/href-counter/ RUN go get -d -v golang.org/x/net/html COPY app.go . RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o app . FROM alpine:latest RUN apk --no-cache add ca-certificates WORKDIR /root/ CMD ["./app"] COPY --from=builder /go/src/github.com/alexellis/href-counter/app .
		- (Page 21)
	- -
	- -
		- podríamos compartir un fichero Dockerfile para que los equipos de desarrollo los incluyan en sus propias aplicaciones. Sin embargo, esta solución sería manual,  poco  sostenible  y  bastante  propensa  a  errores.  Para  situaciones  como  la descrita, tenemos la instrucción ONBUILD de Dockerfile. #flashcard
		  id:: 60235357-ffc1-4e72-9a87-0e5f781fbaa6
		- (Page 22)
	- -
	- -
		- A  veces  generaremos  imágenes  que  servirán  como  plantillas  reutilizables  y podríamos  querer,  o  necesitar,  que  algunas  configuraciones  de  la  aplicación  se realicen  más  adelante,  cuando  se  utilice  la  imagen  como  base  para  una  nueva imagen. En estos casos, podríamos compartir un fichero Dockerfile para que los equipos de desarrollo los incluyan en sus propias aplicaciones. Sin embargo, esta solución sería manual,  poco  sostenible  y  bastante  propensa  a  errores.  Para  situaciones  como  la descrita, tenemos la instrucción ONBUILD de Dockerfile. #flashcard
		  id:: b754e2b5-7931-41af-8c2b-ced24d8cec49
		- (Page 22)
	- -
	- -
		- Para aprovechar mejor la caché a la hora de generar las imágenes, se recomienda separar  la  instalación  de  dependencias  de  la  obtención  de  cambios  en  el  código fuente. Esto se debe a que las dependencias cambian con menor frecuencia y no nos hará falta obtenerlas cada vez que se actualiza el código. #flashcard
		  id:: a2bcf62e-8330-4158-be7b-75ef34b311c6
		- (Page 26)
	- -
	- -
		- Además de nombrar y etiquetar nuestras imágenes podremos compartirlas con otras personas publicándolas en repositorios de los  registros Docker, ya sean públicos o privados, a través del comando docker push. #flashcard
		  id:: 22be138a-0b76-4a66-94a1-958121cdd001
		- (Page 29)
	- -