title:: Contenedores Tema-6 (highlights)
deck:: [[UNI::Contenedores Tema-6]]
author:: [[UNIR]]
full-title:: "Contenedores Tema-6"
category:: #books

tags:: Contenedores UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/c0c51f74-f62c-471b-9561-00094570a0b8.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Qué es Kubernetes? #flashcard
		  id:: f037d208-315e-4287-a2c1-600214a6d434
			- Kubernetes es una herramienta de código abierto que se utiliza para el despliegue y la gestión de contenedores. No se trata de una plataforma de contenerización, sino que ofrece una gestión de aplicaciones multicontenedor.
		- (Page 5)
	- -
	- -
		- Diferencias entre Docker Swarm y Kubernetes #flashcard
		  id:: 2b50722d-def0-44e0-a564-a2d1fbd52447
			-   Docker  Swarm  es  más  sencillo  de  utilizar  y  más  ligero  en  comparación  con Kubernetes, cuya gestión reviste mayor compleja.   Kubernetes  ofrece  un  auto  escalado  basado  en  métricas,  algo  que  no  ofrece Docker Swarm.
		- (Page 6)
	- -
	- -
		- <<<<<<< #flashcard
		  id:: 815b92aa-d980-412f-a9a6-8589ec7425ec
			-   Kubernetes está integrado en los principales proveedores de nube (AWS, Google, Azure, Digital Ocean, etc). Se ofrece como servicios para simplificar el despliegue y gestión de clústeres.   Kubernetes  ofrece  más  funcionalidades  que  Swarm.  Por  ejemplo,  permite  la actualización de aplicaciones de manera segura y eficiente, sin cortes de servicio, pudiendo revertir una versión anterior.   La gestión en Swarm se realiza con el mismo cliente de Docker, sin embargo, en Kubernetes hará falta un nuevo cliente (kubectl).   Por último, y no menos importante, la comunidad de usuarios de Kubernetes es mucho más numerosa que la de Swarm. Esto se traduce en un mayor volumen de contribución de nuevas funcionalidades y mayor ayuda por parte de la comunidad.
		- (Page 7)
	- -
	- -
		- ¿Qué es un servicio en Kubernetes? #flashcard
		  id:: 88252b0a-332f-4069-baeb-07e9dd7b7e77
			-   Servicios: son una capa de abstracción más, que exponen un grupo de Pods como servicio, generalmente mediante balanceo de carga.
		- (Page 8)
	- -
	- -
		- Define el componente API Server de un nodo Master en Kubernetes #flashcard
		  id:: fe3495cd-3db5-486e-8dff-8c2f88dbb20a
			- El componente API server es el encargado de exponer el API REST de Kubernetes para la  interactuar  con  el  clúster.  Actuará  como  punto  de  entrada  de  los  comandos enviados para gestionar el clúster, ya sean de componentes internos del sistema o externos, y será el encargado de procesar las peticiones y ejecutarlas en caso de ser válidas.  Podremos  utilizar  el  API  directamente  mediante  llamadas  REST  o  bien utilizando una herramienta de línea de comandos, como son kuberctl o kubeadm.
		- (Page 10)
	- -
	- -
		- Explica qué hace el componente Scheduler de un nodo Master en Kubernetes #flashcard
		  id:: 5a8e1c31-8f38-4ed8-8b49-62060e4498d4
			- El  planificador  o  Scheduler  atiende  las peticiones  que  recibe  el  API  server  y  las  va asignando a los diferentes nodos worker. Para determinar en qué nodo desplegar los Pods,  el  planificador  tendrá  en  cuenta  el  estado  de  los  nodos,  si  están  corriendo adecuadamente,  cuáles  son  los  recursos  disponibles  de  los  que  dispone  y  los requeridos  para  el  nuevo  despliegue.  En  caso  de  no  disponer  de  ningún  nodo adecuado  para  un  Pod,  se  podrá  en  estado  pendiente  hasta  que  haya  un  nodo disponible que cumpla los requisitos.
		- (Page 10)
	- -
	- -
		- El Controller Manager es el componente que ejecuta varios procesos controladores encargados de mantener el estado deseado en el clúster de Kubernetes. Mediante llamadas  al  API  server  se  obtendrá  el  estado  deseado  en  cada  momento  y  tras comprobar el estado actual de los nodos, se realizarán las acciones necesarias en caso de haber diferencias. #flashcard
		  id:: 3ab961e3-9196-4d42-9662-d81fe4bd7572
		- (Page 10)
	- -
	- -
		- ¿De qué e encarga el componente ***Controller Manager*** en un _nodo Mater_ de _Kubernete_? #flashcard
		  id:: f4906e52-8aa2-45fc-b1a2-cb356cc07e13
			- s
		- (Page 10)
	- -
	- -
		- Enumera los cuatro controladores que incluye el componente **Controller Manager** de un _nodo master_ en Kubernetes #flashcard
		  id:: 4e9b6584-626d-4064-b29b-0dc9bd777886
			- El componente Controller Manager incluye los siguientes controladores:   Replicacion  controller:  el  controlador  de  replicación  será  el  encargado  de  la gestión  de  los  Pods  en  el  clúster.  Crea  nuevos  Pods  para  mantener  el  número deseado y elimina los que han fallado.   Endpoint controller: será el encargado de proporcionar los endpoints del clúster, asegurando la conexión entre servicios y Pods.   Node controller: el controlador de nodo es responsable de la monitorización de los  nodos.  Detectará  cuándo  alguno  deja  de  estar  disponible,  desplegando  sus Pods en otros nodos.   Service controller: se encarga de la creación de las cuentas predeterminadas, así como los tokens de acceso al API cuando se crea un namespaces. Aunque,  desde  un  punto  de  vista  lógico,  cada  controlador  se  ejecutaría  como  un proceso independiente, con el fin de reducir la complejidad todos los controladores están compilados dentro del mismo binario y son ejecutados como un único proceso.
		- (Page 11)
	- -
	- -
		- ¿Qué es, básicamente, **etcd** ? #flashcard
		  id:: e88f6137-f8c8-4efc-bd75-13d47cdf3e9f
			- etcd  es  un  almacén  de  datos  clave-valor  distribuido  y  muy  consistente  que proporciona una forma confiable de almacenar datos a los que un sistema distribuido o  clúster  debe  acceder.  Está  desarrollado  en  Go,  ofreciendo  un  soporte multiplataforma, y utiliza el algoritmo de consenso Raft para la comunicación entre las máquinas del sistema distribuido. Kubernetes utiliza etcd tanto para el almacenamiento de la configuración del clúster como  para  el  descubrimiento  de  servicios.  Además,  permite  la  notificación  de cambios  de  configuración  en  un  nodo  concreto  al  resto  del  clúster  de  una  forma fiable.
		- (Page 11)
	- -
	- -
		- INCLUIR IMÁGEN!!
		  id:: 29a39b3c-1713-4140-aff2-5dfb82e6bb84
		  Define, básicamente, qué es un _nodo worker_ en Kubernetes. #flashcard
			- Los  nodos  worker  serán  los  encargados  de  la  ejecución  de  los  Pods  de  nuestras aplicaciones. Los Pods son agrupaciones lógicas de uno o más contenedores junto a un conjunto de recursos compartidos. En cada uno de estos nodos podremos ejecutar múltiples Pods simultáneamente. Aunque es posible tener un solo nodo worker, para conseguir una alta disponibilidad deberemos  configurar  varios  nodos  en  nuestro  clúster.  En  versiones  iniciales  de Kubernetes a estos nodos también se les conocía con el nombre de «minions».
		- (Page 12)
	- -
	- -
		- ¿Para qué sirve el componente **kubelet** dentro de un *nodo worker* en *Kubernetes* ? #flashcard
		  id:: 94ca7129-3901-4f7e-918d-a3720c0a94c2
			- En cada uno de los nodos worker tendremos un servicio, llamado Kubelet, que será el encargado de comunicarse con el nodo máster, obteniendo la configuración de los
		- (Page 12)
	- -
	- -
		- <<<<<<<< #flashcard
		  id:: 677caab5-6a76-4fd8-811e-c687d6018a29
			- Pods  y  garantizando  que  los  contenedores  definidos  en  ellos  se  estén  ejecutando correctamente. Además,  se  comunicará  con  el  almacenamiento  etcd  del  máster  para  recuperar información de los servicios y así poder registrar los nuevos servicios que se hayan creado.
		- (Page 13)
	- -
	- -
		- ¿Cuál es la función de **kube-proxy** en los *nodos worker* de *Kubernetes* ? #flashcard
		  id:: 5e356efa-d3b8-4503-9552-baa68c9b2318
			- El componente kube-proxy es un agente de red que se ejecuta en cada uno de los nodos y será el responsable de las actualizaciones dinámicas y el mantenimiento de las  reglas  de  red.  Además,  hará  funciones  de  proxy  de  red  y  balanceo  de  carga, redirigiendo el tráfico a los contenedores según la dirección IP y puerto de la petición.
		- (Page 13)
	- -
	- -
		- ¿Qué es un pod en Kubernetes? #flashcard
		  id:: 26a346f3-3859-4340-aca6-fef24f1d0a43
			- En un clúster de Kubernetes, los Pods serán la  unidad más básica de ejecución, el cual  estará  compuesto  por  uno  o  varios  contenedores.  Por  diseño,  los  Pods  son efímeros  por  naturaleza,  es  decir,  pueden  ser  destruidos  en  cualquier  momento  y sustituidos por otros. Todos  los  contenedores  que  forman  un  Pod  compartirán  la  misma  dirección  IP, tendrán acceso a cierto almacenamiento común y seguirán el mismo ciclo de vida. Por  consiguiente,  siempre  podrán  comunicarse  directamente  entre  ellos  y  se ejecutarán en bloque, iniciándose y parándose a la vez.
		- (Page 14)
	- -
	- -
		- ¿Qué es un servicio en Kubernetes? #flashcard
		  id:: 46b53276-9406-492e-9c3b-6c2119cc5ca4
			- referencia un servicio. En Kubernetes un servicio define un único punto de acceso para un conjunto de Pods. De esta manera, los servicios proporcionan una dirección IP y uno o varios puertos para  acceder  a  los  Pods  subyacentes,  permitiendo  tanto  a  usuarios  y  aplicaciones externas  al  clúster,  como  a  Pods  internos  comunicarse  con  los  Pods  a  los  que
		- (Page 15)
	- -
	- -
		- ¿Para qué sirven los namespaces en Kubernetes? #flashcard
		  id:: f3bc00be-9290-48b7-adfa-f121e3cada1f
			- Utilizaremos los Namespaces para organizar nuestros objetos en el clúster. Estos nos permiten agrupar recursos para realizar acciones sobre todos ellos. Un caso de uso típico de los Namespaces es el de crear diferentes entornos de ejecución (desarrollo, test, producción, etc.) para nuestras aplicaciones.
		- (Page 15)
	- -
	- -
		- Define PersistentVolume en Kubernetes. #flashcard
		  id:: 9bde0fed-a483-4f0f-bf0f-45aabb0467f3
			- Kubernetes introduce una nueva abstracción denominada PersistentVolumes, la cual nos permitirá desacoplar los Pods de la infraestructura asociada al almacenamiento. A diferencia de los objetos volumes, los recursos de tipo PersistentVolume tienen un ciclo de vida independiente a los Pods.
		- (Page 15)
	- -
	- -
		- Acerca de los **ConfigMaps** y **Secrets** en *Kubernetes* #flashcard
		  id:: 3c08aa50-ec54-4fb6-b015-a72a8085dc98
			- Los  ConfigMaps  nos  permitirán  separar los  datos  de  configuración  de los contenedores,  están  pensados  para  el  almacenamiento  de información  no confidencial.  Por  el  contrario,  para  la  gestión  de  información  sensible  como contraseñas y certificados, utilizaremos los Secrets.
		- (Page 16)
	- -
	- -
		- Explica qué hace el controlador **Deployment** de Kubernetes. #flashcard
		  id:: 4bfe81e8-b08a-4508-81a4-1206e06cead9
			- En  Kubernetes  utilizaremos  los  Deployments  para  gestionar  los  Pods  de  nuestra aplicación. Estos son ideales para aplicaciones o microservicios sin estado. Además, nos permitirán actualizar los Pods de las aplicaciones sin cortes de actividad. Cuando creamos un Deployment, automáticamente se creará un ReplicaSet para la creación y gestión de los Pods según el número de réplicas deseadas.
		- (Page 16)
	- -
	- -
		- Define ReplicaSet en Kubernetes. #flashcard
		  id:: 9776c512-7663-49ee-ba18-f2167ab2c232
			- Los  ReplicaSets  son  generalmente  creados  por  los  Deployments,  aunque  pueden crearse  independientemente.  Serán  los  encargados  de  crear  en  nuestro  clúster múltiples copias de un mismo Pod. Asimismo, garantizan que nuestra aplicación tiene el  numero  deseado  de  Pods,  creándolos  y  escalándolos  según  los  disparadores configurados en el Deployment.
		- (Page 16)
	- -
	- -
		- En otras palabras, se encargará de crear un  nuevo Pod en caso de que uno de los Pods en ejecución muera o se detenga por algún motivo. #flashcard
		  id:: e05e6f25-2deb-4f8f-8b60-eec920e57496
		- (Page 17)
	- -
	- -
		- ¿Qué es y para qué sirve el controlador **StatefulSets** de Kubernetes? #flashcard
		  id:: 5fafd522-22c9-4e35-ac2e-796631e201cb
			- Al igual que ocurría con los ReplicaSets, los StatefulSets nos permitirán gestionar el despliegue y escalado de un conjunto de Pods según se haya definido. Sin embargo, se diferencia de los Deployments en que los Pods de los StafulSets no se sustituyen completamente,  es  decir,  cada  Pod  tendrá  asociado  un  identificador  único  que  el controlador se encargará de persistir y mantener ante cualquier replanificación del Pod. Los StatefulSets se utilizan para aplicaciones con estado, como puede ser una base de  datos.  Toda  la  información  asociada  al  estado  de  los  Pods  gestionados  por  los StatefulSets será almacenada en un volumen asociado.
		- (Page 17)
	- -