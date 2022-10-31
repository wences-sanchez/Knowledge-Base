title:: Herramientas DevOps Tema-4 (highlights)
deck:: [[UNI::Herramientas DevOps Tema-4]]
author:: [[UNIR]]
full-title:: "Herramientas DevOps Tema-4"
category:: #books

tags:: Herramientas-DevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/c05b5ba7-0c7e-44ec-a901-1407a0a6c414.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
	- Packer es una herramienta que se utiliza para generar imágenes. Las imágenes son un fichero binario que determina los contenidos iniciales (en disco) de una máquina virtual  u  otros  entornos.  Las  imágenes  contienen  todos  los  elementos  que  les componen al momento de su creación, si bien casi todos los proveedores en la nube pueden proporcionar contenido extra después. #flashcard
		- ¿Qué es Packer?
		- (Page 4)
	- -
	- -
	-   Artifacts: los artefactos son el resultado de una compilación o ejecución única, y generalmente son un conjunto de ID o archivos que representan una imagen de la máquina. Cada constructor (builder) produce un solo artefacto. Como ejemplo, en el caso del constructor de Amazon EC2, el artefacto es un conjunto de AMI (uno por  región).  Las  AMI  son  identificadores  únicos  para  las  imágenes.  Para  el constructor  VMware,  el  artefacto  es  un  directorio  de  archivos  que  incluye  la máquina virtual creada. En general, los artefactos son las imágenes y otras salidas deseadas de Packer. #flashcard
		- ¿Qué es un artifact, en Packer?
		- (Page 9)
	- -
	- -
	- Las *builds* o *compilaciones* son una tarea única que finalmente produce una imagen, normalmente para una sola plataforma. Varias versiones se ejecutan en paralelo. En general, cuando se ejecuta Packer se realizarán una serie de compilaciones independientes en paralelo, que pueden requerir múltiples pasos. #flashcard
		- ¿Qué es una build, en Packer?
		- (Page 9)
	- -
	- -
	- Los *builders* o *constructores* son componentes de Packer que pueden crear una imagen de máquina para una plataforma específica. Los constructores leen una configuración y la usan para ejecutar y generar una imagen de máquina. #flashcard
		- ¿Qué es un builder, en Packer?
		- (Page 9)
	- -
	- -
	-   Provisioners:  los  aprovisionadores  son  componentes  de  Packer  que  instalan  y configuran el software dentro de una máquina en funcionamiento antes de que esta se convierta en una imagen estática. Su trabajo principal es el de lograr que la  imagen  contenga  el  software  deseado.  Los  proveedores  de  ejemplo  incluyen scripts de  Shell,  Chef, Puppet,  etc. #flashcard
		- ¿Qué son los provisioners, en Packer?
		- tags:: [[favorite]]
		- (Page 10)
	- -
	- -
	-   Post-processors: los posprocesadores son componentes de Packer que toman el resultado  de  un  constructor  u  otro  posprocesador  y  lo  procesan  para  crear  un nuevo  artefacto.  Como  ejemplos  de  posprocesadores  podemos  nombrar  la compresión  de  artefactos  mediante  compress,  subir  dicha  compresión  a  un servidor para almacenarla mediante upload, etc. #flashcard
		- ¿Qué son los post-processors, en Packer?
		- (Page 10)
	- -
	- -
	-   Templates: los templates son archivos JSON que definen una o más compilaciones (builds)  configurando todos los  componentes  de  Packer  como los aprovisionadores y los compiladores. #flashcard
		- ¿Qué son las templates, en Packer?
		- (Page 10)
	- -
	- -
	- El comando de Packer inspect toma una template y genera los diversos componentes que la definen. Esto puede ayudarte a aprender rápidamente sobre estas sin tener que sumergirte  en  el  JSON.  El  comando  te  dirá  cosas  como  qué  variables  acepta  la template, los constructores y proveedores que define, y el orden en que se ejecutarán. Es  útil  cuando  se  tienen  múltiples  templates  de  Packer  en  una  empresa  y  no recordamos los párametros o proveedores que tenía una template en particular. #flashcard
		- ¿Qué hace el subcomando de packer: inspect?
		- (Page 15)
	- -
	- -
	- si queremos almacenar artefactos en dos lugares distintos, usaremos dos posprocesadores en la lista de post‐processors. Si lo que queremos es comprimir y luego subir a un único lugar, usaremos un único elemento de tipo lista en la sección que incluirá dos posprocesadores dentro como en el ejemplo anterior. #flashcard
		- ¿Cómo podrías combinar varios post-processors en Packer?
		- (Page 24)
	- -
	- -
	- Packer instala y configura todo el software para una máquina en el momento en que se construye la imagen.
		- Sobre por qué es bueno usar  Packer.
		- (Page 30)
	- -