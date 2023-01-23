# SecDevOps Tema-6

deck:: [[UNI::SecDevOps Tema-6]]\
author:: [[UNIR]]\
full-title:: "SecDevOps Tema-6"\
category:: #books\
\
tags:: SecDevOps UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/d7095b61-4205-46b6-b02a-77b13111959c.jpg)
## Highlights
- id:: 63c66a21-c1fd-418d-a2b2-e11549c1806b
   ¿Qué se conoce como VNet? #flashcard 
    Azure Virtual Network (denominada también VNet) es una de las piezas esenciales para la infraestructura de red privada en Azure (Tullock, 2013). VNet permite que muchos tipos de recursos de Azure, como las máquinas virtuales, se comuniquen de manera segura entre sí, con Internet y con las redes locales on-premise. VNet es similar a la red tradicional de un centro de datos, pero tiene beneficios adicionales de la infraestructura nativa de nube, como la escalabilidad y alta disponibilidad.
  
     (Page 5)
-
- id:: 63c66a21-a143-4358-bdef-829ddf76730a
  
  Algunos de los conceptos esenciales de VNet son:  Espacio de direcciones: al crear una red virtual, es necesario especificar un espacio de direcciones IP privadas. Azure asigna IP de este espacio a los recursos conectados a la red virtual. Por ejemplo, una VM desplegada en una red virtual con espacio de direcciones 10.0.0.0/16 recibirá una IP privada dentro de esa subred, por ejemplo, 10.0.0.4.  Subredes: las subredes permiten segmentar la red virtual en una o más redes, y asignar una parte del espacio de direcciones de la red virtual a cada subred. Los recursos podrán desplegarse en la subred necesaria, de acuerdo con las necesidades de la arquitectura de los sistemas. Al igual que en una red tradicional, la segmentación de las subredes mejora la eficiencia de asignación de direcciones. #flashcard 
  
  
     (Page 5)
-
- id:: 63c66a21-91ae-4ba5-95fb-a777c25b613c
  
  Además, los recursos dentro de las subredes se pueden proteger utilizando grupos de seguridad de red.  Regiones: una región es un conjunto de centros de datos, implementados dentro de un perímetro con una latencia definida y conectados a través de una red regional dedicada de baja latencia. Una VNet tiene un alcance para una sola región de Azure; sin embargo, se pueden conectar varias redes virtuales de diferentes regiones mediante el emparejamiento de redes virtuales.  Suscripción: una suscripción de Azure está vinculada a una sola cuenta, la que se utilizó para crear la suscripción y se utiliza para fines de facturación (es un concepto similar al de cuenta en AWS). Los recursos se provisionan dentro de una suscripción. Una VNet tiene un alcance de una suscripción, y una subscripción puede tener tantas VNets como sean necesarias. #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a21-d72c-48cb-8242-f1d0e566b4f6
  
  Los recursos locales y las redes virtuales en la nube se pueden conectar mediante cualquier combinación de las siguientes opciones:  Red privada virtual (VPN) de punto a sitio (point-to-site): en este caso, cada equipo de la red local que necesite conectarse a recursos de Azure puede establecer una VPN. También se pueden denominar VPN de cliente. #flashcard 
  
  
     (Page 7)
-
- id:: 63c66a21-efe6-4ec1-a274-56707a2a13d3
  
   VPN de sitio a sitio (site-to-site): en este caso, un dispositivo VPN específico en la red local establece una conexión VPN con un Azure VPN Gateway. Este dispositivo VPN enruta el tráfico de las máquinas de la red local a la red virtual de Azure.  Azure ExpressRoute: esta solución establece una conexión a través de un colaborador de Azure. Al estilo de un servicio MPLS, este tráfico no se envía por Internet. #flashcard 
  
  
     (Page 8)
-
- id:: 63c66a21-2778-4104-92e5-a8cb98334b86
  
  Se pueden definir más subredes una vez creada la VNet y, como se ha comentado previamente, es recomendable mantener un espacio de direcciones amplio y segmentado para poder ampliar las subredes en el futuro #flashcard 
  
  
     (Page 9)
-
- id:: 63c66a21-517d-4eee-8f27-1ca7bff71fbb
  
  Los grupos de seguridad de aplicación de Azure, o application security groups, permiten agrupar máquinas virtuales e interfaces de red en grupos lógicos, que pueden usarse en grupos de seguridad de red. Esto los convierte en una extensión natural de la estructura de la aplicación, ya que las reglas de los grupos de seguridad de red se pueden definir en base a objetos de la nube y no a IP específicas. #flashcard 
  
  
     (Page 10)
-
- id:: 63c66a21-8958-403e-9a84-f8b6cde99816
  
  Los grupos de seguridad de red, o network security groups, funcionan como firewalls virtuales a nivel de interfaz de máquina virtual y de subred. Contienen listas de reglas definidas a partir del protocolo, rango de IP y puertos de origen y rango de IP y puertos de destino. Un mismo grupo de seguridad de red puede estar asociado a más de una interfaz y subred. #flashcard 
  
  
     (Page 11)
-
- id:: 63c66a21-2ac3-4de6-b3f1-8325dc4dd052
  
  Un appliance se refiere a una máquina virtual que empaqueta el sistema operativo con un software específico. Se pueden distribuir como una imagen o plantilla lista para ser desplegada en un entorno de virtualización. #flashcard 
  
  
     (Page 17)
-
- id:: 63c66a21-afb8-41f9-917e-7cbcce17dfd8
   ¿Qué es un Juniper vSRX? #flashcard 
    El vSRX es un appliance virtual que ofrece servicios de seguridad y de red en entornos de nube pública o privada. Se conoce como firewall de nueva generación, o next generation firewall, porque no solo funciona como firewall avanzado (a nivel de paquetes y de aplicación), sino también como rúter, VPN, NAT o IPS (sistema de detección y prevención de intrusiones).
  
     (Page 18)
-
- id:: 63c66a21-d401-48bd-bdce-26a00f6926f1
  
  Las VPN de cliente sirven para dar acceso remoto a usuarios individuales. Son útiles, por ejemplo, para usuarios itinerantes que necesitan acceder a los recursos de su organización, o para pequeñas oficinas en las que no merece la pena la inversión en un dispositivo de VPN corporativo, y prefieren dar acceso individualmente a sus usuarios. #flashcard 
  
  
     (Page 34)
-
- id:: 63c66a21-d351-40a1-87c5-c7c5deb62390
  
  Las VPN encapsulan el tráfico de la red origen en otros paquetes, y lo desencapsulan en la red destino, depositando el tráfico como si ambas redes estuvieran interconectadas por un simple rúter. En el caso de la VPN de cliente, no hay red origen como tal. El cliente de VPN crea una interfaz de red virtual en el equipo del usuario. Cuando se establece la conexión, el cliente de VPN recibe una IP de la red destino, mediante el servidor DHCP de la VPN, y la configura en la interfaz virtual. A partir de ese momento, el tráfico que los procesos del equipo del usuario envíen a esa interfaz atravesará el túnel de la VPN y llegará a la red de destino. #flashcard 
  
  
     (Page 34)
-