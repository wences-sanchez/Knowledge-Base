file-path:: ../assets/Azure_Modulo-4_Seguridad_1668082128848_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-4]]
tags:: UNIR, Azure, PDFs

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
	- Es posible aprovisionar hosts dedicados dentro de una región, zona de disponibilidad y dominio de error, de modo que se pueden ejecutar máquinas virtuales directamente en sus hosts dedicados en la configuración que mejor se adapte a las necesidades del cliente. Los beneficios que reporta su uso son: Aislamiento de hardware a nivel de servidor. Esto significa que no se colocarán otras máquinas virtuales en estos hosts. Los hosts dedicados comparten la misma red y la misma infraestructura de almacenamiento subyacente que otros hosts no aislados. Control sobre la programación de eventos de mantenimiento. Alineado con las ventajas híbridas de Azure. Con ello el cliente puede aportar sus propias licencias de Windows y SQL. La limitación de este servicio es que no permite utilizar conjuntos de escalado de máquinas virtuales.