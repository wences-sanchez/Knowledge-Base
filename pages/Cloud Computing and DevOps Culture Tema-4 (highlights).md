title:: Cloud Computing and DevOps Culture Tema-4 (highlights)
deck:: [[UNI::Cloud Computing and DevOps Culture Tema-4]]
author:: [[UNIR]]
full-title:: "Cloud Computing and DevOps Culture Tema-4"
category:: #books

tags:: Cloud-Computing-and-DevOps-Culture UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/7920e700-e162-459f-8d31-fec96d5fb474.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Existen tres tipos principales de virtualización de servidores que son: virtualización del sistema operativo (tecnología que se conoce bajo el nombre de Contenedores), imitación  o  emulación  del  hardware  y  paravirtualización. #flashcard
		  id:: 2c27b1c3-fbfb-44c0-b5cf-a820d83e1b7a
		- (Page 4)
	- -
	- -
		- Imitación o emulación del hardware En  este  caso,  el  software  de  virtualización  (denominado  hipervisor)  crea  una máquina virtual que imita todo el entorno de hardware.El sistema operativo,que está cargadoen una máquina virtual,es un producto estándar no modificado. Cuando realiza  llamadas  para  recursos del  sistema,  el  software  de  emulación de  hardware captura la llamada del sistema y la redirige para que pueda gestionar estructuras de datos  proporcionadas  por  el  hipervisor.  Es  el  propio  hipervisor  el  que  realiza  las llamadas al hardware físico real, subyacente a toda la aglomeración de software. #flashcard
		- (Page 5)
	- -
	- -
		- La emulación o imitación de hardware también es conocida como virtualización de metal desnudo (del inglés bare metal virtualization), para simbolizar el hecho de que ningún  software  se  encuentra  entre  hipervisor  y  el  «metal»del  servidor.  Como hemos  mencionado,  el  hipervisor  intercepta  las  llamadas  del  sistema  desde  la máquina virtual huésped y coordina el acceso al hardware subyacente directamente. I ) R N U i j (  a o R a L  e d   l a n o i c a n r e t n I  d a d i s r e v i n U © #flashcard
		  id:: 930d2b3a-5bd0-42fd-8c8a-5e74b9355e71
		- (Page 5)
	- -
	- -
		- La paravirtualización no intenta emular un entorno de hardware en software, sino que  un  hipervisor  de  paravirtualización  coordina  (o  multiplexa)  el  acceso  a  los recursos  de  hardware  subyacentes  del  servidor. #flashcard
		- (Page 6)
	- -
	- -
		- En la paravirtualización, el hipervisor reside en el hardware y, por lo tanto, esta se puede concebir como una arquitectura de virtualización de metal desnudo.Uno o más sistemas operativos huésped (equivalente a máquinas virtuales en virtualización de emulación del hardware) se ejecutan sobre el hipervisor. Un huésped privilegiado se ejecuta como una máquina virtualhuésped,pero tiene privilegios que le permiten acceder directamente a ciertos recursos en el hardware subyacente #flashcard
		  id:: 1cbd0540-a3fe-49f0-8e01-dfd5b3063b47
		- (Page 6)
	- -
	- -
		- VMware,  Citrix  y  Microsoft  son  los  principales  proveedores  de  virtualización  de servidores  x86  en  entornos  profesionales #flashcard
		- (Page 7)
	- -
	- -
		-   VMware:  es  el  proveedor  de  virtualización  de  servidores  más  extendido  y afianzado  en  el  mercado.  La  plataforma  insignia  de  VMware,  vSphere, utiliza  la tecnología de emulación de hardware.   Citrix:  ofrece  un  producto  de  virtualización  de  servidor,  llamado  XenServer, basado en paravirtualización. El huésped privilegiado (llamado control domain en lenguaje  Xen)  y  el  hipervisor  Xen  trabajan  en  equipo  para  permitir  que  las máquinas virtuales huésped interactúen con el hardware subyacente.   Microsoft: Hyper-V, el producto de virtualización del servidor de Microsoft, tiene una  arquitectura  muy  similar  a  la  de  Xen.  En  lugar  de  usar  el  término  control domain para referirse a las máquinas virtuales huésped, Hyper-V se refiere a ellas como  particiones  y  a  la  contraparte  del  control  domain  de  Xen  se  la  denomina partición principal. #flashcard
		- (Page 7)
	- -
	- -
		- Una  definición  sencilla  de  hipervisor  podría  ser:  la  parte  de  la  nube  privada  que gestiona  las  máquinas  virtuales,  es  decir,  es  la  parte  (programa)  que  permite  que múltiples  sistemas  operativos  compartan  el  mismo  hardware.  Cada  sistema operativo podría usar todo el hardware (procesador, memoria) si no hay otro sistema operativo  encendido.  Ese  es  el  hardware  máximo  disponible  para  un  sistema operativo en la nube. Sin embargo, el hipervisor es lo que controla y asigna qué parte de los recursos de hardware debe obtener cada sistema operativo, para que cada uno  obtenga  lo  que  necesita  y  no  se  interrumpa  entre  sí #flashcard
		  id:: b1e77840-4fcf-4fe0-9ce2-e19d69f8c0a1
		- (Page 7)
	- -
	- -
		- Hipervisor tipo 2. Los hipervisores se ejecutan en un sistema operativo host que proporciona servicios de virtualización, como soporte de dispositivos de E/S y administración de memoria. #flashcard
			- Hay  dos  tipos  de hipervisores:   Hipervisor de tipo 1. Los hipervisores se ejecutan directamente en el hardware del sistema: un hipervisor integrado «básico».
		- (Page 7)
	- -
	- -
		-   Hipervisor tipo 2. Los hipervisores se ejecutan en un sistema operativo host que proporciona  servicios  de  virtualización,  como  soporte  de  dispositivos  de  E/S  y administración de memoria. #flashcard
		  id:: adedb674-ca5d-4dfc-b768-0d9772227893
		- (Page 8)
	- -
	- -
		- Nombra algunos hipervisores de tipo 1 #flashcard
		  id:: d736cb16-502c-46c1-beb0-fd807644fc90
			- VMware ESX y ESXi Estos  hipervisores  ofrecen  funciones  avanzadas  y  escalabilidad,  pero  requieren licencia, por  lo que  los  costos  son  más  altos. VMware  ofrece  algunos  paquetes  de menor costo y pueden hacer que la tecnología de hipervisor sea más asequible para infraestructuras pequeñas. VMware es el líder en los hipervisores tipo 1. Su producto vSphere ESXi está disponible en una edición gratuita y en cinco ediciones comerciales. Microsoft Hyper-V El  hipervisor de Microsoft,  Hyper-V, no ofrece  muchas  de  las funciones  avanzadas que  ofrecen  los  productos  de  VMware.  Sin  embargo,  con  XenServer  y  vSphere, Hyper-V es uno de los tres principales hipervisores tipo 1. Se lanzó por primera vez con  Windows  Server,  pero  ahora,  Hyper-V  se  ha  mejorado  enormemente  con Windows Server 2012 Hyper-V. Hyper-V está disponible tanto en una edición gratuita (sin  GUI  y  sin  derechos  de  virtualización)  como  en  cuatro  ediciones  comerciales:
		- (Page 8)
	- -
	- -
		- CONTINUE #flashcard
		  id:: b6aeecd8-1426-4f75-8a00-57b1ec38c1e0
			- Fundamentos (solo OEM), Essentials, Standard y Datacenter Hyper-V. Actualmente, las nuevas versiones de supervisores de Microsoft están íntimamente relacionadas a sus productos de Cloud Platform y se les conoce como Azure Stack. Citrix XenServer Comenzó como un proyecto de código abierto. La tecnología principal del hipervisor es gratuita, pero al igual que ESXi gratuito de VMware, casi no tiene características avanzadas.  Xen  es  un  hipervisor  de  tipo  desnudo  de  tipo  1  y,  así  como  Red  Hat Enterprise Virtualization usa KVM, Citrix usa Xen en el XenServer comercial. Hoy, los proyectos y la comunidad de código abierto de Xen están en Xen.org. Hoy, XenServer es una solución comercial de hipervisor tipo 1 de Citrix, que se ofrece en cuatro  ediciones.  Confusamente,  Citrix  también  ha  calificado  sus  otras  soluciones propietarias como XenApp y XenDesktop con el nombre Xen. Oracle VM El hipervisor Oracle se basa en el código abierto Xen. Sin embargo, si necesita soporte de hipervisor y actualizaciones de productos, le costará. Oracle VM carece de muchas de  las  características  avanzadas  que  se  encuentran  en  otros  hipervisores  de virtualización de metal desnudo.
		- (Page 9)
	- -
	- -
		- Nombra algunos hipervisores de tipo 2 #flashcard
		  id:: e21c6f16-cb8c-41a5-a6a8-63ce61d4e347
			- VMware Workstation/Fusion/Player VMware Player es un hipervisor de virtualización gratuito. Está destinado a ejecutar solo  una  máquina  virtual  (en  siglas,  VM)  y  no  permite  crear  máquinas  virtuales. VMware  Workstation  es  un  hipervisor  más  robusto  con  algunas  características avanzadas, como grabación y reproducción y compatibilidad con instantáneas de VM.
		- (Page 9)
	- -
	- -
		- CONTINUE #flashcard
			- VMware Workstation tiene tres casos de uso principales:   Para ejecutar múltiples sistemas operativos.   Para ejecutar versiones diferentes de un sistema operativo en un escritorio.   Para desarrolladores que necesitan entornos de  sandbox e instantáneas, o para laboratorios y con fines de demostración. Servidor VMware Microsoft Virtual PC Oracle VM VirtualBox VMware Server es un hipervisor de virtualización alojado gratuito que es muy similar a VMware Workstation. VMware ha detenido el desarrollo en el servidor desde 2009. Esta  es  la  última  versión  de  Microsoft  de  esta  tecnología  de  hipervisor,  Windows Virtual  PC  y  solo  se  ejecuta  en  Windows  7  y  solo  es  compatible  con  los  sistemas operativos Windows que se ejecutan en él. La tecnología de hipervisor VirtualBox proporciona un rendimiento y características razonables  si  desea  virtualizar  con  un  presupuesto  limitado.  A  pesar  de  ser  un producto alojado gratuito con una huella muy pequeña, VirtualBox comparte muchas características con VMware vSphere y Microsoft Hyper-V.
		- (Page 10)
	- -
	- -
		- -V. La máquina virtual basada en el kernel (en siglas, KVM) de Red Hattiene cualidades tanto  de  un  hipervisor  de  virtualización  alojado  como  virtual.  Puede  convertir  el núcleo  de  Linux  en  un  hipervisor  para  que  las  máquinas  virtuales  tengan  acceso directo al hardware físico #flashcard
		- (Page 10)
	- -
	- -
		- Acerca de la virtualización del almacenamiento #flashcard
		  id:: 5398f4e0-6854-4b81-b20a-54beb74485f8
			- La  virtualización  del  almacenamiento  puede  ser  entendida  como  el  proceso  de abstracción lógica del almacenamiento físico. Los recursos de almacenamiento físico (como las unidades de disco) se agregan en agrupaciones de almacenamiento, desde donde el almacenamiento lógico se crea y se presenta al entorno de aplicación. Esta se  puede  implementar  dentro  del  almacenamiento  de  matrices  en  sí  misma (virtualización basada en matrices) o bien en el nivel de red, donde múltiples matrices de discos o almacenamiento en red de sistemas de diferentes proveedores, dispersos por la red, se pueden agrupar en un único dispositivo de almacenamiento monolítico. Esto permite que las matrices múltiples se administren de manera uniforme como si si se tratase de un solo grupo.
		- (Page 11)
	- -
	- -
		- Network Attached Storage (en siglas, NAS) #flashcard
		  id:: 7baf5101-1173-42c2-a9f1-2d4dbd5912a8
			- El almacenamiento conectado a la red, o NAS, es un dispositivo de almacenamiento que se encuentra en la propia red y ofrece almacenamiento a los servidores en la red. Permite  que múltiples  clientes,  como  usuarios  de PC  y servidores,  compartan archivos  a  través  de  una  red  de  área  local  (en  siglas,  LAN).  NAS  utiliza  archivos basados en protocolos como  Network File System (en siglas, NFS), Server Message Block  (en  siglas,  SMB)  o  Common  Internet  File  System  (en  siglas,  CIFS),  donde  el almacenamiento  es  remoto  y  las  ordenadoras  solicitan  un  archivo  en  lugar  de  un bloque de disco. El hecho de tener todos los archivos movidos a una única ubicación central hace que se simplifique la administración de estos. Es decir que, en lugar de tener  que  hacer  un  seguimiento  de  todos  los  archivos  repartidos  entre  docenas, cientos, o incluso miles de máquinas, todos los datos se encuentran en un lugar, lo que  permite  realizar  una  mejor  copia  de  seguridad,  archivado,  etc.  Una  de  las ventajas más acusadas del NAS es que está basado en Internet Protocol (en siglas, IP) y es fácil de usar, desplegar y gestionar. Los usos más comunes incluyen archivos de rápido almacenamiento para rich media, documentos y archivos de back-up y correo electrónico.
		- (Page 12)
	- -
	- -
		- Storage Area Network (en siglas, SAN) #flashcard
		  id:: 45da545f-e330-4a57-a8d1-7a5c6c23f662
			- Una red de área de almacenamiento, o SAN, es un dispositivo de almacenamiento (como una matriz de  discos o una biblioteca de cintas) accesible a los servidores para  que  los  dispositivos  puedan  permanecer  localmente  conectados  al  sistema operativo.  La  SAN,  normalmente,  tiene  su  propia  red  de  dispositivos  de almacenamiento  a  los  que  usualmente  no  se  puede  acceder  a  través  de  una  red ordinaria de dispositivos. Una SAN sola no proporciona la abstracción del «archivo» como en el caso de NAS, sino que solo provee operaciones a nivel de bloque. La mayoría de las SAN usan la conectividad del canal de fibra, del inglés Fibre Channel Connectivity  (en  siglas,  FC),  una  tecnología  de  red  especialmente  diseñada  para gestionar comunicaciones de almacenamiento, o Internet SCSI (en siglas, iSCSI), que es un estándar de red basado en IP para vincular dispositivos de almacenamiento. Las empresas utilizan almacenamiento este tipo de almacenamiento para centralizar la  gestión  de  los  datos  corporativos.  Los  usos  comunes  de  una  SAN  incluyen  el aprovisionamiento de datos de acceso transaccional que requieren acceso a nivel de bloque de alta velocidad a los discos duros de almacenamiento, tales como servidores de correo electrónico, bases de datos y servidores de archivos de acusado uso.
		- (Page 13)
	- -
	- -
		- ¿De qué sirve tener máquinas virtuales y almacenamiento (que se pueda virtualizar y migrar, según sea necesario) cuando los dispositivos físicos de endpoint de entrada y salida (en adelante, E/S) que residen en el servidor son no son ágiles? La administración manual de un recurso clave en un entorno virtualizado significa que la eficiencia está reñida con la capacidad que tenga esa organización de TI para administrar manualmente estos dispositivos de E/S. #flashcard
		  id:: d25efeb5-5db6-4a3f-b629-8e9381c19ecf
			- Virtualización de E/S La  virtualización de  servidores  involucra  a  máquinas que funcionan  en un  servidor físico, lo que hace posible la ejecución de múltiples máquinas virtuales en un único sistema  físico.  La  virtualización  del  almacenamiento  permite  que  los  datos  se transfieran a un almacenamiento centralizado y compartido, lo que permite que se gestione de manera eficiente y rentable. Sin embargo, obtener datos de la máquina requiere pasar por endpoints de red y almacenamiento en el servidor, lo que puede traer aparejado otro conjunto de problemas
		- (Page 13)
	- -
	- -
		- Como  es  de  esperar,  la  virtualización  también  se  ha trasladado a la red y, en lugar de realizar cambios en la red moviendo cables entre diferentes  recursos  físicos,  la  tecnología  de  virtualización  se  aplica  a  la  red  en  sí misma. lógicamente. La virtualización de red permite que la red se configure sobre la marcha, sin necesidad de tocar ni un solo cable o dispositivo. Por tanto, los dispositivos de red con capacidad de  virtualización  se  administran  de  forma  remota  y  se  pueden  reconfigurar #flashcard
		- (Page 14)
	- -
	- -
		- La virtualización de aplicaciones es una separación de la ejecución del programa y de la visualización de este.En otras palabras, un programa como Microsoft Word se ejecuta en un servidor ubicado en el centro de datos, pero la salida gráfica se envía a un  dispositivo  cliente  remoto.  El  usuario  final  ve  la  pantalla  gráfica  completa  del programa y puede interactuar con él a través del teclado y el ratón. #flashcard
		  id:: 72f21e82-cfb7-48a6-926c-282a0746b7b7
		- (Page 15)
	- -
	- -
		- qué sucede con nuestra aplicación favorita que ejecutamos a diario en nuestro ordenador. ¿Desaparecería con la virtualización de escritorio? La respuesta es no. Los datos y configuraciones se pueden guardar por separado y se aplican a la imagen clonada, para garantizar que cada usuario tenga sus aplicaciones y datos listos para cuando abra su escritorio. #flashcard
		- (Page 16)
	- -
	- -
		- ¿Qué es el streaming de escritorio, o check-in check-out? #flashcard
			- Cuando finaliza la sesión, el usuario apaga el sistema y la imagen del ordenador se escribe en el repositorio central y no queda nada en el hardware del usuario.
		- (Page 17)
	- -
	- -
		- Esta  forma  de  entrada  y  salida  de  virtualización  cliente  está  comenzando  a explorarse, pero es muy prometedora para los entornos donde la disponibilidad de conectividad de red de alta velocidad es incierta. Por ejemplo, cuando alguien trabaja de  forma  remota  desde  casa,  puede  que  no  esté  claro  si  su  conexión  es  lo suficientemente  sólida  como  para  permitir  la  virtualización  de  aplicaciones  o  la virtualización  de  escritorio  tradicional.  En  estos  casos,  una  única  descarga  del escritorio a un dispositivo cliente puede ser una buena opción. #flashcard
		  id:: 1400b21e-29fe-4f47-8203-4e77f67d1ffc
		- (Page 17)
	- -