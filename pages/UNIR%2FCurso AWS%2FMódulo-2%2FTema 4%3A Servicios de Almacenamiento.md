title:: UNIR/Curso AWS/Módulo-2/Tema 4: Servicios de Almacenamiento
tags:: UNIR, AWS
deck:: [[AWS::CCP::Módulo-2]]

-
- ## Amazon Elastic Block Store (Amazon EBS)
	- ### Amazon EBS
		- Permite el poder almacenar información a nivel de bloque
		- Así, podemos guardar los datos de los discos duros virtuales de nuestras instancias
		- Admite copia de seguridad
		- #### Características:
			- Instantáneas:
				- Coste de guardar imágen en S3 por GB-mes
			- Cifrado
				- Volúmenes de Amazon EBS cifrados sin coste adicional
			- Elasticidad
				- Aumento de la capacidad
			- Transferencia de datos
- ## Amazon Simple Storage Service (Amazon S3)
	- ### Amazon S3
		- Guarda los datos como objetos
		- Cambiar un fichero requiere borrarlo y crearlo de nuevo
	- ### Precios de Amazon S3
		- Solo se paga por lo que se utiliza, incluido:
			- GB al mes
			- Transferencias **salientes** de datos a otras regiones
			- Solicitudes PUT, COPY, POST, LIST y GET
		- No se para por lo siguiente:
			- Transferencias **entrantes** de datos a Amazon S3
			- Transferencias **salientes** de datos desde Amazon S3 a Amazon CloudFron o EC2 **dentro** de la misma región
			-
- ## Amazon Elastic File System (Amazon EFS)
	-
- ## Amazon S3 Glacier
	- Es un caso especial de S3.
-