# Contenedores Tema-9

deck:: [[UNI::Contenedores Tema-9]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-9"\
category:: #books\
\
tags:: Contenedores UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/68a52c90-f8f9-41a1-a380-c294cddbad73.jpg)
## Highlights
- id:: 63c669f1-0dac-4f2e-8cef-00072bb3b580
  
  En Kubernetes los volúmenes serán directorios accesibles por todos los contenedores que forman parte de un Pod. Las modificaciones realizadas en el sistema de ficheros locales de los contenedores se perderán cuando se reinicien. Sin embargo, la información en los volúmenes sí se mantendrán tras un reinicio del contenedor. #flashcard 
  
  
     (Page 5)
-
- id:: 63c669f1-6237-4b47-89d7-6e9de9bd94df
   ¿Qué son los **volúmenes** en Kubenetes? #flashcard 
    r
  
     (Page 5)
-
- id:: 63c669f1-68df-4315-a798-a20804d914e8
   Explica qué es un volumen **emptyDir** #flashcard 
    Los volúmenes de tipo emptyDir nos permitirán compartir ficheros entre los contenedores de un Pod. Como su nombre indica, estos se crean vacíos. Todos los contenedores que forman parte del Pod podrán tener acceso de lectura y escritura a los ficheros del volumen, aunque cada contenedor podrá montar el volumen en una ruta diferente. Los volúmenes emptyDir están ligados a la vida útil del Pod, es decir, los datos almacenados serán borrados cuando el Pod sea eliminado del nodo.
  
     (Page 5)
-
- id:: 63c669f1-7fc0-4fa0-a22e-22ef67aa507b
   Ejemplo de volumen **emptyDir** #flashcard 
    Los volúmenes emptyDir se crearán en el disco del nodo que esté alojando al Pod. Esto quiere decir que el rendimiento dependerá del tipo de disco que se utilice. Sin embargo, podemos indicarle a Kubernetes que queremos utilizar un sistema de ficheros en memoria (tmpfs), el cual será muchísimo más rápido, aunque deberemos tener en cuenta los límites de memoria de los contenedores. La definición del volumen quedaría de la siguiente manera: ... volumes: - name: html-content emptyDir: medium: Memory
  
     (Page 7)
-
- id:: 63c669f1-4e42-44f9-8b06-9405410323df
   ¿Qué es un volument **gitRepo** en Kubernetes?
   AÑADIR IMAGEN #flashcard 
    Los volúmenes de tipo gitRepo nos permiten disponer de un volumen en el cual se ha clonado una rama específica de un repositorio de Git. Funciona de manera similar a los emptyDir, pero, a diferencia de este, el contenido del repositorio es copiado antes de la creación de los contenedores. Estos volúmenes no sincronizan los cambios realizados en el repositorio Git. Una vez inicializados no se volverán a copiar los archivos del repositorio, a menos que se haya replicado un nuevo Pod, en cuyo caso se creará un nuevo volumen clonando el estado actual del repositorio.
  
     (Page 7)
-
- id:: 63c669f1-c77a-4101-a932-5e6084c94436
   ¿Qué es un volumen de tipo **hostPath**?´ #flashcard 
    Los volúmenes de tipo hostPath referenciarán un directorio o archivo específico del sistema de ficheros del nodo, permitiendo a los Pods que lo monten, acceder a su contenido en la ruta local especificada. Es importante tener en cuenta que dicha ruta será la misma en todos los nodos y deberemos saber previamente si existe o no, y si tenemos los permisos necesarios. Algunos ejemplos de casos de uso son:  El contenedor necesita acceder a la información interna de Docker  Se quiere ejecutar cAdvisor en el contenedor para el análisis de recursos (/sys) (/var/lib/Docker)
  
     (Page 9)
-
- id:: 63c669f1-4b96-4a70-8773-ad46e3fb14c6
   INCLUIR IMAGEN #flashcard 
    Kubernetes nos permite desacoplar el método de almacenamiento al ocultar la infraestructura subyacente a los desarrolladores. Estos últimos solo tendrán que solicitar la cantidad de almacenamiento requerido para sus aplicaciones y será Kubernetes el encargado de ponerlo a disposición de los Pods. Por lo tanto, serán los administradores del clúster los encargados de configurar el almacenamiento disponible, indicando el tamaño y los modos de acceso permitidos, y registrarlo en Kubernetes utilizando recursos de tipo PersistentVolume. Posteriormente, cuando un usuario necesite almacenamiento lo solicitará por medio de un manifiesto PersistenVolumeClaim, indicando cuánta capacidad necesita y el modo de acceso requerido, y, finalmente, será Kubernetes el encargado de asociarle un PersistentVolume adecuado.
  
     (Page 13)
-
- id:: 63c669f1-1d67-4afa-8805-a9b40c2ed9bc
   ¿Cuáles son los modos de acceso permitidos para un **peristentVolume**? #flashcard 
    Los modos de acceso permitidos son: ReadWriteOne (RWO): únicamente se permite que un nodo monte el volumen para ReadOnlyMany (ROX): está permitido que múltiples nodos monten el volumen para ReadWriteMany (RWX): varios nodos pueden montar el volumen tanto para lectura lectura y escritura. solo lectura. como escritura
  
     (Page 14)
-
- id:: 63c669f1-d4b5-4415-8d42-27f8ac059d6a
  
  Antes de poder utilizar en los Pods el almacenamiento que acabamos de configurar, deberemos reclamarlo mediante un PersistentVolumentClaim. Este proceso se realiza de forma previa e independiente a la creación de los Pods. A diferencia de los PersistentVolume que eran globales al clúster, estos objetos de reclamo o claims existen a nivel de Namespace. Esto quiere decir que solo los Pods creados en dicho Namespace podrán utilizarlo. Para hacer esta solicitud de almacenamiento crearemos un fichero en formato YAML con su definición, en la que indicaremos la cantidad de almacenamiento requerido, así como los modos de acceso #flashcard 
  
  
     (Page 16)
-
- id:: 63c669f1-6dad-4fbc-a8aa-3f3b99c84e01
  
  Kubernetes soporta el aprovisionamiento dinámico del almacenamiento externo, creando, además, su objeto PersistentVolume al eliminar la necesidad de crear y registrar previamente el almacenamiento. Para ello definiremos recursos StorageClass y será Kubernetes el encargado de crear el PersistentVolume cada vez que se solicite almacenamiento mediante un PersistentVolumeClaim. Kubernetes soporta el aprovisionamiento dinámico para la mayoría de los proveedores de nube. Al definir un StorageClass especificaremos el proveedor a utilizar (provisioner), así como los parámetros (parameters) que se utilizarán cuando se realice el aprovisionamiento dinámico. Cada proveedor tendrá su propio conjunto de parámetros #flashcard 
  
  
     (Page 18)
-
- id:: 63c669f0-cf05-46e8-96ca-b71713ecab89
  
  El siguiente ejemplo crea un StorageClass para discos EBS en AWS: kind: StorageClass apiVersion: storage.k8s.io/v1 metadata: name: gp2-ebs-sc provisioner: kubernetes.io/aws-ebs parameters: type: gp2 fsType: ext4 $ kubectl create -f gp2-ebs-sc.yaml storageclass "gp2-ebs-sc" created #flashcard 
  
  
     (Page 19)
-
- id:: 63c669f0-0925-4b20-b758-a039e098bd99
   INCLUIR IMAGEN #flashcard 
    Kubernetes también nos permite desacoplar de los Pods sus opciones de configuración, de manera que sean reutilizables en diferentes entornos. Separaremos la configuración en objetos de tipo ConfigMap, que estarán compuestos por pares clave/valor. A la hora de desplegar nuestros Pods, estos se combinarán con los valores de configuración del ConfigMap antes de ejecutarse. Los ConfigMap serán referenciados mediante su nombre en la definición de los Pods. Ello nos permite utilizar los mismos Pods en diferentes entornos creando diferentes ConfigMaps en cada Namespace:
  
     (Page 20)
-