deck:: [[UNIR::Curso Azure::Microsoft Learn Course]]
tags:: Azure, Microsoft-Learn
id:: 637df55b-de1e-4f79-9e1b-8ff28edaf32c

-
- ## Describe Cost Management in Azure
  id:: 637df5fd-0dc0-43d1-991e-65d6ca060cbe
	- ### Comparación de las calculadoras de precios y costo total de propiedad
		- #### Calculadora de precios
			- La calculadora de precios está diseñada para proporcionarle un costo estimado para el aprovisionamiento de recursos en Azure. Puede obtener una estimación de recursos individuales, crear una solución o usar un escenario de ejemplo para ver una estimación del gasto de Azure. La calculadora de precios se centra en el costo de los recursos aprovisionados en Azure.
			- ![Captura de pantalla de la calculadora de precios para referencia.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-cost-management-azure/media/price-calculator-0a750ac3.png)
		- #### Calculadora de TCO
			- La calculadora de TCO está diseñada para ayudarle a comparar los costos de ejecución de una infraestructura local en comparación con una infraestructura en la nube de Azure. Con la calculadora de TCO, se especifica la configuración de infraestructura actual, incluidos los servidores, las bases de datos, el almacenamiento y el tráfico de red saliente. Después, la calculadora de TCO compara los costos previstos del entorno actual con un entorno de Azure que admite los mismos requisitos de infraestructura.
			- ![Captura de pantalla de la calculadora de Coste total de propiedad.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-cost-management-azure/media/total-cost-ownership-657fe344.png)
-
- ## Describe features and tools in Azure for Governance and Compliance
  id:: 637df651-0cbe-4c7c-895e-37a8b565531b
	- ### Descripción del propósito de Azure Blueprints
		- Azure Blueprints le permite estandarizar las implementaciones de entorno o suscripción en la nube. En lugar de tener que configurar características como Azure Policy para cada nueva suscripción, con Azure Blueprints puede definir la configuración repetible y las directivas que se aplican a medida que se crean suscripciones. ¿Necesita un nuevo entorno de pruebas y desarrollo? Azure Blueprints permite implementar un nuevo entorno de pruebas y desarrollo con las opciones de seguridad y cumplimiento ya configuradas. De este modo, los equipos de desarrollo pueden crear e implementar rápidamente nuevos entornos sabiendo que se crean de acuerdo con los estándares organizativos.
	- ### Descripción del propósito de Azure Policy
		- #### ¿Qué son las iniciativas Azure Policy?
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
	- ### Descripción del propósito de Azure Arc
		- La administración de entornos híbridos y de varias nubes puede complicarse rápidamente. Azure proporciona una serie de herramientas para aprovisionar, configurar y supervisar recursos de Azure. ¿Qué ocurre con los recursos locales en una configuración híbrida o los 
		  recursos de nube en una configuración de varias nubes?
		- Al usar Azure Resource Manager (ARM), Arc le permite ampliar el cumplimiento y la supervisión de Azure a las configuraciones híbridas y de varias nubes. Azure Arc simplifica el gobierno y la administración al ofrecer una plataforma de administración local y multinube coherente.
	- ### Descripción de las plantillas de Azure Resource Manager y Azure ARM
		- Azure Resource Manager (ARM) es el servicio de implementación y administración de Azure. Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos de la cuenta de Azure. Cada vez que haga algo con los recursos de Azure, ARM está implicado.
		- Cuando un usuario envía una solicitud de cualquiera de las herramientas, API o SDK de Azure, ARM la recibe. ARM autentica y autoriza la solicitud. Después, ARM envía la solicitud al servicio de Azure, que lleva a cabo la acción solicitada. Verá resultados y funcionalidades coherentes en todas las herramientas, ya que todas las solicitudes se controlan mediante la misma API.
- ## Describe monitoring tools in Azure
  id:: 637df68c-8293-4ae9-9a0f-91eb6e63ff72
-