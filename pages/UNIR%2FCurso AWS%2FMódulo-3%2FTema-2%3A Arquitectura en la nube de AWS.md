title:: UNIR/Curso AWS/Módulo-3/Tema-2: Arquitectura en la nube de AWS
tags:: UNIR, AWS
deck:: [[AWS::CCP::Módulo-3]]

-
- ## Marco de Buena Arquitectura de AWS
	- Es una guía para el diseño de infraestructuras que reúnan las siguientes características:
		- Seguras
		- De alto desempeño
		- Resilientes
		- Eficaces
	- Es una forma de brindar prácticas recomendadas que se desarrollaron a partir de las lecciones aprendidas a través de al revisión de arquitecturas de clientes.
	- ### Pilares #flashcard
	  id:: 634e69b5-5d7d-4d8f-8dca-4d3c97d3564b
		- Excelencia operativa
			- Aportar valor de negocio
			- Se recomienda que todo esté como código
			- Comentarios
			- Cambios frecuentes, pequeños y reversibles
			- Preveer, y aprender de los errores
		- Seguridad
			- Proteger la información y sabe cómo se evalúa el riesgo
			- Trazabilidad
			- Proteger datos en tránsito y en reposo
			- Mantener a las personas alejadas de los datos
		- Fiabilidad
			- Que funcionen los proyectos y que sean robustos y fiables
			- Probar y testear
			- Escalar horizontalmente
			- Evitar asumir estimaciones sobre capacidad
		- Eficacia del rendimiento
			- Cómo usamos los recursos de AWS y que solo usemos los que necesitemos
			- Usar arquitecturas sin servidor
			- Experimentar a menudo
		- Optimización de costos
			- Cómo AWS nos guía para ahorrar costes
	- ### AWS Well-Architected Tool
		- Compara lo que usamos con las buenas prácticas de AWS
		-
- ## Fiabilidad y disponibilidad #flashcard
  id:: 634e690e-d851-4c30-88f6-f9437042db34
	- ### Fiabilidad
		- Que proporcione lo pedido cuando el usuario lo solicite
		- Probabilidad de que todo el sistema funcione según lo previsto durante un periodo especificado.
	- ### Disponibilidad
		- Cuánto tiempo (porcentaje) está funcionando un sistema correctamente realizando las operaciones que se esperan de él.
		- Un sistema de alta disponibilidad es el que puede soportar una medida de degradación sin dejar de estar disponible.
- ## AWS Trusted Advisor #flashcard
  id:: 634e691d-d93c-4278-af93-3d8b7765d160
	- Es una herramienta a modo de panel con consejos y alertas de nuestros servicios
	- Tiene una capa gratuita con funcionalidades básicas.
	-
-
-