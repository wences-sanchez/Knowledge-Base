file-path:: ../assets/UNIR-AWS_Modulo-1_1664869606733_0.pdf
file:: [UNIR-AWS_Modulo-1_1664869606733_0.pdf](../assets/UNIR-AWS_Modulo-1_1664869606733_0.pdf)
title:: hls__UNIR-AWS_Modulo-1_1664869606733_0
tags:: UNI, AWS

- #tags #UNI #AWS
-
- El concepto de **«informática en la nube»** hace referencia a la entrega bajo demanda de potencia de computación, bases de datos, almacenamiento, aplicaciones y otros recursos de las tecnologías de la información por medio de **Internet** y bajo un sistema de precios de **pago por uso**.
  hl-page:: 3
  ls-type:: annotation
  id:: 633c0c7f-b662-4aa0-b220-8d8e6b3cf537
	-
	- Estos recursos se ejecutan en enormes equipos de servidores ubicados en grandes centros de datos en diferentes partes del mundo. La informática en la nube permite ver la infraestructura como software. Esto es de gran ayuda a los desarrolladores y departamentos de TI, que evitan arduas tareas, como el aprovisionamiento, el mantenimiento y la planificación de la capacidad para centrarse en lo que más importa.
-
-
- Existen **tres modelos principales de servicios en la nube**. Cada modelo ofrece un nivel diferente de control sobre sus recursos de TI:
  hl-page:: 4
  ls-type:: annotation
  id:: 633c0cf3-edf0-4857-ae23-bab2c75c4d8f
	-  **Infraestructura como servicio (IaaS):** hace referencia a los servicios básicos y son el pilar fundamental de la nube. Con ellos, se accede a las características de redes, a los equipos (virtuales o en hardware dedicado) y al espacio de almacenamiento de datos. IaaS ofrece el mayor nivel de flexibilidad y control de administración en relación con sus recursos de TI.
	-  **Plataforma como servicio (PaaS):** aquí se concentran los servicios que reducen la necesidad de gestionar la infraestructura (normalmente, el hardware y los sistemas operativos) y facilitan el desarrollo de aplicaciones.
	-  **Software como servicio (SaaS):** son servicios que ofrecen un producto completo mediante aplicaciones para el usuario final. No hay que administrar ni gestionar la infraestructura y mantener el servicio. El servicio de correo electrónico de Google es un ejemplo de SaaS.
-
- Por otra parte, también conviven **tres implementaciones de servicios en la nube**:
  hl-page:: 4
  ls-type:: annotation
  id:: 633c0d7e-5fb2-45c4-aa84-a95a9789fbaf
	-  **Nube**: todas las partes de una aplicación o desarrollo se encuentran completamente en la nube y usan todos sus servicios.
	-  **Híbrida**: una solución implementada conectando la infraestructura propia y los recursos en la nube para extender sus soluciones.
	-  **En las instalaciones (on premises)**: también conocida como nube privada. Es casi idéntico al modelo de infraestructura propia y clásica que puede aprovecharse para lanzar tecnologías de virtualización y administración.
	-
- Por una parte, los servicios ofertados por los proveedores de nube pueden llegar desde ofrecer servidores virtuales hasta gestionar absolutamente todos los recursos necesarios para abstraernos y crear nosotros nuestros productos software. #spaced
	- Por otra parte, hay tres tipos de implementación de dichos servicios; independientemente:
	- Una empresa puede tener contratado un servicio de PaaS y usar nube pública.
	- Otra empresa puede tener servidores virtuales con IaaS pero usar nube privada (porque su ecosistema provea sus recursos dados).
	- Otra empresa puede tener una nube híbrida y usar (por ejemplo) SaaS para un proyecto específico que tengan y que se haya decidido implementarlo de esa manera.
		-
- ¿Qué se entiende por servicio web? #flashcard
  hl-page:: 5
  ls-type:: annotation
  id:: 633c13f1-1af3-4832-bf48-03413aee6fb9
	- Por servicio web se entiende cualquier componente software que está disponible a través de Internet mediante una interacción con una interfaz de programación de aplicaciones (API). AWS es una plataforma en la nube segura con un amplio abanico de productos globales listo para usarse en cuestión de minutos.
	-
		- [:span]
		  ls-type:: annotation
		  hl-page:: 6
		  id:: 633c1444-aee7-4d91-9642-12c5a6d726fe
		  hl-type:: area
		  hl-stamp:: 1664881732947
- AWS fundamenta sus costos en 3 fuentes fundamentales: la informática(computación) en la que se cobra por hora o por segundo, el almacenamiento de datos (por GB) y la transferencia de datos de salida (por GB). En la mayoría de los casos, no se aplican cargos por la transferencia de datos de entrada ni por la transferencia de datos entre servicios de AWS dentro de la misma región (con excepciones). El modelo de precios implica pagar por lo que se usa, pagar menos al reservar servicios, pagar menos cuanto más uso se le dé y pagar aún menos a medida que AWS crece.
  ls-type:: annotation
  hl-page:: 8
  id:: 633c15a7-05fe-47e9-91d7-cf17df04a217
- AWS ofrece a nuevos clientes una capa gratuita (https://aws.amazon.com/es/free/) durante 1 año para determinados servicios y opciones. Además, servicios como Amazon Virtual Private Cloud (Amazon VPC), AWS Identity and Access Management(IAM), Auto Scaling, AWS CloudFormation, AWS OpsWorks y AWS Elastic Beanstalk se ofrecen sin cargo adicional, si bien es posible que haya otros cargos por los servicios que usen con ellos.
  ls-type:: annotation
  hl-page:: 9
  id:: 633c1602-db47-4fea-b688-45219c1ff48a
- Se define el coste total de la propiedad como «la estimación financiera que ayuda a identificar los costes directos e indirectos de un sistema». (AWS Pricing Work, 2020). Se utiliza para comparar el coste de ejecutar una infraestructura completa o una carga de trabajo en las instalaciones propias frente hacerlo en AWS. Además, sirve para presupuestar el negocio en caso de migrar a la nube.
  ls-type:: annotation
  hl-page:: 9
  id:: 633c1650-387b-40c3-a930-8be94718e919
- [:span]
  ls-type:: annotation
  hl-page:: 10
  id:: 633c1680-5ba1-4e8a-b7f9-e2bd4c654e17
  hl-type:: area
  hl-stamp:: 1664882304228
-
- En la nube, la mayoría de los costes son iniciales y se pueden estimar fácilmente. AWS ofrece precios transparentes basados en diferentes métricas de uso, como RAM, almacenamiento y ancho de banda, entre otras. Además, los precios se determinan por unidad de tiempo. Los clientes ganan confianza con respecto a los precios y son capaces de calcular fácilmente los costes en función de diversas estimaciones de uso. Con la tecnología en las instalaciones los clientes deben tener en cuenta los costes directos (espacio, electricidad, etc.) y los indirectos (almacenamiento, red, etc.). En las instalaciones los costes son predictivos porque se incurre en costes se use o no la capacidad.
  ls-type:: annotation
  hl-page:: 10
  id:: 633c1702-fe1f-49e3-9d8b-f0aa4e4e2d54