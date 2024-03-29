title:: Contenedores Tema-7 (highlights)
deck:: [[UNI::Contenedores Tema-7]]
author:: [[UNIR]]
full-title:: "Contenedores Tema-7"
category:: #books

tags:: Contenedores UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/fa317805-1e8b-47a1-bb48-006b2fab8523.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Define **kubectl**
		  id:: 0814d933-d4d5-4c26-870a-36041f60d13e
		  
		  AÑADIR IMÁGEN #flashcard
			- El Cliente kubectl es la herramienta de línea de comandos de Kubernetes que nos permitirá  desplegar  y  gestionar  aplicaciones  en  el  clúster.  Los  comandos  que ejecutemos con el cliente serán enviados a Kubernetes mediante llamadas HTTP a su API REST. Figura 1. El Cliente kubectl envía comandos mediante llamadas al API de Kubernetes. Fuente: Weibel, D. (2019). I ) R N U i j ( a o R a L e d l a n o i c a n r e t n I d a d i s r e v i n U ©
		- (Page 5)
	- -
	- -
		- ¿Qué es un pod en Kubernetes? #flashcard
		  id:: fbfa6476-d917-45e9-8dc1-a6567c2b10f8
			- Un Pod está formado por una colección de contenedores más sus volúmenes. Este se ejecutará como una única unidad dentro de un mismo entorno de ejecución, es decir, todos los contenedores de un determinado Pod residirán en el mismo nodo. El Pod es la unidad mínima desplegable dentro de un clúster de Kubernetes. Cuando se despliegan en un nodo, permanecerán allí durante toda su ejecución, hasta que finalicen o sean eliminados. Nunca se moverán de nodo. En caso de fallo se planificará la creación de un nuevo Pod en otro nodo disponible del clúster.
		- (Page 7)
	- -
	- -
		- Los contenedores están diseñados para ejecutar un único proceso. Sin embargo, en nuestras aplicaciones, a veces querremos que varios procesos se ejecuten los más cerca  posible  y  se  comuniquen  entre  sí.  Este  es  el  principal  motivo  por  el  que  en Kubernetes la unidad mínima de despliegue, el Pod, puede estar formada por más de un contenedor. #flashcard
		  id:: dc3ff099-9c43-4afe-9373-e96d39e65dd0
		- (Page 8)
	- -
	- -
		- AÑADIR IMAGEN #flashcard
		  id:: 25880df0-fbbd-4150-a825-5ef937262b06
			- En Kubernetes, todos los Pods desplegados en cualquiera de los nodos comparten el mismo espacio de direcciones de red. Esto significa que, por defecto, cualquier Pod del clúster podría comunicarse con otro a partir de su dirección IP.
		- (Page 8)
	- -
	- -
		- Podríamos pensar que los Pods actúan como máquinas virtuales donde alojar toda nuestra  aplicación.  Sin  embargo,  deberemos  aprender  a  descomponer  nuestra aplicación y organizarla en múltiples Pods, de manera que sea posible escalar cada capa de la aplicación de manera individual. Normalmente utilizaremos Pods con un único  contenedor,  sin  embargo,  habrá  ocasiones  en  las  que  tendremos  un contenedor  principal  y  varios  de  apoyo  para  tareas  específicas,  pero  que  están relacionadas con el principal. #flashcard
		  id:: 991cb435-6eb6-4c4f-97d4-137959f380c0
		- (Page 9)
	- -
	- -
		- si listamos todos los Pods veremos el estado en que se encuentra nuestro  Pod.  No es  posible  listar directamente todos  los  contenedores, ya  que  en Kubernetes el Pod es la unidad mínima de despliegue: $ kubectl get pods NAME        READY   STATUS    RESTARTS   AGE app-nginx   1/1     Running   0          14s Sin embargo, sí que podemos consultar los detalles de un Pod concreto mediante el comando kubectl describe. Podemos utilizar este comando para consultar todo tipo de recursos de Kubernetes. $ kubectl describe pods app-nginx ... #flashcard
		  id:: 7a3a32f2-bce6-4134-9130-f6b7e98b5679
		- (Page 10)
	- -
	- -
		- ¿Cómo podrías establecer un túnel entre la máquina local u una instancia de un pod en Kubernetes?
		  id:: 04512333-2b4c-4cbc-af94-5cd2b37e20e3
		  
		  INCLUIR IMAGEN #flashcard
			- El siguiente ejemplo establecería un túnel seguro entre nuestra máquina local y una de las instancias del Pod que se ejecuta en los nodos del clúster. Mientras el comando este  ejecutándose, nuestra  máquina  escuchará por  el  puerto  8888,  redirigiendo el tráfico al puerto 8080 del Pod. $ kubectl port-forward pod/mypod 8888:8080 ... Forwarding from 127.0.0.1:8888 -> 8080 ... Forwarding from [::1]:8888 -> 8080
		- (Page 11)
	- -
	- -
		- ¿Cómo ejecutarías un comando custom en un pod de Kubernetes? #flashcard
		  id:: ae2cb345-e51e-46d9-b7db-9b5acdfc2c91
			- Cuando depuramos nuestros contenedores, en ocasiones, la información obtenida de los logs no nos será suficiente para determinar el problema y querremos ejecutar algún comando dentro del contexto del propio contenedor. Para ello, disponemos del  comando  kubectl  exec.  Las  opciones  -it nos  permiten  establecer  una  sesión interactiva con el contenedor. Veamos algún ejemplo: $ kubectl exec mypod date $ kubectl exec mypod -it sh
		- (Page 12)
	- -
	- -
		- Ejemplos de copia de ficheros de *pods* en Kubernetes #flashcard
		  id:: 8e224e5e-7117-4362-8ee4-fd2cc72508bf
			- $ kubectl cp mypod:/data/app.dump ./app.dump $ kubectl cp $HOME/config.txt mypod:/config.txt
		- (Page 13)
	- -
	- -
		- ¿Cuáles son las secciones más importantes que se usarán en la mayoría de los objetos de Kubernetes? #flashcard
		  id:: ab9d0c45-2e3d-4bb9-96db-9878560d16aa
			- las tres secciones más importantes que se usarán en la mayoría de los objetos de Kubernetes:   La sección «metadata» incluirá información sobre el Pod, como son el nombre, el Namespace, etiquetas, etc.   En la sección «spec» describiremos el comportamiento deseado del Pod, además de su contenido, es decir, los contenedores, volúmenes, etc.   La sección «status» es de solo lectura e incluirá información relativa al estado de la ejecución del Pod. A la hora de crear un Pod obviaremos esta propiedad.
		- (Page 13)
	- -
	- -
		- Ejemplo sencillo de *pod* en Kubernetes #flashcard
		  id:: 37dc0855-8a7f-4220-bdad-82851a1e7780
			- apiVersion: v1 kind: Pod metadata: name: ejemplo-nginx spec: containers:
		- (Page 13)
	- -
	- -
		- <<<< #flashcard
		  id:: 967e48d1-d717-48bb-990d-674f85003650
			- image: nginx name: servidor-nginx ports: - containerPort: 8080 protocol: TCP $ kubectl create -f ejemplo-nginx.yaml pod "ejemplo-nginx" created
		- (Page 14)
	- -
	- -
		- el comando kubectl explain, el cual nos permite listar los atributos soportados por un recurso. #flashcard
		  id:: bf543ccd-78ff-4e9f-9b02-87ada901692d
		- (Page 14)
	- -
	- -
		- ¿Cómo se podrían implementar los *checks* **livenessProbe** y **readinessProbe** en Kubernetes? #flashcard
		  id:: 2c0cb42b-aa62-4cae-b41e-da92b2048ccc
			- Estas  pruebas  se  podrán  realizar  de  tres maneras:   Mediante la ejecución de un comando (exec).   Al realizar una llamada HTTP (httpGet).   Conectándose a un socket TCP (tcpSocket). Si la prueba de vida definida falla, Kubernetes entiende que no está funcionando bien y reiniciará el Pod. Veamos algunos ejemplos de cómo configurarlos en la definición de los Pods: spec: containers: - name: liveness livenessProbe: exec: command: - cat - /tmp/healthy httpGet: path: /health port: 8080
		- (Page 16)
	- -
	- -
		- <<<<<<< #flashcard
		  id:: 1ceb1a4b-2b02-4f9f-ba88-d048b18f7c3c
			- tcpSocket: port: 8080
		- (Page 17)
	- -
	- -
		- ¿Qué checks hay disponibles en Kubernetes, además de las *liveness probe*?` #flashcard
		  id:: aee1cd9e-d1fa-4f4d-b1dd-23f94ef1015c
			- Además de las pruebas de vida, también podemos definir dos tipos más de pruebas:   Pruebas de arranque (startup probe), para detectar problemas en el arranque de un Pod. Si el Pod tarda más de lo esperado creará uno nuevo.   Pruebas  de  disponibilidad  (readiness  probe),  para  detectar  interrupciones temporales del servicio. En este caso, el Pod no se reiniciará, sino que dejará de recibir tráfico mientras esté fallando la prueba.
		- (Page 17)
	- -
	- -
		- Ejemplo de definición de recursos a un pod en YAML #flashcard
		  id:: c95dffac-ae89-47c5-b5ce-b23e0f8e3330
			- ... spec: containers: - image: app-image:latest name: app resources: requests: cpu: "500m" memory: "128Mi" limits: cpu: "1000m" memory: "256Mi"
		- (Page 17)
	- -
	- -
		- Al  listar  recursos  de  Kubernetes,  la  opción  --show-labels  nos  permitirá  ver  las etiquetas  asociadas  a  un  determinado  objeto.  Además,  la  opción  -L  nos  permite mostrar  en  una  columna  el  valor  de  una  etiqueta  específica. #flashcard
		  id:: 17628bc6-c032-4c1f-ac91-851a84b6ec94
		- (Page 19)
	- -
	- -
		- ¿Cómo puedes mostrar las etiquetas de un objeto en Kubernetes?
		  id:: c679b9e4-5a15-4d1e-a866-a59613052f61
		  ¿Y las adicionales que queramos? #flashcard
			- a.  Veamos  un  par  de ejemplos: $ kubectl get pods nginx --show-labels NAME        READY   STATUS    RESTARTS   AGE    LABELS app-nginx   1/1     Running   0          7m6s   autor=efren,environment=staging
		- (Page 19)
	- -
	- -
		- $ kubectl get pods nginx -L autor,environment NAME        READY   STATUS    RESTARTS   AGE   AUTOR   ENVIRONMENT app-nginx   1/1     Running   0          11m   efren   staging #flashcard
		  id:: 3dd25013-b692-4fa4-a013-4b8ff19fcf32
		- (Page 20)
	- -
	- -
		- <<<<<< #flashcard
		  id:: 1df78c8a-db55-4d5d-aa62-9daa64dbb035
			- Sin embargo, si en lugar de asignar etiquetas nuevas lo que queremos es actualizar el valor  de  una  etiqueta  que  ya  está  asociada  al  recurso,  tendremos  que  utilizar  la opción --overwrite para poder sobrescribirla. Pero si lo que queremos es eliminar una etiqueta del recurso, indicaremos un guion tras las key de la etiqueta: $ kubectl label pod app-nginx --overwrite autor=david $ kubectl label pod app-nginx autor
		- (Page 20)
	- -
	- -
		- Tabla 1. Operadores disponibles del comando kubectl para los selectores. Fuente: elaboración propia. #flashcard
		  id:: fbb76f31-6b56-4c15-844d-786c3b598e2d
		- (Page 22)
	- -
	- -
		- INCLUIR IMAGEN #flashcard
		  id:: 57e88c93-bb9d-4969-ab2f-9f995ee40cad
			- Por ejemplo, podríamos utilizar un selector para listar todos los Pods del entorno de desarrollo  que  pertenecen  a  las  aplicaciones  demo  o  test,  suponiendo  que  los tenemos correctamente etiquetados: $ kubectl get pods --selector="environment=desarrollo,app in (demo, test)"
		- (Page 22)
	- -
	- -
		- Ejemplo de matchExpressions de Kubernetes en YAML.
		  id:: b5534c49-da77-4eb6-bdba-fa76713b7483
		  
		  INCLUIR IMAGEN #flashcard
			- matchExpressions: - {key: app, operator: In, values: [demo, test]}
		- (Page 23)
	- -
	- -
		- Tabla 2. Operadores disponibles en la sección matchExpressions de los selectores. Fuente: elaboración propia. #flashcard
		  id:: eca6c721-cbb7-47f8-84d8-24f5b533be92
		- (Page 23)
	- -
	- -
		- ¿Qué **namespaces** por defecto tiene Kubernetes? #flashcard
		  id:: 0bd7c3ed-1875-4e55-9da2-69fefbcdbe77
			- Cuando  creamos  un  clúster  de  Kubernetes  habitualmente  este  comienza  con  tres Namespaces  por  defecto,  aunque  dependiendo  de  la  instalación  podría  tener inicialmente alguno más. Los Namespaces iniciales por defecto son:   Default: será el utilizado cuando no especifiquemos un Namespace.   Kube-system: es el Namespace para los objetos que han sido creados por el propio sistema de Kubernetes. Los usuarios no deberían desplegar aplicaciones en él.   Kube-public:  visible  y  accesible  por  todos  los  usuarios  del  clúster.  Aunque normalmente se utiliza de manera interna al clúster puede ser utilizado para que algunos recursos sean visibles en todo el clúster y accesible por cualquier usuario. El  comando  kubectl  en  este  caso  lo  utilizamos  para  operar  sobre  los  objetos  del Namespace default. El siguiente comando obtiene la lista de Namespaces definidos en nuestro clúster: $ kubectl get ns NAME              STATUS   AGE default           Active   12d docker            Active   12d
		- (Page 25)
	- -
	- -
		- <<<<<<< #flashcard
		  id:: 59c4b74c-3e80-43e6-82e0-2a08730a0866
			- kube-node-lease   Active   12d kube-public       Active   12d kube-system       Active   12d
		- (Page 26)
	- -
	- -
		- Comandos para listar y crear **namespaces** en *Kubernetes* #flashcard
		  id:: 3ad96d80-50bb-4e22-919c-566d23c2fdaa
			- En  caso  de  querer  interactuar  con  los  objetos  de  todos  los  Namespaces  definidos podemos utilizar la opción --all-namespaces. $ kubectl get pods --all-namespaces El  siguiente  comando  crearía  un  Namespace  de  manera  imperativa  indicando  el nombre que queremos utilizar: $ kubectl create namespace custom-namespace namespace "custom-namespace" created
		- (Page 26)
	- -
	- -
		- ¿De qué elementos están formados los contextos en Kubernetes?
		  id:: 424051ee-b61a-449f-b270-2e25e6bd4435
		  
		  INCLUIR IMAGEN #flashcard
			- En  Kubernetes  los  contextos  están  formados  por  tres elementos: contexto.   Clúster: vendrá especificado por la URL al API de Kubernetes.   Usuario: incluirá las credenciales para un usuario concreto en dicho clúster.   Namespace:  será  el  Namespace  que  se  utilizará  cuando  seleccionemos  este
		- (Page 28)
	- -
	- -
		- ¿Cómo podemos listar los contextos disponibles, en Kubernetes?
			- Podemos consultar la lista de contextos disponibles, así como cual es contexto actual de la siguiente manera: $ kubectl config get-contexts CURRENT   NAME                 CLUSTER          AUTHINFO         NAMESPACE *         docker-desktop       docker-desktop   docker-desktop $ kubectl config current-context docker-desktop
		- (Page 29)
	- -
	- -
		- ¿Cómo podemos establecer un contexto como el actual en Kubernetes? #flashcard
		  id:: 0560c40c-5959-4b6b-820d-122280848d33
			- Si queremos establecer el contexto que acabamos de crear como el contexto actual, deberemos hacer un cambio de contexto de la siguiente manera: $ kubectl config use-context dev-context Switched to context "dev-context".
		- (Page 29)
	- -