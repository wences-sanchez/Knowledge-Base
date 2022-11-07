# Herramientas DevOps Tema-4

deck:: [[UNI::Herramientas DevOps Tema-4]]\
author:: [[UNIR]]\
full-title:: "Herramientas DevOps Tema-4"\
category:: #books\
\
tags:: Herramientas-DevOps UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/c05b5ba7-0c7e-44ec-a901-1407a0a6c414.jpg)
## Highlights
- id:: 6363991b-21e8-4e10-8b37-ee538171a13c
   ¿Qué es Packer? #flashcard 
    Packer es una herramienta que se utiliza para generar imágenes. Las imágenes son un fichero binario que determina los contenidos iniciales (en disco) de una máquina virtual u otros entornos. Las imágenes contienen todos los elementos que les componen al momento de su creación, si bien casi todos los proveedores en la nube pueden proporcionar contenido extra después.
  
     (Page 4)
-
- id:: 6363991b-3859-44d0-9e5e-6fcbc249c90d
   ¿Qué es un artifact, en Packer? #flashcard 
     Artifacts: los artefactos son el resultado de una compilación o ejecución única, y generalmente son un conjunto de ID o archivos que representan una imagen de la máquina. Cada constructor (builder) produce un solo artefacto. Como ejemplo, en el caso del constructor de Amazon EC2, el artefacto es un conjunto de AMI (uno por región). Las AMI son identificadores únicos para las imágenes. Para el constructor VMware, el artefacto es un directorio de archivos que incluye la máquina virtual creada. En general, los artefactos son las imágenes y otras salidas deseadas de Packer.
  
     (Page 9)
-
- id:: 6363991b-ee7e-4bc5-a073-2e758374294e
   ¿Qué es una build, en Packer? #flashcard 
    Las *builds* o *compilaciones* son una tarea única que finalmente produce una imagen, normalmente para una sola plataforma. Varias versiones se ejecutan en paralelo. En general, cuando se ejecuta Packer se realizarán una serie de compilaciones independientes en paralelo, que pueden requerir múltiples pasos.
  
     (Page 9)
-
- id:: 6363991b-73c8-4ae4-b85b-f0ce7de8ef55
   ¿Qué es un builder, en Packer? #flashcard 
    Los *builders* o *constructores* son componentes de Packer que pueden crear una imagen de máquina para una plataforma específica. Los constructores leen una configuración y la usan para ejecutar y generar una imagen de máquina.
  
     (Page 9)
-
- id:: 6363991b-504e-443f-a547-b0767b2abee1
   ¿Qué son los provisioners, en Packer? #flashcard  #favorite 
     Provisioners: los aprovisionadores son componentes de Packer que instalan y configuran el software dentro de una máquina en funcionamiento antes de que esta se convierta en una imagen estática. Su trabajo principal es el de lograr que la imagen contenga el software deseado. Los proveedores de ejemplo incluyen scripts de Shell, Chef, Puppet, etc.
  
     (Page 10)
-
- id:: 6363991b-acc0-490a-80af-bdb03d722d0f
   ¿Qué son los post-processors, en Packer? #flashcard 
     Post-processors: los posprocesadores son componentes de Packer que toman el resultado de un constructor u otro posprocesador y lo procesan para crear un nuevo artefacto. Como ejemplos de posprocesadores podemos nombrar la compresión de artefactos mediante compress, subir dicha compresión a un servidor para almacenarla mediante upload, etc.
  
     (Page 10)
-
- id:: 6363991b-e634-4485-8d44-c1cd3cd21372
   ¿Qué son las templates, en Packer? #flashcard 
     Templates: los templates son archivos JSON que definen una o más compilaciones (builds) configurando todos los componentes de Packer como los aprovisionadores y los compiladores.
  
     (Page 10)
-
- id:: 6363991b-29cf-4010-9214-1f3452ff0789
   ¿Qué hace el subcomando de packer: inspect? #flashcard 
    El comando de Packer inspect toma una template y genera los diversos componentes que la definen. Esto puede ayudarte a aprender rápidamente sobre estas sin tener que sumergirte en el JSON. El comando te dirá cosas como qué variables acepta la template, los constructores y proveedores que define, y el orden en que se ejecutarán. Es útil cuando se tienen múltiples templates de Packer en una empresa y no recordamos los párametros o proveedores que tenía una template en particular.
  
     (Page 15)
-
- id:: 6363991b-9cce-4352-bc86-c4402d15c6dc
   ¿Cómo podrías combinar varios post-processors en Packer? #flashcard 
    si queremos almacenar artefactos en dos lugares distintos, usaremos dos posprocesadores en la lista de post‐processors. Si lo que queremos es comprimir y luego subir a un único lugar, usaremos un único elemento de tipo lista en la sección que incluirá dos posprocesadores dentro como en el ejemplo anterior.
  
     (Page 24)
-
- id:: 6363991b-8999-40aa-b445-6169ffd5a5ea
   Sobre por qué es bueno usar Packer. #flashcard
	- Packer instala y configura todo el software para una máquina en el momento en que se construye la imagen.
		- Si hay errores en estos scripts, se detectarán de forma inmediata, en lugar de varios minutos después del lanzamiento.
		- Mayor capacidad de prueba.
		- Después de construir una imagen de máquina, la imagen de la máquina puede iniciarse rápidamente y ser probada para verificar que todo funcione. Si todo ha ido bien, puedes estar seguro de que cualquier otra máquina lanzada desde esa imagen funcionará correctamente.
		  
		       (Page 30)
-