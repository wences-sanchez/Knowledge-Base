deck:: [[UNIR::Curso Azure::Módulo-5]]
tags:: UNIR, Azure

-
- ## PDF
	- ![Azure_Modulo-5_Identidad-gobernanza-privacidad-y-cumplimiento.pdf](../assets/Azure_Modulo-5_Identidad-gobernanza-privacidad-y-cumplimiento_1668160422073_0.pdf)
	-
-
- ## Tema 1: Servicios principales de identidad de Azure #flashcard
  id:: 636e2aa5-2207-4a39-b123-30f6ac1e1662
	- ### Autenticación VS Autorización
		- La **autenticación** es identificar la persona o servicio que está intentando acceder a un recurso
		- Quiero identificar **quién** está accediendo a un recurso concreto
		- Se solicitan credenciales de acceso. Por ejemplo, usuario y contraseña
		- La **autorización** consiste en, sabiendo quién eres, determinar a qué datos y recursos puedes tener acceso.
	- ### Azure AD
		- Es el servicio principal que nos da Azure para administración de identidad y acceso basado en la nube de Microsoft
	- ### MFA
		- Multi Factor Authentication
		- Proporciona seguridad adicional al requerir **al menos dos o más** elementos para la autenticación completa
		- Algo que conoces + algo que posees + algo intrínseco a ti
	- ### SSO
	- ### CA
		- **Acceso Condicional**
		- Es lo que utiliza Azure Active Directory para reunir señales, tomar decisiones y aplicar directivas de la organización referentes a la autenticación.
		- ![image.png](../assets/image_1668160199070_0.png)
	-
	-
- ## Tema 2: Gobernanza en Azure #flashcard
  id:: 636e2b0e-9821-4582-a40d-b598f6cae196
	- ### RBAC
		- **Acceso Basado en Roles**
		- Nos permite asociar un rol a un grupo de personas, un grupo de procesos, un único recurso o proceso
	- ### Bloqueos de recursos y etiquetas
		- Nos permite proteger todos nuestros recursos para no eliminarlos o para no modificarlos. Accidentalmente.
	- ### Políticas, Blueprints y CAF
		- #### Azure Policy
			- Ayuda a hacer cumplir los estándares que una organización haya definido a la hora de gestionar los recursos de las suscripciones.
			- Son reglas de alto nivel.
			- Hay predefinidas
		- #### Azure Blueprints
			- La diferencia entre blueprints y las plantillas de ARM es que ARM se centra en los recursos y Blueprints incluye muchas maś cosas. Como:
				- Roles necesarios
				- Políticas necesarios
				- Plantillas de Azure Resource Manager necesarias
				- Grupos de recursos necesarios
	-
- ## Tema 3: Privacidad, cumplimiento y estándares de protección de datos #flashcard
  id:: 636e3259-869d-4430-be0c-6f5cb76d31ad
	- ### Términos y requisitos de cumplimiento de Azure
		- ![image.png](../assets/image_1668166549577_0.png)
		-
	- ### Declaración de privacidad y condiciones de uso
		- Es una declaración que Microsoft realiza de manera obligada.
		- Igual que cuaalquier otro proveedor de un servicio o producto.
	- ### Regiones soberanas
		- Algunas regiones no están disponibles de forma pública. Ejemplos:
			- Azure China
			- Azure Government
	-