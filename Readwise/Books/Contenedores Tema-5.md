# Contenedores Tema-5

deck:: [[UNI::Contenedores Tema-5]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-5"\
category:: #books\
\
tags:: Contenedores UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/8184ee50-30f0-4aad-9d8a-0a568bff6963.jpg)
## Highlights
- id:: 63c669ee-c87f-496e-a9e4-14421e9ff7ed
  
  Las versiones actuales de Docker ofrecen un orquestador integrado en el propio engine llamado «modo enjambre» o «modo Swarm» para permitir una configuración distribuida. Sin embargo, antes de la versión 1.12 de Docker se utilizaba un modelo independiente denominado «Docker Swarm». #flashcard 
  
  
     (Page 5)
-
- id:: 63c669ee-dfb5-4964-896c-bbbfcaa1a0c2
  
  La ejecución de Docker en modo Swarm no impide que se ejecuten contenedores de manera independiente, como hemos visto en temas anteriores, en cualquiera de los nodos del clúster. La principal diferencia entre contenedores independientes y los servicios de Swarm es que solo los mánagers de Swarm pueden gestionar estos servicios, mientras que los contenedores independientes se pueden iniciar en cualquier host. #flashcard 
  
  
     (Page 6)
-
- id:: 63c669ee-4f77-454c-9bb3-e87081f576f2
  
  Las principales características que ofrece el modo Swarm son:  Administración de clústeres integrada en Docker Engine.  Diseño descentralizado.  Modelo de servicio declarativo. #flashcard 
  
  
     (Page 6)
-
- id:: 63c669ee-1493-45a4-a6ab-7e6857a8c94f
   <<<<<< #flashcard 
     Escalabilidad.  Conciliación de estado deseado.  Soporte de redes en múltiples host.  Descubrimiento de servicios.  Balanceo de carga.  Seguridad de forma predeterminada.  Actualizaciones continuas.
  
     (Page 7)
-
- id:: 63c669ee-9cdb-4c35-8845-1ce1fa17c361
  
  Un nodo será cualquier máquina, ya sea física o en la nube, con el motor de Docker que forma parte de un clúster de Swarm. Tenemos dos tipos de nodos:  Mánagers: serán los encargados de desplegar las aplicaciones en el clúster enviando tareas a los nodos de tipo worker.  Workers: ejecutan las tareas recibidas por los nodos mánagers. Además, notificarán periódicamente el estado de estas. #flashcard 
  
  
     (Page 7)
-
- id:: 63c669ee-7ee4-40e6-be07-922719a5d021
   Explica qué son los nodos manager de Docker Swarm #flashcard 
    Los nodos mánager del clúster trabajarán para mantener en todo momento el estado deseado definido, planificarán los servicios entre los nodos y, además, atenderán las llamadas al API de Swarm.
  
     (Page 8)
-
- id:: 63c669ee-02e6-4062-82aa-9453fb0bc37f
   ¿Para qué sirven los nodos de trabajo (o workers) en **Docker Swarm**? #flashcard 
    La finalidad de los nodos de trabajo o workers en el clúster será exclusivamente la ejecución de tareas, es decir, de contenedores. Podríamos tener un clúster sin nodos worker, ya que por defecto un nodo mánager también atiende tareas como los workers. Pero no podremos, ni tampoco tendría sentido, crear un clúster con solo nodos worker.
  
     (Page 8)
-
- id:: 63c669ee-f9c5-4ac9-a73a-f1e5ab3bdfa3
  
  Para evitar que se planifiquen tareas para los nodos mánagers podemos ponerlos en modo drenaje (drain). Si ya tenía tareas asignadas se planificarán de nuevo en otros nodos. #flashcard 
  
  
     (Page 8)
-
- id:: 63c669ee-bd89-4a0b-9b8d-067b48de4077
   INCLUIR IMAGEN #flashcard 
    Cuando indiquemos que queremos varias réplicas un determinado servicio, será el nodo mánager quien distribuya las tareas entre los diferentes nodos del clúster hasta lograr el estado deseado. Estas tareas se ejecutarán de manera independiente.
  
     (Page 9)
-
- id:: 63c669ee-4615-4706-aad1-67d8f7fb7988
  
  Los clústeres Swarm utilizan TLS para autenticar, autorizar y encriptar las comunicaciones entre los nodos. Cuando inicializamos el clúster el nodo inicial se convierte en mánager y en él se crearán una autoridad certificadora raíz (CA) junto con un par de claves que servirán para establecer una comunicación segura con el resto de los nodos que se añadan al clúster. #flashcard 
  
  
     (Page 11)
-
- id:: 63c669ee-ff6e-468b-9602-f244d7cea91a
  
  Tabla 1. Comandos para la gestión de servicios. Fuente: elaboración propia. #flashcard 
  
  
     (Page 15)
-
- id:: 63c669ee-2b7f-4b2a-82ec-81dc874090ef
   Cambio de rol de un nodo en Docker Swarm #flashcard 
    Es posible promover un nodo worker para convertirlo en nodo mánager, y viceversa, podemos degradar un nodo mánager a worker. Para realizar estas tareas de cambio de rol de los nodos utilizaremos los siguientes comandos desde un nodo de administración: $ docker node promote nombreNodoWorker $ docker node demote nombreNodoManager
  
     (Page 21)
-
- id:: 63c669ee-bb81-4048-9122-a2ce877cbb89
   Nombra las diferencias entre **config** y **secret** en *Docker Swarm* #flashcard 
     Los objetos config no se almacenan en claro cuando los creamos. Sin embargo, los secret se almacenan encriptados. Ambos se transmiten de forma encriptada  La ruta de montaje por defecto de los config es /<config-name>, y en los secret entre los nodos. es /run/secrets/<secret_name>.  Los objetos config se montan directamente en el sistema de ficheros del contenedor. Sin embargo, los secret utilizan sistemas de ficheros en memoria (RAM disk).  Un determinado objeto secret solamente será accesible por aquellos servicios a los que hemos dado acceso explícitamente.
  
     (Page 23)
-
- id:: 63c669ee-b349-4772-9232-e822018d5f0d
  
  Tabla 2. Comandos para la gestión de stacks. Fuente: elaboración propia. #flashcard 
  
  
     (Page 26)
-