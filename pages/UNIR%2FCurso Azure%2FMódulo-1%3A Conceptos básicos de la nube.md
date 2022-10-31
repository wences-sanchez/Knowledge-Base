tags:: UNIR, Azure
deck:: [[UNIR::Curso Azure::Módulo-1]]

-
- ## Tema 1: Modelos de nube
  collapsed:: true
	- ### 1.2 Computación en la nube
		- #### Definición de computación en la nube #flashcard
		  id:: 635ff09c-8330-42f8-aad0-68292d825400
			- El término **computación en la nube** o **informática en la nube** es la prestación de servicios informáticos **a través de Internet**, lo que permite disponer de recursos de forma flexible a precios modulables y acelerar la innovación.
			- Al final, la nube no deja de ser un conjunto de centros de datos accesibles por Internet que tienen en su interior una gran cantidad de servidores físicos que, gracias a la virtualización, permiten alojar muchas máquinas virtuales y almacenar discos y proveer su análisis.
			- Si una empresa invierte en un servidor físico, tendrá que hacer frente a unos costos fijos los cuales suponen, por ejemplo, mantenerlos en unas instalaciones y refrigerarlos. Si quisiera escalar sus recursos para crecer o para hacer frente a un pico más alto de carga, tendría que comprar más servidores, irreversiblemente.
		- #### Modelos de implementación de nube
			- **Nube pública**: #flashcard
			  id:: 635ff0c4-4ada-4f1d-8c4b-849b2b7e16dd
				- ![image.png](../assets/image_1667233852893_0.png)
				- Los **recursos**, tales como servidores o almacenamiento, son **propiedad del proveedor de servicios en la nube** que los explota y distribuye a través de Internet.
					- Los recursos son propiedad del proveedor de nube
				- El proveedor proporciona recursos y servicios a sus usuarios.
				- El acceso a los recursos se realiza a través de una conexión de red segura (generalmente a través de Internet).
			- **Nube privada:** #flashcard
			  id:: 635ff31f-e353-4d13-b150-b6afbdce28e4
				- Las organizaciones crean entornos en la nube en sus propios centros de datos locales o bien pueden estar hospedadas por un proveedor de servicios a terceros.
				- La organización es responsable de operar los servicios que brinda.
				- No proporciona acceso a usuarios ajenos a la organización.
					- Solo accedemos nosotros
					- Tiene la desventaja de que tenemos que parchear y mantener los servidores.
			- **Nube híbrida:** #flashcard
			  id:: 635ff419-ea37-4ec4-8e93-f8fb02a4af7a
				- Combina nubes públicas y privadas para permitir que las aplicaciones se ejecuten en la ubicación más adecuada.
					- Es la opción adecuada si, por ejemplo, queremos tener los datos sensibles en servidores locales de nuestra nube privada y las aplicaciones ejecutándose en la nube pública
		- #### Comparación de los modelos de nube #flashcard
		  id:: 635ff454-53a9-4f38-bf6e-36824aaf38b2
			- ![image.png](../assets/image_1667232918510_0.png)
			-
-
- ## Tema 2: Beneficios y consideraciones de la nube
	- ![image.png](../assets/image_1667236714098_0.png)
	- ### Alta disponibilidad
		- Nos aseguramos de una redundancia para que nuestras aplicaciones nunca se caigan ni en el caso de