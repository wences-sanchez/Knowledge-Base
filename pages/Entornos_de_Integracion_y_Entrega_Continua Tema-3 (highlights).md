title:: Entornos_de_Integracion_y_Entrega_Continua Tema-3 (highlights)
deck:: [[UNI::Entornos_de_Integracion_y_Entrega_Continua Tema-3]]
author:: [[UNIR]]
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-3"
category:: #books

tags:: Entornos-CI-CD UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/27d33c78-ee6e-48d0-83ab-975dbcb53921.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Sistema de control de versiones centralizados Estos  sistemas  almacenan  el  histórico  de  cambios  en  un  servidor  en  el  que  se conectan los desarrolladores. Solo hay una base de datos, pero los ficheros pueden existir en múltiples equipos. Permiten el trabajo en equipo y siguen un modelo tan sencillo que, actualmente, continúan en uso. Un error en el servidor puede implicar la pérdida del proyecto, por lo que es fundamental protegerlo y mantener copias de seguridad de este. El  principal  problema  para  el  trabajo  colaborativo  es  la  necesidad  de  bloquear archivos  en  uso.  Aunque  esto  es  mejor  que  lo  que  ofrece  un  sistema  local,  dista mucho  de  ser  una  situación  ideal  en  la  que  cualquier  desarrollador  pueda  editar cualquier  fichero.  El  bloqueo  de  ficheros  es  una  fuente  de  frustración  para  los desarrolladores, sobre todo cuando existen grandes ficheros con detalles comunes a todo el proyecto. #flashcard
		  id:: 339b3f94-c920-46b5-84be-1eb1483e07b2
		- (Page 5)
	- -
	- -
		- En un sistema distribuido, o descentralizado, no hay un único servidor que almacene la  base  de  datos  con  el  histórico  de  cambios.  Cada  cliente,  el  equipo  de  cada desarrollador, almacena una copia del repositorio junto al histórico de cambios. Cada repositorio puede actualizarse con los cambios de cualquier otro repositorio (del mismo proyecto, claro), por ejemplo: un desarrollador que esté trabajando en una nueva característica puede recuperar un arreglo que haya hecho un compañero suyo e incorporarlo a su trabajo. #flashcard
		  id:: 41678a52-8831-4260-af36-7f7260a7c480
		- (Page 6)
	- -
	- -
		- ¿Qué ocurre si dos desarrolladores clonan el repositorio remoto al mismo tiempo y durante sus cambios se alteran líneas próximas del mismo fichero? Git no es capaz de mezclar cambios si afectan a las mismas líneas, por lo que el desarrollador que suba dichos cambios se encontrará con un mensaje de error. En este caso, se debe resolver el conflicto siguiendo estos pasos:   Descargará  los  últimos  cambios  desde  el  repositorio  central  con  git  pull  rebase  origin  master. La opción  --rebase  le  indica a Git que, tras actualizar master, los nuevos commits se añadirán a la punta (HEAD) de la rama master.   Git mostrará un mensaje de error indicando que ha detectado conflictos y no ha podido completar la operación.   El desarrollador resuelve los conflictos. Este paso es delicado, ya que requiere de un análisis de los cambios que pretendía hacer y de los introducidos por el otro desarrollador. Es decir, no sirve con borrar los cambios anteriores y reemplazarlos   Una vez resueltos, añade los ficheros con git add <fichero> (igual que si fuera a   Con todos los ficheros modificados en el área de staging, termina la operación con los nuevos. hacer un commit normal). inicial con git rebase --continue. #flashcard
		  id:: e107ae0c-4fe3-42bf-971a-cbafd0157b0e
		- (Page 8)
	- -
	- -
		- AÑADIR IMAGEN #flashcard
		  id:: d41a92ba-7ff0-4646-b8ef-f19153245754
			-   release-*: estas ramas parten de  develop  y se fusionan con  master y  develop. Cuando este último está casi listo para una nueva versión, se crea una nueva rama con  el  identificador  de  dicha  versión,  por  ejemplo,  release-1.4.0.  No  debe contener los cambios de las ramas de características planificadas para versiones futuras. Puede recibir arreglos de las características de la nueva versión, que se añadirán también a develop mientras se prepara la liberación de la versión. Una vez release-1.4.0 es aprobada, se fusiona tanto en master como en develop. Se pueden borrar una vez fusionadas.
		- (Page 11)
	- -
	- -
		- El mecanismo para añadir los cambios al repositorio principal sin acceso de escritura es mediante una pull request. Esta funcionalidad, propia de la plataforma (es algo que ofrecen  GitHub  o  Bitbucket,  no  es  una  función  nativa  de  Git),  consiste  en  una solicitud, iniciada desde el repositorio del desarrollador hacia el repositorio principal, para fusionar los cambios de una rama del desarrollador en la rama master principal. Los  administradores  del  repositorio  principal  evalúan  la  solicitud  y,  si  están satisfechos con ella, la fusionan. La rama del desarrollador no ha llegado a existir en el repositorio principal, pero los commits de esta pasan a formar parte de master. #flashcard
		  id:: 34b0a42e-bfea-4922-977e-233f1b74e417
		- (Page 14)
	- -
	- -
		- AÑADIR IMAGEN #flashcard
		  id:: 5c113798-ff59-40f1-93bc-a9a481107b71
			- La  estrategia  de  state  branching,  también  denominada  GitLab  flow,  consiste  en nombrar  las  ramas  según  el  entorno  en  el  que  se  despliegan.  Así,  el  repositorio tendría  ramas  llamadas  local,  develop,  staging  y  production  (que  podría  ser master). Cada rama se va fusionando con la siguiente cuando el código está listo para ser promocionado al siguiente entorno. La figura 3 muestra un ejemplo de este flujo. Cada nueva característica o arreglo se fusiona primero en  develop y va avanzando hasta que llega a master, que es desde donde se despliega el entorno de producción.
		- (Page 16)
	- -