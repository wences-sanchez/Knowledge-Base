title:: UNIR/Curso AWS/Módulo-2/Tema-2: Amazon Elastic Compute Cloud(EC2)
tags:: UNIR, AWS
deck:: [[UNIR::Curso AWS::Módulo-2]]

-
-
-
- ## Servicios de informática de AWS #flashcard
  id:: 63497f97-05b1-45e8-bca5-9c79311b049b
	- ![image.png](../assets/image_1665761621374_0.png)
	- AWS Elastic Beanstalk es un servicio PaaS que levanta un servidor web y BBDD para hacer funcionar la aplicación
- ## Amazon EC2
	- ### Características de EC2 #flashcard
	  id:: 6349834b-7e76-4af7-b27c-8e6b5bdbd731
		- Es uno de los servicios más importantes de AWS
		- Es de tipo IaaS
		- Es **Elastic** porque puede aumentar o reducir la *cantidad* de servidores y el *tamaño* de ellos
		- Es **Compute** porque procesa datos mediante capacidad de procesamiento (CPU) y la memoria (RAM).
		- Es **Cloud** porque las instancias se alojan en la nube
	- ### Lanzamiento de instancias predeterminadas #flashcard
	  id:: 63498e4f-5225-4a86-bcb6-0324bf0db7f6
		- Se pueden lanzar instancias de cualquier tamaño en una zona de disponiblidad en cualquier lugar del mundo
		- Es compatible con lanzar desde **Amazon Machine Images (AMI)**
		- Nos permite tener un total control sobre el sistema operativo invitado
	- ### Pasos para crear una instancia de EC2 #flashcard
	  id:: 634982a1-40af-4630-b437-6d470e42ef96
		- #### 1. Seleccionar una AMI
			- **Plantilla** que se usa para crear una instancia EC2 (una máquina virtual que se ejecuta en la nube de AWS)
			- Contiene un SO.
			- También suele tener algún sistema de software preinstalado proporcionados por AWS, comunidad o MarketPlace (por terceros)
		- #### 2. Seleccionar un tipo de instancia
			- El tipo de instancia que elegir determina los siguientes elementos:
				- La memoria (RAM)
				- La CPU (Capacidad de Procesamiento)
				- El espacio en disco y tipo de disco (almacenamiento)
				- El rendimiento de red
			- Categorías de tipos de instancias:
				- Ej. *t3.large* => **T** es la familia, **3** es la generación, **Large** es el tamaño
		- #### 3. Configuración de la red
			- ![image.png](../assets/image_1665762548492_0.png)
			- Cuando se lanza la máquina, se crea de forma automática una VPC con una dirección pública para poder conectarnos a ella.
		- #### 4. Asociar rol de IAM
			- **Opcional**: para poder interactuar el software de la instancia con AWS. El rol se gestiona de AWS IAM. Nos permitirá, por ejemplo, acceder a un bucket de S3, ejecutar una lambda, o acceder a DynamoDB.
		- #### 5. Script de datos de usuario
			- **Opcional**: se ejecutará la primera vez que se inicia la instancia.
		- #### 6. Especificar el almacenamiento
			- Cómo queremos y dónde guardar los datos de la máquina
				- Configurar el volúmen raíz (donde está alojado el SO).
					- Se mide en GB
					- Puede ser SSD o HDD
				- Lo que no es SO se puede almacenar en:
					- **EBS**: en bloques. Se puede detener al instancia y sigue
					- **EFS**: no para el raíz
					- **S3**: no para el raíz
		- #### 7. Agregar etiquetas
			- Poner parejas clave-valor como metadatos para ayudarnos con la gestión de recursos
		- #### 8. Configurar el grupo de seguridad
			- Conjunto de reglas de firewall que controlan el tráfico a la instancia
		- #### 9. Crear el par de claves
			- Clave pública / privada (nueva o seleccionada por nosotros)
	- ### Ciclo de vida de las instancias de EC2 #flashcard
	  id:: 63498816-7f81-49ca-9a88-79380ded6beb
		- ![image.png](../assets/image_1665763348645_0.png)
- ## Modelo de precios de EC2
	- ### Resumen del modelo de precios de EC2 #flashcard
	  id:: 63498a73-aae5-4d03-abb2-891a6bda01ca
		- ![image.png](../assets/image_1665763533297_0.png)
	- ### ¿Qué son las instancias reservadas? #flashcard
	  id:: 63498bcb-cf5b-425b-ad03-d4871160e666
		- Son instancias de EC2 las cuales se pagan al inicio, completa o parcialmente, al reservarlas.
		- Plazo de 1 o 3 años.
	- ### Qué son las instancias reservadas programadas? #flashcard
	  id:: 63498c6c-1b1b-4050-808b-fdab56642714
		- Son instancias reservadas de EC2 que estén disponibles siempre según la programación periódica que especifique.
		- Plazo de 1 año.
	- ### ¿Qué es una instancia de spot? #flashcard
	  id:: 634988ce-2116-4e7a-a5c7-d035f4149768
		- Las instancias de spot son instancias que se ejecutan siempree que haya disponibles y que su oferta esté por encima del precio de la instancia de spot
		- AWS puede interrumpirlas con una notificación de 2 minutos
		- Los precios son los más económicos, aunque su uso queda acotado a ejecutar cosas *no importantes*.
	- ### ¿Qué son los hosts dedicados? #flashcard
	  id:: 634989eb-74ca-4714-b635-633fecd79047
		- Son servidores **físicos** que están dedicados solamente para el cliente.
		- Pueden usar sus licencias de *software*
	- ### ¿Qué son las instancias dedicadas? #flashcard
	  id:: 63498cd6-52ac-4147-b97f-53753a3e0c55
		- Son instancias que se ejecutan en una VPC en un hardware que está dedicado a un solo cliente. Están **físicamente** aisladas de los hosts de otras **cuentas** de **AWS**.
- ## Pilares de la optimización de costos #flashcard
  id:: 63498067-419b-4d8a-9fcf-3803874c7ce8
	- ![image.png](../assets/image_1665764048371_0.png)
	- ### Adaptación del tamaño
		- Primero, tenemos que pensar en el **tamaño** que pueda tener nuestra instancia (+ tamaño, + caro).
		- Buscar el equilibrio adecuado de los tipos de instancias y usar CloudWatch para métricas de rendimiento.
	- ### Aumento de elasticidad
		- Desactivar instancias cuando no están en uso y habilitar el escalado automático para satisfacer las necesidades.
		- Usar la **elasticidad**. La capacidad se puede escalar.
	- ### Modelo de precios óptimo
		- Si sabemos que vamos a lanzar un proyecto a 1+ años, podemos ahorrarnos dinero
		- Analizar patrones de uso para poder ejecutar **instancias** EC2 con la combinación adecuada de opciones de precios o valorar usar soluciones sin servidor como **AWS Lambda**
	- ### Optimización de las opciones de almacenamiento
		- Analizar los requisitos de almacenamiento, cambiar el tamaño de los volúmenes de EBS y reducir la sobrecarga de sus implementaciones.
		- Si queremos HDD, SSD,...
		-
-