title:: Administración de Sistemas para la Cloud Tema-10 (highlights)
author:: [[UNIR]]
full-title:: "Administración de Sistemas para la Cloud Tema-10"
category:: #books

tags:: #[[Administración-de-Sistemas-para-la-Cloud]] #[[UNI]]

- #tags #[[Administración-de-Sistemas-para-la-Cloud]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/020c6328-86e7-48f6-ba02-69d3ef02a9d0.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- ¿Cuáles son los dos enfoques habituales para actualizar un entorno de producción? #car
	  id:: 634014ed-7101-4a69-99ae-c7e9586f3a38
		- En  un  entorno  virtualizado,  ya  sea  de  nube  pública  o  privada,  hay  dos  enfoques habituales para estas actualizaciones (Lucifredi y Ryan, 2018):   Despliegue basado en instancias: cada instancia se actualiza individualmente en el momento del despliegue de la aplicación.   Despliegue basado en imágenes: se crea una nueva imagen cada vez que se lanza una  versión  de  producción,  a  partir  de  la  cual  se  crean  nuevas  instancias  y  se destruyen las antiguas.
		- (Page 5)
	- -
	- -
	- En  este  modelo  de  despliegue,  todos  los  roles  de  servidor  se  basan  en  una  única imagen maestra (o unas pocas, en caso de necesitar diferentes sistemas operativos o  distribuciones  para  diferentes  roles).  La  configuración  del  rol  ocurre  durante  el arranque  de  la  instancia  mediante  la  ejecución  de  un  script  a  partir  de  algún mecanismo concreto: user data en AWS, extensiones de máquina virtual de Azure o herramientas con Ansible o Puppet. Una posible actualización de una aplicación de la versión 1.0 a la versión 1.1 con este modelo seguiría estos pasos:   Una  vez  completados  los  pasos  generales,  los  binarios  o  los  paquetes  de actualización, se etiquetan con el número de versión 1.1.   Se modifican los scripts de despliegue para hacer referencia a los paquetes de la versión 1.1.   Todas las instancias desplegadas a partir de este momento ejecutarían los scripts para instalar la versión 1.1, pero las instancias ya desplegadas siguen en la versión 1.0. En un grupo de autoescalado, en el que pueden aparecer instancias nuevas en cualquier  momento,  se  podría  llegar  a  una  situación  con  instancias  en  ambas versiones simultáneamente.   Idealmente,  las  instancias  en  la  versión  1.0  se  destruyen  y  son  sustituidas  por instancias  nuevas,  que  tendrán la  versión  1.1.  Esta  sustitución  ocurre paulatinamente en un  rolling update. Para que una sustitución paulatina pueda ocurrir,  ambas  versiones  deben  poder  convivir, incluso  aunque  sea momentáneamente.  De  lo  contrario,  pueden  aparecer  problemas  con  los esquemas de las bases de datos u otras configuraciones. Si no pueden convivir, es probable  que  sea  necesaria  una  actualización  en  bloque  en  la  que  habrá  un intervalo sin servicio. #ñspace
		- (Page 6)
	- -
	- -
	- Explica el modelo de despliegue basado en instancias #car
	  id:: 634014ed-412e-4205-b017-666bfdf53005
		- v
		- (Page 6)
	- -
	- -
	- CONTINUE #car
		- En ambos casos, es habitual que las instancias estén detrás de un balanceador de carga que solo dirige tráfico a las instancias que pasan una llamada de prueba o healthcheck (que puede ser, por ejemplo, una petición REST a una ruta diseñada expresamente para validar que la instancia funciona bien). No todas las instancias tienen por qué alojar un servidor web: un servicio que se alimente de una cola de mensajes  puede  evitar  la  llamada  de  healthcheck,  ya  que  el  propio  servicio  no recogerá mensajes hasta que no esté listo para hacerlo. Se podría pensar que se podrían aplicar los scripts de la versión 1.1 en las instancias con  la  versión 1.0 para evitar un  despliegue  completo.  Este enfoque  es  realmente más  parecido  al  tradicional,  en  el  que  se  aplican  parches  sobre  un  servidor indefinidamente.
		- (Page 7)
	- -
	- -
	- Explica el despliegue basado en imágenes #car
		- La  creación  de  nuevas  imágenes  proporciona  una  forma  más  limpia  de  ejecutar actualizaciones. Estas imágenes, o plantillas, consisten en una máquina virtual con una configuración y unas aplicaciones concretas, que se apaga y se «congela», en el sentido de que no puede ser arrancada. Esta imagen mantiene la configuración del hardware virtual y los discos de la máquina sin modificaciones desde el apagado. Las instancias  se  despliegan  «clonando»  esta  imagen,  es  decir,  creando  una  nueva máquina virtual con el mismo hardware virtual y con un disco que es una copia del disco de la imagen. Los pasos para una actualización de 1.0 a 1.1 son los siguientes:   Al igual que con el enfoque anterior, una vez completados los pasos generales, se generan los paquetes de instalación con el número de versión 1.1.   Se  arranca  una  instancia  con  una  instalación  básica  del  sistema  operativo,  que podría hacerse con los últimos parches de seguridad. Este sistema operativo suele
		- (Page 7)
	- -
	- -
	- CONTINUE #car
	  id:: 634014ed-78e2-4dbc-9851-351d3cb02d2b
		- ser  el  mismo  que  el  de  la  imagen  de  la  versión  1.0,  pero  no  es  estrictamente necesario.   Se instala la aplicación, versión 1.1, desde cero. Los  scripts de instalación serán parecidos a los del modelo basado en instancias, pero no tienen que tratar con actualizaciones de la aplicación, solo con la instalación inicial, por lo que pueden ser más sencillos.   Una  vez  completada  la  instalación,  se  «generaliza»  la  imagen  y  se  apaga  la máquina virtual (en algunos entornos este proceso es automático).   Dependiendo del entorno  de  nube,  la imagen  se  genera  a partir de  la  máquina virtual, dejando la máquina intacta, o la propia máquina virtual se convierte en una  plantilla.  En  ambos  casos,  la  imagen  es  inmutable  y  no  se  puede  arrancar, salvo mediante un clonado.   Las instancias en ejecución, basadas en la imagen de la versión 1.0, se sustituyen por  instancias nuevas  con  la  versión 1.1.  Al  igual  que en  el modelo anterior,  se puede  seguir  un  proceso  de  rolling  update  o  una  actualización  en  bloque  con parada  del  servicio.  La  problemática  de  convivencia  de  varias  versiones  existe también en este modelo de despliegue. La actualización basada en imágenes es más estable, porque no hay actualizaciones incrementales, sino instalaciones de cero. Como contrapartida, generar una imagen nueva, aun cuando el proceso esté automatizado, lleva más tiempo que cambiar un script  de  despliegue.  En  cualquier  caso,  el  despliegue  basado  en  imágenes  puede seguir  haciendo  uso  de  scripts  de  arranque  (es  decir,  user  data,  extensiones,  etc.) para finalizar la configuración de la aplicación, en caso de que sea necesario.
		- (Page 8)
	- -
	- -
	- Sysprep (Krause, 2019) es una herramienta que prepara el sistema para el clonado, aplicando un proceso llamado generalización. Su nombre oficial es Herramienta de preparación  del  sistema  de  Microsoft.  En  resumen,  permite  crear  una  imagen maestra de un servidor que puede reutilizarse tantas veces como sea necesario para desplegar servidores adicionales. #ñspace
		- (Page 10)
	- -
	- -
	- ¿Qué s Sysprp? #car
		- e
		- (Page 10)
	- -
	- -
	- ¿Cuáles son las fases para preparar una imagen maestra con Sysprep? #car
		- Las fases para preparar una imagen maestra con Sysprep son las siguientes:   Instalación del sistema operativo en un nuevo servidor.   Configuración y actualización.   Ejecución de Sysprep y apagado del servidor.   Creación de imagen maestra del disco duro.   Clonado del disco para desplegar nuevos servidores.
		- (Page 11)
	- -
	- -
	- ¿Qué hace el comando generalize de Sysprep? #car
	  id:: 634014ed-6334-4557-8839-b5f486951ef8
		- /generalize: Sysprep eliminará toda la información única del sistema (SID) de la instalación de Windows, haciendo que la imagen final sea utilizable en múltiples máquinas, ya que cada nuevo servidor creado a partir de la imagen obtendrá un SID nuevo único.
		- (Page 12)
	- -