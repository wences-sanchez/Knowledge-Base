tags:: [[Microsoft Learn Courses]], [[Azure]], [[cloud]]
deck:: [[Cloud Learning::Azure::Practical Skills::Introducción a las redes virtuales de Azure]]

-
- ## Tareas
	- DOING Introducción a las redes virtuales de Azure (1h 18min.) {{renderer :todomaster}}
	  :LOGBOOK:
	  CLOCK: [2022-12-24 Sat 11:07:29]--[2022-12-24 Sat 11:12:27] =>  00:04:58
	  CLOCK: [2022-12-24 Sat 11:40:14]--[2022-12-24 Sat 11:59:36] =>  00:19:22
	  CLOCK: [2022-12-26 Mon 10:21:43]--[2022-12-26 Mon 12:09:08] =>  01:47:25
	  CLOCK: [2022-12-26 Mon 12:40:47]
	  :END:
		- DONE Introducción (1 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-24 Sat 11:07:31]--[2022-12-24 Sat 11:08:11] =>  00:00:40
		  :END:
		- DONE Exploración de las redes virtuales de Azure (11 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-24 Sat 11:08:14]--[2022-12-24 Sat 11:12:08] =>  00:03:54
		  CLOCK: [2022-12-24 Sat 11:40:16]--[2022-12-24 Sat 11:59:34] =>  00:19:18
		  :END:
		- DONE Configurar servicios de IP pública (8 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 10:21:45]--[2022-12-26 Mon 10:30:19] =>  00:08:34
		  :END:
		- DONE Diseño e implementación de una red virtual en Azure (7 min.) #Labs
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 10:30:31]--[2022-12-26 Mon 10:55:46] =>  00:25:15
		  :END:
		- DONE Diseño de la resolución de nombres para la red virtual (10 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 10:57:07]--[2022-12-26 Mon 11:08:07] =>  00:11:00
		  :END:
		- DONE Configuración de lso servidores de nombres de dominio en Azure (7 min.) #Labs
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 11:08:18]--[2022-12-26 Mon 12:09:00] =>  01:00:42
		  :END:
		- DONE Habilitación de la conectividad entre redes virtuales con emparejamiento (6 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 12:40:44]--[2022-12-26 Mon 12:49:51] =>  00:09:07
		  :END:
		- DONE Conexión de dos redes virtuales de Azure mediante el emparejamiento de red virtual global (5 min.) #Labs
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 12:49:55]--[2022-12-26 Mon 12:58:10] =>  00:08:15
		  :END:
		- DONE Implementación del enrutamiento del tráfico de redes virtuales (16 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 12:58:19]--[2022-12-26 Mon 13:09:22] =>  00:11:03
		  :END:
		- DOING Configuración del acceso a Internet con Azure Virtual NAT (6 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-26 Mon 13:09:25]
		  :END:
		- TODO Resumen (1 min.)
		-
-
- ## Introducción
-
- ## Exploración de las redes virtuales de Azure
	- Las redes virtuales de Azure (VNets) son el bloque de creación fundamental de la red privada en Azure. Las redes virtuales permiten crear redes virtuales complejas similares a una red local, con las ventajas adicionales de la infraestructura de Azure, como la escalabilidad, la disponibilidad y el aislamiento. Una red virtual es una representación de su propia red en la nube. Es un aislamiento lógico de la nube de Azure dedicada a su suscripción. Puede usar las redes virtuales para aprovisionar y administrar redes privadas virtuales (VPN) en Azure y, opcionalmente, vincular las redes virtuales con otras redes virtuales en Azure o con sus infraestructura de TI local para crear soluciones híbridas o entre entornos. Cada red virtual que se crea tiene su propio bloque CIDR y se puede vincular a otras redes locales y redes virtuales, siempre que los bloques CIDR no se superpongan. También tiene el control de la configuración del servidor DNS para redes virtuales y de la segmentación de la red virtual en subredes.
	-
	- Comunicación entre los recursos de Azure. Hay tres mecanismos clave a través de los cuales el recurso de Azure puede comunicarse: redes virtuales, puntos de conexión de servicio de red virtual y emparejamiento de redes virtuales. Las redes virtuales no solo pueden conectar máquinas virtuales, sino también otros recursos de Azure, como App Service Environment, Azure Kubernetes Service y conjuntos de escalado de máquinas virtuales de Azure. Los puntos de conexión de servicio se pueden usar para conectarse a otros tipos de recursos de Azure, como cuentas de almacenamiento y bases de datos de Azure SQL. Cuando se crea una red virtual, los servicios y las máquinas virtuales de la red virtual pueden comunicarse de forma directa y segura entre ellas en la nube.
-
- ## Configurar servicios de IP pública
	-