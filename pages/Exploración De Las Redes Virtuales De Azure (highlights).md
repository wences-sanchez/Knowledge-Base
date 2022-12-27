title:: Exploración De Las Redes Virtuales De Azure (highlights)
deck:: [[Across-the-Net]]
author:: [[wwlpublish]]
full-title:: "Exploración De Las Redes Virtuales De Azure"
category:: #articles
url:: https://learn.microsoft.com/es-es/training/modules/introduction-to-azure-virtual-networks/2-explore-azure-virtual-networks

- Highlights first synced by [[Readwise]] [[Saturday, 24-12-2022]]
	- -
		- Las redes virtuales de Azure (VNets) son el bloque de creación fundamental de la red privada en Azure. Las redes virtuales permiten crear redes virtuales complejas similares a una red local, con las ventajas adicionales de la infraestructura de Azure, como la escalabilidad, la disponibilidad y el aislamiento. Una red virtual es una representación de su propia red en la nube. Es un aislamiento lógico de la nube de Azure dedicada a su suscripción. Puede usar las redes virtuales para aprovisionar y administrar redes privadas virtuales (VPN) en Azure y, opcionalmente, vincular las redes virtuales con otras redes virtuales en Azure o con sus infraestructura de TI local para crear soluciones híbridas o entre entornos. Cada red virtual que se crea tiene su propio bloque CIDR y se puede vincular a otras redes locales y redes virtuales, siempre que los bloques CIDR no se superpongan. También tiene el control de la configuración del servidor DNS para redes virtuales y de la segmentación de la red virtual en subredes. #flashcard
		  id:: 63aac1bd-bb24-4d37-9d04-77e2bc9209eb
		- ([View Highlight](https://read.readwise.io/read/01gn1vhamkqkxfk3emea1y0tgg))
	- -
	- -
		- **Comunicación entre los recursos de Azure.** Hay tres mecanismos clave a través de los cuales el recurso de Azure puede comunicarse: redes virtuales, puntos de conexión de servicio de red virtual y emparejamiento de redes virtuales. Las redes virtuales no solo pueden conectar máquinas virtuales, sino también otros recursos de Azure, como App Service Environment, Azure Kubernetes Service y conjuntos de escalado de máquinas virtuales de Azure. Los puntos de conexión de servicio se pueden usar para conectarse a otros tipos de recursos de Azure, como cuentas de almacenamiento y bases de datos de Azure SQL. Cuando se crea una red virtual, los servicios y las máquinas virtuales de la red virtual pueden comunicarse de forma directa y segura entre ellas en la nube. #flashcard
		  id:: 63aac1bd-bf0a-42b3-8b16-0fd85bf9966b
		- ([View Highlight](https://read.readwise.io/read/01gn1vpnfgmf1cdrby6a55344a))
	- -
	- -
		- **Enrutamiento del tráfico de red.** De forma predeterminada Azure enruta el tráfico entre subredes, redes virtuales conectadas, redes locales e Internet. Puede implementar tablas de rutas o rutas del protocolo de puerta de enlace de borde (BGP) para invalidar las rutas predeterminadas que crea Azure. #flashcard
		  id:: 63aac1bd-2d68-48b0-9783-2afcb83975fe
		- ([View Highlight](https://read.readwise.io/read/01gn1vv1bmefgtknfkh1x7mb9j))
	- -
	- -
		- Una subred es un intervalo de direcciones IP de la red virtual. Puede segmentar redes virtuales en subredes de diferentes tamaños y crear tantas subredes como necesite para la organización y la seguridad dentro del límite de la suscripción. A continuación, puede implementar los recursos de Azure en una subred específica. Al igual que en una red tradicional, las subredes permiten segmentar el espacio de direcciones de red virtual en segmentos que sean adecuados para la red interna de la organización. Esto también mejora la eficacia de la asignación de dirección. La subred IPv4 más pequeña admitida es /29 y la más grande es /2 (con definiciones de subred CIDR). Las subredes IPv6 deben tener un tamaño exactamente de /64. Al planear la implementación de subredes, debe tener en cuenta lo siguiente: #flashcard
		  id:: 63aac1bd-87f0-4864-b94c-eaa0e7a36edf
		- ([View Highlight](https://read.readwise.io/read/01gn1w033kzr2y8k0w1wvstkkj))
	- -
	- -
		- Aunque las subredes son la unidad más pequeña que puede crear a partir del direccionamiento IP, puede segmentar aún más la red mediante grupos de seguridad de red (NSG) para controlar el acceso a la subred. Cada grupo de seguridad de red contiene reglas que permiten o niegan el paso del tráfico hacia y desde los orígenes y destinos. #flashcard
		  id:: 63aac1bd-b3a6-474d-a968-cd8519071f17
		- ([View Highlight](https://read.readwise.io/read/01gn1w4t2yb66jwvgvp7w5n4cz))
	- -