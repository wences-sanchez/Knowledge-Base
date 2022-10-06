title:: Cloud Computing and DevOps Culture Tema-9 (highlights)
author:: [[UNIR]]
full-title:: "Cloud Computing and DevOps Culture Tema-9"
category:: #books

tags:: #[[Cloud-Computing-and-DevOps-Culture]] #[[UNI]]

- #tags #[[Cloud-Computing-and-DevOps-Culture]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/2cda4bdf-bed7-4bda-93f7-413c6cc41494.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- Los DevOps tienen, como parte de sus cometidos, no solo el desarrollar y desplegar los entornos de producción, sino el asegurar su correcto funcionamiento. Para hablar del  correcto  funcionamiento  de  un  sistema,  la  monitorización  es  una  pieza fundamental y necesaria. #ñspace
		- (Page 4)
	- -
	- -
	- ¿Qué tres tipos de herramientas de observabilidad existen? #card
		- Comenzaremos  por  mencionar  a la  agregación  de  métricas.  Este  tipo  de herramientas  son,  habitualmente,  las  que  primero  deberíamos  incluir,  ya  que  son fáciles  de  integrar  en,  prácticamente,  cualquier  aplicación  escrita  en  un  lenguaje moderno.  La  siguiente  prioridad  podría  ser,  por  ejemplo,  monitorizar  la  sesión porque,  aunque  probablemente  requiera  pequeñas  modificaciones  en las aplicaciones, proporciona un tremendo valor. El tercer nivel son las alertas y sistemas de  visualización  que,  para  su  correcta  implementación,  se  requerirá  que  las  dos primeras  herramientas  (métricas  y  monitorización  de la  sesión)  estén  bien implementadas.
		- (Page 6)
	- -
	- -
	- Acerca de las herramientas de tipo de observabilidad de agregación de métricas. #card
		-   Agregación de métricas. Este tipo de herramienta consiste un conjunto de series de datos temporales. Estas series son datos ordenados en el tiempo y tomados normalmente  con  un  intervalo  interno  consistente.  Su  consistencia  es  la  que permite  aplicar  cálculos  avanzados  a  las  series  y  proporcionar  un  análisis predictivo utilizando simples regresiones o también algoritmos más avanzados.
		- (Page 6)
	- -
	- -
	- Acerca del tipo de herramientas de observabilidad de agregación de registros. #card
		-   Agregación de registros. Estas herramientas interactúan con tipos de datos que están más relacionados con eventos que con una serie de datos consistentes. Esta salida, a menudo, se emite cuando un sistema entra en un estado no deseado. Pensemos en ellos como una forma de componer información relevante.
		- (Page 6)
	- -
	- -
	- Acerca del tipo de herramientas de observabilidad de alertas/visualizaciones. #card
		-   Alertas/visualizaciones. Puede parecer que esto no encaja con los otros tipos de herramientas, ya que es realmente posterior y más avanzado que las demás, pero proporciona una forma eficiente de consumo para los otros tipos e incluso puede producir su propia salida. Este tipo de herramienta hace que el sistema sea más comprensible  y  también  ayuda  a  crear  sistemas  más  interactivos  a  través  de proactividad y reacción ante estados negativos del sistema.
		- (Page 7)
	- -
	- -
	- Acerca del tipo de herramientas de observabilidad de rastreo distribuido. #card
		-   Rastreo  distribuido.  Al  igual  que  el  rastreo  dentro  de  una  sola  aplicación,  el rastreo  distribuido  nos  permite  seguir  una  sola  transacción,  a  través  de  una transacción que ocurre sobre el sistema completo.  Esto permite concentrarnos en  transacciones  específicas  solo  cuando  estas  podrían  estar  experimentando problemas.  Por  supuesto,  es  imposible  trazar  todo  y,  por  lo  tanto,  (debido  al rendimiento) lo más habitual y aconsejable es aplicar un algoritmo de muestreo.
		- (Page 7)
	- -
	- -
	- Sobre pull-push en herramientas de agregación de métricas #card
		- No se puede escribir ningún texto sobre las herramientas de agregación de métricas sin abordar el debate push vs. pull. ¿Qué es? El debate se centra en si es mejor tener un sistema de agregación para que se envíen datos o tener un sistema de agregación de métricas que reúna datos preguntando a un API.
		- (Page 11)
	- -
	- -
	- Sobre Prometheus #card
		- Esta es la herramienta de monitorización de series temporales más reconocida (y popular) y la solución ideal para aplicaciones nativas de la nube. Está alojada dentro del Cloud Native Computing Foundation (en siglas, CNCF), pero fue creado por Matt Proud  y  Julius  Volz,  y  patrocinado  por  SoundCloud.  Existe  mucha  documentación sobre Prometheus que te ayudará a entender cómo funciona, por ejemplo, visitando su página web. Prometheus es un sistema basado en extracción (pull) que utiliza una configuración local para definir cómo recolectar los datos. Esta información se recopila y guarda en un motor de almacenamiento altamente eficiente, dentro del disco local.
		- (Page 11)
	- -
	- -
	- Acerca de Graphite #card
		- Graphite  existe  desde  hace  mucho  tiempo  y  se  ha  vuelto  omnipresente  en  la industria. Es un sistema de inserción de logs que recibe datos desde las aplicaciones. El funcionamiento es relativamente simple, cada aplicación inyecta (push) los datos hacia el componente de Graphite. Carbon, por su parte, almacena estos datos en la base  de  datos  Whisper,  y  esa  base  de  datos  junto  con  Carbon  se  leen  desde  el componente  web  Graphite,  que  actúa  como  interfaz  de  usuario  para  representar gráficamente  sus  datos en  un navegador.
		- (Page 13)
	- -
	- -
	- ¿Qué es OpenTSDB? #card
		- OpenTSDB  es una  base de  datos de  series de tiempo  de  código  abierto,  como  su nombre  lo  indica  (Open  Time  Series  Data  Base  u  OpenTSDB).  Esta  herramienta almacena sus métricas en Hadoop y esto significa que es inherentemente escalable. Si  en  tu  entorno  de  trabajo  tienes  un  clúster  Hadoop,  esta  podría  ser  una  buena opción para almacenar métricas a largo plazo. En el caso contrario, si no cuentas con un  clúster  Hadoop,  la  sobrecarga  operativa  podría  ser  demasiado  grande
		- (Page 14)
	- -
	- -
	- ¿Para qué sirve una herramienta de observabilidad de tipo de sistema de agregación de registros? #card
		- Un sistema de agregación de registros sirve, principalmente, para coleccionar datos de  eventos,  es  decir,  actividades  irregulares  que  son  significativas.  Un  ejemplo podrían  ser  los  registros  de  acceso  para  un  servidor  web,  que  resultan  relevantes porque queremos saber qué o quién está accediendo a nuestros sistemas y cuándo. Otro  ejemplo  sería  un  error  de  aplicación,  porque  no  es  una  condición  de funcionamiento normal.
		- (Page 16)
	- -
	- -
	- Acerca de Fluentd #card
		- Fluentd  fue  desarrollado  por  Treasure  Data.  Está  escrito  en  C  y  es  una  de  las herramientas  de  referencia  recomendadas  por  AWS  y  Google  Cloud.  Para  muchas empresas, se ha convertido en un posible reemplazo para Logstash. Actúa como un agregador local que recopila todos los registros de nodos y los envía a los sistemas de almacenamiento centralizados. Utiliza un robusto sistema de complementos para proporcionar variadas integraciones que lo hacen compatible con numerosas fuentes de  datos  y  formatos  de  salidas.  Hay  más  de  500  complementos  diferentes disponibles, así que los casos de uso más comunes están totalmente resueltos. Y, de hecho, en el caso excepcional de que no exista, el usuario puede optar por contribuir y construir uno. Fluentd es una opción muy común en el entorno de Kubernetes, debido a sus bajos requisitos  de  memoria  (solo  decenas  de  megabytes)  y  su  alto  rendimiento.
		- (Page 21)
	- -