file:: [Azure_Modulo-2_Servicios-principales-de-Azure_1667813268169_0.pdf](../assets/Azure_Modulo-2_Servicios-principales-de-Azure_1667813268169_0.pdf)
file-path:: ../assets/Azure_Modulo-2_Servicios-principales-de-Azure_1667813268169_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-2]]
tags:: UNIR, Azure, PDFs

-
- El término {{cloze región}} corresponde con la zona geográfica en la que Azure tiene presencia física (mediante uno o varios centros de datos conectados por redes de baja latencia) y por tanto puede ofrecer servicios con una baja latencia a los clientes en dicha zona. #flashcard
  hl-page:: 3
  ls-type:: annotation
  id:: 6368d26a-bf01-4714-aa1b-05b148938b54
  hl-color:: yellow
-
-
- [:span]
  ls-type:: annotation
  hl-page:: 4
  hl-color:: yellow
  id:: 6368d2fd-715d-43d3-a209-f65b1ee2f734
  hl-type:: area
  hl-stamp:: 1667814140818
-
- Las características principales de una región son: #flashcard
  hl-page:: 4
  ls-type:: annotation
  id:: 6368d332-525e-49c3-9dcc-82aa28938d8f
  hl-color:: yellow
	-  Están compuestas de uno o más centros de datos próximos.
	-  Proporcionan flexibilidad y capacidad de adaptación para reducir la latencia de los clientes.
	-  Permiten conservar la residencia de los datos de forma que se aseguren los requerimientos de cumplimiento normativo.
-
- Existen una serie de {{cloze regiones especiales}} que Azure denomina geografías, que dan servicio a una serie de mercados especiales y preservan la residencia de los datos y los límites de cumplimiento. Ello permite que clientes con necesidades específicas de residencia y cumplimiento de datos mantengan sus datos y aplicaciones muy cerca. #flashcard
  hl-page:: 4
  ls-type:: annotation
  id:: 6368d399-3981-4fcb-bd03-d02f06cf9d14
  hl-color:: yellow
-
- Azure ofrece a los usuarios diferentes opciones para conseguir una alta disponibilidad y recuperación ante desastres. Las opciones posibles son: #flashcard
  hl-page:: 5
  ls-type:: annotation
  id:: 6368d3f3-fe80-4da1-9df5-47ec9cabee3c
  hl-color:: yellow
	-  {{c1 Zonas de disponibilidad (Availability Zones)}} que brindan protección contra fallos completos del centro de datos.
	  id:: 6368d400-588b-4530-920c-0b1c5d456d5d
	-  {{c1 Conjuntos de disponibilidad (Availability Sets)}} para poder mantener las aplicaciones disponibles durante ventanas de mantenimiento o ante errores de hardware.
	  id:: 6368d405-c027-442d-a37e-509e8ae964e9
	-  {{c1 Pares de regiones}} que permiten una protección regional sin salir de los límites de residencia de datos.
	  id:: 6368d40a-e040-4a0c-95bf-b58427c5e46f
-
-
- Las **zonas de disponibilidad (Availability Zones)** actúan como límites de aislamiento de la infraestructura de nuestras aplicaciones. Funcionan de modo que, si **una zona de disponibilidad** se **desactiva**, las otras **siguen funcionando**. Se caracterizan por: #flashcard
  hl-page:: 6
  ls-type:: annotation
  id:: 6368d4c2-bd9d-4ca8-9e35-eddb66e36f05
  hl-color:: yellow
	-  Proporcionar **protección** contra el tiempo de inactividad debido a **errores** del centro de datos.
	-  Pertenecer a centros de datos **separados** físicamente dentro de una **misma** región.
	-  Cada centro de datos está **equipado** con redes, alimentación y refrigeración independientes.
	-  Cuentan con conexiones de red **privadas** de fibra óptica para alta disponibilidad y replicación de **baja latencia**.
	- [:span]
	  ls-type:: annotation
	  hl-page:: 6
	  hl-color:: yellow
	  id:: 6368d4d6-f241-4311-b19a-5c1aeed65f09
	  hl-type:: area
	  hl-stamp:: 1667814613985
-
-
- Los conjuntos de disponibilidad permiten mantener las aplicaciones disponibles durante ventanas de mantenimiento o ante errores de hardware. Se componen de: #flashcard
  hl-page:: 7
  ls-type:: annotation
  id:: 6368d617-a600-4d3f-8c3c-5feb1983f988
  hl-color:: yellow
	-  **Dominios de actualización (Update Domains, UD)**, de modo que las operaciones de mantenimiento programado, actualizaciones por cuestiones de rendimiento o seguridad se secuencian a través de os dominios de actualización.
	-  **Dominios de error (Fault Domains, FD)**, que proporcionan separación física de cargas de trabajo distribuidas a través del hardware del centro de datos.
	- [:span]
	  ls-type:: annotation
	  hl-page:: 7
	  hl-color:: yellow
	  id:: 6368d622-5bfb-42d7-a7d0-58e925142f4b
	  hl-type:: area
	  hl-stamp:: 1667814946036
-
-