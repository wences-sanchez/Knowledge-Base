title:: Contenedores Tema-3 (highlights)
author:: [[UNIR]]
full-title:: "Contenedores Tema-3"
category:: #books

tags:: #[[Contenedores]] #[[UNI]]

- #tags #[[Contenedores]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/12d87d45-655c-4203-9630-83f9afcbd8cd.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- INCLUIR IMAGEN #flashcard
		- La siguiente figura resume los diferentes estados de un contenedor y qué comandos provocan los cambios de éstos:
		- (Page 5)
	- <<<<<<<<<< #flashcard
		-   Created: el contenedor ha sido creado, pero aún no se ha iniciado su ejecución.   Restarting: el contenedor está en proceso de reinicio.   Started: el contenedor se encuentra actualmente en ejecución.   Paused: los procesos del contenedor han sido pausados.   Exited: la ejecución del contenedor ha finalizado.   Dead: cuando encontramos este estado generalmente es porque el demonio no pudo detener ordenadamente el contenedor.
		- (Page 6)
	- ¿Cómo puedo ejecutar un contenedor *Docker*? #flashcard
		- Tenemos  dos  opciones  para  ejecutar  nuestros  contenedores.  Podríamos  crearlos primero  con  docker  create,  quedando  el  contenedor  en  estado  created,  y posteriormente iniciarlo con docker start. O bien, directamente utilizar el comando docker  run  que  crearía  el  contenedor  e  iniciaría  su  ejecución.  Esta  última  será  la opción que normalmente utilizaremos. Al ejecutar un contenedor con docker run podemos indicar una serie de opciones de configuración,  seguido  de  la  imagen  que  se  utilizará  para  crearlo.  Por  último, indicaríamos  el  comando  a  ejecutar.  Si  no  indicamos  ninguno,  se  ejecutará  el establecido por defecto en la imagen. La sintaxis es la siguiente: docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
		- (Page 6)
	- ¿Cómo puedo hacer para que un contenedor se ejecute, pero en segundo plano? #flashcard
		- Si ejecutamos el comando  docker  run con la opción  -d o  --detach, el contenedor iniciará su ejecución, pero lo hará en segundo plano, quedando así el terminal libre. El comando simplemente imprimirá el identificador del contenedor creado.
		- (Page 7)
	- ¿Cómo puedo hacer que un contenedor se ejecute, pero pudiendo interactuar con él y con su terminal también? #flashcard
		- Si  lo  que  queremos  es  interactuar  con  el  contenedor  que  estamos  creando, manteniendo la entrada estándar abierta y creando un terminal para ella, podemos utilizar la opción -it. $ docker run -it alpine sh / # ls / # exit $ bin    dev    etc    home   lib    media  ...
		- (Page 7)
	- Exposición de puertos Cuando utilizamos la instrucción EXPOSE en un Dockerfile, esta indica que podemos conectarnos  al  servicio  del  contenedor  en  el  puerto  indicado.  Sin  embargo,  no  se realiza ninguna configuración de red por defecto. Dos contenedores que estén en la misma red sí que se podrán comunicar a través de los puertos expuestos, pero dichos puertos no serán accesibles desde fuera del contenedor. Para publicar en el host los puertos expuestos en la imagen utilizaremos las siguientes opciones:   -p, --publish. Publica un puerto del contenedor al host.   -P,  --publish-all.  Publica  todos  los  puertos  expuestos  en el  contenedor  a  un puerto aleatorio del host. #spaced
		- (Page 8)
	- Veámoslo con un ejemplo. La imagen de nginx tiene expuesto el puerto ochenta, si al crear el contenedor no los publicamos entonces lo veremos como disponible, pero solo dentro de la red del contenedor. Con las opciones -p y -P vemos como sí están disponibles en el host: $ docker run -d --name contA nginx:alpine $ docker run -d --name contB -P nginx:alpine $ docker run -d --name contC -p 8080:80 nginx:alpine $ docker ps CONTAINER ID    IMAGE             ...    PORTS                    NAMES 8f7cb48b9141    nginx:alpine             80/tcp                   contA 0da034beb842    nginx:alpine             0.0.0.0:32768->80/tcp    contB 2a3cd13b135c    nginx:alpine             0.0.0.0:8080->80/tcp     contC #spaced
		- (Page 9)
	- <<<<<<< #flashcard
		- /
		- (Page 9)
	- Listar los contenedores existentes Una vez creados nuestros contenedores, podremos listar los que están actualmente en ejecución con el comando docker ps. Si queremos ver también los que están en otros estados podemos utilizar la opción -a: #spaced
		- (Page 9)
	- ¿Cómo podemos parar *manualmente* la ejecución de un contenedor? #flashcard
		- Podemos detener manualmente la ejecución de un contenedor con cualquiera de los siguientes comandos:   docker kill. Envía la señal SIGKILL al contendor.   docker  stop.  Envía  la  señal  SIGTERM  y,  tras  un  periodo  de  prórroga  de  diez segundos, envía la señal SIGKILL si el contenedor sigue en ejecución.   docker pause. Envía la señal SIGSTOP, pausando los procesos en ejecución.
		- (Page 10)
	- ¿Cómo podemos acceder al terminal de un contenededor *Docker* en ejecución? #flashcard
		- Si  lo  que  queremos  es  acceder  al  terminal  de  un  contenedor  en  ejecución, utilizaremos el comando docker  attach, indicando el nombre del contenedor o su identificador.  Este  comando  no  crea  un  nuevo  proceso,  sino  que  accedemos  al terminal que tenemos en ejecución. Esto quiere decir que si salimos con el comando exit la ejecución del contenedor finalizaría. $ docker attach contenedora
		- (Page 11)
	- ¿Cómo podemos acceder a los logs de un contenedor *Docker*? #flashcard
		- Podemos  acceder  fácilmente  a  los  logs  de  un  contenedor  en  ejecución  con  el comando docker logs indicando el nombre o identificador del contenedor. Además, si especificamos la opción -t obtendremos el timestamp en la salida, y con -f se irá actualizando automáticamente. Veamos un ejemplo: $ docker logs -ft 3d518bfea9dd 2020-08-30T09:36:14.209496900Z /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration ...
		- (Page 12)
	- ¿Cuáles son las cuatro *políticas de reinicio* disponibles en **Docker**? #flashcard
		- Las políticas de reinicio disponibles son las siguientes:   no. No reinicia en ningún caso el contenedor. Es el valor por defecto.   on-failure.  Reinicia  automáticamente  en  caso  de  error,  es  decir  cuando  el contenedor termine con un código de error distinto de cero.   always.  Siempre  reiniciará  el  contenedor.  Sin  embargo,  en  caso  de  haberlo detenido manualmente se iniciará en próximo reinicio del demonio de Docker.   unless-stop. Es similar a always, excepto cuando el contenedor es parado, ya sea manualmente u otro motivo.
		- (Page 14)
	- Nombra los tres tipos de montaje de sistemas de ficheros de Docker.
	  
	  AÑADIR IMAGEN #flashcard
		-   volumes.  Gestionado  por  Docker.  Desde  el  anfitrión  no  podemos  modificar directamente los ficheros, solamente a través de comandos de Docker.   bind mounts. El almacenamiento se encuentra en cualquier parte del sistema de ficheros anfitrión. Los procesos del sistema anfitrión pueden modificarlos.   tmpfs  mounts.  No  se persiste  en  disco,  ya  que  se  encuentra  en  la  memoria  del sistema anfitrión.
		- (Page 16)
	- Los  volumes  son  la  manera  recomendada  en  Docker  de  persistir  los  datos  de nuestros contenedores. Algunas de sus principales ventajas son:   Las copias de seguridad y migración a otros hosts son sencillas.   Podemos gestionarlos tanto con comandos de Docker como mediante su API.   Funcionan en Linux y Windows.   Se pueden compartir de manera más segura entre múltiples contenedores.   Existen  controladores  que  nos  permitirán  tenerlos  en  hosts  remotos  o  añadir características como, por ejemplo, cifrar su contenido. #spaced
		- (Page 17)
	- Ejemplos de comandos de Docker Volume
	  
	  AÑADIR IMAGEN #flashcard
		- $ docker volume create mis-datos mis-datos $ docker volume ls DRIVER              VOLUME NAME local               mis-datos
		- (Page 17)
	- Maneras de montar un volume a Docker mediante la CLI. #flashcard
		- Para ejecutar un contenedor montando en el nuestro volumen de datos utilizaremos el comando docker run con la opción --mount o -v. Ambas opciones permiten hacer prácticamente  lo  mismo,  pero  tienen  diferente  sintaxis.  La  opción  --mount es  más explícita y la recomendada por Docker. Veamos ambas sintaxis: Con la opción --mount indicaremos pares clave-valor separados por coma. Las claves que podemos utilizar son:   type. Puede valer volume, bind o tmpfs.   source o src. Nombre del volumen que queremos montar. Si se omite se creará   target,  destination o  dst.  Ruta  dentro  del  contenedor  donde  se  montarán  los un volumen anónimo. datos.   readonly. Si se especifica se montará como solo lectura dentro del contenedor. Por otro lado, con la opción --v indicaremos tres campos en un orden determinado separados por dos puntos: El primer parámetro será el nombre del volumen. Si se omite se creará un volumen anónimo. El segundo la ruta donde se montarán los datos.
		- (Page 18)
	- <<<<<<< #flashcard
		-   El  ultimo,  opcional,  es  una  lista  de  opciones  separadas  por  coma,  como  por ejemplo ro (solo lectura). Para crear un contenedor montando nuestro volumen en la ruta /datos lo haríamos de una de las siguientes maneras: $ docker run -dit --rm --mount source=mis-datos,target=/datos \ --name ContDatos alpine sh $ docker run -dit --rm -v mis-datos:/datos \ --name ContDatos alpine sh
		- (Page 19)
	- ¿Cómo funcionan los *bind mounts* en **Docker**? #flashcard
		- Los  bind  mounts  nos  permiten  montar  directorios  de  la  máquina  host  en  un contenedor.  Se  diferencian  principalmente  de  los  volúmenes  de  Docker  en  que necesitan existir en el sistema de ficheros del host y que no se pueden administrar con comandos de Docker. Al igual que en el caso anterior, para ejecutar un contenedor montando un directorio del sistema de ficheros del host utilizaremos el comando docker run con la opción -mount  o  -v.  Si  el directorio especificado no  existe  en el  host,  la opción  -v  creará automáticamente el directorio, sin embargo --mount devuelve un error.
		- (Page 20)
	- Explica en qué consisten los *tmpfs mounts* en Docker. #flashcard
		- En Linux tenemos la opción de utilizar tmpfs mounts. En este caso los datos también se guardarán fuera de la capa de escritura del contenedor, pero en vez de persistirse en disco se guardan en memoria. Es decir, que una vez que paremos el contenedor este almacenamiento desaparece. Además, tiene una limitación adicional, y es que este almacenamiento no puede ser compartido con otros contenedores. Aunque pueda parecernos de poca utilidad, un caso de uso típico de los tmpfs seria guardar ficheros datos sensibles que no queremos que se persistan ni en el host ni en la capa de escritura. Como en los casos anteriores, tenemos dos sintaxis posibles para montar tmpfs al crear un contenedor, --mount  y --tmpfs, siendo la primera la recomendada ya que nos permite especificar alguna opción adicional.
		- (Page 21)
	- <<<<<<<<< #flashcard
		- $ docker run -dit --mount type=tmpfs,destination=/datosTmp/ \ --name contDatos alpine sh $ docker run -dit --tmpfs /datosTmp/ \ --name contDatos alpine sh
		- (Page 22)
	- AÑADIR IMAGEN #flashcard
		- Para  crear  nuestro  contenedor  de  datos,  lo  habitual  es  utilizar  como  imagen  base busybox, se trata de una imagen muy reducida, incluso más ligera que alpine. Ya que no vamos a ejecutar nada en el contenedor, nos será suficiente: $ docker run -v /datos-compartidos --name contenedorDatos busybox \ touch /datos-compartidos/ficheroVacio Si  queremos  copiar  archivos  en  el  contenedor  de  datos  tendremos  que  utilizar  el comando docker cp, ya que no es accesible directamente desde el host. El siguiente comando copiaría un fichero de configuración en el directorio /config del contenedor de datos: $ docker cp config.conf contenedorDatos:/config/ Una  vez  creado  y  configurado  nuestro  contenedor  de  datos  montaremos  sus volúmenes al ejecutar otros contenedores con la opción –volumes-from, indicando el identificador o nombre del contenedor de datos. $ docker run -it --name ContenedorA \ --volumes-from contenedorDatos busybox /bin/sh / # ls /datos-compartidos ficheroVacio
		- (Page 23)
	- Importar y exportar contenedores de datos Cuando utilizamos contenedores de datos, el proceso de moverlos de una máquina a otra  se  simplifica  muchísimo.  Podemos  exportarlos  a  un  fichero  TAR  y  después importarlo en otra máquina: $ docker export contenedorDatos > contenedorDatosExport.tar $ docker import contenedorDatosExport.tar #spaced
		- (Page 24)
	- AÑADIR IMAGEN #flashcard
		- Tabla 2. Comandos para la gestión de redes.
		- (Page 25)
	- Controladores de red para Docker: #flashcard
		-   bridge.  Es  el  controlador  por  defecto.  Permite  la  comunicación  entre  dos contenedores independientes ejecutándose en el mismo anfitrión o host.   host. Permite eliminar el aislamiento de red entre el contenedor y el anfitrión.   overlay.  Nos  permitirá  conectar  contenedores  y/o  servicios  de  Docker  Swarm corriendo en diferentes demonios Docker, es decir en distintos nodos.   macvlan. Nos permite asignar una dirección MAC a un contenedor, permitiendo así redirigir directamente tráfico de red hacia ellos.   none. Deshabilita todas las redes del contenedor.
		- (Page 25)
	- $ docker network create --driver bridge miRed $ docker run -dit --rm --name contenedorA --network miRed alpine sh $ docker run -dit --rm --name contenedorB --network miRed alpine sh #spaced
		- (Page 28)
	- Cuando  utilizamos  el  controlador  de  red  host,  nuestro  contenedor  no  tendrá aislamiento de red y no se le asignará una dirección IP propia, ya que compartirá de del anfitrión o host. El  mapeo  de  puertos  que  definamos  no  tendrá  efecto,  ya  que  estarán automáticamente disponibles en el anfitrión. Además, no será posible tener más de un contenedor a la vez utilizando este controlar en el mismo host. #spaced
		- (Page 30)