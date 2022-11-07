# Contenedores Tema-7

deck:: [[UNI::Contenedores Tema-7]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-7"\
category:: #books\
\
tags:: Contenedores UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/fa317805-1e8b-47a1-bb48-006b2fab8523.jpg)
## Highlights
- id:: 63639916-ea43-42cb-b822-7adafc79c8c6
   Define **kubectl**
   AÑADIR IMÁGEN #flashcard 
    El Cliente kubectl es la herramienta de línea de comandos de Kubernetes que nos permitirá desplegar y gestionar aplicaciones en el clúster. Los comandos que ejecutemos con el cliente serán enviados a Kubernetes mediante llamadas HTTP a su API REST. Figura 1. El Cliente kubectl envía comandos mediante llamadas al API de Kubernetes. Fuente: Weibel, D. (2019). I ) R N U i j ( a o R a L e d l a n o i c a n r e t n I d a d i s r e v i n U ©
  
     (Page 5)
-
- id:: 63639916-316f-4db6-9966-33070a0fa564
   ¿Qué es un pod en Kubernetes? #flashcard 
    Un Pod está formado por una colección de contenedores más sus volúmenes. Este se ejecutará como una única unidad dentro de un mismo entorno de ejecución, es decir, todos los contenedores de un determinado Pod residirán en el mismo nodo. El Pod es la unidad mínima desplegable dentro de un clúster de Kubernetes. Cuando se despliegan en un nodo, permanecerán allí durante toda su ejecución, hasta que finalicen o sean eliminados. Nunca se moverán de nodo. En caso de fallo se planificará la creación de un nuevo Pod en otro nodo disponible del clúster.
  
     (Page 7)
-
- id:: 63639916-dfb5-481b-8c17-e7db9d7399f2
  
  Los contenedores están diseñados para ejecutar un único proceso. Sin embargo, en nuestras aplicaciones, a veces querremos que varios procesos se ejecuten los más cerca posible y se comuniquen entre sí. Este es el principal motivo por el que en Kubernetes la unidad mínima de despliegue, el Pod, puede estar formada por más de un contenedor. #flashcard 
  
  
     (Page 8)
-
- id:: 63639916-2b38-422e-a272-3fba514e97e6
   AÑADIR IMAGEN #flashcard 
    En Kubernetes, todos los Pods desplegados en cualquiera de los nodos comparten el mismo espacio de direcciones de red. Esto significa que, por defecto, cualquier Pod del clúster podría comunicarse con otro a partir de su dirección IP.
  
     (Page 8)
-
- id:: 63639916-bbf4-4fc9-8335-aa97760a5cc1
  
  Podríamos pensar que los Pods actúan como máquinas virtuales donde alojar toda nuestra aplicación. Sin embargo, deberemos aprender a descomponer nuestra aplicación y organizarla en múltiples Pods, de manera que sea posible escalar cada capa de la aplicación de manera individual. Normalmente utilizaremos Pods con un único contenedor, sin embargo, habrá ocasiones en las que tendremos un contenedor principal y varios de apoyo para tareas específicas, pero que están relacionadas con el principal. #flashcard 
  
  
     (Page 9)
-
- id:: 63639916-fbde-4eeb-8fd2-9e68af412c5c
  
  si listamos todos los Pods veremos el estado en que se encuentra nuestro Pod. No es posible listar directamente todos los contenedores, ya que en Kubernetes el Pod es la unidad mínima de despliegue: $ kubectl get pods NAME READY STATUS RESTARTS AGE app-nginx 1/1 Running 0 14s Sin embargo, sí que podemos consultar los detalles de un Pod concreto mediante el comando kubectl describe. Podemos utilizar este comando para consultar todo tipo de recursos de Kubernetes. $ kubectl describe pods app-nginx ... #flashcard 
  
  
     (Page 10)
-
- id:: 63639916-8fc6-413f-8e62-1f0c3a30cb89
   ¿Cómo podrías establecer un túnel entre la máquina local u una instancia de un pod en Kubernetes?
   INCLUIR IMAGEN #flashcard 
    El siguiente ejemplo establecería un túnel seguro entre nuestra máquina local y una de las instancias del Pod que se ejecuta en los nodos del clúster. Mientras el comando este ejecutándose, nuestra máquina escuchará por el puerto 8888, redirigiendo el tráfico al puerto 8080 del Pod. $ kubectl port-forward pod/mypod 8888:8080 ... Forwarding from 127.0.0.1:8888 -> 8080 ... Forwarding from [::1]:8888 -> 8080
  
     (Page 11)
-
- id:: 63639916-79a0-4155-8997-0afc97ae7197
   ¿Cómo ejecutarías un comando custom en un pod de Kubernetes? #flashcard 
    Cuando depuramos nuestros contenedores, en ocasiones, la información obtenida de los logs no nos será suficiente para determinar el problema y querremos ejecutar algún comando dentro del contexto del propio contenedor. Para ello, disponemos del comando kubectl exec. Las opciones -it nos permiten establecer una sesión interactiva con el contenedor. Veamos algún ejemplo: $ kubectl exec mypod date $ kubectl exec mypod -it sh
  
     (Page 12)
-
- id:: 63639916-875a-4a1b-93a8-08093099d759
   Ejemplos de copia de ficheros de *pods* en Kubernetes #flashcard 
    $ kubectl cp mypod:/data/app.dump ./app.dump $ kubectl cp $HOME/config.txt mypod:/config.txt
  
     (Page 13)
-
- id:: 63639916-3ff0-409a-b42f-c255b51245c4
   ¿Cuáles son las secciones más importantes que se usarán en la mayoría de los objetos de Kubernetes? #flashcard 
    las tres secciones más importantes que se usarán en la mayoría de los objetos de Kubernetes:  La sección «metadata» incluirá información sobre el Pod, como son el nombre, el Namespace, etiquetas, etc.  En la sección «spec» describiremos el comportamiento deseado del Pod, además de su contenido, es decir, los contenedores, volúmenes, etc.  La sección «status» es de solo lectura e incluirá información relativa al estado de la ejecución del Pod. A la hora de crear un Pod obviaremos esta propiedad.
  
     (Page 13)
-
- id:: 63639916-81e9-4550-9520-59f4f68e07a1
   Ejemplo sencillo de *pod* en Kubernetes #flashcard 
    apiVersion: v1 kind: Pod metadata: name: ejemplo-nginx spec: containers:
  
     (Page 13)
-
- id:: 63639916-847b-4ca0-bc0d-069bb68eff5d
   <<<< #flashcard
	- image: nginx name: servidor-nginx ports: - containerPort: 8080 protocol: TCP $ kubectl create -f ejemplo-nginx.yaml pod "ejemplo-nginx" created
	  
	       (Page 14)
-
- id:: 63639916-a4af-40b7-946f-e09350305586
  
  el comando kubectl explain, el cual nos permite listar los atributos soportados por un recurso. #flashcard 
  
  
     (Page 14)
-
- id:: 63639916-d250-4098-bcd7-4c212d35a1f0
   ¿Cómo se podrían implementar los *checks* **livenessProbe** y **readinessProbe** en Kubernetes? #flashcard 
    Estas pruebas se podrán realizar de tres maneras:  Mediante la ejecución de un comando (exec).  Al realizar una llamada HTTP (httpGet).  Conectándose a un socket TCP (tcpSocket). Si la prueba de vida definida falla, Kubernetes entiende que no está funcionando bien y reiniciará el Pod. Veamos algunos ejemplos de cómo configurarlos en la definición de los Pods: spec: containers: - name: liveness livenessProbe: exec: command: - cat - /tmp/healthy httpGet: path: /health port: 8080
  
     (Page 16)
-
- id:: 63639916-c1bf-4c97-a8f3-cfa4b43b0d96
   <<<<<<< #flashcard 
    tcpSocket: port: 8080
  
     (Page 17)
-
- id:: 63639916-a736-479f-bc80-90b3ab17c567
   ¿Qué checks hay disponibles en Kubernetes, además de las *liveness probe*?` #flashcard 
    Además de las pruebas de vida, también podemos definir dos tipos más de pruebas:  Pruebas de arranque (startup probe), para detectar problemas en el arranque de un Pod. Si el Pod tarda más de lo esperado creará uno nuevo.  Pruebas de disponibilidad (readiness probe), para detectar interrupciones temporales del servicio. En este caso, el Pod no se reiniciará, sino que dejará de recibir tráfico mientras esté fallando la prueba.
  
     (Page 17)
-
- id:: 63639916-1c03-426f-bc43-a05b9cf22bf9
   Ejemplo de definición de recursos a un pod en YAML #flashcard 
    ... spec: containers: - image: app-image:latest name: app resources: requests: cpu: "500m" memory: "128Mi" limits: cpu: "1000m" memory: "256Mi"
  
     (Page 17)
-
- id:: 63639916-1440-4f8d-826f-f4e9dc10ff29
  
  Al listar recursos de Kubernetes, la opción --show-labels nos permitirá ver las etiquetas asociadas a un determinado objeto. Además, la opción -L nos permite mostrar en una columna el valor de una etiqueta específica. #flashcard 
  
  
     (Page 19)
-
- id:: 63639916-059a-4c9d-bf4b-b02a503db4af
   ¿Cómo puedes mostrar las etiquetas de un objeto en Kubernetes?
   ¿Y las adicionales que queramos? #flashcard 
    a. Veamos un par de ejemplos: $ kubectl get pods nginx --show-labels NAME READY STATUS RESTARTS AGE LABELS app-nginx 1/1 Running 0 7m6s autor=efren,environment=staging
  
     (Page 19)
-
- id:: 63639916-28f6-473a-9572-59c84ae455f1
  
  $ kubectl get pods nginx -L autor,environment NAME READY STATUS RESTARTS AGE AUTOR ENVIRONMENT app-nginx 1/1 Running 0 11m efren staging #flashcard 
  
  
     (Page 20)
-
- id:: 63639916-01c8-451b-815e-a7c5ab03936c
   <<<<<< #flashcard 
    Sin embargo, si en lugar de asignar etiquetas nuevas lo que queremos es actualizar el valor de una etiqueta que ya está asociada al recurso, tendremos que utilizar la opción --overwrite para poder sobrescribirla. Pero si lo que queremos es eliminar una etiqueta del recurso, indicaremos un guion tras las key de la etiqueta: $ kubectl label pod app-nginx --overwrite autor=david $ kubectl label pod app-nginx autor
  
     (Page 20)
-
- id:: 63639916-c48f-4afd-9365-bd542f6e4845
  
  Tabla 1. Operadores disponibles del comando kubectl para los selectores. Fuente: elaboración propia. #flashcard 
  
  
     (Page 22)
-
- id:: 63639916-05dd-4c7f-8133-395f970b88b6
   INCLUIR IMAGEN #flashcard 
    Por ejemplo, podríamos utilizar un selector para listar todos los Pods del entorno de desarrollo que pertenecen a las aplicaciones demo o test, suponiendo que los tenemos correctamente etiquetados: $ kubectl get pods --selector="environment=desarrollo,app in (demo, test)"
  
     (Page 22)
-
- id:: 63639916-a1d2-4be9-80eb-6dbf53cb86ff
   Ejemplo de matchExpressions de Kubernetes en YAML.
   INCLUIR IMAGEN #flashcard 
    matchExpressions: - {key: app, operator: In, values: [demo, test]}
  
     (Page 23)
-
- id:: 63639916-cf80-4ef3-b71c-16aaabc81df6
  
  Tabla 2. Operadores disponibles en la sección matchExpressions de los selectores. Fuente: elaboración propia. #flashcard 
  
  
     (Page 23)
-
- id:: 63639916-2b7e-4eff-87a9-4cba6309db7a
   ¿Qué **namespaces** por defecto tiene Kubernetes? #flashcard 
    Cuando creamos un clúster de Kubernetes habitualmente este comienza con tres Namespaces por defecto, aunque dependiendo de la instalación podría tener inicialmente alguno más. Los Namespaces iniciales por defecto son:  Default: será el utilizado cuando no especifiquemos un Namespace.  Kube-system: es el Namespace para los objetos que han sido creados por el propio sistema de Kubernetes. Los usuarios no deberían desplegar aplicaciones en él.  Kube-public: visible y accesible por todos los usuarios del clúster. Aunque normalmente se utiliza de manera interna al clúster puede ser utilizado para que algunos recursos sean visibles en todo el clúster y accesible por cualquier usuario. El comando kubectl en este caso lo utilizamos para operar sobre los objetos del Namespace default. El siguiente comando obtiene la lista de Namespaces definidos en nuestro clúster: $ kubectl get ns NAME STATUS AGE default Active 12d docker Active 12d
  
     (Page 25)
-
- id:: 63639916-163f-4dd3-a899-f38c24d18389
   <<<<<<< #flashcard 
    kube-node-lease Active 12d kube-public Active 12d kube-system Active 12d
  
     (Page 26)
-
- id:: 63639916-f9a4-45e8-ae19-4b426214c261
   Comandos para listar y crear **namespaces** en *Kubernetes* #flashcard 
    En caso de querer interactuar con los objetos de todos los Namespaces definidos podemos utilizar la opción --all-namespaces. $ kubectl get pods --all-namespaces El siguiente comando crearía un Namespace de manera imperativa indicando el nombre que queremos utilizar: $ kubectl create namespace custom-namespace namespace "custom-namespace" created
  
     (Page 26)
-
- id:: 63639916-d806-49ab-adb4-4599323b132e
   ¿De qué elementos están formados los contextos en Kubernetes?
   INCLUIR IMAGEN #flashcard 
    En Kubernetes los contextos están formados por tres elementos: contexto.  Clúster: vendrá especificado por la URL al API de Kubernetes.  Usuario: incluirá las credenciales para un usuario concreto en dicho clúster.  Namespace: será el Namespace que se utilizará cuando seleccionemos este
  
     (Page 28)
-
-
	- ¿Cómo podemos listar los contextos disponibles, en Kubernetes?
		- ¿Cómo podemos saber cuál es nuestro contexto actual? #flashcard 
		  id:: 63639916-0691-4eac-85b1-262c40b3c3bc
		      Podemos consultar la lista de contextos disponibles, así como cual es contexto actual de la siguiente manera: $ kubectl config get-contexts CURRENT NAME CLUSTER AUTHINFO NAMESPACE * docker-desktop docker-desktop docker-desktop $ kubectl config current-context docker-desktop
		  
		  (Page 29)
-
- id:: 63639916-87e6-46ce-826c-3adf86a07b3d
   ¿Cómo podemos establecer un contexto como el actual en Kubernetes? #flashcard 
    Si queremos establecer el contexto que acabamos de crear como el contexto actual, deberemos hacer un cambio de contexto de la siguiente manera: $ kubectl config use-context dev-context Switched to context "dev-context".
  
     (Page 29)
-