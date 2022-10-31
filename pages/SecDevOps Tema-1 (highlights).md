title:: SecDevOps Tema-1 (highlights)
deck:: [[UNI::SecDevOps Tema-1]]
author:: [[UNIR]]
full-title:: "SecDevOps Tema-1"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/cea640ad-9b5b-4aa0-bcba-957220ce8e67.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
	- No  hay  excepciones  en  la  incorporación  de  controles  de  seguridad  a  un  entorno DevOps. Sí hay diferencias esenciales en cuanto a su aplicación, ya que la velocidad de iteración y las herramientas disponibles son diferentes. #flashcard
		- ¿Cómo de diferente es la incorporación de los controles de seguridad en devops?
		- (Page 4)
	- -
	- -
	- El modelo tradicional de  un  único  ordenador  para  todas  las  necesidades  de  computación  de  una organización  ha  sido  reemplazado  por  un  modelo  en  el  que  un  gran  número  de ordenadores independientes pero interconectados realizan el mismo trabajo. Estos sistemas se denominan redes de ordenadores #flashcard
		- Define "Red de ordenadores".
		- (Page 5)
	- -
	- -
	- «El modelo tradicional de  un  único  ordenador  para  todas  las  necesidades  de  computación  de  una organización  ha  sido  reemplazado  por  un  modelo  en  el  que  un  gran  número  de ordenadores independientes pero interconectados realizan el mismo trabajo. Estos sistemas se denominan redes de ordenadores». Se observa que la definición no habla de servidores y clientes, ni de centros de datos, ni de proveedores de nube. De hecho, los autores usan para su definición la diferencia principal frente un ordenador monolítico: la interconexión de múltiples ordenadores. Esto  sigue  siendo  verdad  a  pesar  de  la  cantidad  de  protocolos  disponibles  en  el mercado #flashcard
		- Define "Red de ordenadores".
		- (Page 5)
	- -
	- -
	- Desde el punto de vista de un administrador, una red puede ser una red privada, que pertenece a un único sistema autónomo y no se puede acceder fuera de su ámbito físico o dominio lógico, o también puede ser pública, a la que todos pueden acceder. En  este  sentido,  una  red  casera  formada  por  un  dispositivo  ADSL  o  de  fibra  y  los equipos  informáticos  conectados  a  ella  con  o  sin  cable  (ordenadores,  teléfonos móviles,  televisiones,  impresoras,  etc.)  es  una  red  privada.  La  red  pública  por antonomasia es Internet. #flashcard
		- Tipos de redes desde el punto de vista de un administrador:
		- (Page 6)
	- -
	- -
	- Los dispositivos pueden conectarse entre sí de diferentes maneras. Esta conectividad puede ser lógica, física o combinada, y existir a diferentes niveles. #flashcard
		- Tipos de red según la interconectividad +++
		- (Page 7)
	- -
	- -
	- Este criterio se refiere al rol que cumplen los dispositivos que pertenecen a la red:   Puede haber uno o más sistemas que actúen como servidor. Un cliente solicita al servidor  que  atienda  las  solicitudes.  El  servidor  toma  y  procesa  la  solicitud  en nombre de los clientes.   Dos sistemas pueden estar conectados punto a punto y formar una red peer-to peer. Ambos residen en el mismo nivel, se les denomina pares. #flashcard
		- Tipos de redes según su arquitectura:
		- (Page 9)
	- -
	- -
	-   Redes de área personal o personal area network (PAN): aquellas con un alcance de  hasta  diez  metros.  Pueden  incluir  dispositivos  habilitados  para  bluetooth  o dispositivos habilitados para infrarrojos.   Redes de área local o local area network (LAN): aquellas que abarcan una oficina o  un  edificio  y  están  operadas  bajo  un  único  sistema  administrativo. Normalmente,  una  LAN  abarca  un  hogar,  una  oficina  o  un  edificio,  pero  puede abarcar  una  extensión  de  un  campus  de  universidad.  El  número  de  sistemas conectados en LAN puede variar desde al menos dos hasta dieciséis millones. Es la topología  habitual  para  compartir  los  recursos  como  impresoras,  servidores  de archivos  o  incluso  acceso  a  Internet  por  parte  de  dispositivos  en  una  misma ubicación.   Redes de área metropolitana o metropolitan area network (MAN): aquellas que cubren  una  ciudad.  Se  pueden  citar  como  ejemplos  las  redes  de  televisión  por cable y las redes WiMAX, aunque solo han tenido aceptación en algunos países.   Redes  de  área  amplia  o  wide  área  network  (WAN):  cubren  una  extensa  zona geográfica que puede expandirse a través de provincias o países. Una WAN tiende a interconectar otras redes. Por ejemplo, cada sucursal de una organización puede tener una LAN para compartir el acceso a Internet y las impresoras, mientras que una WAN, mediante la conmutación de etiquetas de protocolo múltiple (MPLS), conecta todas las LAN para permitir el acceso a una aplicación corporativa ubicada en una oficina principal. #flashcard
		- Explica los cuatro tipos de redes según su extensión geográfica.
		- (Page 10)
	- -
	- -
	- paradigma en el que se integran los procesos de desarrollo de software y operaciones considerando requisitos de seguridad y conformidad». #flashcard
		- ¿Qué se define como SecDevOps? +++
		- (Page 12)
	- -
	- -
	- «Cuando la seguridad se convierte en una parte integral de DevOps, los ingenieros de seguridad puedan desarrollar los controles directamente en el producto, en vez de insertarlo a la fuerza una vez construido» #flashcard
		- ¿Cuándo se introduce la seguridad en el producto en SecDevOps?
		- (Page 12)
	- -
	- -
	-   Deposita una carga útil (payload) en los servidores de destino. Típicamente, será un  script  autocontenido  lo  suficientemente  pequeño  como  para  descargarlo  y ejecutarlo sin llamar la atención.   El script despliega una puerta trasera que contacta con un servidor remoto. En esta  conexión  establece  un  canal  de  comando  y  control  (C2,  command-and control). Los canales C2 pueden consistir en una página HTML con palabras clave ocultas, un registro DNS de tipo TXT que contenga comandos o en una conexión de IRC.   La  puerta  trasera  aplica  las  instrucciones  que  recibe  en  el  canal  C2.  Intentará replicarse a otros nodos de la red con el objetivo de encontrar datos valiosos.   Si se da el caso, usará un segundo canal para hacer llegar los datos al atacante. #flashcard
		- ¿Cuales son los pasos que siguen los atacantes cuando se introducen en una infraestructura?
		- (Page 23)
	- -
	- -
	-   Sistema  de  detección  de  intrusos  o  intrusion  detection  system  (IDS):  los  IDS analizan  el  tráfico  de  red  con  el  objetivo  de  detectar  actividad  fraudulenta. Mientras que un firewall bloquea tráfico en base a unos parámetros fijos de las capas  de  red,  transporte  y  aplicación,  los  IDS  buscan  patrones  específicos  que identifiquen  canales  C2  y  actividades  sospechosas.  La  Figura  6  muestra  un diagrama general de un IDS.   Auditoría de conexión: además de la búsqueda de amenazas en tiempo real, es fundamental  mantener  una  auditoría  de  conexiones  para  llevar  a  cabo  análisis forenses tras un incidente.   Auditoría del sistema: no solo es necesario auditar las conexiones de red, sino el acceso a los sistemas. Un atacante puede ser capaz de ganar acceso a un sistema, pero necesitará, además, ocultar sus pasos para pasar realmente desapercibido. El pipeline de registros podría usar estos datos para detectar intrusiones. #flashcard
		- Herramientas para análisis y detección de intrusiones +++
		- (Page 24)
	- -
	- -
	-   Preparación:  garantizar  que  la  organización  ha  definido  los  procesos  mínimos necesarios para lidiar con un incidente.   Identificación: decidir rápidamente si una anomalía es un incidente de seguridad.   Contención: impedir que la violación se extienda.   Erradicación: eliminar las amenazas de la organización.   Recuperación: devolver la organización a las operaciones normales.   Lecciones aprendidas: analizar el incidente a posteriori para aprender de él. #flashcard
		- Las 6 fases de reacción ante un incidente de seguridad:
		- (Page 25)
	- -