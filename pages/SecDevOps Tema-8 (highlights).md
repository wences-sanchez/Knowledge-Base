title:: SecDevOps Tema-8 (highlights)
author:: [[UNIR]]
full-title:: "SecDevOps Tema-8"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/554fa67d-89eb-4910-84a0-6544a20836da.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Qué es Kubernetes? #flashcard
		  id:: cc321da4-b71d-4067-80e9-9aef957220c6
			- Kubernetes  es  un  sistema  que  automatiza  el  despliegue,  el  escalado  y  la administración  de  aplicaciones  diseñadas  como  contenedores.  Un  clúster  de Kubernetes está formado por múltiples nodos (que pueden ser físicos o virtuales) en
		- (Page 4)
	- -
	- -
		- CONTINUE #flashcard
		  id:: 35151c37-6a49-4013-bd4d-906ade34b711
			- los que se despliegan contenedores que ejecutan los procesos de las aplicaciones. La comunicación de red y el ciclo de vida de estos contendores se gestionan con tipos de recursos nativos de Kubernetes, como los pods, servicios y políticas de red.
		- (Page 5)
	- -
	- -
		- ¿Qué es un pod? #flashcard
		  id:: bf2c7dbf-885e-4166-afdb-8ee7fc64e144
			- Un pod es un grupo de contenedores localizados en el mismo nodo y representa el componente  básico  de  Kubernetes.  En lugar  de  desplegar  contenedores individualmente, siempre es obligatorio desplegar los contenedores en pods. Esto no significa que un pod deba incluir más de un contenedor, y, de hecho, es habitual que los pods contengan solo un contenedor. La idea principal de los pods es que, cuando un pod contiene múltiples contenedores, todos  ellos  se  ejecutan  siempre  en  un  solo  nodo.  Los  contenedores  comparten  el mismo  nombre  de  host  y  la  misma  tarjeta  de  red.  No  comparten  el  sistema  de ficheros,  pero  pueden  usar  un  mismo  directorio  mediante  un  volumen  de Kubernetes.
		- (Page 6)
	- -
	- -
		- Además, todos los contenedores en un  pod comparten la interfaz de red de bucle invertido  (el  loopback),  por  lo  que  un  contenedor  puede  comunicarse  con  otros contenedores en el mismo pod a través de localhost. #flashcard
		  id:: 6122b3f1-2e90-4cae-bdb4-639610d456fb
		- (Page 6)
	- -
	- -
		- mismo servicio. Un  servicio,  o  service,  de  Kubernetes  es  un  recurso  que  crea  un  único  punto  de entrada  permanente  para  un  pod,  o  para  un  grupo  de  pods,  que  proporcionan  el Cada servicio tiene una dirección IP y un puerto que nunca cambian durante la vida del servicio. Los clientes pueden abrir conexiones a esa IP y puerto, y esas conexiones se enrutan a uno de los pods que respaldan ese servicio. De esta manera, los clientes de  un  servicio  no  necesitan  conocer  la  ubicación,  ni  las  direcciones,  de  los  pods individuales que brindan el servicio, lo que facilita su mantenimiento. #flashcard
		  id:: 984e9dd7-1ae8-4f41-9e88-2521a01d9a96
		- (Page 11)
	- -
	- -
		- ¿Cómo se pueden seleccionar los pods y exponer servicios al exterior, con Kubernetes? #flashcard
		  id:: f9eb6ed0-1e51-4511-96eb-5498a279daf0
			- La selección de pod se hace con etiquetas: el servicio wordpress tiene la propiedad  selector, que indica dos  etiquetas:  app=wordpress y  tier=frontend. La definición de los pods de WordPress incluía esas dos etiquetas. La  misma  técnica  se  usa  con  el  servicio  y  el  pod  de  MySQL,  pero  con  etiquetas diferentes. Kubernetes ofrece varios métodos para exponer servicios al exterior: mediante un servicio de tipo NodePort, un servicio de tipo LoadBalancer o mediante un Ingress, que es otro tipo de recurso que trabaja junto al servicio.
		- (Page 14)
	- -
	- -
		- ¿En qué consiste el servicio NodePort de Kubernetes? #flashcard
		  id:: d5568d20-083d-4124-a273-189dfab97e8f
			- El primer método para exponer un conjunto de pods a clientes externos es crear un servicio  y  establecer  su  tipo  como  NodePort.  Al  crear  un  servicio  NodePort, Kubernetes reserva un puerto en todos sus nodos, el mismo número de puerto en todos ellos, y reenvía las conexiones entrantes en esos puertos a los pods que forman parte del servicio. Esta reserva del puerto es similar a un servicio normal de tipo  ClusterIP, pero un servicio  NodePort  es  accesible  no  solo  a  través  de  la  IP  interna  del  clúster,  sino también a través de la IP de cualquier nodo. Estas IP no pertenecen a la red de los pods, sino a la subred a la que están conectadas las interfaces de los nodos y, por tanto, son accesible desde fuera del clúster.
		- (Page 14)
	- -
	- -
		- ¿En qué consiste el servicio de balanceador de carga de Kubernetes? #flashcard
		  id:: e003d0d6-a4bf-4461-8c88-c4b91f2049e7
			- Los  clústeres  de  Kubernetes  que  se  ejecutan  en  proveedores  de  la  nube, generalmente, admiten la provisión automática de un balanceador de carga desde la infraestructura  de  la  nube.  Esto  es  posible  si  el  clúster  se  aprovisiona  como  un servicio nativo del proveedor, por ejemplo, mediante el servicio EKS en AWS, AKS en Azure o GKE en Google Compute Cloud . Si  se  configura  un  clúster  de  Kubernetes  manualmente  a  partir  de  instancias  de cómputo  (EC2,  por  ejemplo),  el  servicio  de  balanceador  no  tiene  por  qué  estar disponible, a menos que el proveedor ofrezca la posibilidad de instalar los plugins de su entorno en un clúster propio. Si el clúster lo soporta, todo lo que se necesita hacer es establecer el tipo de servicio en  LoadBalancer  en  lugar  de  NodePort.  El  balanceador  de  carga  tendrá  su  propia dirección IP única, y de acceso público, y redirigirá todas las conexiones a su servicio.
		- (Page 15)
	- -
	- -
		- CONTINUE #flashcard
		  id:: c5ee5bc8-ba48-4aa4-8c16-3b1f321d98a9
			- De este modo, los clientes pueden acceder al servicio a través de la dirección IP del balanceador.  Este  balanceador  será  un  recurso  de  tipo  ELB  en  AWS,  Azure  Load Balancer en Azure  o Cloud Load Balancing en GCE . Si Kubernetes se ejecuta en un entorno que no admite los servicios de LoadBalancer, el balanceador no se aprovisionará y el servicio seguirá comportándose como si fuera de tipo NodePort. Esto se debe a que un servicio LoadBalancer es una extensión de un servicio NodePort.
		- (Page 16)
	- -
	- -
		- ¿En qué consiste el recurso Ingress de Kubernetes? #flashcard
		  id:: d61b43ca-27f6-4026-9a3f-d3b9f1a979ad
			- Los recursos Ingress varían de un clúster a otro ya que, aunque son un objeto nativo de Kubernetes, la implementación se basa en un controlador de Ingress, que no se instala por defecto en todos los clústeres. Los controladores disponibles suelen estar
		- (Page 16)
	- -
	- -
		- CONTINUE #flashcard
		  id:: a245177a-bf80-495e-ab44-463dc78211b1
			- basados  en  algún  producto  que  ya  ofrezca  las  funcionalidades  previstas  para  un Ingress, como nginx o envoy, o con un servicio propio de un proveedor de nube, como el Application Load Balancer de AWS . Hay dos razones principales para usar un objeto  Ingress en vez de un servicio. La primera es que cada servicio de tipo  LoadBalancer requiere su propio balanceador de carga con su propia dirección IP pública, mientras que un Ingress solo requiere uno,  incluso  cuando  proporciona  acceso  a  más  de  un  servicio.  Cuando  un  cliente envía  una  petición  HTTP  al  Ingress,  el  nombre  de  host  y  la  ruta  en  la  solicitud determinan a qué servicio se reenvía el tráfico. La  otra  razón  es  que  los  Ingress  ofrecen  más  funcionalidades  que  un  servicio: afinidad  de  sesión  basada  en  cookie,  terminación  de  conexiones  seguras  con certificados TLS, etc.
		- (Page 17)
	- -
	- -
		- ¿Cómo funciona Ingress, en Kubernetes? #flashcard
		  id:: 1d5f57d8-0518-4e57-8f7a-3ffd69f602f6
			- El funcionamiento de un Ingress es el siguiente:   El cliente realiza una búsqueda DNS del equipo al que quiere enviar la petición. El nombre estará registrado con la IP pública del Ingress.   El  cliente  envía  una  petición  HTTP  al  controlador  Ingress  y  especifica  el encabezado Host con el nombre que acaba de resolver mediante DNS.   A  partir  de  ese  encabezado,  el  controlador  determina  a  qué  servicio  está intentando acceder el cliente.   El controlador redirige la petición a la IP de uno de los pods asociados al servicio.
		- (Page 17)
	- -
	- -
		- Los pods reciben una IP de una única subred en todo el clúster, al margen del número de nodos que lo compongan. Los pods pueden comunicarse entre sí sin restricciones. Esto  puede no  ser  relevante  si  el  clúster  está dedicado  a  una  única  aplicación  y  la seguridad de red está correctamente aplicada en los servicios expuestos al exterior. En clústeres compartidos (o multi-tenant), esto puede no ser deseable. Para aplicar reglas de seguridad, en la red interna, hay que usar recursos de tipo NetworkPolicy. #flashcard
		  id:: 50a789c0-560d-4852-9f14-2a7c18b82afa
		- (Page 18)
	- -
	- -
		- ¿Cómo interacciona Kubernetes? #flashcard
		  id:: d2a6a6f3-3a10-4b72-a564-52aa0b1ae765
			- Cualquier interacción con Kubernetes se lleva a cabo en la API mediante peticiones REST, ya sea desde la línea de comandos con kubectl, en el panel web (o dashboard) o desde una aplicación ejecutándose en un pod. Cada llamada atraviesa las fases de autenticación, autorización y control de admisión. En un clúster típico, la API escucha en el puerto 6443 mediante HTTPS. Una vez que se  establece  la  conexión  TLS,  la petición  HTTP  se  mueve  al  paso  de  autenticación. Kubernetes no realiza la autenticación por sí mismo, sino que lo delega a módulos externos.
		- (Page 23)
	- -
	- -
		- Si bien Kubernetes usa nombres de usuario para las decisiones de control de acceso, no almacena nombres de cuenta ni ninguna otra información sobre los usuarios #flashcard
		  id:: c9b8196c-06e1-41ba-9b40-baac717572e3
		- (Page 23)
	- -