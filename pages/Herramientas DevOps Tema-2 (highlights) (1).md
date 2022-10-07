title:: Herramientas DevOps Tema-2 (highlights) (1)
author:: [[UNIR]]
full-title:: "Herramientas DevOps Tema-2"
category:: #books

tags:: Herramientas-DevOps UNI

- #tags #Herramientas-DevOps #UNI
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/3b22eac9-0447-4713-889e-9855b3774798.jpg)
- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- ¿A qué nos referimos cuando hablamos de componente en DevOps? #flashcard
		- En el caso de DevOps, hablaremos de un componente como una pieza desplegable, independientemente de que pudiera tener su propio ciclo de vida. En ocasiones varios componentes compartirán su ciclo de vida, pero no es necesario que todos los componentes de una aplicación compartan el mismo ciclo de vida.
		- (Page 5)
	- -
	- -
	- ¿Cuándo se dice que un componente guarda un estado? #flashcard
		- la pieza de  información  más  relevante  sobre  un  componente  es  si guarda  estado  o  no.  Un  componente  guarda  estado  cuando  puede  variar  su respuesta una misma pregunta sin necesidad de que haya variado la respuesta de algunas de las peticiones a otros componentes.
		- (Page 5)
	- -
	- -
	- ¿Qué caracteriza a un componente sin estado? #flashcard
		- Los componentes sin estado son fácilmente reemplazables ya que una copia idéntica del mismo componente debería poder responder a las peticiones idénticamente. Esto tiene  amplias  consecuencias  operacionales  que  nos  permiten  adoptar  estrategias sencillas  de  balanceo  de  carga  o  reemplazar  completamente  un  componente  que está funcionando incorrectamente por uno nuevo.
		- (Page 5)
	- -
	- -
	- ¿Cuándo puede (o no) un estado de un componente ser reconstruido? #flashcard
		- En realidad, esta dicotomía es un gradiente, ya que parte de la pregunta es cuánto nos cuesta reconstruir la información. Es posible que sea imposible, que sea necesario volver a preguntar a nuestros clientes, que necesitemos recuperar otras copias o realizar costosos cómputos o por último que la información sea barata de replicar, pero solo perdamos unos pocos recursos sin afectar operacionalmente a la aplicación completa.
		- (Page 6)
	- -
	- -
	- Un componente, ¿puede ser reusable? #flashcard
		- Los componentes pueden o no ser reusables entre proyectos de la misma empresa o de otras. Cuando  una  componente  puede  definirse  con  una  API  reusable  que  es frecuentemente  necesaria,  podremos  encontrar  componentes  en  el  mercado  que podemos incluir en nuestra arquitectura de forma reusable. Frecuentemente, habrá partes de la aplicación que son únicas de nuestra aplicación y sobre estos componentes habremos de programar nuestra lógica, o bien configurar esa lógica si hemos encontrado una solución que nos permita reusar partes.
		- (Page 6)
	- -
	- -
	- ¿Cuáles son los componentes que más frecuentemente cambian en las aplicaciones? #flashcard
		- Los componentes de cómputo son algunos de los componentes más comunes y que más frecuentemente cambian en las aplicaciones. La lógica de negocio suele cambiar más frecuentemente que otros componentes y es la  parte  que  se  desarrolla  localmente,  en  lugar  de  usar  componentes  puramente reusables; por ese motivo es importante desarrollar técnicas y adoptar prácticas y herramientas que permitan la gestión de este tipo de componentes.
		- (Page 8)
	- -
	- -
	- ¿Cuáles son las principales necesidades de un componente de cómputo? #flashcard
		- Las principales características son las necesidades de procesamiento (CPU), las de memoria volátil (RAM) y las de memoria más lenta pero grande (disco).
		  
		  Las necesidades de procesamiento (CPU) hace años que han dejado de crecer exponencialmente para crecer mucho más lentamente, lo que ha ocasionado que en ocasiones se hable simplemente del número de cores o vcpu que se le da al componente de cómputo.
		  
		  La memoria RAM permite almacenar información de precálculo (ciertas cachés), así como información de las peticiones en curso. Si la información de precálculo acaba siendo demasiado grande o compleja de recalcular, el componente puede empezar a comportarse como un componente con estado.
		  
		  Frecuentemente, la memoria se invertirá en guardar la información necesaria para calcular la peticiones o tareas en curso.
		  
		  El disco no deja de ser un almacenamiento de memoria más a largo plazo. Suele sobrevivir a reinicios lo que lo hace conveniente para almacenar el estado
		- (Page 8)
	- -
	- -
	- ¿Qué es la IaaS? #flashcard
		- Esta es la tecnología básica para obtener cómputo en la nube. En este caso lo que hacemos  es  obtener  servidores,  virtuales  o  no,  como  un  servicio  donde  nosotros configuraremos sus funciones de cómputo.
		- (Page 9)
	- -
	- -
	- ¿Qué es la PaaS? #flashcard
		- Las plataformas como servicios frecuentemente se definen en base a una plataforma de ejecución que es capaz de tomar código y levantar procesos que se asemejan a servidores dependiendo del consumo que requiramos. En este caso, la plataforma de ejecución suele conllevar  restricciones importantes para que pueda tomar nuestro código y ejecutar y las aplicaciones suelen ser menos portables  entre  proveedores  que  con  otras  tecnologías.  A  cambio,  este  tipo  de aplicaciones suelen traer herramientas sofisticadas de integración de nuestro código y de despliegue que pueden ayudar a reducir el esfuerzo en automatismos que debe realizar un equipo de DevOps. A cambio, este tipo de plataformas frecuentemente cobran el cómputo considerablemente más caro que otras soluciones y es un factor que tendremos que considera según vaya cambiando nuestra escala.
		- (Page 11)
	- -
	- -
	- ¿Qué es el CaaS? #flashcard
		- Las  plataformas  de  contenedores  como  servicio  son  plataformas  que  permiten ejecutar nuestros contenedores basados en las imágenes que nosotros generemos sin necesidad de gestionar los nodos de cómputo. Este tipo de plataformas está experimentando un gran crecimiento y hay un amplio ecosistema  de  herramientas  que  nos  permiten  generar  a  nosotros  un  CaaS,  como podría ser Docker Swarm, Nomad o Kubernetes. Por otro lado, muchos proveedores de nube nos ofrecen un sistema como Kubernetes pero gestionado por ellos lo que se comporta como CaaS.
		- (Page 12)
	- -
	- -
	- ¿Qué es el FaaS? #flashcard
		- Las funciones como servicio son componentes de cómputo que se definen con una pieza de código o función que reacciona a un evento. En este paradigma, no se define un proceso que sirve peticiones u obtiene trabajo de una cola de mensajes, sino que la función es “ejecutada” cuando ocurre un evento, que podría ser una nueva petición o un nuevo mensaje en una cola de trabajo, y ejecuta hasta que el evento se completa y la ejecución de la función finaliza.
		- (Page 12)
	- -
	- -
	- Características de las FaaS: +++ #flashcard
		- En el caso de FaaS existen varios impactos para DevOps que tenemos que considerar:   Cada función realizará una tarea relativamente pequeña. Esto hace cada función sencilla  pero  la  coordinación  entre  ellas  y  la  arquitectura  global  puede  ser complicada.  Es  importante  tener  una  estrategia  de  compatibilidad  entre  las distintas funciones y una buena separación y coordinación de los despliegues al haber más piezas. Si no hay peticiones, no existe consumo. Por este motivo las funciones o lambdas son muy utilizadas para peticiones infrecuentes y pueden conllevar un gran ahorro de recursos en estos casos.   La  ejecución  de  una  función  implica  arrancar  un  entorno.  Aunque  esto  es relativamente rápido es importante medir lo que se suele denominar cold start o arranque  en  frío.  Si  la  función  se  ha  ejecutado  recientemente,  los  proveedores suelen tener una caché de parte del arranque y las ejecuciones serán mucho más rápidas.   El coste de las ejecuciones suele ser más elevado que la misma ejecución en un servidor o un contenedor siempre que ese contendor tenga una utilización alta.
		- (Page 13)
	- -
	- -
	- Existen arquitecturas y proyectos completos que se empiezan a realizar con Functions o Lambdas, pero la mayoría no las usan exclusivamente. Sin embargo, estas funciones son  extraordinariamente  útiles  para  realizar  automatizaciones  alrededor  del ecosistema  DevOps.  Por  ejemplo,  realizar  backups,  comprobaciones  después  de escalados, tareas recurrentes o pequeñas tareas muy esporádicas, pero importantes, que  no  encajan  bien  en  otras  piezas  de  la  arquitectura.  Es  una  herramienta importante, aunque ahora mismo no sea conveniente utilizarla exclusivamente. #spaced
		- (Page 14)
	- -
	- -
	- Acrca d las Lambdas n l Cloud. #flashcard
		- e
		- (Page 14)
	- -
	- -
	- ¿Cómo se pueden escalar las aplicaciones dependiendo de si tienen estado o no? #flashcard
		- La  gestión  del  estado  es  una  de  las  tareas  más  importantes  y  complicadas  en aplicaciones DevOps. Mientras las aplicaciones sin estado suelen ser fáciles de escalar “horizontalmente”,  es  decir,  añadir  más  piezas  idénticas,  esto  suele  ser  más complicado en la gestión del estado. En muchas ocasiones utilizaremos un escalado “vertical” es decir, aumentando las capacidades de cómputo y almacenamiento para almacenar y responder a consultas más rápidamente. Existen  componentes  de  gestión  del  estado  con  buenas  capacidades  de  escalado horizontal y existen técnicas, como el sharding, que consiste en partir la información en bloques distintos y guardarlos en componentes distintos permitiéndonos escalar horizontalmente.
		- (Page 14)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente al contenido y consulta, conocido como OLAP. #flashcard
		-   OLAP (On-Line Analytical Processing) son bases de datos que se utilizan para dar servicio a los clientes en vivo respondiendo a preguntas, tradicionalmente sobre el estado actual y gestionando este estado. Son las bases de datos más utilizadas y  la  mayoría  de  las  bases  de  datos  SQL  y  muchas  otras  como  las  orientadas  a documento o grafo frecuentemente se utilizan de esta forma. En estas bases de datos,  es  importante  la velocidad  de  consulta  y guardado  y  la  integridad  de  los datos (véanse garantías como consistencia eventual y ACID).
		- (Page 15)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente al contenido y consulta, conocido como Data Warehouse. #flashcard
		-   Data Warehouse o almacenamiento de datos, son bases de datos que se utilizan para  almacenar  datos  históricos  del  progreso  del  sistema  para  un  análisis posterior. En este tipo lo importante suele ser el coste de almacenamiento a largo plazo, la capacidad de consulta y agregación de grandes cantidades de datos y la capacidad  de  ingesta  de  grandes  cantidades  de  datos  en  grupos  (trabajos  de backup diarios) o en vivo mediante un stream. No es tan importante el tiempo de respuesta de una escritura en concreto sino la velocidad del conjunto.
		- (Page 15)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como SQL. #flashcard
		-   SQL:  las  bases  de  datos  SQL  son  las  más  conocidas  y  utilizadas.  Existen implementaciones  de  código  abierto  muy  utilizadas  como  MySQL,  PostreSQL  o SQLite y otras de código privativo como Oracle DB extraordinariamente potentes. Son muy utilizadas en la industria. Su principal característica es la definición de esquemas  basados  en  tablas  y  sus  relaciones  que  permiten  realizar  consultas cruzadas bastante eficientemente. Debido a la madurez de las implementaciones, pueden ser aplicadas en muchos entornos.
		- (Page 16)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como orientadas a documentos. #flashcard
		-   Orientadas  a  documentos:  las  bases  de  datos  orientadas  a  documentos almacenan un concepto de Documento y se basan principalmente en obtenerlo y procesarlo. En esta categoría entran desde bases de datos clave valor como Redis, bases  de  datos  de  documentos  que  permiten  consultas  más  complejas  como MongoDB o Couchbase y algunas bases de datos que veremos posteriormente de búsqueda como ElasticSearch.
		- (Page 16)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como orientadas a grafo. #flashcard
		- Las bases de datos orientadas a grafo se basan en definir unas entidades o Nodos que se relacionan entre ellos mediante Vértices. La principal característica de estas bases de datos es que incluyen algoritmos para recorrer esas relaciones de formas potentes y con un rendimiento bueno.
		- (Page 16)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como orientadas a columna. #flashcard
		-  Orientadas a columna: las bases de datos orientadas a columna se basan principalmente en guardar documentos, pero el foco es en la especificación de las columnas y su almacenamiento conjunto. En lugar de guardar cada documento en un sitio, se guarda el valor de una columna para todos los documentos conjuntamente. Esto permite realizar agregaciones muy eficientes.
		- (Page 16)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como Backups. #flashcard
		-   Backups: es esencial tener un sistema de backups con automatización para poder recuperarlos (no solo almacenar el backup, también un proceso para restaurarlo). Los  backups  permiten  reducir  la  cantidad  de  datos  perdidos  en  el  caso  de  un incidente y aumentar la velocidad de restauración de servicio.
		- (Page 17)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como migración de esquemas y datos. #flashcard
		-   Migración  de  esquemas  y  datos:  es importante  tener  técnicas  para  el mantenimiento de los datos con las necesidades de la aplicación. Es frecuente que los  datos  deban  cambiar  de  estructura,  cambiarse  esquemas,  añadirse  campos adicionales  o  migrar  un  tipo  de  organización  a  otra.  Tener  automatismos  o  al menos procesos para realizar estos cambios reduce drásticamente el número de desperfectos cuando estos cambios se necesitan.
		- (Page 17)
	- -
	- -
	- Habla acerca del tipo de BBDD, referente a su interfaz exterior o paradigma, conocido como Redundancia y alta disponibilidad. #flashcard
		-   Redundancia y alta disponibilidad: la redundancia nos permite tener más de un componente idéntico disponible que puede reemplazar otro en caso de problema. Existen diferentes técnicas de redundancia y alta disponibilidad y algunas de ellas también permiten una escalabilidad horizontal. Las técnicas más frecuentes son el Activo-Pasivo, donde hay dos bases de datos con una funcionando (activa) y una segunda  lista  para  trabajar  con  una  copia  idéntica  de  los  datos  si  hubiera  un problema.  Activo-Activo  permite  a  dos  bases  de  datos  estar  trabajando simultáneamente repartiendo la carga. Esto solo aumentaría la redundancia es la caída de uno o varios nodos no hace la utilización subir por encima del 100 %
		- (Page 17)
	- -
	- -
	- ¿Cómo funciona el concepto maestro-esclavo en bases de datos? #flashcard
		- otra técnica, Maestro-Esclavo o Replica Set donde uno de los nodos es el que gestiona las escrituras y el resto responden a las lecturas. Si los nodos de lectura pueden promocionar a un nodo de escritura cuando este se rompa, esto también ayudará a la disponibilidad.
		- (Page 18)
	- -
	- -
	- Las colas de mensajería se utilizan para distribuir mensajes entre diferentes componentes del sistema. Existen muchos tipos de colas de mensaje y diversas implementaciones. Estas en general permiten comunicar a un productor con uno o varios consumidores del mensaje.
	  
	  Una de las principales características de esta tecnología es que las peticiones son asíncronas, el productor envía el mensaje y el consumir puede recibirlo tiempo después.
	  
	  Esto permite aumentar la resistencia del sistema a picos de consumo ya que la cola de mensajes puede balancear la carga. #spaced
		- (Page 18)
	- -
	- -
	- Patrón de consumo de cola de mensajes conocido como Colas de trabajo: +++ #flashcard
		-   Colas de trabajo: en estas se tiene un productor y varios consumidores. Todos los consumidores toman tareas de la misma cola y cada tarea o mensaje es consumida por  solo  uno  de  estos  consumidores.  Esta  técnica  permite  distribuir  la  carga  y atender a los mensajes rápidamente. Si uno de los consumidores falla, no se pierde el servicio solo se tardará más en atender un mensaje determinado.
		- (Page 19)
	- -
	- -
	- Patrón de consumo de cola de mensajes conocido como Pub/Sub o publicación y suscripción #flashcard
		-   Pub/Sub o publicación y suscripción: en este modelo, los mensajes se envían a un “tema” y los consumidores pueden apuntarse a uno o varios  “temas” de donde recibirán  todos  los  mensajes  que  lleguen.  La  principal  diferencia  con  la  cola  de trabajo  es  que  los  mensajes  que  lleguen  ahí  se  van  a  distribuir  a  todos  los consumidores  no  solo  a  uno.
		- (Page 20)
	- -
	- -
	- Patrón de consumo de cola de mensajes conocido como Enrutado sofisticado: +++ #flashcard
		-   Enrutado sofisticado: muchos sistemas de mensajería permiten definir diferentes colas  de  mensajes  dependiendo  de  características  del  mensaje.  Esto  permite realizar diferentes tipos de patrones más sofisticados.
		- (Page 20)
	- -
	- -
	- Patrón de consumo de cola de mensajes conocido como Llamada a un procedimiento remoto. #flashcard
		- Esta técnica es menos usada ya que realmente implementa un protocolo de pregunta y respuesta tradicional donde el productor va a recibir una contestación del servicio consumidor. Para este tipo de casos de uso es más frecuente realice una llamada directa, pasando por un proxy reverse si es necesaria la flexibilidad.
		- (Page 21)
	- -
	- -
	- ¿Qué son los motores de búsqueda? #flashcard
		- Los  motores  de  búsqueda  son  bases  de  datos  especializadas  en  la  búsqueda  de información, frecuentemente de texto, aunque soportan búsquedas por campos en muchos casos.
		- (Page 22)
	- -