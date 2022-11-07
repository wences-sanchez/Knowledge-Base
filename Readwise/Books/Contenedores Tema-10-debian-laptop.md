# Contenedores Tema-10

deck:: [[UNI::Contenedores Tema-10]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-10"\
category:: #books\
\
tags:: UNI Contenedores  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/673e4247-86d7-421b-8346-963806a9ab69.jpg)
## Highlights
- id:: 63639915-bd65-4673-988e-343df77b4ef1
  
  Cuando ejecutemos comandos con kubectl para crear o actualizar un Deployment, podremos especificar la opción --record para anotar en el recurso el comando ejecutado. Esta información se guardaría en la anotación kubernetes.io/change cause y podrá ser consultada en el histórico de las revisiones del Deployment. $ kubectl create -f nginx-deployment.yaml --record deployment "nginx-deployment" created $ kubectl apply -f nginx-deployment.yaml --record #flashcard 
  
  
     (Page 7)
-
- id:: 63639915-3320-4288-a245-5f944d7de423
   ¿Con qué comando de Kubernetes puedes comprobar el estado de un despliegue? #flashcard 
    Una vez ejecutado un comando de creación o actualización del Deployment, podemos consultar el estado en que se encuentra el despliegue de los Pods con el comando kubectl rollout status.
  
     (Page 7)
-
- id:: 63639915-709d-4e6a-b723-39df9a4c19ba
   ¿Cuándo se activa el lanzamiento de un **Deployment** en *Kubernetes* ? #flashcard 
    El proceso de despliegue de un recurso Deployment actualizará los Pods asociados con una nueva versión, por lo tanto, se disparará solamente cuando modifiquemos la plantilla de los Pods, por ejemplo, modificando la imagen utilizada. Cuando modifiquemos otra configuración del Deployment como puede ser el número de réplicas o la estrategia utilizada, no se lanzará el despliegue de actualización de Pods, ya que en estos casos la definición de estos es la misma. En todo caso se crearán o eliminarán Pods.
  
     (Page 8)
-
- id:: 63639915-61b7-4c83-8ed9-88c67c7284d2
   ¿Cuáles son las dos **estrategias de despliegue** que se pueden usar en *Kubernetes* ? #flashcard 
    Deployments: Kubernetes soporta dos estrategias de despliegue para la actualización de los  La estrategia Recreate, que elimina primero los Pods de la versión actual y vuelve a crearlos de nuevo con los cambios aplicados. Existe cierta pérdida de servicio durante la actualización.  La estrategia RollingUpdate, utilizada por defecto, en la que los Pods se van reemplazando progresivamente. La aplicación debe soportar el funcionamiento eventual con Pods de dos versiones diferentes. Esta estrategia se basa en la configuración de dos propiedades: • maxSurge, que indica el número de Pods que puede haber por encima del valor deseado. • maxUnavailable, que establece el número máximo de Pods que pueden no estar disponibles en un momento dado.
  
     (Page 10)
-
- En **Kubernetes**,
	- ¿Cómo podemos volver a un despliegue anterior?
	- ¿Cómo podemos volver a un despliegue concreto? #flashcard 
	  id:: 63639915-cc81-47f6-a021-421191d194b6
	      Si después de desplegar los cambios queremos volver al estado anterior porque las actualizaciones no están funcionando como esperábamos, utilizaremos el comando kubectl rollout undo. El Deployment utilizará el Replicaset que ya teníamos creado, y aún no ha sido eliminado, el cual ahora estaría con cero réplicas. $ kubectl rollout undo deployment nginx-deployment Si en lugar de volver a la revisión previa queremos restablecer una en concreto, podemos utilizar el parámetro --to-revision: $ kubectl rollout undo deployment nginx-deployment --to-revision=2
	  
	  (Page 12)
-
- id:: 63639915-4d45-4fb9-aee2-08a258c743cd
   UNIR CON EL DE DEBAJO
   INCLUIR LA IMAGEN #flashcard 
    Los StatefulSets se utilizarán para gestionar aplicaciones con estado. Al igual que los Replicasets, nos permitirán gestionar varias réplicas de Pods. Sin embargo, los StatefulSets nos ofrecen algunas propiedades únicas:  A cada una de las réplicas de los Pods se le asignará un hostname e IP persistente, además de nombrar los Pods con un índice único. El hostname estará compuesto por el nombre del StatefulSet y el ordinal del Pod: $(statefulset-name)-$(ordinal). Por ejemplo: web-0, web-1, etc.
  
     (Page 22)
-
- id:: 63639915-1927-4a46-bc64-e6af1e7b5442
  
   Las réplicas se crean en orden, comenzando por el índice más bajo. Además, hasta que el Pod de una réplica no esté creado y disponible, no se comenzará con el de la siguiente réplica. Esto aplica tanto en la creación como en el escalado.  Al borrar un StatefulSet, las réplicas de los Pods serán eliminados en orden inverso, es decir, comenzando por el índice más alto. Igualmente, también aplica durante un escalado al reducir el número de réplicas.  Cada una de las réplicas tendrá su propio almacenamiento persistente. #flashcard 
  
  
     (Page 23)
-
- id:: 63639915-734b-498f-bc75-2378064dde36
   INCLUIR IMÁGENES #flashcard 
    En los Replicasets todas las réplicas compartían el mismo almacenamiento persistente reclamado por un PersistentVolumeClaim. Sin embargo, en las aplicaciones con estado, cada una de las réplicas deberá tener su propio almacenamiento persistente. Para ello, el StatefulSet creará un PersistentVolumeClaim en cada una de las réplicas: Figura 4. Los StatefulSets crearan Pods con su propio almacenamiento. Fuente: Luksa, M. (2018). Este almacenamiento persistente asociado a cada réplica no será eliminado cuando un Pod sea eliminado por haberse reducido el número de réplicas. El PersistentVolumeClaim simplemente se desvinculará del Pod, de manera que pueda volver a asociarse al Pod si la réplica se vuelve a escalar más adelante. Veamos cómo funciona con el siguiente ejemplo gráfico:
  
     (Page 24)
-