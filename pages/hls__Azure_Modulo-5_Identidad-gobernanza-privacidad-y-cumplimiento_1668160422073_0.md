file-path:: ../assets/Azure_Modulo-5_Identidad-gobernanza-privacidad-y-cumplimiento_1668160422073_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-5]]
tags:: UNIR, Azure, PDFs

-
- ## Tema 1: Servicios principales de identidad de Azure
	- El concepto de {{cloze autenticación}}: #flashcard
		-  Identifica a la persona o el servicio que intenta acceder a un recurso.
		-  Solicita credenciales de acceso legítimas.
		-  Es la base para crear principios seguros de identidad y control de acceso.
		-
	- El concepto de {{cloze autorización}}: #flashcard
	  hl-page:: 5
	  ls-type:: annotation
	  id:: 636e1c26-9b17-4390-862a-f57cb348b9cc
	  hl-color:: yellow
		-  Determina el nivel de acceso de una persona o servicio autenticados.
		-  Define a qué datos pueden acceder y qué pueden hacer con ellos.
		-
	- La {{cloze autenticación multifactor}} proporciona seguridad adicional para las identidades de una organización al requerir dos o más elementos para la autenticación completa. Dichos elementos pertenecen a las categorías siguientes: #flashcard
	  hl-page:: 5
	  ls-type:: annotation
	  id:: 636e1cbb-8baf-40e9-a99e-2beab5edbf97
	  hl-color:: yellow
		-  Algo que sepa: contraseña o respuesta a una pregunta de seguridad.
		-  Algo que tenga: aplicación móvil que recibe una notificación o un dispositivo generador de tokens.
		-  Algo que sea: algún tipo de propiedad biométrica, como una huella digital o escaneo facial (utilizado en muchos dispositivos móviles).
		-
	- El {{cloze Directorio Activo de Azure o Azure Active Directory (AAD)}} es el servicio de administración de identidad y acceso basado en la nube de Microsoft. Sus funcionalidades principales son:
	  hl-page:: 6
	  ls-type:: annotation
	  id:: 636e1cd6-069c-4315-9911-84b2536a4417
	  hl-color:: yellow
		-  Autenticación (los usuarios de la organización inician sesión para acceder a los recursos).
		-  Identidad de negocio a cliente (Business to Client, B2C).
		-  Identidad de negocio a negocio (Business to Business, B2B).
		-  Inicio de sesión único (Single Sign-On, SSO).
		-  Administración de aplicaciones.
		-  Administración de dispositivos.
		-
	- Un **inquilino** (**Tenant**) de Azure es una instancia propia y segura de Azure AD que se crea automáticamente cuando la organización adquiere una suscripción a un servicio en la nube de Microsoft, como por ejemplo Microsoft Azure u Office 365. Cada inquilino de Azure representa una única organización. Cada inquilino de Azure cuenta con un directorio de Azure AD propio y seguro. Dicho AAD incluye los usuarios, grupos y aplicaciones del inquilino, y sirve para llevar a cabo funciones de administración de acceso e identidad para los recursos del inquilino. #flashcard
	  hl-page:: 6
	  ls-type:: annotation
	  id:: 636e1d1a-fa21-4bd9-aee1-7d50f3fd7d46
	  hl-color:: yellow
-
	- El acceso condicional es el mecanismo utilizado por Azure Active Directory para reunir señales, tomar decisiones y aplicar las directivas de la organización. #flashcard
	  hl-page:: 7
	  ls-type:: annotation
	  id:: 636e1d33-e61e-4965-aeae-c94f7f50db2a
	  hl-color:: yellow
		- El uso de directivas de acceso condicional permite aplicar los controles de acceso correctos cuando sea necesario para mantener la organización segura y no interferir con los usuarios cuando no se necesita.
		- Las principales señales de entrada a las directivas de acceso condicional son:
			-  Usuario o pertenencia a un grupo.
			-  Ubicación de la dirección IP.
			-  Dispositivo.
			-  Aplicación.
			-  Detección de riesgos.
		- [:span]
		  ls-type:: annotation
		  hl-page:: 7
		  hl-color:: yellow
		  id:: 636e1d3e-bac2-4bbf-b239-b1d08e086682
		  hl-type:: area
		  hl-stamp:: 1668160830178