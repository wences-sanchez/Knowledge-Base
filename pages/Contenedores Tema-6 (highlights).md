title:: Contenedores Tema-6 (highlights)
author:: [[UNIR]]
full-title:: "Contenedores Tema-6"
category:: #books

tags:: #[[Contenedores]] #[[UNI]]

- #tags #[[Contenedores]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/c0c51f74-f62c-471b-9561-00094570a0b8.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- ¿Qué es Kubernetes? #car
		- Kubernetes es una herramienta de código abierto que se utiliza para el despliegue y la gestión de contenedores. No se trata de una plataforma de contenerización, sino que ofrece una gestión de aplicaciones multicontenedor.
		- (Page 5)
	- -
	- -
	- Diferencias entre Docker Swarm y Kubernetes #car
	  id:: 63401500-fc4a-423b-b805-aa2eca1a411f
		-   Docker  Swarm  es  más  sencillo  de  utilizar  y  más  ligero  en  comparación  con Kubernetes, cuya gestión reviste mayor compleja.   Kubernetes  ofrece  un  auto  escalado  basado  en  métricas,  algo  que  no  ofrece Docker Swarm.
		- (Page 6)
	- -
	- -
	- <<<<<<< #car
	  id:: 63401500-0b25-496c-8120-5d1e7c534fd1
		-   Kubernetes está integrado en los principales proveedores de nube (AWS, Google, Azure, Digital Ocean, etc). Se ofrece como servicios para simplificar el despliegue y gestión de clústeres.   Kubernetes  ofrece  más  funcionalidades  que  Swarm.  Por  ejemplo,  permite  la actualización de aplicaciones de manera segura y eficiente, sin cortes de servicio, pudiendo revertir una versión anterior.   La gestión en Swarm se realiza con el mismo cliente de Docker, sin embargo, en Kubernetes hará falta un nuevo cliente (kubectl).   Por último, y no menos importante, la comunidad de usuarios de Kubernetes es mucho más numerosa que la de Swarm. Esto se traduce en un mayor volumen de contribución de nuevas funcionalidades y mayor ayuda por parte de la comunidad.
		- (Page 7)
	- -
	- -
	- ¿Qué es un servicio en Kubernetes? #car
	  id:: 63401500-c03e-4f8c-8d2c-439f2f85553b
		-   Servicios: son una capa de abstracción más, que exponen un grupo de Pods como servicio, generalmente mediante balanceo de carga.
		- (Page 8)
	- -
	- -
	- Define el componente API Server de un nodo Master en Kubernetes #car
	  id:: 63401500-5768-4e88-95c6-9d292b222903
		- El componente API server es el encargado de exponer el API REST de Kubernetes para la  interactuar  con  el  clúster.  Actuará  como  punto  de  entrada  de  los  comandos enviados para gestionar el clúster, ya sean de componentes internos del sistema o externos, y será el encargado de procesar las peticiones y ejecutarlas en caso de ser válidas.  Podremos  utilizar  el  API  directamente  mediante  llamadas  REST  o  bien utilizando una herramienta de línea de comandos, como son kuberctl o kubeadm.
		- (Page 10)
	- -
	- -
	- Explica qué hace el componente Scheduler de un nodo Master en Kubernetes #car
	  id:: 63401500-c713-4c3e-a575-1f1a8c857c36
		- El  planificador  o  Scheduler  atiende  las peticiones  que  recibe  el  API  server  y  las  va asignando a los diferentes nodos worker. Para determinar en qué nodo desplegar los Pods,  el  planificador  tendrá  en  cuenta  el  estado  de  los  nodos,  si  están  corriendo adecuadamente,  cuáles  son  los  recursos  disponibles  de  los  que  dispone  y  los requeridos  para  el  nuevo  despliegue.  En  caso  de  no  disponer  de  ningún  nodo adecuado  para  un  Pod,  se  podrá  en  estado  pendiente  hasta  que  haya  un  nodo disponible que cumpla los requisitos.
		- (Page 10)
	- -
	- -
	- El Controller Manager es el componente que ejecuta varios procesos controladores encargados de mantener el estado deseado en el clúster de Kubernetes. Mediante llamadas  al  API  server  se  obtendrá  el  estado  deseado  en  cada  momento  y  tras comprobar el estado actual de los nodos, se realizarán las acciones necesarias en caso de haber diferencias. #ñspace
		- (Page 10)
	- -
	- -
	- ¿De qué e encarga el componente ***Controller Manager*** en un _nodo Mater_ de _Kubernete_? #car
		- s
		- (Page 10)
	- -
	- -
	- Enumera los cuatro controladores que incluye el componente **Controller Manager** de un _nodo master_ en Kubernetes #car
		- El componente Controller Manager incluye los siguientes controladores:   Replicacion  controller:  el  controlador  de  replicación  será  el  encargado  de  la gestión  de  los  Pods  en  el  clúster.  Crea  nuevos  Pods  para  mantener  el  número deseado y elimina los que han fallado.   Endpoint controller: será el encargado de proporcionar los endpoints del clúster, asegurando la conexión entre servicios y Pods.   Node controller: el controlador de nodo es responsable de la monitorización de los  nodos.  Detectará  cuándo  alguno  deja  de  estar  disponible,  desplegando  sus Pods en otros nodos.   Service controller: se encarga de la creación de las cuentas predeterminadas, así como los tokens de acceso al API cuando se crea un namespaces. Aunque,  desde  un  punto  de  vista  lógico,  cada  controlador  se  ejecutaría  como  un proceso independiente, con el fin de reducir la complejidad todos los controladores están compilados dentro del mismo binario y son ejecutados como un único proceso.
		- (Page 11)
	- -
	- -
	- ¿Qué es, básicamente, **etcd** ? #car
		- etcd  es  un  almacén  de  datos  clave-valor  distribuido  y  muy  consistente  que proporciona una forma confiable de almacenar datos a los que un sistema distribuido o  clúster  debe  acceder.  Está  desarrollado  en  Go,  ofreciendo  un  soporte multiplataforma, y utiliza el algoritmo de consenso Raft para la comunicación entre las máquinas del sistema distribuido. Kubernetes utiliza etcd tanto para el almacenamiento de la configuración del clúster como  para  el  descubrimiento  de  servicios.  Además,  permite  la  notificación  de cambios  de  configuración  en  un  nodo  concreto  al  resto  del  clúster  de  una  forma fiable.
		- (Page 11)
	- -
	- -
	- INCLUIR IMÁGEN!!
	  id:: 63401500-e37d-42da-8eab-b0228aed0f79
	  Define, básicamente, qué es un _nodo worker_ en Kubernetes. #car
		- Los  nodos  worker  serán  los  encargados  de  la  ejecución  de  los  Pods  de  nuestras aplicaciones. Los Pods son agrupaciones lógicas de uno o más contenedores junto a un conjunto de recursos compartidos. En cada uno de estos nodos podremos ejecutar múltiples Pods simultáneamente. Aunque es posible tener un solo nodo worker, para conseguir una alta disponibilidad deberemos  configurar  varios  nodos  en  nuestro  clúster.  En  versiones  iniciales  de Kubernetes a estos nodos también se les conocía con el nombre de «minions».
		- (Page 12)
	- -
	- -
	- ¿Para qué sirve el componente **kubelet** dentro de un *nodo worker* en *Kubernetes* ? #car
	  id:: 63401500-f1ad-4c8d-a349-40aa0997500a
		- En cada uno de los nodos worker tendremos un servicio, llamado Kubelet, que será el encargado de comunicarse con el nodo máster, obteniendo la configuración de los
		- (Page 12)
	- -
	- -
	- <<<<<<<< #car
		- Pods  y  garantizando  que  los  contenedores  definidos  en  ellos  se  estén  ejecutando correctamente. Además,  se  comunicará  con  el  almacenamiento  etcd  del  máster  para  recuperar información de los servicios y así poder registrar los nuevos servicios que se hayan creado.
		- (Page 13)
	- -
	- -
	- ¿Cuál es la función de **kube-proxy** en los *nodos worker* de *Kubernetes* ? #car
	  id:: 63401500-14b0-431b-b2be-c587fc3d2fd2
		- El componente kube-proxy es un agente de red que se ejecuta en cada uno de los nodos y será el responsable de las actualizaciones dinámicas y el mantenimiento de las  reglas  de  red.  Además,  hará  funciones  de  proxy  de  red  y  balanceo  de  carga, redirigiendo el tráfico a los contenedores según la dirección IP y puerto de la petición.
		- (Page 13)
	- -
	- -
	- ¿Qué es un pod en Kubernetes? #car
		- En un clúster de Kubernetes, los Pods serán la  unidad más básica de ejecución, el cual  estará  compuesto  por  uno  o  varios  contenedores.  Por  diseño,  los  Pods  son efímeros  por  naturaleza,  es  decir,  pueden  ser  destruidos  en  cualquier  momento  y sustituidos por otros. Todos  los  contenedores  que  forman  un  Pod  compartirán  la  misma  dirección  IP, tendrán acceso a cierto almacenamiento común y seguirán el mismo ciclo de vida. Por  consiguiente,  siempre  podrán  comunicarse  directamente  entre  ellos  y  se ejecutarán en bloque, iniciándose y parándose a la vez.
		- (Page 14)
	- -
	- -
	- ¿Qué es un servicio en Kubernetes? #car
	  id:: 63401500-0b6b-4a77-a9c7-0c5311227621
		- referencia un servicio. En Kubernetes un servicio define un único punto de acceso para un conjunto de Pods. De esta manera, los servicios proporcionan una dirección IP y uno o varios puertos para  acceder  a  los  Pods  subyacentes,  permitiendo  tanto  a  usuarios  y  aplicaciones externas  al  clúster,  como  a  Pods  internos  comunicarse  con  los  Pods  a  los  que
		- (Page 15)
	- -
	- -
	- ¿Para qué sirven los namespaces en Kubernetes? #car
		- Utilizaremos los Namespaces para organizar nuestros objetos en el clúster. Estos nos permiten agrupar recursos para realizar acciones sobre todos ellos. Un caso de uso típico de los Namespaces es el de crear diferentes entornos de ejecución (desarrollo, test, producción, etc.) para nuestras aplicaciones.
		- (Page 15)
	- -
	- -
	- Define PersistentVolume en Kubernetes. #car
		- Kubernetes introduce una nueva abstracción denominada PersistentVolumes, la cual nos permitirá desacoplar los Pods de la infraestructura asociada al almacenamiento. A diferencia de los objetos volumes, los recursos de tipo PersistentVolume tienen un ciclo de vida independiente a los Pods.
		- (Page 15)
	- -
	- -
	- Acerca de los **ConfigMaps** y **Secrets** en *Kubernetes* #car
		- Los  ConfigMaps  nos  permitirán  separar los  datos  de  configuración  de los contenedores,  están  pensados  para  el  almacenamiento  de información  no confidencial.  Por  el  contrario,  para  la  gestión  de  información  sensible  como contraseñas y certificados, utilizaremos los Secrets.
		- (Page 16)
	- -
	- -
	- Explica qué hace el controlador **Deployment** de Kubernetes. #car
	  id:: 63401500-4b96-4ed3-add0-ee98bc3141b0
		- En  Kubernetes  utilizaremos  los  Deployments  para  gestionar  los  Pods  de  nuestra aplicación. Estos son ideales para aplicaciones o microservicios sin estado. Además, nos permitirán actualizar los Pods de las aplicaciones sin cortes de actividad. Cuando creamos un Deployment, automáticamente se creará un ReplicaSet para la creación y gestión de los Pods según el número de réplicas deseadas.
		- (Page 16)
	- -
	- -
	- Define ReplicaSet en Kubernetes. #car
		- Los  ReplicaSets  son  generalmente  creados  por  los  Deployments,  aunque  pueden crearse  independientemente.  Serán  los  encargados  de  crear  en  nuestro  clúster múltiples copias de un mismo Pod. Asimismo, garantizan que nuestra aplicación tiene el  numero  deseado  de  Pods,  creándolos  y  escalándolos  según  los  disparadores configurados en el Deployment.
		- (Page 16)
	- -
	- -
	- En otras palabras, se encargará de crear un  nuevo Pod en caso de que uno de los Pods en ejecución muera o se detenga por algún motivo. #ñspace
		- (Page 17)
	- -
	- -
	- ¿Qué es y para qué sirve el controlador **StatefulSets** de Kubernetes? #car
	  id:: 63401500-3fac-4746-99fe-5d5641689463
		- Al igual que ocurría con los ReplicaSets, los StatefulSets nos permitirán gestionar el despliegue y escalado de un conjunto de Pods según se haya definido. Sin embargo, se diferencia de los Deployments en que los Pods de los StafulSets no se sustituyen completamente,  es  decir,  cada  Pod  tendrá  asociado  un  identificador  único  que  el controlador se encargará de persistir y mantener ante cualquier replanificación del Pod. Los StatefulSets se utilizan para aplicaciones con estado, como puede ser una base de  datos.  Toda  la  información  asociada  al  estado  de  los  Pods  gestionados  por  los StatefulSets será almacenada en un volumen asociado.
		- (Page 17)
	- -