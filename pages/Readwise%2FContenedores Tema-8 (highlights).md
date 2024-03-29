title:: Readwise/Contenedores Tema-8 (highlights)
deck:: [[Across-the-Net]]
author:: [[UNIR]]
full-title:: "Contenedores Tema-8"
category:: #articles

tags:: Contenedores UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/32ba186b-4f2e-404f-9b48-c6df76fd1f74.jpg)
- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- Tres motivos para tener una replicación de nuestros **pods** #flashcard
			- Los principales motivos para tener una replicación de nuestros Pods son:   Redundancia:  al  tener  múltiples  instancias  de  nuestros  Pod  en  ejecución, conseguiremos que el sistema sea tolerante a fallos.   Escalabilidad:  nuestros  sistemas  podrán  atender  más  peticiones  o  cargas  de trabajo simultáneamente.   Fragmentación  (sharding):  será  posible  gestionar  diferentes  partes  de  los procesos y cálculos de forma paralela en diferentes replicas.
		- (Page 5)
	- -
	- -
		- ¿De qué se encargan los objetos **ReplicaSet** en Kubernetes? #flashcard
			- Los ReplicaSets serán los encargados de gestionar nuestros Pods a lo largo del clúster, garantizando que en todo momento se están ejecutando el número y tipo de Pods deseados. Todos aquellos Pods gestionados por un ReplicaSets serán replanificados automáticamente en caso de fallo del nodo en el que se están ejecutando. A la hora de definir un objeto ReplicaSet, deberemos incluir la propia definición de los Pods que se gestionarán y, por supuesto, cuál es el número de réplicas deseado. Tendrá  lugar  un  proceso  de  reconciliación,  que  se  ejecutará  constantemente, observará  el  estado  actual  y  lo  comparará  con  el  deseado.  En  caso  de  encontrar diferencias,  actuará  en  consecuencia  creando  los  Pods  necesarios.  Además,  dicho proceso de reconciliación del ReplicaSets deberá ser capaz de identificar cuáles son los Pods que gestiona.
		- (Page 5)
	- -
	- -
		- Ejemplo de **ReplicaSet** en YAML #flashcard
			- apiVersion: apps/v1 kind: ReplicaSet metadata: name: web-rs labels: env: dev role: web
		- (Page 6)
	- -
	- -
		- <<<<<< #flashcard
			- spec: replicas: 4 selector: matchLabels: role: web template: metadata: labels: role: web spec: containers: - name: nginx-server image: nginx
		- (Page 7)
	- -
	- -
		- ¿Cómo puedo eliminar un *ReplicaSet*? #flashcard
			- $ kubectl delete rs web-rs $ kubectl delete -f web-rs.yaml replicaset.apps "web-rs" deleted Al eliminar un ReplicaSet, por defecto también serán eliminados automáticamente aquellos Pods gestionados por él. En caso de que no queramos que se eliminen sus Pods deberemos utilizar la opción --cascade=false.
		- (Page 10)
	- -
	- -
		- ¿Cómo puedes definir un escalado horizontal automático en Kubernetes? #flashcard
			- El  comando  kubectl  autoscale  nos  permite  crear  de  manera  imperativa  un Horizontal Pod Autoscaler (HPA), indicando el tipo de controlador que auto escalará, el mínimo y el máximo del número de réplicas permitidas, así como el porcentaje de uso de CPU que disparará el auto escalado. $ kubectl autoscale rs nombre-replicaset --min=2 --max=5 --cpu-percent=80
		- (Page 12)
	- -
	- -
		- INCLUIR IMAGEN #flashcard
			- Ya  sabemos  cómo  los  ReplicaSets  nos  permiten  ejecutar  cierto  número  de  Pods distribuidos a lo largo de un clúster de Kubernetes, siendo el propio ReplicaSet el que decide dónde ejecutar los Pods. Sin embargo, a veces necesitaremos ejecutar un Pod en todos y cada uno de los nodos del clúster o, al menos, en un conjunto especifico de ellos. Los DaemonSets se aseguran de que, en todos los nodos del clúster o en aquellos que hemos seleccionado se ejecute un Pod determinado. Además, se encargan de ejecutar un nuevo Pod cuando nuevos nodos son añadidos al clúster.
		- (Page 13)
	- -
	- -
		- ¿Cómo puedo etiquetar un nodo en Kubernetes? #flashcard
			- $ kubectl label nodes <nobre-nodo> disk=ssd $ kubectl get nodes --selector disk=ssd
		- (Page 15)
	- -
	- -
		- ... spec:
		  ... template:
		  spec:
		  nodeSelector:
		  disk: ssd
		  containers:
		- (Page 16)
	- -
	- -
		- ¿Cómo funciona la **afinidad** (o *affinity*) de un nodo en Kubernetes? #flashcard
			- La selección de nodos en base a la afinidad es similar a los selectores de nodo, ya que restringe los nodos en base a sus etiquetas. Sin embargo, la afinidad establece reglas que  deben  cumplirse  en  el  momento  de  la  planificación  de  los  nodos,  pero  no después. Estas se definen en la propiedad spec.template.spec.affinity. Veamos un ejemplo: spec: affinity: nodeAffinity: requiredDuringSchedulingIgnoredDuringExecution: nodeSelectorTerms: - matchExpressions: - key: kubernetes.io/e2e-az-name operator: In values: - e2e-az1 - e2e-az2
		- (Page 17)
	- -
	- -
		- Aunque todos Pods tengan una dirección IP única, esta no será expuesta al exterior a menos  que  sea a través  de un  Servicio.  La  manera  en  que  los Pods  son  expuestos dependen del tipo de servicio que utilicemos:   ClusteIP: es el tipo por defecto y expone el servicio en una dirección IP interna del clúster, por lo que solamente será accesible desde dentro del clúster.   NodePort: expone el servicio fuera del clúster a través de la dirección IP de cada nodo, utilizando el mismo puerto en cada uno de ellos.   LoadBalancer: creará un balanceador de carga externo en el proveedor de nube utilizado  y  se  asignará  una  dirección  IP  fija  al  servicio.  En  caso  de  no  estar soportado en la nube, actuará como el tipo NodePort. #flashcard
		- (Page 19)
	- -
	- -
		-   ExternalName:  expone  el  servicio  a  través  de  un  nombre  especificado  en  la definición, asociándolo con un nombre de dominio mediante un registro CNAME. #flashcard
		- (Page 20)
	- -
	- -
		- ¿De qué manera expone **NodePort** la IP? #flashcard
			- Ahora  el  servicio  será  accesible  a  través  de  la  dirección  IP  de  cualquier  nodo  de nuestro clúster:
		- (Page 24)
	- -
	- -
		- Al crear un servicio de tipo LoadBalancer, se creará un balanceador de carga con su propia IP pública, el cual distribuirá las peticiones recibidas a las IP públicas de todos los nodos. En caso de que nuestro clúster este ejecutándose en un entorno que no soporta balanceadores de carga, el servicio se comportará exactamente igual que el tipo NodePort. #flashcard
		- (Page 24)
	- -
	- -
		- Los  servicios  de  tipo  ExternalName  nos  permiten  crear  un  alias  para  un  servicio externo  al  clúster.  En  este  tipo  de  servicios  no  utilizaremos  ningún  selector  ni obtendrán ninguna dirección IP del clúster. Simplemente mapearán el nombre del servicio con un DNS externo, el cual se especificará como un registro CNAME en la definición YAML. #flashcard
		- (Page 26)
	- -
	- -
		- INCLUIR IMÁGEN #flashcard
			- Además  de  los  servicios  de  tipo  NodePort  y  LoadBalancer,  disponemos  de  otra manera de acceder a nuestros Pods desde fuera del clúster. Kubernetes nos ofrece una abstracción más, denominada Ingress, para el balanceo de carga en el clúster. Los  objetos  Ingress  actuarán  como  punto  de  entrada  al  clúster,  permitiéndonos utilizar la misma dirección IP para exponer múltiples servicios, mediante HTTP(S), a través de las reglas de enrutamiento.
		- (Page 27)
	- -