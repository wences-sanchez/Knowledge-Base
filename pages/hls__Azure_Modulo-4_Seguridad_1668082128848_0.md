file-path:: ../assets/Azure_Modulo-4_Seguridad_1668082128848_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-4]]
tags:: UNIR, Azure, PDFs

-
- ## Tema 1: Características de Azure Security
-
	- {{cloze Azure Security Center}} es un sistema de gestión de seguridad de infraestructura unificada que refuerza la posición de seguridad de sus centros de datos y ofrece una protección contra amenazas muy avanzada, tanto para cargas de trabajo híbridas en la nube (estén o no en Azure), como en centros de datos locales. Azure ofrece este sistema como servicio dentro de su oferta. #flashcard
	  hl-page:: 3
	  ls-type:: annotation
	  id:: 636cea2b-f171-4f54-9057-8cebf3589e19
	  hl-color:: yellow
-
	- ¿Cuáles son las **funcionalidades** de Azure Security Center? #flashcard
	  hl-page:: 4
	  ls-type:: annotation
	  id:: 636cea48-e020-4927-957c-3560c31520dd
	  hl-color:: yellow
		-  **Cumplimiento de directivas**. Security Center se sustenta sobre los controles de Azure Policy para que el usuario pueda configurar y supervisar sus directivas de forma que se ejecuten en grupos de administración, entre suscripciones e incluso para una organización completa.
		-  **Alertas de seguridad**. Security Center recopila, analiza e integra de forma automática datos registrados de los recursos de Azure, como la protección de puntos de conexión o firewall, para poder detectar amenazas reales. Con ello es posible mostrar la lista de alertas de seguridad priorizadas en Security Center junto con la información necesaria para investigar y remediar rápidamente cualquier ataque.
		-  **Puntuación (scoring) de seguridad**. Security Center evalúa continuamente los recursos en busca de problemas de seguridad y posteriormente agrega todos los resultados en una única puntuación para que el usuario pueda conocer realmente su nivel de seguridad actual.
		-  **Protección de seguridad de recursos**. Permitiendo la visibilidad de la seguridad y recomendaciones por recurso.
		-
	- ¿Cuáles son las principales capacidades de Azure Security Center? #flashcard
	  hl-page:: 4
	  ls-type:: annotation
	  id:: 636cea55-5212-42f2-b9d0-46595e069762
	  hl-color:: yellow
		-  **Cumplimiento de directivas**. Permitiendo ejecutar directivas en grupos de administración, suscripciones u organizaciones.
		-  **Evaluaciones continuas**. Con el fin de asegurar que tanto los nuevos recursos como los ya implementados están configurados correctamente.
		-  **Recomendaciones personalizadas** basadas en cargas de trabajo reales con instrucciones sobre cómo implementarlas.
		-  **Protección contra amenazas** mediante el análisis de los intentos de amenazas mediante alertas e informes de recursos afectados. Azure Security Center está integrado con Azure Advisor para que este último servicio pueda presentar la información relativa a seguridad y así prevenir potenciales ataques
		-
	- {{cloze Azure Sentinel}} es una solución de gestión de la información de seguridad (Security Information and Event Management, SIEM) y de respuesta automatizada de seguridad (**Security Orchestration, Automation and Response, SOAR**) que brinda análisis e inteligencia contra amenazas a nivel empresarial. #flashcard
	  hl-page:: 5
	  ls-type:: annotation
	  id:: 636cea64-93a8-487d-bc98-c7212e96eb7c
	  hl-color:: yellow
-
	- ¿Cuáles son las principales funcionalidades de Azure Sentinel? #flashcard
	  hl-page:: 5
	  ls-type:: annotation
	  id:: 636cea6d-ab2a-4af9-88ef-d3bbe1e4b071
	  hl-color:: yellow
		-  Recopilar datos de todos los usuarios, dispositivos, aplicaciones e infraestructuras, tanto locales como en diferentes nubes.
		-  Detectar amenazas y disminuir los falsos positivos mediante análisis.
		-  Investigar amenazas con inteligencia artificial y rastrear actividades sospechosas a escala.
		-  Responder ante incidentes con la organización y la automatización integradas de tareas comunes.
		-
	- {{cloze Azure Key Vault}} almacena los secretos de las aplicaciones en una ubicación centralizada en la nube y sirve para controlar de forma segura los permisos de acceso y el registro de acceso. Sus principales funcionalidades son: #flashcard
	  hl-page:: 6
	  ls-type:: annotation
	  id:: 636cea9d-04fc-4225-a0fe-ee21945b7143
	  hl-color:: yellow
		-  Administración de secretos.
		-  Administración de claves.
		-  Administración de certificados.
		-  Almacenamiento de secretos respaldados por módulos de seguridad de hardware(HSM).
-
	- El servicio Host dedicado de Azure proporciona servidores físicos que alojan una o varias máquinas virtuales y está dirigido a una única suscripción de Azure. Azure provee el servicio con los mismos servidores físicos con los que proporciona recursos desde sus centros de datos.
	  hl-page:: 6
	  ls-type:: annotation
	  id:: 636ceaae-37c7-40b7-af90-49978781ece1
	  hl-color:: yellow
		- Es posible aprovisionar hosts dedicados dentro de una región, zona de disponibilidad y dominio de error, de modo que se pueden ejecutar máquinas virtuales directamente en sus hosts dedicados en la configuración que mejor se adapte a las necesidades del cliente.
		- Los beneficios que reporta su uso son:
			-  **Aislamiento de hardware a nivel de servidor**. Esto significa que no se colocarán otras máquinas virtuales en estos hosts. Los hosts dedicados comparten la misma red y la misma infraestructura de almacenamiento subyacente que otros hosts no aislados.
			-  **Control sobre** la programación de **eventos de mantenimiento**.
			-  Alineado con las **ventajas híbridas de Azure**. Con ello el cliente puede aportar sus propias licencias de Windows y SQL.
		- La **limitación** de este servicio es que **no permite** utilizar **conjuntos de escalado de máquinas virtuales**.
-
- ## Tema 2: Conectividad de red segura
	-
	- Los **grupos de seguridad de red** (Network Security Groups, NSG) filtran el tráfico de red hacia y desde los recursos de Azure en redes virtuales de Azure. Sus principales características son: #flashcard
	  hl-page:: 10
	  ls-type:: annotation
	  id:: 636e0d76-8fe3-4492-9b92-78cc26b4b342
	  hl-color:: yellow
		-  Permiten **establecer reglas de entrada y salida** para filtrar por **dirección IP**, puerto y **protocolo** de **origen** y **destino**.
		-  Se pueden añadir **varias reglas**, según sea necesario, dentro de los límites de la suscripción.
		-  Azure aplica las **reglas de seguridad predeterminadas** de línea de base a los **nuevos** NSG.
		-  Las reglas de **mayor prioridad anulan** las reglas **predeterminadas**.
-
	- Los grupos de seguridad de aplicaciones (Applications Security Groups) permiten configurar la seguridad de red como una extensión natural de la estructura de una aplicación. Sus principales características son: #flashcard
	  hl-page:: 11
	  ls-type:: annotation
	  id:: 636e0d98-5507-491b-af07-14713bca9d00
	  hl-color:: yellow
		-  Permiten agrupar máquinas virtuales y directivas de seguridad de red basadas en esos grupos.
		-  Se pueden reutilizar las directivas de seguridad a escala sin necesidad de modificar manualmente direcciones IP.
		- Con grupos de seguridad de aplicaciones se pueden habilitar o denegar determinados tráficos desde y hacia las interfaces de red pertenecientes al ASG.
	-
	- **Azure Firewall** es un Firewall como servicio (FaaS) con estado y administrado que permite o deniega el acceso a los servidores en función de la dirección IP de origen para proteger los recursos de la red. Sus principales características son: #flashcard
	  hl-page:: 11
	  ls-type:: annotation
	  id:: 636e0db8-b49b-43f9-8df4-f3eafca03291
	  hl-color:: yellow
		-  Permite aplicar reglas de filtrado de tráfico de entrada y de salida.
		-  Alta disponibilidad.
		-  Escalabilidad ilimitada que aporta la nube.
		-  Utiliza el registro de Azure Monitor.
		- Por otro lado, Azure también ofrece un servicio de firewall de aplicaciones web (Web Application Firewall, WAF) denominado Azure Application Gateway. Este servicio de WAF ofrece una protección centralizada del tráfico entrante para aplicaciones web.
	-
	- Los ataques DDoS saturan y agotan los recursos de la red, motivando que las aplicaciones vayan lentas o bien dejen de responder. La protección contra DDoS en Azure corrige el tráfico de red no deseado antes de que afecte a la disponibilidad del servicio. Azure DDoS Protection proporciona dos niveles de servicio: #flashcard
	  hl-page:: 12
	  ls-type:: annotation
	  id:: 636e0de0-253a-4848-8661-e022bd5a4faf
	  hl-color:: yellow
		-  **Básico**, que está habilitado automáticamente sin coste como parte de la suscripción. Garantiza que la infraestructura de Azure no se vea afectada por un ataque DDoS a gran escala.
		-  **Estándar**, que ofrece El nivel de servicio estándar añade capacidades de mitigación, ajustadas para proteger los recursos de Azure Virtual Network. Ambas modalidades proporcionan supervisión continua del tráfico y mitigación en tiempo real de los ataques a nivel de red más comunes.
		- [:span]
		  ls-type:: annotation
		  hl-page:: 12
		  hl-color:: yellow
		  id:: 636e0f4f-89a2-435c-87e8-e55025349317
		  hl-type:: area
		  hl-stamp:: 1668157262988
	- Los tipos de ataques que ayuda a evitar DDoS Protection son: #flashcard
	  hl-page:: 13
	  ls-type:: annotation
	  id:: 636e0df5-34d9-4757-81f9-6ca74b15a8c7
	  hl-color:: yellow
		-  Ataques volumétricos, cuyo objetivo es desbordar la capa de red con una gran cantidad de tráfico aparentemente legítimo.
		-  Ataques de protocolo que vuelven un destino inaccesible al aprovechar una vulnerabilidad en la pila de protocolo de capa 3 y 4.
		-  Ataques a nivel de recurso (nivel de aplicación) aplicaciones web para interrumpir la transmisión de datos entre hosts. Para la defensa contra este tipo de ataque DDoS Protection estándar requiere un firewall de aplicaciones web (WAF).