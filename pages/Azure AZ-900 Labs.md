- ## Labs de https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/
	- DONE [Crear una máquina virtual en el portal](https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/Instructions/Walkthroughs/01-Create%20a%20virtual%20machine.html)
	- DONE [Crear una aplicación web (10 min.)](https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/Instructions/Walkthroughs/02-Create%20a%20Web%20App.html)
	  :LOGBOOK:
	  CLOCK: [2022-12-22 Thu 10:08:33]--[2022-12-22 Thu 10:19:10] =>  00:10:37
	  :END:
	- DONE [Implementación de Azure Container Instances (10 min.)](https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/Instructions/Walkthroughs/03-Deploy%20Azure%20Container%20Instances.html)
	  collapsed:: true
	  :LOGBOOK:
	  CLOCK: [2022-12-22 Thu 10:20:53]--[2022-12-22 Thu 10:30:17] =>  00:09:24
	  :END:
		- ![image.png](../assets/image_1671701455577_0.png)
		- ![image.png](../assets/image_1671701491090_0.png)
		-
	- DONE [Crear una red virtual (20 min.)](https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/Instructions/Walkthroughs/04-Create%20a%20virtual%20network.html)
	  collapsed:: true
	  :LOGBOOK:
	  CLOCK: [2022-12-22 Thu 10:32:50]--[2022-12-22 Thu 10:58:54] =>  00:26:04
	  :END:
		- ![image.png](../assets/image_1671703167483_0.png)
		- ![image.png](../assets/image_1671703194333_0.png)
		- ![image.png](../assets/image_1671703217144_0.png)
		- ![image.png](../assets/image_1671703239837_0.png)
		-
	- DONE [Crear almacenamiento de blobs (5 min.)](https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/Instructions/Walkthroughs/05-Create%20Blob%20storage.html)
	  collapsed:: true
	  :LOGBOOK:
	  CLOCK: [2022-12-22 Thu 11:01:46]--[2022-12-22 Thu 11:17:37] =>  00:15:51
	  :END:
		- ![image.png](../assets/image_1671704299301_0.png)
		- ![image.png](../assets/image_1671704341625_0.png)
		-
	- DONE [Crear una base de datos SQL (5 min.)](https://microsoftlearning.github.io/AZ-900T0xES-MicrosoftAzureFundamentals/Instructions/Walkthroughs/06-Create%20a%20SQL%20database.html)
	  collapsed:: true
	  :LOGBOOK:
	  CLOCK: [2022-12-22 Thu 11:20:48]--[2022-12-22 Thu 11:40:08] =>  00:19:20
	  :END:
		- He creado la base de datos con el nombre db1
		- He creado el servidor SQL con nombre único
		- He configurado los detalles de la base de datos acorde con la documentación
		- He añadido mi IP al firewall del servidor SQL a través del portal Azure
		- Me he conectado al servidor y he ejecutado la consulta SQL
		- He borrado el grupo de recursos
		- ![image.png](../assets/image_1671705974550_0.png)
		- ![image.png](../assets/image_1671705999466_0.png)
		- ![image.png](../assets/image_1671706028684_0.png)
		- ![image.png](../assets/image_1671706077654_0.png)
		- ```sql
		   SELECT TOP 20 pc.Name as CategoryName, p.name as ProductName
		   FROM SalesLT.ProductCategory pc
		   JOIN SalesLT.Product p
		   ON pc.productcategoryid = p.productcategoryid;
		  ```
		-