file-path:: ../assets/Azure_Modulo-2_Servicios-principales-de-Azure_1667895294380_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-2]]
tags:: UNIR, Azure

-
- # Tema 2: Productos principales de carga de trabajo de Azure
-
	- ## 2.3 Servicios de computación
-
	- Las {{cloze máquinas virtuales (Virtual Machines)}} son emulaciones de software de equipos físicos. Incluyen procesadores virtuales, memoria, almacenamiento y redes. Forma parte de la oferta de IaaS, lo que proporciona al usuario un control y personalización total. #flashcard
	  hl-page:: 16
	  ls-type:: annotation
	  id:: 636a12a6-ac82-44a2-99e9-75c96f307016
	  hl-color:: yellow
-
	- El servicio de {{cloze aplicaciones de Azure (Azure App Services)}} es una plataforma totalmente administrada para crear, implementar y escalar aplicaciones web y API rápidamente. Forma parte de la oferta de PaaS, lo que permite al usuario abstraerse de la infraestructura subyacente y satisface requisitos de cumplimiento, seguridad y rendimiento de nivel empresarial. #flashcard
	  hl-page:: 17
	  ls-type:: annotation
	  id:: 636a12b9-485c-4beb-bf97-58965d02339b
	  hl-color:: yellow
-
	- El servicio {{cloze de contenedores de Azure}} ofrece un entorno virtualizado ligero que no requiere administración del sistema operativo y puede responder a los cambios bajo demanda. #flashcard
	  hl-page:: 18
	  ls-type:: annotation
	  id:: 636a12ca-9b33-401c-8407-29769435be99
	  hl-color:: yellow
-
	- Azure ofrece actualmente dos servicios de contenedores: #flashcard
	  hl-page:: 18
	  ls-type:: annotation
	  id:: 636a12f3-658d-488e-aefb-8fe10650f831
	  hl-color:: yellow
		-  **Azure Container Instances**: oferta de PaaS que ejecuta un contenedor en Azure sin la necesidad de administrar una máquina virtual o servicios adicionales.
		-  **Azure Kubernetes Service:** servicio de completo para la ejecución de contenedores con arquitecturas distribuidas y grandes volúmenes de contenedores.
		-
	- El servicio {{cloze de escritorio virtual Windows (Windows Virtual Desktop)}} permite la virtualización de aplicaciones y escritorios Windows que se ejecutan en la nube. #flashcard
	  hl-page:: 18
	  ls-type:: annotation
	  id:: 636a1319-9818-40c2-9c14-6436a4faa241
	  hl-color:: yellow
-
	- ## 2.4 Servicios de redes
-
	- {{cloze Azure Virtual Network (VNet) que}} permite que los recursos de Azure se comuniquen entre sí, con Internet y con redes locales. #flashcard
	  hl-page:: 19
	  ls-type:: annotation
	  id:: 636a136f-7e9a-44af-bb0b-e71f564f04d3
	  hl-color:: yellow
-
	- {{cloze Balanceador de carga (Azure Load Balancer) que}} permite habilitar alta disponibilidad y modular el rendimiento de red de las aplicaciones. #flashcard
	  hl-page:: 20
	  ls-type:: annotation
	  id:: 636a137a-6fc6-4f9e-aa99-63d623851f3d
	  hl-color:: yellow
-
	- {{cloze Pasarela de aplicaciones/firewall de aplicaciones web (Application Gateway/WAF) que}} permite construir frontales web escalables y altamente disponibles. #flashcard
	  hl-page:: 20
	  ls-type:: annotation
	  id:: 636a1380-df26-44e8-991e-36fbdadbe7b8
	  hl-color:: yellow
-
	- Protección contra ataques distribuidos de denegación de servicio (DDoS Protection) que permite proteger los recursos de Azure contra este tipo de ataques.
	  hl-page:: 20
	  ls-type:: annotation
	  id:: 636a1384-bc4b-49d6-9813-c2784f6ab9f9
	  hl-color:: yellow
-
	- {{cloze Pasarela de red privada virtual (Virtual Private Network Gateway, VPN Gateway)}} que se usa para enviar tráfico cifrado entre una red virtual de Azure y una ubicación local a través de Internet público. #flashcard
	  hl-page:: 20
	  ls-type:: annotation
	  id:: 636a138b-4801-4b9d-ae60-b32b02b280e9
	  hl-color:: yellow
-
	- {{cloze Azure Express Route (ER)}} que extiende las redes locales a Azure a través de una conexión privada que facilita un proveedor de conectividad. #flashcard
	  hl-page:: 20
	  ls-type:: annotation
	  id:: 636a13a4-4cfa-4547-97e9-0901334b0808
	  hl-color:: yellow
-
	- Los servicios de almacenamiento de Azure proporcionan diferentes niveles de acceso que conviene conocer: #flashcard
	  hl-page:: 22
	  ls-type:: annotation
	  id:: 636a14bf-e4d7-4abf-a494-7fc96e3596eb
	  hl-color:: yellow
		-  **Frecuente**: Optimizado para almacenar datos a los que se accede con frecuencia.
		-  **Poco frecuente**: Optimizado para almacenar datos a los que se accede con poca frecuencia y se almacenan durante **al menos 30 días**.
		-  **Optimizado** para almacenar datos a los que rara vez se accede y se almacenan durante **al menos 180 días** con **requisitos de latencia flexibles**.
-
	- El servicio {{cloze Instancia administrada de Azure SQL (Azure SQL Managed Instance)}} permite a los clientes de SQL Server subir y trasladar sus aplicaciones locales a la nube con cambios mínimos en las aplicaciones y en la base de datos. Presenta las características siguientes: #flashcard
	  hl-page:: 24
	  ls-type:: annotation
	  id:: 636a151b-88a5-4f2c-b9de-73c7687de9ed
	  hl-color:: yellow
		-  Plataforma como servicio (PaaS) totalmente administrada y permanentemente disponible.
		-  Conserva todas las capacidades de una PaaS (parches automáticos y actualizaciones de versiones, copias de seguridad automáticas y alta disponibilidad).
		-  El cliente puede intercambiar sus licencias existentes por tarifas con descuento en SQL Managed Instance mediante la ventaja híbrida de Azure.
-
- # Tema 1: Componentes arquitectónicos principales de Azure
	- ## 1.3 Regiones
		- El término {{cloze región}} corresponde con la zona geográfica en la que Azure tiene presencia física (mediante uno o varios centros de datos conectados por redes de baja latencia) y por tanto puede ofrecer servicios con una baja latencia a los clientes en dicha zona. Las características principales de una región son: #flashcard
		  hl-page:: 3
		  ls-type:: annotation
		  id:: 636a1dba-0b79-4fcd-b7f5-1140171ab65e
		  hl-color:: yellow
			- [:span]
			  ls-type:: annotation
			  hl-page:: 4
			  hl-color:: yellow
			  id:: 636a1e34-acea-4ecf-b7d8-ad84cf8756f4
			  hl-type:: area
			  hl-stamp:: 1667898931758
			-  Están compuestas de uno o más centros de datos próximos.
			  hl-page:: 4
			  ls-type:: annotation
			  id:: 636a1e6f-c7e2-4ea6-aec7-972c2b8c0ad9
			  hl-color:: yellow
			-  Proporcionan flexibilidad y capacidad de adaptación para reducir la latencia de los clientes.
			-  Permiten conservar la residencia de los datos de forma que se aseguren los requerimientos de cumplimiento normativo.
	- ## 1.4 Regiones especiales
		- Existen una serie de regiones especiales que Azure denomina {{cloze geografías}}, que dan servicio a una serie de mercados especiales y preservan la residencia de los datos y los límites de cumplimiento. Ello permite que clientes con necesidades específicas de residencia y cumplimiento de datos mantengan sus datos y aplicaciones muy cerca. #flashcard
		  hl-page:: 4
		  ls-type:: annotation
		  id:: 636a1e7f-4ed3-4af1-b85d-6f6e7a9bf457
		  hl-color:: yellow
-
	- ## 1.5 Opciones de disponibilidad
		- Azure ofrece a los usuarios diferentes opciones para conseguir una alta disponibilidad y recuperación ante desastres. Las opciones posibles son: #flashcard
		  hl-page:: 5
		  ls-type:: annotation
		  id:: 636a1e8b-b8c1-466c-bac8-2615cae6f494
		  hl-color:: yellow
			-  **Zonas de disponibilidad (Availability Zones)** que brindan protección contra fallos completos del centro de datos.
			- ** Conjuntos de disponibilidad (Availability Sets)** para poder mantener las aplicaciones disponibles durante ventanas de mantenimiento o ante errores de hardware.
			-  **Pares de regiones** que permiten una protección regional sin salir de los límites de residencia de datos.
		-
		- Las {{c1 zonas de disponibilidad (Availability Zones)}} actúan como límites de aislamiento de la infraestructura de nuestras aplicaciones. Funcionan de modo que, si una {{c1 zona de disponibilidad}} se desactiva, las otras siguen funcionando. Se caracterizan por: #flashcard
		  hl-page:: 6
		  ls-type:: annotation
		  id:: 636a1e9c-6bf0-48b1-a4e9-b3558d6b550e
		  hl-color:: yellow
			-  Proporcionar protección contra el tiempo de inactividad debido a errores del centro de datos.
			-  Pertenecer a centros de datos separados físicamente dentro de una misma región.
			-  Cada centro de datos está equipado con redes, alimentación y refrigeración independientes.
			-  Cuentan con conexiones de red privadas de fibra óptica para alta disponibilidad y replicación de baja latencia.
		- Conjuntos de disponibilidad #flashcard
		  hl-page:: 7
		  ls-type:: annotation
		  id:: 636a1ea6-2f61-41c4-8351-ae5ee46ad9d6
		  hl-color:: yellow
			- Los conjuntos de disponibilidad permiten mantener las aplicaciones disponibles durante ventanas de mantenimiento o ante errores de hardware. Se componen de:
				-  **Dominios de actualización (Update Domains, UD)**, de modo que las operaciones de mantenimiento programado, actualizaciones por cuestiones de rendimiento o seguridad se secuencian a través de os dominios de actualización.
				-  **Dominios de error (Fault Domains, FD)**, que proporcionan separación física de cargas de trabajo distribuidas a través del hardware del centro de datos.
		- Pares de regiones #flashcard
		  hl-page:: 7
		  ls-type:: annotation
		  id:: 636a1eb2-bd12-48b8-a27a-543d6f7f773c
		  hl-color:: yellow
			- Azure agrupa sus regiones en pares con la finalidad de conseguir beneficios relacionados con la recuperación ante desastres.
			- Los pares de regiones se caracterizan por lo siguiente:
				-  Entre pares de regiones existe al menos 300 millas (unos 482 Km) de separación.
				-  Replicación automática para algunos servicios.
				-  Se prioriza la recuperación de una región en caso de interrupción.
				-  Las actualizaciones se implementan secuencialmente para minimizar el tiempo de inactividad
	- ## 1.6 Recursos de Azure
		- Los recursos de Azure son componentes que permite crear soluciones informáticas en la nube. Los principales son: #flashcard
		  hl-page:: 8
		  ls-type:: annotation
		  id:: 636a1ec7-e175-4076-a978-7c3512905661
		  hl-color:: yellow
			-  Máquinas virtuales (Virtual Machines).
			-  Cuentas de almacenamiento (Storage Accounts).
			-  Redes virtuales (Virtual Networks).
			-  Servicios gestionados de aplicaciones (App Services).
			-  Bases de datos SQL (SQL Database).
			-  Funciones (Azure Functions).
	- ## 1.7 Suscripciones de Azure
		- Una suscripción de Azure (Azure Subscription) proporciona acceso autenticado y autorizado a las cuentas de Azure. Una cuenta puede tener una o varias suscripciones, como se observa en el ejemplo de la figura siguiente: #flashcard
		  ls-type:: annotation
		  hl-page:: 11
		  hl-color:: yellow
		  id:: 636a1f21-ead4-4970-9df0-908d2a4b5314
			- [:span]
			  ls-type:: annotation
			  hl-page:: 11
			  hl-color:: yellow
			  id:: 636a1f2c-6873-4e7a-9e44-ed011629f166
			  hl-type:: area
			  hl-stamp:: 1667899179781