id:: 637df55b-de1e-4f79-9e1b-8ff28edaf32c
deck:: [[Cloud Learning::Azure::Microsoft Learn Course]] 
tags:: Azure, Microsoft-Learn

-
- ## Describe Cost Management in Azure
  id:: 637df5fd-0dc0-43d1-991e-65d6ca060cbe
	- ### Comparación de las calculadoras de precios y costo total de propiedad #flashcard
	  id:: 637df848-cbc6-4d77-847e-0315be7dad6f
		- #### Calculadora de precios
			- La calculadora de precios está diseñada para proporcionarle un costo estimado para el aprovisionamiento de recursos en Azure. Puede obtener una estimación de recursos individuales, crear una solución o usar un escenario de ejemplo para ver una estimación del gasto de Azure. La calculadora de precios se centra en el costo de los recursos aprovisionados en Azure.
			- ![Captura de pantalla de la calculadora de precios para referencia.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-cost-management-azure/media/price-calculator-0a750ac3.png)
		- #### Calculadora de TCO
			- La calculadora de TCO está diseñada para ayudarle a comparar los costos de ejecución de una infraestructura local en comparación con una infraestructura en la nube de Azure. Con la calculadora de TCO, se especifica la configuración de infraestructura actual, incluidos los servidores, las bases de datos, el almacenamiento y el tráfico de red saliente. Después, la calculadora de TCO compara los costos previstos del entorno actual con un entorno de Azure que admite los mismos requisitos de infraestructura.
			- ![Captura de pantalla de la calculadora de Coste total de propiedad.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-cost-management-azure/media/total-cost-ownership-657fe344.png)
-
- ## Describe features and tools in Azure for Governance and Compliance
  id:: 637df651-0cbe-4c7c-895e-37a8b565531b
	- ### Descripción del propósito de Azure Blueprints #flashcard
	  id:: 637dff6b-5087-411f-baec-e051ccf86b47
		- Azure Blueprints le permite estandarizar las implementaciones de entorno o suscripción en la nube. En lugar de tener que configurar características como Azure Policy para cada nueva suscripción, con Azure Blueprints puede definir la configuración repetible y las directivas que se aplican a medida que se crean suscripciones. ¿Necesita un nuevo entorno de pruebas y desarrollo? Azure Blueprints permite implementar un nuevo entorno de pruebas y desarrollo con las opciones de seguridad y cumplimiento ya configuradas. De este modo, los equipos de desarrollo pueden crear e implementar rápidamente nuevos entornos sabiendo que se crean de acuerdo con los estándares organizativos.
	- ### Descripción del propósito de Azure Policy
		- #### ¿Qué son las iniciativas Azure Policy? #flashcard
		  id:: 637e00f5-6590-49c2-aebc-54c9eae0d9b6
			- Una iniciativa de Azure Policy es una forma de agrupar las directivas relacionadas. La definición de iniciativa contiene todas las definiciones de directiva para facilitar el seguimiento del estado de cumplimiento de cara a un objetivo mayor.
			- Por ejemplo, Azure Policy incluye una iniciativa denominada Habilitar la supervisión en Azure Security Center, Su objetivo es supervisar todas las recomendaciones de seguridad disponibles para todos los tipos de recursos de Azure en Azure Security Center.
			- En esta iniciativa se incluyen las siguientes definiciones de directiva:
				- **Supervisar base de datos SQL sin cifrar en Security Center:** esta directiva supervisa servidores y bases de datos SQL sin cifrar.
				- **Supervisión de los puntos vulnerables del sistema operativo en Security Center:** esta directiva supervisa los servidores que no cumplen la línea base de la vulnerabilidad del sistema operativo configurada.
				- **Supervisar la falta de Endpoint Protection en Security Center:** esta directiva supervisa los servidores que no tienen instalado un agente de Endpoint Protection.
			- La iniciativa Habilitar la supervisión en Azure Security Center 
			  contiene más de 100 definiciones de directiva independientes, de hecho.
- ## Describe features and tools for Managing and Deploying Azure resources
  id:: 637df670-a5ca-4a7e-9014-89c6ee61de66
	- ### Descripción del propósito de Azure Arc #flashcard
	  id:: 637e04f4-6f23-46ae-8481-b973fd9d9d43
		- La administración de entornos híbridos y de varias nubes puede complicarse rápidamente. Azure proporciona una serie de herramientas para aprovisionar, configurar y supervisar recursos de Azure. ¿Qué ocurre con los recursos locales en una configuración híbrida o los 
		  recursos de nube en una configuración de varias nubes?
		- Al usar Azure Resource Manager (ARM), Arc le permite ampliar el cumplimiento y la supervisión de Azure a las configuraciones híbridas y de varias nubes. Azure Arc simplifica el gobierno y la administración al ofrecer una plataforma de administración local y multinube coherente.
	- ### Descripción de las plantillas de Azure Resource Manager y Azure ARM #flashcard
	  id:: 637e05d9-461b-41e6-bfd8-db6181e515a2
		- Azure Resource Manager (ARM) es el servicio de implementación y administración de Azure. Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos de la cuenta de Azure. Cada vez que haga algo con los recursos de Azure, ARM está implicado.
		- Cuando un usuario envía una solicitud de cualquiera de las herramientas, API o SDK de Azure, ARM la recibe. ARM autentica y autoriza la solicitud. Después, ARM envía la solicitud al servicio de Azure, que lleva a cabo la acción solicitada. Verá resultados y funcionalidades coherentes en todas las herramientas, ya que todas las solicitudes se controlan mediante la misma API.
- ## Describe monitoring tools in Azure
  id:: 637df68c-8293-4ae9-9a0f-91eb6e63ff72
	- ### Descripción del propósito de Azure Advisor #flashcard
	  id:: 637df6a1-6442-42ca-bec8-2fa0303233bc
		- Azure Advisor evalúa los recursos de Azure y hace recomendaciones que contribuyen a mejorar la confiabilidad, la seguridad y el rendimiento, lograr la excelencia operativa y reducir los costos. Azure Advisor está diseñado para ayudarle a ahorrar tiempo en la optimización en la nube. El servicio de recomendaciones sugiere medidas que puede adoptar de inmediato, posponer o descartar.
		- Las recomendaciones se dividen en cinco categorías:
			- La **fiabilidad** se usa para garantizar y mejorar la continuidad de las aplicaciones críticas para la empresa.
			- La **seguridad** se usa para detectar amenazas y vulnerabilidades que podrían conducir a vulneraciones de la seguridad.
			- El **rendimiento** se usa para mejorar la velocidad de las aplicaciones.
			- La **excelencia operativa** se usa para aumentar la eficiencia de procesos y flujos de trabajo, mejorar la administración de recursos y obtener procedimientos recomendados para la implementación.
			- El **costo** se usa para optimizar y reducir el gasto general de Azure.
	- ### Descripción de Azure Service Health #flashcard
	  id:: 637e07de-5d73-446f-ba89-6f7874184a33
		- Azure Service Health le permite realizar un seguimiento de los recursos de Azure, tanto los recursos implementados específicamente como el estado general de Azure.
		- Azure Service Health lo hace combinando tres servicios de Azure diferentes:
			- **Estado de Azure** es una visión general del estado de Azure de forma global. Estado de Azure informa de las interrupciones de servicio en Azure en la página de estado de Azure . La página es una vista global del estado de todos los servicios y regiones de Azure. Es una buena referencia de los incidentes con un impacto generalizado.
			- **Service Health** proporciona una vista más limitada del estado de los servicios y regiones de Azure. Se centra en los servicios y regiones de Azure que usa. Es el mejor lugar para buscar comunicaciones que afecten a los servicios relativas a interrupciones, actividades de mantenimiento planeado y otros avisos de mantenimiento, ya que tras la autenticación, Service Health conoce los servicios y recursos que usa en la actualidad. Incluso puede configurar las alertas de Service Health para que le envíen notificaciones cuando se produzcan problemas del servicio, mantenimientos planeados o cualquier otro cambio que pueda afectar a los servicios y regiones de Azure que usa.
			- **Resource Health** es una vista personalizada de los recursos reales de Azure. Proporciona información sobre el estado de los recursos en la nube individuales, como una instancia de máquina virtual concreta. Mediante Azure Monitor también puede configurar alertas que le notifiquen los cambios de disponibilidad de los recursos en la nube.
	- ### Descripción de Azure Monitor #flashcard
	  id:: 637e0772-1ab4-4b02-b3f7-84bab0e9735f
		- Azure Monitor es una plataforma para recopilar datos sobre los recursos, analizar esos datos, visualizar la información e incluso actuar en función de los resultados. Azure Monitor puede supervisar los recursos de Azure, los recursos locales e incluso los recursos de varias nubes, como las máquinas virtuales hospedadas con otro proveedor de nube.
		- ![Ilustración en la que se muestra el flujo de información que usa Azure Monitor para proporcionar supervisión y visualización de datos.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-monitoring-tools-azure/media/azure-monitor-overview-614cd2fd.svg)
		- #### Application Insights #flashcard
		  id:: 637e09b4-b477-4242-969a-60f4e4ad61e9
			- Application Insights, una característica de Azure Monitor, supervisa las aplicaciones web. Application Insights es capaz de supervisar aplicaciones que se ejecutan en Azure, en el entorno local o en otro entorno de nube.
			- Hay dos maneras de configurar Application Insights para ayudar a supervisar la aplicación. Puede instalar un SDK en la aplicación, o bien puede usar el agente de Application Insights.
			- Una vez que Application Insights esté en funcionamiento, puede usarlo para supervisar una amplia gama de información, como la siguiente:
				- Tasas de solicitudes, tiempos de respuesta y tasas de error
				- Las tasas de dependencia, los tiempos de respuesta y las tasas de error muestran si los servicios externos ralentizan el rendimiento.
				- Vistas de página y rendimiento de carga notificados por los exploradores de los usuarios
				- Llamadas AJAX desde páginas web, incluyendo tasas, tiempos de respuesta y tasas de error
				- Recuentos de usuarios y sesiones
				- Contadores de rendimiento de las máquinas de servidor de Windows o Linux, como CPU, memoria y uso de la red
-
-