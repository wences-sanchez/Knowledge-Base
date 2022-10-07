title:: Herramientas DevOps Tema-3 (highlights) (1)
author:: [[UNIR]]
full-title:: "Herramientas DevOps Tema-3"
category:: #books

tags:: Herramientas-DevOps UNI

- #tags #Herramientas-DevOps #UNI
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/796ee1a6-399d-47f7-966b-eb374b1f110e.jpg)
- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- ¿Qué se entiende como cliente ligero cuando hablamos de aplicaciones de cliente? #flashcard
		- se conoce como cliente ligero a un ordenador liviano que se ha optimizado para establecer una conexión remota con un entorno informático basado en  servidor.  El  servidor  realiza  la  mayor  parte  del  trabajo,  y  entre  estas  tareas  se puede incluir iniciar programas de software, realizar cálculos y almacenar datos.
		- (Page 8)
	- -
	- -
	- ¿Qué se entiende como cliente pesado cuando hablamos de aplicaciones de cliente? #flashcard
		- esto contrasta con un cliente pesado o un ordenador convencional; el primero también está destinado a trabajar en un modelo cliente-servidor, pero tiene un  poder  de  procesamiento  local  significativo,  mientras  que  el  segundo  pretende realizar su función principalmente a nivel local.
		- (Page 8)
	- -
	- -
	- ¿Cuándo decimos que un sistema software tiene una arquitectura monolítica? #flashcard
		- Un sistema de software se llama "monolítico" si tiene una arquitectura en la que los aspectos  funcionalmente  distinguibles  (por  ejemplo,  entrada  y  salida  de  datos, procesamiento de datos, manejo de errores y la interfaz de usuario) están juntos, en lugar de contener componentes arquitectónicamente separados. Una  aplicación  monolítica  es  autónoma  e  independiente  de  otras  aplicaciones informáticas. La filosofía de diseño es que la aplicación es responsable no solo de una tarea en particular, sino que puede realizar todos los pasos necesarios para completar una función en particular
		- (Page 11)
	- -
	- -
	- ¿Qué es una aplicación multicapa? +++ #flashcard
		- Las  aplicaciones  multicapa  son  aplicaciones  compuestas  por  diferentes componentes que se llaman los unos a los otros de una forma lineal. Es decir, cada componente  es  llamado  por  el  inmediatamente  anterior  y  llama  al  posterior.  En ocasiones  se  permite  que  un  componente  se  “salte  capas”  y  llame  a  otros componentes posteriores, pero nunca debería llamarse a capas anteriores. Las capas que  podemos  saltar  se  suelen  denominar  “capas  abiertas”  y  las  que  no,  “capas cerradas”.
		- (Page 15)
	- -
	- -
	- ¿Cuándo es posible aumentar la escalabilidad horizontal desplegando múltiples capas? #flashcard
		- si se tiene cuidado de que la capa de aplicación sea de computación pura y no se permite introducir estado de ningún  tipo  ahí,  es  posible  desplegar  la  capa  de  aplicación  múltiples  veces  para aumentar la escalabilidad horizontal.
		- (Page 16)
	- -
	- -
	- Características más importantes de los microservicios: #flashcard
		-   Divide las piezas en componentes llamados microservicios.   Cada microservicio se comunica con otros microservicios mediante protocolos de petición  y  respuesta  (como  puede  ser  HTTP  o  gRPC)  o  mediante  envío  de mensajes.   Los microservicios no deben acceder a bases de datos compartidas, sino que cada servicio gestiona su propio estado.   No  existe  una  exigencia  de  que  cada  microservicio  esté  formado  por  un  único componente, pero si deben exponer una interfaz única como forma de exponer funcionalidad al sistema completo.   Los  microservicios  deben  ser  resistentes  a  problemas  en  otros  microservicios impactando el servicio global lo menos posible.
		- (Page 18)
	- -
	- -
	- ¿Qué son las mallas de servicios? #flashcard
		- Las  mallas  de  servicios  son  un  complemento  y  una  herramienta  frecuentemente utilizada  junto  con  microservicios.  En  los  microservicios,  hemos  visto  que  cada servicio puede llamar a otro mediante protocolos sencillos. Cuando la cantidad y la escala de los microservicios aumenta, puede ser conveniente generar patrones de comunicación entre los microservicios que nos permitan tener visibilidad sobre cómo se comportan y dotar de un poco más de inteligencia a la red. Las mallas de servicio son una capa de infraestructura configurable que permite una comunicación rápida, con baja latencia y con capacidad de grandes cargas en gran cantidad de servicios.
		- (Page 20)
	- -
	- -
	- Componentes de malla de microservicios #flashcard
		- Marco  de  orquestación  de  servicios.A  medida  que  se  agregan  más  servicios  y componentes  a  la  infraestructura  de  una  aplicación,  una  herramienta  separada para monitorear y administrar el conjunto de los componentes se vuelve esencial. Esta herramienta es frecuentemente Kubernetes, que se estudiará en detalle en la asignatura de contenedores
		- (Page 21)
	- -
	- -
	- Componentes de malla de microservicios #flashcard
		- Servicios  e  instancias.Una  instancia  es  una  copia  única  en  ejecución  de  un microservicio. A veces la instancia es un componente único. Los clientes rara vez acceden a una instancia directamente; más bien acceden a un servicio, que es un conjunto de instancias idénticas que es escalable y tolerante a fal
		- (Page 21)
	- -
	- -
	- Componentes de malla de microservicios #flashcard
		- los. Proxy  sidecar.Un  proxy  de  sidecar  se  ejecuta  junto  con  una  sola  instancia.  El propósito del proxy de sidecar es enrutar, el tráfico desde y hacia el componente al  que  apoya.  El  sidecar  se  comunica  con  otros  proxys  de  su  mismo  tipo  y  es administrado por el marco de orquestación. Muchas implementaciones de malla de servicio usan un proxy sidecar para interceptar y administrar todo el tráfico de entrada y salida a la instancia para asegurarse que siempre se está usando.
		- (Page 21)
	- -
	- -
	- Componentes de malla de microservicios #flashcard
		- Servicio  de  descubrimiento.  Cuando  una  instancia  necesita  interactuar  con  un servicio  diferente,  necesita  encontrar  y  descubrir  una  instancia  saludable  y disponible del otro servicio. Normalmente, la instancia realiza una búsqueda de DNS para este propósito. El marco de la orquestación de componentes mantiene una  lista  de  instancias  que  están  listas  para  recibir  solicitudes  y  proporciona  la interfaz para consultas DNS.
		- (Page 21)
	- -
	- -
	- Componentes de malla de microservicios.
	  
	  parámetros de equilibrio de carga se pueden modificar a través de API, lo que hace posible orquestar implementaciones azul-verde o canarios3. #flashcard
		- Balanceo  de  carga.La  mayoría  de los  frameworksde  orquestación  ya proporcionan  balanceo  de  carga  de  capa  4  (capa  de  transporte).  Una  malla  de servicio  implementa  un  balanceo  de  carga  de  capa  7  (capa  de  aplicación)  más sofisticado,  con  algoritmos  más  ricos  y una  gestión de tráfico  más potente.  Los
		- (Page 21)
	- -
	- -
	- Componentes de malla de microservicios. #flashcard
		-   Cifrado.  La  malla  de  servicios  puede  cifrar  y  descifrar  solicitudes  y  respuestas, eliminando esa carga de cada uno de los servicios. La malla de servicio también puede  mejorar  el  rendimiento  al  priorizar  la  reutilización  de  las  conexiones existentes  y  persistentes, lo  que  reduce la  necesidad  de la  creación computacionalmente costosa de otras nuevas (la mayoría de la criptografía para los  protocolos  como  TLS  consume  muchos  más  recursos  al  inicializar  la comunicación  que  para  enviar  tráfico).  La  implementación  más  común  para encriptar  el  tráfico  es el  TLS  mutuo  (mTLS),  donde  una  infraestructura  de  clave pública  (PKI)  genera  y  distribuye  certificados  y  claves  para el uso  de  los  proxies sidecar.
		- (Page 22)
	- -
	- -
	- Componentes de malla de microservicios. #flashcard
		-   Autenticación  y  autorización.  La  malla  de  servicio  puede  autorizar  y  autenticar solicitudes  realizadas  desde  fuera  y  dentro  de  la  aplicación,  enviando  solo solicitudes validadas a instancias.
		- (Page 22)
	- -
	- -
	- Componentes de malla de microservicios. #flashcard
		-   Soporte  para  el  patrón  del  interruptor  de  circuito.  La  malla  de  servicio  puede admitir el patrón de interruptor, que aísla las instancias poco saludables, y luego las vuelve a colocar gradualmente en el grupo de instancias saludables si vuelven a funcionar.
		- (Page 22)
	- -