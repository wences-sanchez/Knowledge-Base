# Exploración De Las Redes Virtuales De Azure

deck:: [[Across-the-Net]]\
author:: [[wwlpublish]]\
full-title:: "Exploración De Las Redes Virtuales De Azure"\
category:: #articles\
url:: https://learn.microsoft.com/es-es/training/modules/introduction-to-azure-virtual-networks/2-explore-azure-virtual-networks\
tags:: azure Azure microsoft learn Microsoft Learn  

![](https://learn.microsoft.com/en-us/media/logos/logo-ms-social.png)

## Highlights
- 

Las redes virtuales de Azure (VNets) son el bloque de creación fundamental de la red privada en Azure. Las redes virtuales permiten crear redes virtuales complejas similares a una red local, con las ventajas adicionales de la infraestructura de Azure, como la escalabilidad, la disponibilidad y el aislamiento. Una red virtual es una representación de su propia red en la nube. Es un aislamiento lógico de la nube de Azure dedicada a su suscripción. Puede usar las redes virtuales para aprovisionar y administrar redes privadas virtuales (VPN) en Azure y, opcionalmente, vincular las redes virtuales con otras redes virtuales en Azure o con sus infraestructura de TI local para crear soluciones híbridas o entre entornos. Cada red virtual que se crea tiene su propio bloque CIDR y se puede vincular a otras redes locales y redes virtuales, siempre que los bloques CIDR no se superpongan. También tiene el control de la configuración del servidor DNS para redes virtuales y de la segmentación de la red virtual en subredes. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn1vhamkqkxfk3emea1y0tgg))
-
- 

**Comunicación entre los recursos de Azure.** Hay tres mecanismos clave a través de los cuales el recurso de Azure puede comunicarse: redes virtuales, puntos de conexión de servicio de red virtual y emparejamiento de redes virtuales. Las redes virtuales no solo pueden conectar máquinas virtuales, sino también otros recursos de Azure, como App Service Environment, Azure Kubernetes Service y conjuntos de escalado de máquinas virtuales de Azure. Los puntos de conexión de servicio se pueden usar para conectarse a otros tipos de recursos de Azure, como cuentas de almacenamiento y bases de datos de Azure SQL. Cuando se crea una red virtual, los servicios y las máquinas virtuales de la red virtual pueden comunicarse de forma directa y segura entre ellas en la nube. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn1vpnfgmf1cdrby6a55344a))
-
- 

**Enrutamiento del tráfico de red.** De forma predeterminada Azure enruta el tráfico entre subredes, redes virtuales conectadas, redes locales e Internet. Puede implementar tablas de rutas o rutas del protocolo de puerta de enlace de borde (BGP) para invalidar las rutas predeterminadas que crea Azure. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn1vv1bmefgtknfkh1x7mb9j))
-
- 

Una subred es un intervalo de direcciones IP de la red virtual. Puede segmentar redes virtuales en subredes de diferentes tamaños y crear tantas subredes como necesite para la organización y la seguridad dentro del límite de la suscripción. A continuación, puede implementar los recursos de Azure en una subred específica. Al igual que en una red tradicional, las subredes permiten segmentar el espacio de direcciones de red virtual en segmentos que sean adecuados para la red interna de la organización. Esto también mejora la eficacia de la asignación de dirección. La subred IPv4 más pequeña admitida es /29 y la más grande es /2 (con definiciones de subred CIDR). Las subredes IPv6 deben tener un tamaño exactamente de /64. Al planear la implementación de subredes, debe tener en cuenta lo siguiente: #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn1w033kzr2y8k0w1wvstkkj))
-
- 

Aunque las subredes son la unidad más pequeña que puede crear a partir del direccionamiento IP, puede segmentar aún más la red mediante grupos de seguridad de red (NSG) para controlar el acceso a la subred. Cada grupo de seguridad de red contiene reglas que permiten o niegan el paso del tráfico hacia y desde los orígenes y destinos. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn1w4t2yb66jwvgvp7w5n4cz))
-
- 

**Espacio de direcciones**
     Al configurar una red virtual, se define el espacio de direcciones internas con el formato de Enrutamiento de interdominios sin clases (CIDR). Este espacio de direcciones debe ser único dentro de la suscripción y de cualquier otra red a la que se conecte.
     Supongamos que elige un espacio de direcciones de 10.0.0.0/24 para la primera red virtual. Las direcciones definidas en este espacio de direcciones van de 10.0.0.1 a 10.0.0.254. Luego cree una segunda red virtual y elija un espacio de direcciones de 10.0.0.0/8. La dirección de este espacio de direcciones va de 10.0.0.1 a 10.255.255.254. Algunas de las direcciones se superponen y no se pueden usar si planea conectar las dos redes virtuales entre sí.
     Pero se puede usar 10.0.0.0/16, con direcciones comprendidas entre 10.0.0.1 - 10.0.255.254, y 10.1.0.0/16, con direcciones comprendidas entre 10.1.0.1 - 10.1.255.254. Puede asignar estos espacios de direcciones a las redes virtuales porque ninguna dirección se superpone. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn1wbbn3d5vqnmr0sg2ba0zt))
-
- 

**Protección de Denegación de servicio distribuido (DDoS)**
     Puede seleccionar habilitar la protección contra DDoS estándar. DDoS Protection estándar es un plan de servicio de pago que ofrece funcionalidades mejoradas de mitigación de DDoS a través del ajuste adaptable, la notificación de ataques y la telemetría para proteger todos los recursos protegidos dentro de esta red virtual frente a los efectos de un ataque DDoS. La protección contra DDoS básica se integra en la plataforma de Azure de forma predeterminada y sin costo adicional. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gn6v13mn89jndfjf5rmyz1a4))
-
