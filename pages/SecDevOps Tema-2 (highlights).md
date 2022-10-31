title:: SecDevOps Tema-2 (highlights)
deck:: [[UNI::SecDevOps Tema-2]]
author:: [[UNIR]]
full-title:: "SecDevOps Tema-2"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/3b418aca-9399-4b13-a473-aa28b48392b9.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Cómo funciona la arquitectura del modelo de capas de red? #flashcard
		  id:: 6e2a6801-fe30-4bb4-89d8-f8f3086868e3
			- En la arquitectura en capas todo el proceso de intercambio de tráfico de red se divide en pequeñas tareas. Cada tarea se asigna a una capa determinada, que funciona de manera  dedicada  para  procesar  esa  tarea  específica.  De  esta  forma,  cada  capa  se encarga de  todos  los detalles de  un  trabajo concreto.  Cada  capa  suele  solucionar varios problemas para las capas superiores. En el sistema de comunicación por capas, una capa de un host se ocupa de la tarea realizada por su capa homónima en el mismo nivel, en el host remoto
		- (Page 5)
	- -
	- -
		- ¿Qué se entiende por un host, en una red? #flashcard
		  id:: 3a88cb19-365b-47b7-b5f7-e4ac9ac73bb4
			- Un host se puede referir a un elemento de la red: un switch, un router, un amplificador de señal, una interfaz de red, etc. Básicamente, cualquier equipo que actúa en la red, es decir, que recibe y envía tráfico en cualquiera de las capas, puede ser considerado un host.
		- (Page 5)
	- -
	- -
		- ¿Qué hace la capa de red Aplicación? #flashcard
		  id:: 2999a8f3-59d0-4468-a0a7-6b7615f49cf0
			-   Aplicación: el tráfico en la capa de aplicación es extremo a extremo. El contenido transferido por el protocolo HTTPS de la capa de aplicación a la capa de transporte debe permanecer inalterado hasta que llegue al servidor. Los nodos intermedios no tienen por qué interpretar siquiera este tráfico: podría ser una transferencia de archivos por FTP y las capas inferiores no cambiarían.
		- (Page 7)
	- -
	- -
		- ¿Qué hace la capa de red Transporte? #flashcard
		  id:: 88f15dc7-57f3-43b9-834a-d0e4ff4af06b
			-   Transporte: el flujo en esta capa es también extremo a extremo. La pila TCP/IP de Windows abrirá un socket en un puerto aleatorio en el cliente y añadirá cabeceras a las tramas HTTPS, en las que indicará el puerto del equipo de destino, 443 por ser HTTPS. Además, dividirá las tramas en unidades de menor tamaño e iniciará el envío poco a poco, aumentando la velocidad para evitar congestionar la línea. Si  algún  paquete  se  pierde,  TCP  lo  reenviará  sin  que  el  servidor  web,  ni  el navegador, hagan nada al respecto. Además, el servidor recibirá los paquetes en orden. Este tipo de tráfico se denomina orientado a conexión.
		- (Page 7)
	- -
	- -
		- ¿Qué hace la capa de red "Red"? #flashcard
		  id:: a9986e2a-8508-47f4-9ad7-fa3efec2a326
			-   Red: el tráfico IP no es extremo a extremo. Cada equipo enviará los paquetes a su gateway por defecto o, en el caso de los routers, al siguiente salto en función de su  tabla  de  rutas.  Cada paquete  del  flujo  TCP  superior puede  seguir un camino diferente  sin  que  por  ello  IP  incumpla  sus  garantías  de  servicio.  Aunque  el diagrama solo muestra un router del ISP, es habitual que haya más de uno. En caso de caída de uno, el router de fibra doméstico seguiría enviando los paquetes al router activo. Los equipos sin IP, como el punto de acceso Wifi y el switch ethernet, solo reenvían los paquetes, sin considerar la ruta IP.
		- (Page 8)
	- -
	- -
		- ¿Qué hace la capa de red Enlace? #flashcard
		  id:: d09efb87-c509-488d-85f3-ecc063296374
			-   Enlace: esta capa se encarga de asegurar que no haya errores de transmisión en cada enlace físico. Por ejemplo, el punto de acceso WiFi recibe los paquetes por la antena  WiFi  y  los  retransmite,  sin  errores,  por  su  tarjeta  ethernet.  Todos  los equipos, salvo los que solo se involucran en la capa física, reciben y reenvían los paquetes en esta capa.
		- (Page 8)
	- -
	- -
		- ¿Qué hace la capa de red "Física"? #flashcard
		  id:: c7f44661-635c-4ef5-80ba-bd85d7333038
			-   Física: el medio físico puede ser tan diverso como sea necesario. En el ejemplo hay un medio inalámbrico en la conexión entre el portátil y el punto de acceso, varios cables ethernet que pueden ser de diferentes categorías y un enlace de fibra entre el  router  doméstico  y  el  router  del  ISP.  El  amplificador  de  fibra  se  encarga  de amplificar  la  señal  óptica  analógica,  sin  siquiera  interpretar  la  señal  digital  (los amplificadores de señal son más habituales en medios electromagnéticos, pero el ejemplo a nivel de capas aplica igualmente).
		- (Page 8)
	- -
	- -
		- ¿Cómo interaccionan las capas entre ellas? #flashcard
		  id:: afc8f8a8-281f-4d19-b6b2-f7f0b68a2c4e
			- De manera formal, cada capa ofrece un servicio a la capa superior. Por ejemplo, la capa N puede ofrecer garantías de entregas sin errores a la capa N+1. Las reglas para el funcionamiento interno de una capa definen un protocolo. Una capa ofrece un servicio mediante una interfaz, es decir, una serie de primitivas de software a modo de funciones con sus parámetros.
		- (Page 8)
	- -
	- -
		- Menciona los dos modelos de red en uso. #flashcard
		  id:: f8ba0f1e-b5e6-45a0-8100-45780751a534
			- Hay dos modelos de red principales en uso: el modelo OSI y el modelo TCP/IP. El modelo OSI no ha llegado a ver una implementación en la industria y, por tanto, sus protocolos  no  se  usan.  No  obstante,  el  diseño  se  usa  extensivamente.  El  modelo TCP/IP,  por  el  contrario,  tiene  como  punto  fuerte  sus  protocolos,  ya  que  es  el estándar de facto en las redes de ordenadores e Internet.
		- (Page 9)
	- -
	- -
		- Internet  utiliza  la  suite  de  protocolos  TCP/IP,  por  lo  que  este  modelo  se  puede denominar  también  modelo  de  Internet.  El  modelo  OSI  es  un  modelo  de comunicación  general,  pero  el  modelo  TCP/IP  es  una  colección  de  protocolos concreta,  utilizada  en  Internet  y  en  multitud  de  redes  privadas.  Mientras  que  el modelo OSI precedió a los protocolos OSI, la implementación de TCP/IP vino primero y el modelo se definió después. Sin entrar en detalles sobre su historia, los criterios que dieron pie a TCP/IP fueron:   Resistencia a la pérdida de elementos de red, sin afectar al tráfico existente.   Arquitectura  flexible  capaz  de  soportar  tanto  transferencia  de  ficheros,  como tráfico en tiempo real. El  resultado  fue  una  red  de  conmutación  de  paquetes  basada  en  una  capa  no orientada a conexión, capaz de interconectar múltiples subredes. #flashcard
		  id:: 678a136a-4972-470c-be3f-d3187592ed0d
		- (Page 10)
	- -
	- -
		- Modelos OSI -- TCP/IP: #flashcard
		  id:: 1b1cbabd-712f-4e12-ad66-a3981002474d
			- n
		- (Page 10)
	- -
	- -
		- Comparación entre modelos OSI y TCP/IP: +++ #flashcard
		  id:: bcf5ab75-b835-47e2-8dc3-2c502a93dd1e
			- Como  modelos  que  son,  ambos  son  útiles  para  razonar  sobre  los  servicios  y protocolos  de  la  red.  Sin  embargo,  cada  modelo  tiene  sus  ventajas  y  sus inconvenientes: conexión.   En la capa de transporte, TCP/IP define un protocolo orientado a conexión y uno no orientado a conexión, mientras que OSI solo define un protocolo orientado a   Los protocolos de OSI no han llegado a implementarse, mientras que el modelo TCP/IP se definió como modelo después de la implementación de los protocolos. La industria no llegó a implementar los protocolos de OSI porque TCP/IP ya estaba muy  extendido  y  ninguna  compañía  quería  soportar  dos  pilas  de  protocolos diferentes, aunque el modelo OSI tuviera una definición formal más correcta que la de TCP/IP.
		- (Page 11)
	- -
	- -
		- +++ #flashcard
		  id:: ff766284-9f2c-4c27-a4dd-884d79576158
			-   Aunque el modelo TCP/IP no hace distinciones claras entre servicios, interfaces y protocolos, y no es tan general como OSI. Sus protocolos tienen implementaciones para  múltiples  sistemas.  La  implementación  original  de  TCP/IP  para  UNIX  fue rápidamente aceptada por su calidad, extendiendo su uso en la comunidad.   La  elección  de  siete  capas  en  el  modelo  OSI  fue  más  política  que  técnica  y  las interacciones entre capas son tan complejas, que las primeras implementaciones fueron de muy mala calidad.
		- (Page 12)
	- -
	- -
		- ¿De qué es responsable la capa física de red? #flashcard
		  id:: b29a0641-7035-4524-9f5a-8412d9b7ed3f
			- La  capa  física  es  la  responsable  de  definir  cómo  trabaja  el  hardware  de  red,  las propiedades de los cables, las frecuencias y modulaciones, etc. En el modelo OSI es la única capa que hace referencia a la conectividad física entre dos equipos, ya que el resto de las capas trabajan con abstracciones de software.
		- (Page 12)
	- -
	- -
		- ¿De qué es responsable la capa de enlace? #flashcard
		  id:: 1248333f-b1ba-4db6-b7f3-91e1e91c536d
			- La capa de enlace de datos usa la interfaz de la capa física para pasarle tramas, que esta  convierte  en  pulsos  eléctricos  en  un  cable  de  cobre,  en  señales electromagnéticas en un protocolo inalámbrico y en pulsos de luz en un cable de fibra óptica.
		- (Page 12)
	- -
	- -
		- Explica las cuatro diferentes maneras en que una señal tiende a deteriorarse. #flashcard
		  id:: c77dd163-fabb-40da-8f3d-cd9999ccaa8b
			- Las  señales  tienden  a  deteriorarse  cuando  viajan  a  través  del  medio  por  diversas razones, por ejemplo:   Atenuación:  la  potencia  de  la  señal  (o  más  concretamente,  la  densidad  de potencia de la señal) se reduce a medida que ésta se transmite por el medio. La señal debe tener suficiente potencia en la recepción para que el receptor pueda interpretarla correctamente.   Dispersión: a medida que la señal viaja a través del medio, la banda de frecuencia tiende a extenderse y solaparse.   Retardo: aunque el protocolo defina la velocidad y frecuencia de transmisión, los equipos  pueden  tener  defectos  en  el  hardware,  que  hagan  que  los  parámetros varíen. Si la velocidad de la señal y la frecuencia no coinciden en ambos extremos, hay posibilidades de que la señal llegue al destino de manera arbitraria.   Ruido: se llama ruido en la señal a la perturbación aleatoria que tiene la capacidad de  distorsionar  la  información  real  que  se  está  transmitiendo.  Se  pueden identificar, entre otros: medio. •Ruido térmico: producido por la agitación de los conductores electrónicos del •Intermodulación: producido en transmisiones en banda cuando la frecuencia usada por un canal no se limita adecuadamente y solapa con otros canales. •Crosstalk: producido por señales ajenas a la transmisión, pero que comparten el mismo medio. •Impulso: producido por perturbaciones irregulares e instantáneas.
		- (Page 13)
	- -
	- -
		- ¿Qué hace un multiplexor de red? #flashcard
		  id:: 81f6215e-db5e-4c96-b539-eb70c6a916b1
			- La multiplexación es la técnica que permite aprovechar un medio para enviar más de un flujo continuo de información. En la fuente, un sistema multiplexor combina los canales (así se denominan los flujos) y los transmite en un único medio. En el destino, un  demultiplexor  extrae  cada  canal  y  lo  entrega  de  manera  individual.
		- (Page 14)
	- -
	- -
		- ¿Cómo funciona un FDMA (o Multiplexor por Dvisión de Frecuencia)? #flashcard
		  id:: 4faf533c-9b66-4edc-bfd0-8b522c80fb3b
			-   Multiplexación por división de frecuencia o FDMA: aprovecha la transmisión en bandas de frecuencia para compartir un canal. La transmisión de radio y televisión analógica sirve de ejemplo familiar: hay múltiples canales y cada canal ocupa un cierto ancho de banda (kHz en el caso de la radio, MHz en el caso de  la TV). El diagrama  de  la  Figura  4  muestra  tres  canales  en  banda  base  (que  podrían  ser señales analógicas de telefonía de 4 KHz, por ejemplo) que son mezclados en tres bandas  diferentes.  Cada  canal  mantiene  su  ancho  de  banda  original,  pero  se transmite con una portadora, o frecuencia central, superior.
		- (Page 14)
	- -
	- -
		- ¿Cómo funciona un TDMA (o Multiplexor por División de Tiempo)? #flashcard
		  id:: c8919b3b-278c-46b0-a042-ef0fac6a3b64
			-   Multiplexación por división de tiempo o TDMA: divide el flujo de tiempo en un número  fijo  de  intervalos.  Por  ejemplo,  en  una  división  en  tres  intervalos  se pueden  multiplexar  tres  canales,  tal  como  muestra  la  Figura  5.  Cada  canal aprovecha  todo  el  ancho  de  banda  posible  en  su  intervalo  asignado.  En  esta técnica, el medio multiplexado debe usar una velocidad de transmisión más alta que la suma de velocidades de todos los canales.
		- (Page 15)
	- -
	- -
		- ¿Cómo funciona un CDMA (o Multiplexor por División de Código)? #flashcard
		  id:: 5c6de41c-d992-4421-a0f4-47b687b07af7
			-   Multiplexación  por  división  de  código  o  CDMA:  convierte  una  señal  de  banda estrecha (el equivalente a un canal de FDMA, por ejemplo) en una señal de banda ancha multiplicándola por un código digital mucho más rápido que la variación de la señal de datos. La multiplexación se consigue usando códigos diferentes para cada canal.
		- (Page 15)
	- -
	- -
		- La conmutación es el mecanismo que permite transmitir datos desde una fuente a un destino que no están conectados directamente. Los  nodos  de  interconexión  de  la  red  reciben  datos  de  fuentes  conectadas directamente,  los  almacenan,  analizan  y,  finalmente,  los  envían  hacia  el  siguiente dispositivo de interconexión más próximo al destino. A nivel general, la conmutación puede dividirse en dos categorías principales:   Sin conexión: no se requiere ningún enlace previo y la confirmación de recepción es opcional.   Orientado a la conexión: es necesario establecer el circuito a lo largo de la ruta entre ambos extremos antes de poder intercambiar tráfico. Los datos se envían entonces a lo largo del circuito. El circuito puede cerrarse nada más terminar la transferencia o puede mantenerse temporalmente para un uso posterior. #flashcard
		  id:: 9d1516e9-a6db-4a40-bff8-f665a759df15
		- (Page 16)
	- -
	- -
		- ¿Qué es la conmutación, en redes?
		  id:: 0d050daa-9014-4967-85b9-db73ef797ea2
		  ¿Cuáles son sus dos categorías principales? #flashcard
			- er
		- (Page 16)
	- -
	- -
		- Define qué se entiende como 'conmutación de circuitos' para la capa física. #flashcard
		  id:: b63724e4-57a6-4cba-8611-01d1a2fd1c5f
			- En un sistema de conmutación de circuitos, los datos se transmiten a través de un canal exclusivo. Es necesario que estén especificados los datos que viajan por esa ruta, ya que no se permiten otros en la misma ruta. Además, el  circuito debe estar establecido  para  que  la  transferencia  de  datos  pueda  tener  lugar.  Los  circuitos pueden  establecerse  antes  de la  primera  comunicación  y  mantenerse indefinidamente  (como  en  MPLS)  o  establecerse  y  cerrarse  a  demanda  para  cada transmisión.
		- (Page 16)
	- -
	- -
		- +++ #flashcard
		  id:: 176fc890-5430-4559-a276-aea1cd8480d4
			- El  ejemplo  más  claro  de  conmutación  de  circuitos  es  la  telefonía  analógica tradicional, ya que la señal viaja por un canal exclusivo, no compartido, durante toda la duración de la comunicación.
		- (Page 17)
	- -
	- -
		- ¿Cómo podrías definir la conmutación de mensajes en la capa física de red? #flashcard
		  id:: 333143b3-bd07-4a10-a23a-4a9bd1947bf6
			- La  conmutación  de  mensajes  está  a  medio  camino  entre  la  de  circuitos  y  la  de paquetes: cada mensaje se trata como una unidad y se transmite a lo largo de un canal exclusivo. Un conmutador de mensajes recibe el mensaje entero y  almacena los  datos  temporalmente  hasta  que  haya  recursos  disponibles  para  transferirlo  al siguiente salto del circuito. El conmutador almacenará los datos y se mantendrá a la espera hasta que el conmutador del siguiente salto tenga suficientes recursos. Al igual que en la conmutación de circuitos, la red debe reservar una ruta exclusiva para  la  transmisión.  La  conmutación  de  mensajes  tiene  dos  inconvenientes principales:   Cada dispositivo en la trayectoria del tránsito necesita capacidad de almacenaje suficiente para gestionar el mensaje entero.   La técnica de almacenamiento y reenvío, junto a la latencia debido a las esperas intermedias,  hacen  que  esta  técnica  sea  muy  lenta  en  comparación  a  la conmutación de paquetes. La conmutación de mensajes se sustituyó por conmutación de paquetes al no ser una buena solución para los medios de transmisión en tiempo real.
		- (Page 17)
	- -
	- -
		- ¿Qué es, básicamente, la conmutación de paquetes? +++ #flashcard
		  id:: bc11911a-e157-4633-9546-cbbb5cacecf3
			- En la conmutación, cada mensaje se fragmenta en paquetes de menor tamaño. Cada uno lleva asociado una serie de cabeceras con información sobre el destino, control de  errores,  etc.  Cada  paquete,  con  sus  cabeceras,  se  transmite  de  manera independiente al resto de paquetes.
		- (Page 17)
	- -
	- -
		- ¿De qué se encarga la capa de enlace? #flashcard
		  id:: a0d0bd73-d87a-46d4-b413-3ccebf2495ee
			- la capa encargada de traducir los datos en parámetros que el hardware puede convertir en señales físicas. El receptor recoge los datos del hardware, que están  en  forma  de  señales  eléctricas  u  ópticas,  los  ensambla  en  un  formato  de reconocible, y los entrega a la capa superior.
		- (Page 18)
	- -