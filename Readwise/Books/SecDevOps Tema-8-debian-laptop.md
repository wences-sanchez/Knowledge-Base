# SecDevOps Tema-8

deck:: [[UNI::SecDevOps Tema-8]]\
author:: [[UNIR]]\
full-title:: "SecDevOps Tema-8"\
category:: #books\
\
tags:: UNI SecDevOps  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/554fa67d-89eb-4910-84a0-6544a20836da.jpg)
## Highlights
- id:: 63639930-76c0-4ad5-b708-42a35050f8e9
   ¿Qué es Kubernetes? #flashcard 
    Kubernetes es un sistema que automatiza el despliegue, el escalado y la administración de aplicaciones diseñadas como contenedores. Un clúster de Kubernetes está formado por múltiples nodos (que pueden ser físicos o virtuales) en
  
     (Page 4)
-
- id:: 63639930-2ca3-44c4-bdfd-c89b33ad5105
   CONTINUE #flashcard 
    los que se despliegan contenedores que ejecutan los procesos de las aplicaciones. La comunicación de red y el ciclo de vida de estos contendores se gestionan con tipos de recursos nativos de Kubernetes, como los pods, servicios y políticas de red.
  
     (Page 5)
-
- id:: 63639930-e9e9-4dea-962f-42eb80bd2363
   ¿Qué es un pod? #flashcard 
    Un pod es un grupo de contenedores localizados en el mismo nodo y representa el componente básico de Kubernetes. En lugar de desplegar contenedores individualmente, siempre es obligatorio desplegar los contenedores en pods. Esto no significa que un pod deba incluir más de un contenedor, y, de hecho, es habitual que los pods contengan solo un contenedor. La idea principal de los pods es que, cuando un pod contiene múltiples contenedores, todos ellos se ejecutan siempre en un solo nodo. Los contenedores comparten el mismo nombre de host y la misma tarjeta de red. No comparten el sistema de ficheros, pero pueden usar un mismo directorio mediante un volumen de Kubernetes.
  
     (Page 6)
-
- id:: 63639930-cd62-4f47-b82a-3f490bd776c0
  
  Además, todos los contenedores en un pod comparten la interfaz de red de bucle invertido (el loopback), por lo que un contenedor puede comunicarse con otros contenedores en el mismo pod a través de localhost. #flashcard 
  
  
     (Page 6)
-
- id:: 63639930-cbfe-4047-8a5f-06574781a806
  
  mismo servicio. Un servicio, o service, de Kubernetes es un recurso que crea un único punto de entrada permanente para un pod, o para un grupo de pods, que proporcionan el Cada servicio tiene una dirección IP y un puerto que nunca cambian durante la vida del servicio. Los clientes pueden abrir conexiones a esa IP y puerto, y esas conexiones se enrutan a uno de los pods que respaldan ese servicio. De esta manera, los clientes de un servicio no necesitan conocer la ubicación, ni las direcciones, de los pods individuales que brindan el servicio, lo que facilita su mantenimiento. #flashcard 
  
  
     (Page 11)
-
- id:: 63639930-391a-4f19-8ada-c559638b3617
   ¿Cómo se pueden seleccionar los pods y exponer servicios al exterior, con Kubernetes? #flashcard 
    La selección de pod se hace con etiquetas: el servicio wordpress tiene la propiedad selector, que indica dos etiquetas: app=wordpress y tier=frontend. La definición de los pods de WordPress incluía esas dos etiquetas. La misma técnica se usa con el servicio y el pod de MySQL, pero con etiquetas diferentes. Kubernetes ofrece varios métodos para exponer servicios al exterior: mediante un servicio de tipo NodePort, un servicio de tipo LoadBalancer o mediante un Ingress, que es otro tipo de recurso que trabaja junto al servicio.
  
     (Page 14)
-
- id:: 63639930-81b2-4616-b54a-971b0be9059f
   ¿En qué consiste el servicio NodePort de Kubernetes? #flashcard 
    El primer método para exponer un conjunto de pods a clientes externos es crear un servicio y establecer su tipo como NodePort. Al crear un servicio NodePort, Kubernetes reserva un puerto en todos sus nodos, el mismo número de puerto en todos ellos, y reenvía las conexiones entrantes en esos puertos a los pods que forman parte del servicio. Esta reserva del puerto es similar a un servicio normal de tipo ClusterIP, pero un servicio NodePort es accesible no solo a través de la IP interna del clúster, sino también a través de la IP de cualquier nodo. Estas IP no pertenecen a la red de los pods, sino a la subred a la que están conectadas las interfaces de los nodos y, por tanto, son accesible desde fuera del clúster.
  
     (Page 14)
-
- id:: 63639930-13b2-462e-b0fc-aca0840a9533
   ¿En qué consiste el servicio de balanceador de carga de Kubernetes? #flashcard 
    Los clústeres de Kubernetes que se ejecutan en proveedores de la nube, generalmente, admiten la provisión automática de un balanceador de carga desde la infraestructura de la nube. Esto es posible si el clúster se aprovisiona como un servicio nativo del proveedor, por ejemplo, mediante el servicio EKS en AWS, AKS en Azure o GKE en Google Compute Cloud . Si se configura un clúster de Kubernetes manualmente a partir de instancias de cómputo (EC2, por ejemplo), el servicio de balanceador no tiene por qué estar disponible, a menos que el proveedor ofrezca la posibilidad de instalar los plugins de su entorno en un clúster propio. Si el clúster lo soporta, todo lo que se necesita hacer es establecer el tipo de servicio en LoadBalancer en lugar de NodePort. El balanceador de carga tendrá su propia dirección IP única, y de acceso público, y redirigirá todas las conexiones a su servicio.
  
     (Page 15)
-
- id:: 63639930-4647-4c11-a687-f5c144d51a80
   CONTINUE #flashcard 
    De este modo, los clientes pueden acceder al servicio a través de la dirección IP del balanceador. Este balanceador será un recurso de tipo ELB en AWS, Azure Load Balancer en Azure o Cloud Load Balancing en GCE . Si Kubernetes se ejecuta en un entorno que no admite los servicios de LoadBalancer, el balanceador no se aprovisionará y el servicio seguirá comportándose como si fuera de tipo NodePort. Esto se debe a que un servicio LoadBalancer es una extensión de un servicio NodePort.
  
     (Page 16)
-
- id:: 63639930-cefc-451e-b216-151672b63de1
   ¿En qué consiste el recurso Ingress de Kubernetes? #flashcard 
    Los recursos Ingress varían de un clúster a otro ya que, aunque son un objeto nativo de Kubernetes, la implementación se basa en un controlador de Ingress, que no se instala por defecto en todos los clústeres. Los controladores disponibles suelen estar
  
     (Page 16)
-
- id:: 63639930-dc41-4a17-b3fe-6ae0db577a54
   CONTINUE #flashcard 
    basados en algún producto que ya ofrezca las funcionalidades previstas para un Ingress, como nginx o envoy, o con un servicio propio de un proveedor de nube, como el Application Load Balancer de AWS . Hay dos razones principales para usar un objeto Ingress en vez de un servicio. La primera es que cada servicio de tipo LoadBalancer requiere su propio balanceador de carga con su propia dirección IP pública, mientras que un Ingress solo requiere uno, incluso cuando proporciona acceso a más de un servicio. Cuando un cliente envía una petición HTTP al Ingress, el nombre de host y la ruta en la solicitud determinan a qué servicio se reenvía el tráfico. La otra razón es que los Ingress ofrecen más funcionalidades que un servicio: afinidad de sesión basada en cookie, terminación de conexiones seguras con certificados TLS, etc.
  
     (Page 17)
-
- id:: 63639930-1a01-4d6d-be58-6ab2032e2b3f
   ¿Cómo funciona Ingress, en Kubernetes? #flashcard 
    El funcionamiento de un Ingress es el siguiente:  El cliente realiza una búsqueda DNS del equipo al que quiere enviar la petición. El nombre estará registrado con la IP pública del Ingress.  El cliente envía una petición HTTP al controlador Ingress y especifica el encabezado Host con el nombre que acaba de resolver mediante DNS.  A partir de ese encabezado, el controlador determina a qué servicio está intentando acceder el cliente.  El controlador redirige la petición a la IP de uno de los pods asociados al servicio.
  
     (Page 17)
-
- id:: 63639930-3a1d-4314-8f9d-2365f66f555d
  
  Los pods reciben una IP de una única subred en todo el clúster, al margen del número de nodos que lo compongan. Los pods pueden comunicarse entre sí sin restricciones. Esto puede no ser relevante si el clúster está dedicado a una única aplicación y la seguridad de red está correctamente aplicada en los servicios expuestos al exterior. En clústeres compartidos (o multi-tenant), esto puede no ser deseable. Para aplicar reglas de seguridad, en la red interna, hay que usar recursos de tipo NetworkPolicy. #flashcard 
  
  
     (Page 18)
-
- id:: 63639930-bb9b-40d6-9a03-5b5c5a8cd7fa
   ¿Cómo interacciona Kubernetes? #flashcard 
    Cualquier interacción con Kubernetes se lleva a cabo en la API mediante peticiones REST, ya sea desde la línea de comandos con kubectl, en el panel web (o dashboard) o desde una aplicación ejecutándose en un pod. Cada llamada atraviesa las fases de autenticación, autorización y control de admisión. En un clúster típico, la API escucha en el puerto 6443 mediante HTTPS. Una vez que se establece la conexión TLS, la petición HTTP se mueve al paso de autenticación. Kubernetes no realiza la autenticación por sí mismo, sino que lo delega a módulos externos.
  
     (Page 23)
-
- id:: 63639930-bc25-4c67-a590-45ed39abaa15
  
  Si bien Kubernetes usa nombres de usuario para las decisiones de control de acceso, no almacena nombres de cuenta ni ninguna otra información sobre los usuarios #flashcard 
  
  
     (Page 23)
-