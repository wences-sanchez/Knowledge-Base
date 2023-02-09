title:: Herramientas DevOps Tema-4 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas DevOps Tema-4"
category:: #books

tags:: #[[Herramientas-DevOps]] #[[UNI]]

- #tags #[[Herramientas-DevOps]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/c05b5ba7-0c7e-44ec-a901-1407a0a6c414.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- ¿Qué es Packer? #card
		- Packer es una herramienta que se utiliza para generar imágenes. Las imágenes son un fichero binario que determina los contenidos iniciales (en disco) de una máquina virtual  u  otros  entornos.  Las  imágenes  contienen  todos  los  elementos  que  les componen al momento de su creación, si bien casi todos los proveedores en la nube pueden proporcionar contenido extra después.
		- (Page 4)
	- -
	- -
	- ¿Qué es un artifact, en Packer? #card
		-   Artifacts: los artefactos son el resultado de una compilación o ejecución única, y generalmente son un conjunto de ID o archivos que representan una imagen de la máquina. Cada constructor (builder) produce un solo artefacto. Como ejemplo, en el caso del constructor de Amazon EC2, el artefacto es un conjunto de AMI (uno por  región).  Las  AMI  son  identificadores  únicos  para  las  imágenes.  Para  el constructor  VMware,  el  artefacto  es  un  directorio  de  archivos  que  incluye  la máquina virtual creada. En general, los artefactos son las imágenes y otras salidas deseadas de Packer.
		- (Page 9)
	- -
	- -
	- ¿Qué es una build, en Packer? #card
		- Las *builds* o *compilaciones* son una tarea única que finalmente produce una imagen, normalmente para una sola plataforma. Varias versiones se ejecutan en paralelo. En general, cuando se ejecuta Packer se realizarán una serie de compilaciones independientes en paralelo, que pueden requerir múltiples pasos.
		- (Page 9)
	- -
	- -
	- ¿Qué es un builder, en Packer? #card
		- Los *builders* o *constructores* son componentes de Packer que pueden crear una imagen de máquina para una plataforma específica. Los constructores leen una configuración y la usan para ejecutar y generar una imagen de máquina.
		- (Page 9)
	- -
	- -
	- ¿Qué son los provisioners, en Packer? #card
		-   Provisioners:  los  aprovisionadores  son  componentes  de  Packer  que  instalan  y configuran el software dentro de una máquina en funcionamiento antes de que esta se convierta en una imagen estática. Su trabajo principal es el de lograr que la  imagen  contenga  el  software  deseado.  Los  proveedores  de  ejemplo  incluyen scripts de  Shell,  Chef, Puppet,  etc.
		- (Page 10)
		- #[[favorite]]
	- -
	- -
	- ¿Qué son los post-processors, en Packer? #card
		-   Post-processors: los posprocesadores son componentes de Packer que toman el resultado  de  un  constructor  u  otro  posprocesador  y  lo  procesan  para  crear  un nuevo  artefacto.  Como  ejemplos  de  posprocesadores  podemos  nombrar  la compresión  de  artefactos  mediante  compress,  subir  dicha  compresión  a  un servidor para almacenarla mediante upload, etc.
		- (Page 10)
	- -
	- -
	- ¿Qué son las templates, en Packer? #card
		-   Templates: los templates son archivos JSON que definen una o más compilaciones (builds)  configurando todos los  componentes  de  Packer  como los aprovisionadores y los compiladores.
		- (Page 10)
	- -
	- -
	- ¿Qué hace el subcomando de packer: inspect? #card
		- El comando de Packer inspect toma una template y genera los diversos componentes que la definen. Esto puede ayudarte a aprender rápidamente sobre estas sin tener que sumergirte  en  el  JSON.  El  comando  te  dirá  cosas  como  qué  variables  acepta  la template, los constructores y proveedores que define, y el orden en que se ejecutarán. Es  útil  cuando  se  tienen  múltiples  templates  de  Packer  en  una  empresa  y  no recordamos los párametros o proveedores que tenía una template en particular.
		- (Page 15)
	- -
	- -
	- ¿Cómo podrías combinar varios post-processors en Packer? #card
		- si queremos almacenar artefactos en dos lugares distintos, usaremos dos posprocesadores en la lista de post‐processors. Si lo que queremos es comprimir y luego subir a un único lugar, usaremos un único elemento de tipo lista en la sección que incluirá dos posprocesadores dentro como en el ejemplo anterior.
		- (Page 24)
	- -
	- -
	- Sobre por qué es bueno usar  Packer. #card
		- Packer instala y configura todo el software para una máquina en el momento en que se construye la imagen.
		- (Page 30)
	- -