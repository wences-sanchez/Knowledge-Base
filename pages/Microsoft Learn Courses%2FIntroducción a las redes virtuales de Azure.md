tags:: [[Microsoft Learn Courses]], [[Azure]], [[cloud]]
deck:: [[Cloud Learning::Azure::Practical Skills::Introducción a las redes virtuales de Azure]]

-
- ## Tareas
	- DOING Introducción a las redes virtuales de Azure (1h 18min.) {{renderer :todomaster}}
	  :LOGBOOK:
	  CLOCK: [2022-12-24 Sat 11:07:29]--[2022-12-24 Sat 11:12:27] =>  00:04:58
	  CLOCK: [2022-12-24 Sat 11:40:14]
	  :END:
		- DONE Introducción (1 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-24 Sat 11:07:31]--[2022-12-24 Sat 11:08:11] =>  00:00:40
		  :END:
		- DOING Exploración de las redes virtuales de Azure (11 min.)
		  :LOGBOOK:
		  CLOCK: [2022-12-24 Sat 11:08:14]--[2022-12-24 Sat 11:12:08] =>  00:03:54
		  CLOCK: [2022-12-24 Sat 11:40:16]
		  :END:
		- TODO Configurar servicios de IP pública (8 min.)
		- TODO Diseño e implementación de una red virtual en Azure (7 min.) #Labs
		- TODO Diseño de la resolución de nombres para la red virtual (10 min.)
		- TODO Configuración de lso servidores de nombres de dominio en Azure (7 min.) #Labs
		- TODO Habilitación de la conectividad entre redes virtuales con emparejamiento (6 min.)
		- TODO Conexión de dos redes virtuales de Azure mediante el emparejamiento de red virtual global (5 min.) #Labs
		- TODO Implementación del enrutamiento del tráfico de redes virtuales (16 min.)
		- TODO Configuración del acceso a Internet con Azure Virtual NAT (6 min.)
		- TODO Resumen (1 min.)
		-
-
- ## Introducción
-
- ## Exploración de las redes virtuales de Azure
	- Las redes virtuales de Azure (VNets) son el bloque de creación fundamental de la red privada en Azure. Las redes virtuales permiten crear redes virtuales complejas similares a una red local, con las ventajas adicionales de la infraestructura de Azure, como la escalabilidad, la disponibilidad y el aislamiento. Una red virtual es una representación de su propia red en la nube. Es un aislamiento lógico de la nube de Azure dedicada a su suscripción. Puede usar las redes virtuales para aprovisionar y administrar redes privadas virtuales (VPN) en Azure y, opcionalmente, vincular las redes virtuales con otras redes virtuales en Azure o con sus infraestructura de TI local para crear soluciones híbridas o entre entornos. Cada red virtual que se crea tiene su propio bloque CIDR y se puede vincular a otras redes locales y redes virtuales, siempre que los bloques CIDR no se superpongan. También tiene el control de la configuración del servidor DNS para redes virtuales y de la segmentación de la red virtual en subredes.
	-
	-