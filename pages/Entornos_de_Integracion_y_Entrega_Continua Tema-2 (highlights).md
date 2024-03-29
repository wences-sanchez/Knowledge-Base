title:: Entornos_de_Integracion_y_Entrega_Continua Tema-2 (highlights)
deck:: [[UNI::Entornos_de_Integracion_y_Entrega_Continua Tema-2]]
author:: [[UNIR]]
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-2"
category:: #books

tags:: Entornos-CI-CD UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/a1db0259-1f1c-43a7-8ee2-ddcb17940e9c.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Define **Repositorio** #flashcard
		  id:: 44fb99b6-4044-4699-936c-44e3eb37d10b
			-   Repositorio: es el almacenamiento maestro de todos los archivos y su historial de cambios.  Se  almacena  en  el  servidor  de  control  de  versiones.  Cada  proyecto autónomo  debe  tener  su  propio  repositorio,  aunque  un  único  proyecto  puede estar repartido en más de un repositorio.
		- (Page 6)
	- -
	- -
		- Define **Sandbox** #flashcard
		  id:: 967660ee-88e3-4d91-9497-560cf1ceadd5
			-   Sandbox: también se conoce como copia de trabajo. Contiene una copia de todos los  archivos  del  repositorio  de  un  punto  en  particular.  Cada  desarrollador mantiene su propia copia de trabajo a partir del contenido del repositorio.
		- (Page 6)
	- -
	- -
		- Define **Check-out** #flashcard
		  id:: 045afc70-faa2-4e0a-ac93-31e62d52fc64
			-   Check-out: es el proceso de inicializar una copia de trabajo a partir de un punto concreto  de  un  repositorio.  En  algunos  sistemas  de  control  de  versiones  este proceso se define con el término update and lock o actualizar y bloquear.
		- (Page 6)
	- -
	- -
		- Define **Update** #flashcard
		  id:: 5fda5a27-444b-4607-a281-f4f776c0fd86
			-   Update: actualización de la sandbox para obtener los últimos cambios desde el repositorio. También se puede actualizar a un punto en particular en el pasado.
		- (Page 6)
	- -
	- -
		- Define **Lock** #flashcard
		  id:: e858e3ce-4b3b-4b33-b3bc-67f0d3a2b1bc
			-   Lock:  un  bloqueo  hace  posible  que  nadie  pueda  editar  un  archivo  sin  el desarrollador que lo ha bloqueado.
		- (Page 6)
	- -
	- -
		- Define **commit** #flashcard
		  id:: d3abba13-e77f-4e13-91ca-c263069520e6
			-   Check-in o commit: registro de los cambios efectuados en la copia de trabajo. Es el  proceso  fundamental  para  guardar  los  cambios  en  el  repositorio.  Estos  son efímeros  desde  el  punto  de  vista  del  repositorio;  es  decir,  aunque  los  archivos estén guardados en el disco duro, los cambios entre el último commit y el estado actual no están registrados en el repositorio y, por tanto, no existen en el histórico del control de versiones a menos que se registren en un commit.
		- (Page 6)
	- -
	- -
		- Define **Revert** #flashcard
		  id:: bb2b6187-6e9d-47bd-b7ed-bbbb022f8f79
			-   Revert:  destruye  la  sandbox  para  descartar  los  cambios  y  volver  al  punto  de  la última actualización. Esto es útil cuando el código de la copia de trabajo actual se ha vuelvo inestable y no es posible hacerlo funcionar de nuevo. A veces revertir es más rápido que depurar, especialmente, si hay commits recientes.
		- (Page 7)
	- -
	- -
		- Define **Head** #flashcard
		  id:: 5a251e2e-e17c-4223-bacb-9b1831ef087f
			-   Tip o Head: la cabecera del repositorio contiene los cambios más recientes que se han registrado. Al actualizar la copia de trabajo los archivos quedan en el estado de la cabecera. El sistema de control de versiones soporta ramas, cada rama tiene su  propia  cabecera,  por  lo  que  la  copia  de  trabajo  se  puede  actualizar  en  la cabecera de cada una de las ramas.
		- (Page 7)
	- -
	- -
		-   Tag  o  label:  una  etiqueta  marca  un  commit  determinado  en  el  historial  del repositorio, lo que permite acceder fácilmente a él de nuevo. Pueden usarse para indicar una versión liberada (release) o un punto de pase a producción. Aunque es posible borrarlas, no deberían ser modificadas. #flashcard
		  id:: 61d17096-a7f4-4d6a-b145-e478e2d802d3
		- (Page 7)
	- -
	- -
		- Define **Rollback** #flashcard
		  id:: 481fd352-1825-4cdb-bd87-a3901937bb5a
			-   Rollback:  es  el  proceso  en  el  que  se  deshace  un  commit  para  que  los  cambios introducidos  desaparezcan  de  la  cabecera  del  repositorio.  El  mecanismo  para hacerlo varía dependiendo del sistema de control de versiones: en unos casos se genera un segundo commit B que anula los cambios del anterior commit A, por lo que los archivos vuelven al estado anterior (commit A). En otros casos, se puede eliminar el commit A completamente.
		- (Page 7)
	- -
	- -
		-   Rama: las  ramas  permiten  dividir  el  repositorio  en  distintos  historiales alternativos. Suelen partir de un commit común, pero a partir de ese momento los cambios registrados en cada rama pueden divergir tanto como sea necesario. Es habitual, por ejemplo, separar en ramas el trabajo, en diferentes características nuevas, en arreglos o en entornos de trabajo. Las ramas apuntan a un commit, al igual  que  las  etiquetas,  pero  se  actualizan  cada  vez  que  hay  uno  nuevo  (las etiquetas no se modifican una vez asignadas a un commit). #flashcard
		  id:: 0b3c6c44-8881-4889-b417-831fa9456e7d
		- (Page 7)
	- -
	- -
		-   Fusión  o  merge:  es  el  proceso  de  combinar  cambios  de  dos  ramas.  Si  dos programadores le hacen un cambio a uno o varios archivos (cada uno en una rama por separado) y ambos hacen un check-in de los cambios, el segundo programador tendrá  que  fusionar  los  cambios  de  la  primera  persona.  Las  herramientas  más modernas  ayudan  en  este  proceso  e  incluso  lo  hacen  automáticamente  si  los cambios no afectan a las mismas líneas de código. #flashcard
		  id:: 1373dca3-86f8-42d6-b3c7-eac55ae83413
		- (Page 8)
	- -
	- -
		-   Resolución de conflictos: una fusión se puede llevar a cabo automáticamente si los cambios de dos commits afectan a archivos diferentes o a diferentes partes de uno.  Sin embargo,  si  los  cambios  afectan  a  la  misma  sección  de  un  archivo,  las herramientas no son capaces de resolverlo y el desarrollador debe encargarse de identificar  el  estado  original  del  fichero,  los  cambios  introducidos  por  el  otro desarrollador y sus propios cambios, y decidir cómo resolverlo. Los sistemas de control de versiones suelen resaltar los conflictos y muestran, en un mismo editor, los  cambios  de  ambos  commits  con  el  objetivo  de  facilitarle  la  vida  al desarrollador. #flashcard
		  id:: 2bd2edff-0928-4c0e-9d4c-4924b550f8ac
		- (Page 8)
	- -
	- -
		- Uno de los usos más potentes de un sistema de control de versiones es la capacidad de retroceder en el tiempo. Un desarrollador puede actualizar su copia de trabajo con todos los archivos a un punto en particular en el pasado. Por ejemplo, si se ha detectado un error en una versión ya publicada de la aplicación, pero no se encuentra la causa, el desarrollador puede aplicar diff debugging:   Actualiza la copia de trabajo a un punto en el que el error no existía.   A continuación, actualiza la copia de trabajo con los siguientes cambios por orden histórico hasta que logra aislar el commit exacto que introdujo el error.   En ese punto, el desarrollador solo tiene que revisar los cambios de ese commit para  localizar  el  error.  Si  se  trabaja  con  integración  continua  y  el  número  de cambios es pequeño, el error será fácil de corregir. #flashcard
		  id:: a33835ef-66d8-4789-b493-0d91c8925e7b
		- (Page 10)
	- -
	- -
		- Siempre que sea posible, es recomendable mantener en el control de versiones todas las herramientas, librerías, documentación y cualquier elemento con el proyecto. Las herramientas y librerías son particularmente importantes ya que, si se dejan fuera, en algún momento se actualizará una de ellas y ya no se podrá volver a un punto anterior a la actualización, salvo manualmente (con la posibilidad de fallo humano que esto implica). #flashcard
		  id:: 9cfb39b2-d7ed-441f-91a1-7c6343a449ef
		- (Page 11)
	- -
	- -
		- Lo  único  relacionado  con  el  proyecto  que  no  debería  guardarse  en  el  control  de versiones  es  el  código  generado,  es  decir,  binarios  compilados  o  ficheros autogenerados #flashcard
		  id:: ec169ecb-9ce2-4cb4-8f9e-3cbe772f488b
		- (Page 12)
	- -
	- -
		- La  información  de  usuario  también  debe  ir  al  repositorio.  Esto  incluye  la documentación, notas sobre requisitos, escritura técnica (como manuales y guías) y pruebas  de  usuario.  Hay  una  excepción  adicional  en  cuanto  a  lo  que  no  debe almacenar  en  control  de  versiones:  un  código  que  se  va  a  desechar.  Estos  son  los experimentos,  test,  proyectos  de  investigación  que  permanecen  sin  integrarse, etcétera.  Algunos  desarrolladores  mantienen  repositorios  propios  para  almacenar este tipo de información. #flashcard
		  id:: 8d30f814-0589-4d45-bf82-542bee2561d5
		- (Page 12)
	- -
	- -
		- sistemas como Git permiten usar herramientas externas para extraer contenido de texto de un fichero binario y guardar los cambios sobre este texto. El control  de  versiones  almacenará  los  cambios  sobre  el  fichero  binario,  pero  las herramientas de comparación de cambios podrán trabajar con ficheros de texto. Por ejemplo,  se  puede  versionar  un  fichero  PDF  y  usar  la  herramienta  pdfinfo  para comparar detalles del contenido entre dos versiones. #flashcard
		  id:: 767e2a9c-b486-4329-9bbb-2de777617365
		- (Page 13)
	- -
	- -
		- INCLUIR IMAGEN #flashcard
		  id:: a0271fb4-e06e-42fa-b628-22821d0588fc
			- A grandes rasgos, el código atraviesa cuatro niveles de completitud que veremos en la Figura 1:
		- (Page 14)
	- -
	- -
		- Otra opción es incluir la aplicación del repositorio externo como una dependencia.  En  este  caso,  tan  solo  hay  que  modificar  la  referencia  a  la  librería cuando  se  libere una nueva  versión,  los  cambios  de la  versión  sean  interesantes y hayan sido validados con el código local. Muchos sistemas de control de versiones soportan la integración entre repositorios. Al  actualizar  una  copia  de  trabajo,  el  sistema  recuperará  automáticamente  los cambios más recientes del repositorio principal y de sus dependientes. Por ejemplo, Git  soporta  la  funcionalidad  de  submódulos:  un  repositorio  externo  configurado como submódulo que aparece como un directorio dentro del repositorio local. #flashcard
		  id:: 47025504-b60a-4595-bbd5-6ef0bcab7dec
		- (Page 20)
	- -
	- -
		-   Si no está en control de versiones, no existe. •  El código que reside en la máquina de un desarrollador no le vale a nadie más •  Se recomienda habitualmente subir el código al control de versiones al final del día (siempre que no rompa la construcción, o en cualquier caso si se trata de y se puede perder. ramas privadas). #flashcard
		  id:: 08350c63-e91e-44dc-a622-1c19959565d3
		- (Page 21)
	- -
	- -
		- Las ramas de desarrollo son, por norma general, consideradas efímeras. Los cambios ya  se  han  incorporado  en  la  rama  principal  y,  eventualmente,  serán  parte  de  una versión liberada. Por tanto, las ramas de desarrollo se pueden borrar sin que por ello desaparezcan los commits. Se puede pensar en las ramas como punteros a commits concretos, pero el hecho de borrar el puntero no borra el commit. #flashcard
		  id:: 0a030800-0c72-4ae0-ad10-826a9547f8cc
		- (Page 33)
	- -