title:: SecDevOps Tema-3 (highlights)
author:: [[UNIR]]
full-title:: "SecDevOps Tema-3"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/8cc6dcc5-636c-4716-860e-28c0b30bc89e.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿De qué se encarga la capa de red? #flashcard
		  id:: c7426225-fe9b-4959-8d35-d4ed4c49be96
			- La  capa 3 del  modelo  de  referencia  es  también llamada  capa  de red.  Gestiona  las opciones  relacionadas  con  el  host  y  el  direccionamiento  de  red;  la  gestión  de subredes e interconexión. También tiene la responsabilidad de enrutar los paquetes desde el origen hasta el destino tanto dentro como fuera de una subred.
		- (Page 5)
	- -
	- -
		- El direccionamiento en red, ¿en qué está basado? #flashcard
		  id:: e8891bc2-2595-43cf-ba8b-fc56ab88da52
			- El direccionamiento es una de las principales tareas de la capa de red. Las direcciones siempre son lógicas, es decir, son direcciones basadas en software, que pueden ser cambiadas de acuerdo con las configuraciones que se especifiquen.
		- (Page 6)
	- -
	- -
		- ¿Dónde se configura la dirección de red? #flashcard
		  id:: dea20f7e-966e-47a1-a0ef-ab136b955557
			- Una dirección de red puede identificar un host (más concretamente, una interfaz de un host) o una red completa. La dirección de red siempre se configura en una tarjeta de  interfaz  y  casi  siempre  está  mapeada  por  el  sistema  con  la  dirección  MAC (dirección de hardware o de la capa dos) de la máquina.
		- (Page 6)
	- -
	- -
		- ¿Qué es un gateway? #flashcard
		  id:: 378f3e6e-ec4d-4648-a2eb-032607bec6a5
			- El gateway será un rúter equipado con una tabla de rutas para poder decidir cómo enrutar  el  paquete  al  host  de  destino.  Las  tablas  de  rutas  contienen  la  siguiente información:   Dirección de la red de destino.   Siguiente salto. Al recibir un paquete, los enrutadores lo envían a su siguiente salto (es decir, uno de los  enrutadores  adyacentes)  en  dirección  hacia  el  destino  final.  Lo  mismo  hará  el siguiente enrutador y, eventualmente, el paquete de datos llegará a su destino.
		- (Page 7)
	- -
	- -
		- ¿Qué cuatro direccionamientos de red existen? #flashcard
		  id:: aa27bd5f-6f0c-42f2-bce7-eae0420a59e9
			- La dirección de red puede ser una de las siguientes:   Unicast: destinada a un host concreto.   Multicast: destinado un grupo.   Broadcast: destinada a todos los hosts de la red.   Anycast: destinada al host más cercano de un grupo.
		- (Page 10)
	- -
	- -
		- ¿Cómo es el enrutamiento unicast? +++ #flashcard
		  id:: ff437fd5-330c-4f38-9172-0d0d797832aa
			- La mayor parte del tráfico en Internet e intranets se envía con un destino concreto y se  conoce  como  tráfico  unicast.  El  enrutamiento  de  datos  unicast,  a  través  de Internet, es la forma más simple de enrutamiento, porque el destino ya es conocido. Por lo tanto, el rúter solo tiene que mirar la tabla de enrutamiento y enviar los datos hasta  el  siguiente  salto.  En  la  Figura  3, por  ejemplo,  el  tráfico  entre  el  host  A  y  el host 1 solo involucra a ambos hosts y a los rúters que los conectan.
		- (Page 10)
	- -
	- -
		- ¿Cómo es el enrutamiento broadcast? +++ #flashcard
		  id:: 01e75a8a-a1fb-4985-bbd6-c5c405cbbfed
			- De forma predeterminada, los paquetes de broadcast no son enrutados ni enviados por los rúters en ninguna red. Los rúters crean dominios broadcast, pero pueden ser configurados  para  enviarlos  en  casos  especiales.  Un  mensaje  de  broadcast  está destinado a todos los dispositivos de la red.
		- (Page 11)
	- -
	- -
		- ¿Cómo es el enutamiento boadcast? #flashcard
		  id:: 1abee003-46b6-4efd-91ad-eaa229d13dd3
			- r
		- (Page 11)
	- -
	- -
		- ¿Cómo es el enrutamiento multicast? +++ #flashcard
		  id:: 6224b470-b383-4c83-a3c9-316d1ee624bd
			- El enrutamiento  multicast, también conocido como  multidifusión, es un caso muy distinto a los anteriores y conlleva nuevos desafíos. El enrutamiento broadcast podría usarse para hacer llegar un flujo a un subconjunto de  equipos  de  la  red,  pero  habría  tráfico  no  deseado,  ya  que  todos  los  nodos  lo acabarían recibiendo. El enrutamiento multicast busca enviar los datos solamente a los nodos que deseen recibirlos.  En  el  diagrama  de  la  Figura  5,  por  ejemplo,  solo  los  hosts  2  y  3  se  han subscrito al flujo emitido por el Host A. Si la ruta a ambos nodos es R1-R4-R6 y R1 R2-R5,  respectivamente,  los  rúters  R2,  R4  y  R3  no  tiene  siquiera  que  recibir  los paquetes del flujo. Además,  el  ancho  de  banda  usado  en  los  enlaces  indicados,  con  las  flechas,  es  el necesario para un único flujo de paquetes del flujo. Si este tráfico fuera unicast, los enlaces Host A-R1 y R1-R4 estarían usando el doble de ancho de banda.
		- (Page 12)
	- -
	- -
		- ¿Cómo es el enrutamiento anycast? +++ #flashcard
		  id:: 66d01321-be96-407e-b4df-fbd843e63a95
			- El reenvío de paquetes anycast es un mecanismo en el que varios hosts de un grupo pueden tener la misma dirección lógica. Cuando se recibe un paquete, este se envía al host que esté más cerca en la topología de enrutamiento.
		- (Page 13)
	- -
	- -
		- +++ #flashcard
		  id:: 854be824-db51-442a-9048-0bb7326b9c86
			- Este enrutamiento se realiza con la ayuda del servidor DNS. El servidor DNS responde a la solicitud con la dirección IP más cercana para el paquete unicast. Por ejemplo, en la Imagen 6, el nodo A envía un paquete anycast al grupo 2. El Host 1 no recibirá el  paquete  por  no  pertenecer  al  grupo  2.
		- (Page 14)
	- -
	- -
		- ¿Cómo funciona el algoritmo de enrutamiento del camino más corto? #flashcard
		  id:: 14897268-ac14-44d9-8e51-8bb3fd7c9007
			- La decisión de enrutamiento en las redes se toma, principalmente, sobre la base del coste de transmitir un paquete entre la fuente y el destino. La métrica que decide la ruta óptima es el número de saltos. Shortest path es una técnica que utiliza varios algoritmos para decidir qué camino tiene el número mínimo de saltos. Los algoritmos más habituales son Dijkstra's, Bellman Ford y Floyd Warshall.
		- (Page 15)
	- -
	- -
		- a #flashcard
		  id:: 51bc1e25-1db0-41fa-92b8-08e73e8b6e5b
		- (Page 15)
	- -
	- -
		- ¿Cómo funciona el algoritmo de enrutamiento de flooding? #flashcard
		  id:: 5eea95b3-a585-41a8-9318-190ca4463648
			- Este es el método más simple de reenvío de paquetes. Cuando se recibe un paquete, los  enrutadores  lo  envían  a  todas  las  interfaces,  excepto  a  aquella  de  la  que  se recibió. Por tanto, se puede considera que este método es, simplemente, una técnica de reenvío más que un algoritmo de enrutamiento como tal.
		- (Page 15)
	- -
	- -
		- ¿Cómo funciona el algoritmo de enrutamiento de vectores de distancia? +++ #flashcard
		  id:: faef37e9-f843-4ec5-a87b-758856d9d238
			- Es un protocolo de enrutamiento que decide sobre el número de saltos que debe haber entre origen y destino. La ruta que contenga la menor cantidad de saltos es considerada como la mejor ruta.
		- (Page 15)
	- -
	- -
		- +++ #flashcard
		  id:: 201220a0-8cc8-42e8-a524-02d288f40db4
			- Cada rúter anuncia sus mejores rutas establecidas a otros rúters. En última instancia, todos los enrutadores construyen su topología de red, basada en la información que les proveen sus rúters vecinos. RIP, de Routing Information Protocol, es un ejemplo de protocolo que usa un algoritmo de enrutamiento basado en vectores de distancia.
		- (Page 16)
	- -
	- -
		- ¿Cómo funciona el algoritmo de enrutamiento de estado de enlace? #flashcard
		  id:: 90c76460-c43b-47df-a6b1-50433bbfca14
			- El protocolo de estado de enlace es, ligeramente, más complicado que el vector de distancia. Toma en cuenta los estados de enlaces de todos los rúters en una red. Esto ayuda  a  las  rutas  a  construir un  gráfico  común de  toda  la  red.  Los  rúters  calculan luego su mejor camino para fines de enrutamiento. Algunos protocolos que usan este método son Open Shortest Path First (OSPF) e Intermediate System to Intermediate System (ISIS).
		- (Page 16)
	- -
	- -
		- ¿En qué consiste el tunneling? +++ #flashcard
		  id:: 5526d643-fe9f-469a-9425-cf02741f39a0
			- El despliegue de túneles, o tunneling, es una técnica que consiste en encapsular un protocolo de red sobre otro (protocolo de red encapsulador), creando un túnel de información dentro de una red de computadoras. Ambos extremos del  túnel están configurados de manera específica.
		- (Page 17)
	- -
	- -
		- +++ #flashcard
		  id:: 1850bf89-1bb0-404d-a9b7-6729a4ed9dc8
			- Cuando  los  datos  entran  desde  un  extremo  del  túnel,  se  etiquetan  con  unas cabeceras adicionales. Estos datos etiquetados son enrutados en el interior de una red  intermedia  o  de  tránsito  hasta  llegar  al  otro  extremo  del  túnel.  Cuando  la información sale del túnel, se elimina su etiqueta y se entrega en otra parte de la red. Ambos extremos parecen estar conectados directamente y el etiquetado hace que los datos viajen a través de la red sin modificaciones. Los  túneles  alteran  la  arquitectura  de  capas.  En  el  ejemplo  de  la  Figura  8,  el contenido  de  los  paquetes  IPv4  no  son  tramas  del  nivel  de  transporte,  como correspondería, sino tramas de nivel de red del tráfico que se desea transmitir por el túnel. La Figura 9 muestra la estructura de capas de este ejemplo. Como se puede ver, hay dos capas de nivel 3.
		- (Page 18)
	- -
	- -
		- ¿Cómo se define una dirección MAC y cómo puede ser encontrada? #flashcard
		  id:: 05c277c0-e43d-447a-8403-a0c2c12898f7
			- La  dirección  MAC  está  físicamente  grabada  en  la  tarjeta  de  interfaz  de  red  de  un equipo y nunca cambia. En un entorno virtualizado, una NIC virtual recibe una MAC del hipervisor. Esto puede provocar que haya MAC duplicadas, ya que la asignación es  aleatoria,  pero  los  hipervisores  tienen  mecanismos  para  evitar  que  las  MAC  se repitan en una misma red virtual. En cualquier caso, la NIC virtual de una máquina virtual (VM) no suele cambiar a lo largo de su vida. Para conocer la dirección MAC del host remoto en una subred, el ordenador de origen envía un mensaje broadcast ARP preguntando qué host tiene dirección de IP. Debido a que es un mensaje broadcast, todos los hosts del segmento de red, que equivale a un dominio de broadcast, reciben este paquete y lo procesan.
		- (Page 20)
	- -
	- -
		- ¿Cómo es mapeada la dirección MAC a la IP? #flashcard
		  id:: 34e1b4ef-037c-4eb0-aaae-cce041ba4aeb
			- El paquete ARP contiene la dirección IP del host de destino al que el host de origen quiere  contactar.  Cuando  un  host  recibe  un  paquete  ARP  que  se  le  ha  destinado, responde con su propia dirección MAC. Una vez que el host recibe la dirección MAC de destino, puede comunicarse con el host remoto utilizando el protocolo de enlace. Este mapeo del MAC al IP se guarda en una caché de ambos hosts. Si en el futuro necesitan comunicarse pueden, directamente, dirigirse a su caché ARP.
		- (Page 21)
	- -
	- -
		- ¿Qué protocolo es el que usamos cuando hacemos 'ping' en un SO? #flashcard
		  id:: 8c49590c-c77d-4ce0-8f30-6a8545699507
			- Internet Control Message Protocol (ICMP) ICMP es un protocolo de diagnóstico y notificación de errores de red. Pertenece al protocolo IP y utiliza IP como protocolo de encapsulamiento. Después de construir el paquete ICMP, se encapsula en un paquete IP. Los hosts usan ICMP para informar si se produce algún error en la red. Este ofrece opciones para informar que contiene docenas de mensajes de diagnóstico y reporte de errores. operativos). Los  mensajes  de  ICMP-echo  y  ICMP-echo-reply  son  los  mensajes  ICMP  más comúnmente utilizados para comprobar la  accesibilidad de los hosts de extremo a extremo  (son  más  conocidos  como  ping,  y  así  se  llama  la  utilidad  en  los  sistemas Cuando un host recibe una solicitud ICMP-echo, está obligado a enviar una respuesta ICMP-echo. No obstante, es habitual que muchos firewalls de red y de host descarten los mensajes de ping como medida de seguridad
		- (Page 21)
	- -
	- -
		- ¿Cómo podemos expresar un prefijo de red de 16 bits en una dirección IP? #flashcard
		  id:: e69f7159-c462-4fcb-b7c0-c65fcd63dc28
			- Los prefijos se escriben dando la dirección IP más baja en el bloque y el tamaño del bloque. Por convenio, el tamaño del prefijo en bits se escribe después de la dirección IP. Así, si la IP anterior pertenece a una red con un prefijo de 16 bits, el prefijo de red se indicaría como 172.16.0.0/16.
		- (Page 22)
	- -
	- -
		- +++ #flashcard
		  id:: ee1bba7e-48cc-4574-a828-ce3e74657d3c
			- La longitud del prefijo corresponde a una máscara binaria de unos en la parte de la red,  llamada  máscara  de  red.  Si  se  aplica  un  AND  lógico  entre  la  dirección  IP  y  su máscara,  se  obtiene  el  bloque  de  red.  En  el ejemplo,  con un prefijo de 16  bits,  la máscara  de  subred  es  255.255.0.0,  que  consisten  en  2  bytes  de  unos  seguido  de 2 bytes a cero.
		- (Page 23)
	- -
	- -
		- +++ #flashcard
		  id:: 0e7e09b5-edd4-44d9-8bb2-972dd2f129ce
			-   Primero, la dirección IP de un host depende de dónde se encuentre en la red. Las direcciones  Ethernet  se  pueden  usar  en  cualquier  parte  del  mundo,  ya  que  se utilizan  para  direccionamiento  en  un  medio  común;  pero  cada  dirección  IP pertenece  a  una  red  específica,  y  los  rúters  solo  podrán  entregar  paquetes destinados a esa dirección a la red, ya que el direccionamiento es global.
		- (Page 23)
	- -
	- -
		- ¿Por qué es negativo jerarquizar las direcciones IP? #flashcard
		  id:: af2ac4c4-6955-48cf-ad7f-9338fe721547
			-   La  segunda  desventaja  es  que  la  jerarquía  es  un  desperdicio  de  direcciones,  a menos que se administre cuidadosamente. Si las direcciones se asignan a redes en bloques demasiado grandes, habrá muchas direcciones asignadas que no estarán en  uso.  Esta  distribución  no  importaría  mucho  si  hubieran  muchas  direcciones para todos, pero no es el caso. IPv6 es la solución a esta escasez, pero hasta que se implemente de manera amplia, habrá una gran presión para asignar direcciones IP de manera muy eficiente.
		- (Page 24)
	- -
	- -
		- ¿Cuáles son las tres categorías de direcciones IP, teniendo en cuenta sus subredes? +++ #flashcard
		  id:: 25e1efdc-269f-436e-a6be-da75afe97906
			- Las direcciones IP están divididas en tres categorías principales:   Clase  A:  utiliza  el  primer  octeto  para  las  direcciones  de  red  y  los  últimos  tres octetos para el direccionamiento del host.   Clase  B:  utiliza  los  primeros  dos  octetos  para  las  direcciones  de  red  y  los  dos últimos para el direccionamiento del host.   Clase C: utiliza los primeros tres octetos para las direcciones de red y el  último para el direccionamiento del host.
		- (Page 24)
	- -
	- -
		- ¿Qué es el CIDR? #flashcard
		  id:: 2f9fbe2a-de36-4e31-8ef0-2b356b2ee3a1
			- Depende de cada rúter tener la información de prefijo correspondiente. Este diseño funciona  a  base  de  subredes  y  se  llama  Classelss  Inter-Domain  Routing  (CIDR)  o enrutamiento entre dominios sin clase. CIDR permite el diseño de jerarquía de red, sin seguir el tamaño estricto de las clases A, B y C.
		- (Page 25)
	- -
	- -
		- +++ #flashcard
		  id:: 526cbb8b-253b-4669-b221-a53920175610
			- La idea básica detrás de NAT (Network Address Translation, traducción de direcciones de red) es que el ISP asignará a cada cliente una única dirección IP para el tráfico de Internet. Dentro de la red del cliente, cada equipo obtiene una dirección IP única, que se utiliza para enrutar el tráfico local, es decir, entre dos equipos del cliente.
		- (Page 25)
	- -
	- -
		- ¿Qué es y cómo se usa NAT? +++ #flashcard
		  id:: b095d9ca-6d8c-4b9d-b606-400de62e8813
			- Sin embargo, en el tráfico dirigido a Internet, justo antes de que un paquete salga de la red del cliente y vaya al ISP, se realiza una  traducción de la dirección IP interna única a la dirección IP pública compartida. Esta traducción hace uso de tres rangos de direcciones IP que se han declarado como privadas (mostradas previamente en la Tabla 2). Los usuarios pueden usarlas internamente como lo deseen. La única regla es que ningún paquete que contenga estas direcciones puede aparecer en Internet. El funcionamiento de NAT se muestra en la Figura 11. Dentro de las instalaciones del cliente,  cada  máquina tiene una dirección  única  en  la  red  10.x.y.z. Sin  embargo, antes de que un paquete salga de las instalaciones del cliente, pasa a través de un equipo con soporte de NAT que convierte la dirección IP de origen interna, 10.0.0.1 en la Figura 11, a la dirección pública del cliente, 198.60.42.12. La caja NAT a menudo se integra en un solo dispositivo con un firewall o un rúter.
		- (Page 26)
	- -
	- -
		- ¿Qué es TCP y cuáles son sus principales características? #flashcard
		  id:: 3b62a5b1-9d7e-4b8f-89f2-0358c02f2eb3
			- El protocolo de control de transmisión o TCP es uno de los más importantes de la suite de protocolos de Internet.   Es un protocolo fiable. Es decir, el receptor siempre envía una confirmación, ya sea positiva o negativa, sobre la recepción del paquete de datos al remitente, de manera  que  este  último  siempre  está  al  tanto  de  si  el  paquete  ha  llegado  en buenas condiciones, o si hace falta reenviarlo.   Asegura que los datos lleguen a destino en el mismo orden o secuencia en el que han sido enviados. capa superior.   Establece una conexión entre los hosts antes de iniciar el envío de los datos de la   Proporciona un mecanismo de comprobación de errores y recuperación.   Proporciona una comunicación de extremo a extremo, control del flujo y calidad de servicio.   Funciona en modo cliente/servidor, punto a punto.   Ofrece un servicio dúplex completo.
		- (Page 31)
	- -
	- -
		- ¿Cómo se establece la conexión entre un cliente y un servidor con ACKs? +++ #flashcard
		  id:: aee1fcfd-f535-4c01-b7b1-83e3c5f5eb82
			- El  cliente  inicia  la  conexión  y  envía  el  segmento  con  un  número  de  secuencia.  El servidor  lo  reconoce  con  su  propio  número  de  secuencia  y  ACK  del  segmento  del cliente, que es uno más que el número de secuencia del cliente. El cliente, después de recibir el ACK de su segmento, envía un acuse de recibo de la respuesta del servidor.
		- (Page 34)
	- -
	- -
		- +++ #flashcard
		  id:: 9b2f26e1-c647-4b7a-b0a2-ec5a742df0f6
			- Cualquiera  de  los  servidores  y  clientes  pueden  enviar  un  segmento  TCP  con  el indicador  FIN  establecido  en  1.  Cuando  el  extremo  receptor  responde  dando  un acuse de recibo FIN (ACK FIN), en esa dirección de TCP se cierra la comunicación y se libera la conexión.
		- (Page 35)
	- -
	- -
		- ¿Qué se conoce como UDP? #flashcard
		  id:: 8480f1a8-df3e-40fd-b9be-4107185b6c36
			- Protocolo de datagrama de usuario UDP es el protocolo más sencillo de la capa de transporte disponible para la suite TCP/IP. Se suele decir que UDP es poco fiable, pero, realmente, ofrece este servicio como tal: delega el control de entrega a la capa de aplicación para, a cambio, evitar la latencia inicial del 3-way handshake y el reenvío de paquetes si no es necesario. En UDP, el receptor no genera un acuse de recibo del paquete recibido y, por ende, el remitente no lo espera. Esta limitación hace que este protocolo sea poco fiable a la vez que más fácil de procesar.
		- (Page 38)
	- -