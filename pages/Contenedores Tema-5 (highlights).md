title:: Contenedores Tema-5 (highlights)
deck:: [[UNI::Contenedores Tema-5]]
author:: [[UNIR]]
full-title:: "Contenedores Tema-5"
category:: #books

tags:: Contenedores UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/8184ee50-30f0-4aad-9d8a-0a568bff6963.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Las  versiones  actuales  de  Docker  ofrecen  un  orquestador  integrado  en  el  propio engine llamado «modo enjambre» o «modo Swarm» para permitir una configuración distribuida. Sin embargo, antes de la versión 1.12 de Docker se utilizaba un modelo independiente denominado «Docker Swarm». #flashcard
		  id:: 1571e844-2332-4696-b2c3-92d535efc6a1
		- (Page 5)
	- -
	- -
		- La ejecución de Docker en modo Swarm no impide que se ejecuten contenedores de manera independiente, como hemos visto en temas anteriores, en cualquiera de los nodos  del  clúster.  La  principal diferencia entre  contenedores  independientes  y  los servicios  de  Swarm  es  que  solo  los  mánagers  de  Swarm  pueden  gestionar  estos servicios,  mientras  que  los  contenedores  independientes  se  pueden  iniciar  en cualquier host. #flashcard
		  id:: 12ef10c8-9bd1-47bf-b42f-622e3ed62e58
		- (Page 6)
	- -
	- -
		- Las principales características que ofrece el modo Swarm son:   Administración de clústeres integrada en Docker Engine.   Diseño descentralizado.   Modelo de servicio declarativo. #flashcard
		  id:: 6e8522e3-e7dc-412e-8cb5-4ae253818e80
		- (Page 6)
	- -
	- -
		- <<<<<< #flashcard
		  id:: 46f95805-1d20-4a7a-bc01-6f19deb7f9a2
			-   Escalabilidad.   Conciliación de estado deseado.   Soporte de redes en múltiples host.   Descubrimiento de servicios.   Balanceo de carga.   Seguridad de forma predeterminada.   Actualizaciones continuas.
		- (Page 7)
	- -
	- -
		- Un nodo será cualquier máquina, ya sea física o en la nube, con el motor de Docker que forma parte de un clúster de Swarm. Tenemos dos tipos de nodos:   Mánagers:  serán  los  encargados  de  desplegar  las  aplicaciones  en  el  clúster enviando tareas a los nodos de tipo worker.   Workers:  ejecutan  las  tareas  recibidas  por  los  nodos  mánagers.  Además, notificarán periódicamente el estado de estas. #flashcard
		  id:: 4ffffe36-0c8f-4605-8bd4-ed044d29b3d3
		- (Page 7)
	- -
	- -
		- Explica qué son los nodos manager de Docker Swarm #flashcard
		  id:: 51f02c7b-6d65-4fda-87f7-71aa90c6ba44
			- Los nodos mánager del clúster trabajarán para mantener en todo momento el estado deseado definido, planificarán los servicios entre los nodos y, además, atenderán las llamadas al API de Swarm.
		- (Page 8)
	- -
	- -
		- ¿Para qué sirven los nodos de trabajo (o workers) en **Docker Swarm**? #flashcard
		  id:: ea0705dc-dbd7-4fad-9d54-af448b1f3b52
			- La finalidad de los nodos de trabajo o workers en el clúster será exclusivamente la ejecución de tareas, es decir, de contenedores. Podríamos tener un clúster sin nodos worker,  ya  que  por  defecto  un  nodo  mánager  también  atiende  tareas  como  los workers. Pero no podremos, ni tampoco tendría sentido, crear un clúster con solo nodos worker.
		- (Page 8)
	- -
	- -
		- Para evitar que se planifiquen tareas para los nodos mánagers podemos ponerlos en modo drenaje (drain). Si ya tenía tareas asignadas se planificarán de nuevo en otros nodos. #flashcard
		  id:: 6c56cc07-44ff-43e1-a054-bf2f764f42c0
		- (Page 8)
	- -
	- -
		- INCLUIR IMAGEN #flashcard
		  id:: df2cbd7f-97cd-43c2-96b3-5c454754fb83
			- Cuando indiquemos que queremos varias réplicas un determinado servicio, será el nodo mánager quien distribuya las tareas entre los diferentes nodos del clúster hasta lograr el estado deseado. Estas tareas se ejecutarán de manera independiente.
		- (Page 9)
	- -
	- -
		- Los  clústeres  Swarm  utilizan  TLS  para  autenticar,  autorizar  y  encriptar  las comunicaciones  entre  los  nodos.  Cuando  inicializamos  el  clúster  el nodo  inicial  se convierte en mánager y en él se crearán una autoridad certificadora raíz (CA) junto con un par de claves que servirán para establecer una comunicación segura con el resto de los nodos que se añadan al clúster. #flashcard
		  id:: 854f7c55-65ae-49e5-b6bd-916904e26d80
		- (Page 11)
	- -
	- -
		- Tabla 1. Comandos para la gestión de servicios. Fuente: elaboración propia. #flashcard
		  id:: 22191bc2-28be-479a-a155-caf6472b9aaf
		- (Page 15)
	- -
	- -
		- Cambio de rol de un nodo en Docker Swarm #flashcard
		  id:: 648903e1-5529-4dc3-ae0f-0341c6668488
			- Es posible promover un nodo worker para convertirlo en nodo mánager, y viceversa, podemos degradar un nodo mánager a worker. Para realizar estas tareas de cambio de  rol  de  los  nodos  utilizaremos  los  siguientes  comandos  desde  un  nodo  de administración: $ docker node promote nombreNodoWorker $ docker node demote nombreNodoManager
		- (Page 21)
	- -
	- -
		- Nombra las diferencias entre **config** y **secret** en *Docker Swarm* #flashcard
		  id:: fed3af34-a459-4f2d-bbb3-e6caca52b1c3
			-   Los objetos config no se almacenan en claro cuando los creamos. Sin embargo, los secret se almacenan encriptados. Ambos se transmiten de forma encriptada   La ruta de montaje por defecto de los config es /<config-name>, y en los secret entre los nodos. es /run/secrets/<secret_name>.   Los  objetos  config  se  montan  directamente  en  el  sistema  de  ficheros  del contenedor.  Sin  embargo,  los  secret  utilizan  sistemas  de ficheros  en memoria (RAM disk).   Un determinado objeto secret solamente será accesible por aquellos servicios a los que hemos dado acceso explícitamente.
		- (Page 23)
	- -
	- -
		- Tabla 2. Comandos para la gestión de stacks. Fuente: elaboración propia. #flashcard
		  id:: 244872f8-ae47-4947-8a2f-4b2092244e50
		- (Page 26)
	- -