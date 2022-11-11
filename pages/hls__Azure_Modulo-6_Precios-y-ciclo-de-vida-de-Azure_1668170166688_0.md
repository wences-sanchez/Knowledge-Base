file-path:: ../assets/Azure_Modulo-6_Precios-y-ciclo-de-vida-de-Azure_1668170166688_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-6]]
tags:: UNIR, Azure, PDFs

-
- ## Tema 1: Planificación y gestión de costes
-
	- {{cloze La calculadora de precios}} es una herramienta que ayuda al cliente a estimar el coste de los productos de Azure. Las opciones que puede configurar en la calculadora de precios varían entre productos, pero las opciones básicas de configuración incluyen: #flashcard
	  hl-page:: 5
	  ls-type:: annotation
	  id:: 636e422d-8833-4338-adf6-99b1876daec6
	  hl-color:: yellow
		-  Región. Ubicación geográfica en la que aprovisiona el servicio.
		-  Nivel. Distintos ámbitos de disponibilidad o rendimiento.
		-  Opciones de facturación. Diferentes formas de pagar por el servicio. Estas opciones varían según el tipo de cliente y el tipo de suscripción y en ocasiones incluyen opciones de ahorro.
		-  Opciones de soporte técnico. Coberturas de soporte adicionales para determinados servicios.
		-  Programas y ofertas. Dependiendo del tipo de cliente o suscripción es posible poder elegir entre programas de licencia específicos u otras ofertas.
		-  Precios de desarrollo/pruebas de Azure. Disponibles para cargas de trabajo de desarrollo y prueba que se aplican a recursos contenidos en una suscripción basada en una oferta de desarrollo/pruebas.
		-
		- La calculadora de precios proporciona estimaciones y no cotizaciones reales de precios. Los precios reales pueden variar según la fecha de compra, la moneda y el tipo de cliente de Azure.
		- [:span]
		  ls-type:: annotation
		  hl-page:: 6
		  hl-color:: yellow
		  id:: 636e4244-4bb9-458e-940c-fd16b79bf9e9
		  hl-type:: area
		  hl-stamp:: 1668170307965
	- {{cloze La calculadora del coste total de propiedad (Total Cost of Ownership, TCO)}} es una herramienta para estimar los ahorros de costes que puede conseguir el cliente migrando a Azure. Genera un informe comparativo de los costes de las infraestructuras locales (on premise) con los costes del uso de productos y servicios de Azure en la nube. #flashcard
	  hl-page:: 6
	  ls-type:: annotation
	  id:: 636e425a-82e7-4fc3-ac3f-ebb681ea2b19
	  hl-color:: yellow
	-
	- El servicio de administración de costes y facturación de Azure (Azure Cost Management) ofrece a los clientes las funcionalidades siguientes: #flashcard
	  hl-page:: 7
	  ls-type:: annotation
	  id:: 636e426b-123a-45c3-87f6-82e634a0a157
	  hl-color:: yellow
		-  Creación de informes de facturación.
		-  Enriquecimiento de datos.
		-  Fijar presupuestos máximos.
		-  Alertas si se exceden los límites de costes.
		-  Recomendaciones sobre los costes.
	-
	- Recomendaciones para minimizar costes en Azure: #flashcard
		- [:span]
		  ls-type:: annotation
		  hl-page:: 7
		  hl-color:: yellow
		  id:: 636e42fe-176f-4dd2-93cd-59ee5d2bb59f
		  hl-type:: area
		  hl-stamp:: 1668170494346
		- [:span]
		  ls-type:: annotation
		  hl-page:: 8
		  hl-color:: yellow
		  id:: 636e430f-c23d-4f5d-855c-f6e832a79e09
		  hl-type:: area
		  hl-stamp:: 1668170511440
- Los acuerdos de nivel de servicio (Service Level Agreements, SLA) describen los compromisos de Microsoft con respecto a tiempo de actividad y conectividad. Preparación para la certificación AZ-900: Microsoft Azure Fundamentals Módulo 6. Tema 2 10© Universidad Internacional de La Rioja (UNIR) Los SLA se caracterizan por: Representar servicios y productos de manera individual. Recoger acuerdos detallados sobre el servicio ofrecido y cualquier excepción al SLA. Las características de prelanzamiento y los servicios gratuitos no están sujetos a SLA
  ls-type:: annotation
  hl-page:: 9
  hl-color:: yellow
  id:: 636e49b9-2ecf-441b-a6ef-4fd022c8f2c9
- Azure expresa los objetivos de rendimiento como tiempo de actividad y garantías de conectividad. La disponibilidad de un servicio (SLA) va desde el 99 % a 99,999 % con los tiempos de inactividad mensuales que se expresan en la tabla 2. En el caso de que un servicio no cumpla con los SLA acordados, Azure proporcionará crédito por valor de un porcentaje de las tarifas mensuales del servicio.
  ls-type:: annotation
  hl-page:: 10
  hl-color:: yellow
  id:: 636e49c6-46ef-4fae-99ea-e3849b86368d
- Existen múltiples factores pueden empeorar o mejorar un SLA. Para determinar los valores de SLA objetivos se requiere realizar una toma de decisiones basada en los objetivos empresariales. Acciones que resultan en un SLA inferior: Agregar más servicios (de modo que unos dependan de otros). Seleccionar servicios gratis o sin SLA. Acciones que resultan en un SLA superior: Usar zonas de disponibilidad (Availability Zones). Hacer que los sistemas sean redundantes.
  ls-type:: annotation
  hl-page:: 11
  hl-color:: yellow
  id:: 636e49fa-d1dc-4b8f-9ece-902327f16faa
- [:span]
  ls-type:: annotation
  hl-page:: 10
  hl-color:: yellow
  id:: 636e4a08-ebd2-45eb-8ba2-aa5e313eb58a
  hl-type:: area
  hl-stamp:: 1668172296191