title:: Entornos_de_Integracion_y_Entrega_Continua Tema-7 (highlights)
author:: [[UNIR]]
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-7"
category:: #books

tags:: #[[Entornos-CI-CD]] #[[UNI]]

- #tags #[[Entornos-CI-CD]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/5360dc73-d287-4d6f-8309-e6ddfbb2ce3e.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- ¿Qué es Jenkins? #car
		- Jenkins es un sistema de integración y entrega continuas. Es una herramienta de código abierto disponible para múltiples arquitecturas que puede manejar cualquier tipo  de  construcción,  pruebas  y  despliegues  gracias  a  su  formato  de  plugins.
		- (Page 4)
	- -
	- -
	- Jenkins  se  basa  en  una  arquitectura  de  ejecución  distribuida,  con  un  servidor principal y varios agentes. El  servidor  principal,  o  master,  es  el  controlador  del  sistema  y  aloja  toda  la configuración,  definición  de  trabajos,  historial  de  ejecuciones,  etc.  Puede  ejecutar trabajos,  pero  en  entornos  profesionales  se  recomienda  que  el  master  se  limite  a distribuir las tareas entre los agentes. Los  agentes  (también  denominados  esclavos  en  versiones  anteriores)  son  nodos dependientes del master. Están encargados de ejecutar cualquier tarea que este les delegue.  El  software  de  Jenkins  que  se  ejecuta  en  estos  es  bastante  sencillo  en comparación al master ya que no necesita interfaz gráfica ni historial. Los agentes pueden ser nodos estáticos, es decir, servidores desplegados y conectados al master de forma ajena a Jenkins (manual o automáticamente), o dinámicos, de forma que Jenkins los despliega bajo demanda en una nube pública o privada. #ñspace
		- (Page 5)
	- -
	- -
	- Cada agente tiene uno o varios ejecutores. Estos son procesos iniciados por el agente para  un  trabajo  de  Jenkins  concreto.  Así,  es  posible  ejecutar  varios  trabajos  en paralelo en cada agente. #ñspace
		- (Page 6)
	- -
	- -
	- de: Estructura de un trabajo El elemento central de Jenkins es el trabajo, que está compuesto, a grandes rasgos,   Uno o varios triggers (o disparadores) que inician la ejecución.   Una lista de agentes en los que se permite ejecutar el trabajo.   Parámetros de entrada, sin aplica.   Tareas que se ejecutarán (que pueden arrancar otros trabajos).   Tareas de finalización (post-processing).   Artefactos archivados. Los triggers arrancan la ejecución de un trabajo. Pueden ser periódicos (al estilo de las tareas de cron), manuales (es decir, iniciados por un usuario), desde otro trabajo o a partir de un webhook. Los  triggers  periódicos  pueden  estar  condicionados  a  que  existan  cambios  en  un repositorio. Por ejemplo, Jenkins puede comprobar periódicamente un repositorio e iniciar el trabajo solo si han aparecido commits nuevos en una rama concreta. Este modelo síncrono añade demasiada carga tanto a Jenkins como al sistema de control de cambios, por lo que se pueden aprovechar los webhooks para arrancar los trabajos asíncronamente. Por ejemplo, GitHub puede lanzar un webhook cuando se abre una pull request o cuando aparecen commits nuevos en una rama. Jenkins puede arrancar el trabajo al recibir el webhook, evitando así las comprobaciones periódicas. #ñspace
		- (Page 7)
	- -
	- -
	- Los Jenkinsfiles admiten dos tipos de sintaxis: declarativa y en script. La sintaxis en script es imperativa, es decir, el usuario debe definir el control de flujo y de errores y depende de expresiones propias de Groovy. La sintaxis declarativa, introducida en Jenkins 2, define secciones propias de Jenkins (es decir, no usa expresiones generales de Groovy) y delega el control de flujo y de errores en el propio motor de Jenkins. La sintaxis en script es más versátil, pero suele requerir más código. #ñspace
		- (Page 13)
	- -
	- -
	- INCLUIR IMAGEN #car
	  id:: 63401512-f998-43a5-a546-5a11421fd171
		- Estructura de un Jenkinsfile El  código  de  un  Jenkinsfile  con  sintaxis  declarativa  está  formado  por  un  bloque pipeline inicial, directivas iniciales de configuración, un bloque stage para para fase y  unas  directivas  post  al  terminar.  El  siguiente  ejemplo  contiene  algunas  de  estas opciones.
		- (Page 14)
	- -
	- -
	- Figura 21. Código de pipeline. #ñspace
		- (Page 28)
	- -