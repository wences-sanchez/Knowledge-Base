title:: SecDevOps Tema-5 (highlights)
deck:: [[UNI::SecDevOps Tema-5]]
author:: [[UNIR]]
full-title:: "SecDevOps Tema-5"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/ba7ab082-4d1f-4a8a-8a9c-4f28a3a87f58.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Esta red puede ser una red pública, como Internet, u otra red interna. Por ejemplo, es habitual disponer de cortafuegos regulando el tráfico entre la red a la que se conectan los equipos de usuario y las redes con aplicaciones corporativas. Como resultado, cada solicitud de acceso, desde la red de origen a la red protegida, debe pasar a través del cortafuegos, eliminando la necesidad de protección individual en cada servidor y host de la red protegida. #flashcard
			- Un cortafuegos (aunque el término cortafuegos es una traducción válida de firewall, el término en inglés está tan extendido que se usarán ambos a lo largo del tema) es un sistema de seguridad que controla el acceso a una red protegida, como una red corporativa, desde otra red.
		- (Page 4)
	- -
	- -
		- Para que un firewall sea efectivo, las organizaciones deben tener bien definida una política  de  seguridad  de  red.  Esta  política  identifica  los  recursos  que  necesitan protección y las amenazas que existen contra ellos. A partir de estos datos, define cómo  estos  recursos  pueden  ser  utilizados  y  por  quién,  y  establece  las  acciones  a llevar a cabo cuando se violan estas políticas. #flashcard
		- (Page 5)
	- -
	- -
		- Una política se aplica sobre los dispositivos de red como un conjunto de reglas que comprueban  los  paquetes  que  llegan  a  cada  dispositivo.  Estas  reglas  incluyen  qué tráfico IP desea permitir la organización para que acceda a su red, qué direcciones de origen deben excluirse de la red y qué direcciones de destino pueden ser accedidas desde fuera de la red. En cuanto a las acciones específicas, estas incluyen aceptar o rechazar paquetes #flashcard
		- (Page 5)
	- -
	- -
		- Filtros de paquetes Un filtro de paquetes es un cortafuegos que inspecciona cada paquete de acuerdo con  las  reglas  de  filtrado  que  haya  definido  el  usuario.  Por  ejemplo,  una  regla  de filtrado podría requerir que todas las solicitudes de Telnet se eliminen. Teniendo en cuenta  esta  Información,  el  firewall  bloqueará  todos  los  paquetes  con  el  puerto TCP 23 como destino (el puerto predeterminado para Telnet). Las reglas de filtrado pueden estar basadas en:   Dirección IP de origen.   Dirección IP de destino.   Protocolo de capa 4 (TCP/UDP).   Puerto de destino.     Por lo tanto, un filtro de paquetes toma decisiones basadas en la  capa de red y la capa  de  transporte.  Los  filtros  de  paquetes  son  rápidos  y pueden  implementarse, fácilmente, en rúters existentes. #flashcard
		- (Page 6)
	- -
	- -
		- Servidores proxy Un servicio proxy es una aplicación que redirige las solicitudes de los usuarios hacia servicios basados en la política de seguridad de una organización. Así, un servidor proxy actúa como un intermediario de comunicaciones entre los clientes y servidores de  aplicaciones.  Dado  que  actúa  como  un  punto  de  control  donde  se  validan aplicaciones específicas, un servidor proxy puede convertirse en un cuello de botella si hay demasiado tráfico. Los servidores proxy pueden funcionar tanto en la capa de aplicación como en la de transporte. Los primeros se denominan gateway de aplicación y los segundos gateway de circuito. #flashcard
		- (Page 7)
	- -
	- -
		- Gateway de aplicación Un  gateway  de  aplicaciones  es  un  servidor  proxy  que  proporciona  el  control  de acceso a la capa de aplicación. Dado que opera en la capa de aplicación, es capaz de examinar el tráfico de la capa más alta en detalle y, por lo tanto, es considerado el tipo de firewall más seguro. Genera registros de todas las actividades y aplicaciones de la red, de acuerdo con las necesidades de auditoría de seguridad. Los gateways de aplicación también pueden ocultar información hacia el exterior. Dado  que  todos  los  servicios  en  la  red  protegida  pasan  a  través del  gateway,  este puede proporcionar la funcionalidad de traducción de direcciones de red (u ocultar direcciones  IP)  y  ocultar  direcciones  IP  en  la  red  protegida  desde  Internet, reemplazando la dirección IP de cada paquete saliente (es decir, paquetes que van desde la red protegida a Internet) con su propia dirección IP. #flashcard
		- (Page 7)
	- -
	- -
		- Gateway de circuito Un gateway de circuito es un servidor proxy que valida las sesiones TCP y UDP antes de  permitir  una  conexión  o  un  circuito.  Está  activamente  involucrado  en  el establecimiento de la conexión y no permite que los paquetes se envíen hasta que hayan pasado con éxito las normas de control de acceso. No son tan seguros como los de aplicación, porque no analizan la capa superior. Además, una vez que se ha establecido  una  sesión,  cualquier  aplicación  puede  ejecutarse  a  través  de  esa conexión. Este comportamiento expone la red protegida a los ataques de intrusos. #flashcard
		- (Page 8)
	- -
	- -
		- Filtros de paquetes con estado Los  gateway  de  aplicación  ofrecen  la  mejor  seguridad,  pero  tienen,  también,  los requisitos de procesamiento más alto, lo que puede reducir el rendimiento de la red. Un filtro de paquetes con estado intenta proporcionar seguridad sin comprometer el rendimiento. A diferencia de un gateway de aplicación, un filtro con estado comprueba los datos que pasan a través de la capa de red, pero  no los procesa. El firewall mantiene la información de estado para cada sesión. Si los paquetes nuevos no pertenecen a una sesión válida, ni intentan crear una sesión que cumple con las políticas del firewall, se rechazan. #flashcard
		- (Page 8)
	- -
	- -
		- Un equipo dual-homed es aquel que tiene dos tarjetas de red. Si el host ejecuta un proceso de firewall, las interfaces se pueden aprovechar para una  arquitectura de seguridad concreta: una interfaz está conectada a la red interna y otra interfaz está conectada a Internet, o a alguna otra red no confiable (Figura 2). Por lo tanto, todo el tráfico IP de Internet debe pasar por el firewall antes de llegar a un host en la red privada. Del mismo modo, un host interno puede comunicarse con hosts externos a través del host dual-homed #flashcard
		- (Page 9)
	- -
	- -
		- Cualquier  comunicación indirecta  que intente  esquivar  el  cortafuegos  está bloqueada por diseño, ya que no hay otra conectividad entre las redes más que la que atraviesa el cortafuegos. El host dual-homed puede funcionar como un rúter para garantizar que Internet y la red privada están lógicamente desconectadas, de modo que, incluso cuando haya problemas en el sistema, el cortafuegos no falle. #flashcard
		- (Page 10)
	- -
	- -
		- Cortafuegos de host de rastreo En esta arquitectura, el host que actúa como cortafuegos, llamado bastión, solo se conecta a la red privada. Un rúter de rastreo (o de screening) adicional es colocado entre  el  bastión  e  Internet  (Figura  3).  Por  lo  tanto,  esta  arquitectura  combina  un enrutador de filtrado de paquetes y un gateway de aplicación. El rúter de rastreo realiza una función de filtrado de paquetes, y está configurado para que el bastión sea el único host de la red privada al que se puede acceder desde Internet.  Se  puede  proporcionar  seguridad  extra  para  que  el  rastreo  permita  el tráfico solo a puertos específicos del bastión, bloqueando el resto por defecto. Dado que el anfitrión del bastión es el huésped más expuesto en la red privada, suele ser  el  más  protegido.  Generalmente,  no  hay  un  único  bastión,  sino  varios.  Estos suelen actuar como servidores proxy para servicios públicos como FTP, HTTP o SMTP #flashcard
		- (Page 10)
	- -
	- -
		- Cortafuegos de subred o DMZ El cortafuegos de subred se puede considerar una extensión del cortafuegos de host de rastreo.También incorpora un rúter de rastreo, denominado externo, y un host bastión.  Sin  embargo,  este  cortafuegos  crea  una  capa  adicional  de  seguridad añadiendo una red de perímetroque aísla a la red privada de Internet. Esta  capa define  una  Demilitarized  Zoneo  zona desmilitarizada(DMZ) demarcada por el rúter externo y un rúter interno, tal como muestra la Figura4. Este último es localizado más cerca de la red privada que del enrutador externo. El  bastión servidores de acceso público se encuentran,entonces,dentro de la DMZ #flashcard
		- (Page 11)
	- -