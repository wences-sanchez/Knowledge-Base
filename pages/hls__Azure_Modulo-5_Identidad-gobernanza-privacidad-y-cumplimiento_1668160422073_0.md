file-path:: ../assets/Azure_Modulo-5_Identidad-gobernanza-privacidad-y-cumplimiento_1668160422073_0.pdf
deck:: [[UNIR::Curso Azure::Módulo-5]]
tags:: UNIR, Azure, PDFs

-
- ## Tema 1: Servicios principales de identidad de Azure
	- El concepto de {{cloze autenticación}}: #flashcard
	  id:: 636e2aab-4754-4651-9168-5bdcde295ebe
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
-
- ## Tema 2: Gobernanza en Azure
	- El {{cloze control de acceso basado en el rol de Azure (Role-Based Access Control, RBAC)}} es un sistema de autorización basado en Azure Resource Manager que proporciona administración de acceso específico a los recursos de Azure. El uso de este sistema proporciona los beneficios siguientes: #flashcard
	  hl-page:: 10
	  ls-type:: annotation
	  id:: 636e2f2b-c446-497e-9512-d0e8787cdbff
	  hl-color:: yellow
		-  Ayuda a administrar quién tiene acceso a los recursos, qué puede hacer con esos recursos y a qué áreas puede acceder.
		-  Permite separar las tareas dentro del equipo y conceder a los usuarios solo el acceso mínimo necesario para realizar su trabajo.
		-  Permite controlar el acceso a Azure Portal y a los recursos en la nube.
		-
		- Cada rol está compuesto de:
		  ls-type:: annotation
		  hl-page:: 11
		  hl-color:: yellow
		  id:: 636e2f3c-d0f2-4d8e-a182-504811722f3a
			-  Acciones que puede realizar (Actions).
			-  Acciones que no puede realizar (Not Actions).
			-  Alcances (Scopes).
		-
	- El {{cloze bloqueo de recursos}} es un mecanismo de control que permite a los administradores proteger los recursos de Azure contra la eliminación o la modificación accidental. La administración de bloqueos se puede realizar a nivel de suscripción, grupo de recursos o recursos individuales en Azure Portal. #flashcard
	  hl-page:: 12
	  ls-type:: annotation
	  id:: 636e2fc6-986d-4c2d-a3bb-78c9b0ee63cb
	  hl-color:: yellow
		- [:span]
		  ls-type:: annotation
		  hl-page:: 12
		  hl-color:: yellow
		  id:: 636e2fd2-aa3d-4250-aa58-15d369ffa78c
		  hl-type:: area
		  hl-stamp:: 1668165585647
-
	- El servicio {{cloze Azure Policy}} ayuda a hacer cumplir los estándares de la organización y a evaluar el cumplimiento a escala. Proporciona gobernanza y consistencia de recursos con cumplimiento normativo, seguridad, costes y administración. #flashcard
	  hl-page:: 13
	  ls-type:: annotation
	  id:: 636e2ff7-8c4e-41bd-bd1e-9b5424b9d15f
	  hl-color:: yellow
		- Sus funcionalidades principales son:
			-  Evaluar e identificar los recursos de Azure que no cumplen las directivas.
			-  Proporcionar definiciones de directivas e iniciativas integradas, en categorías, tales como almacenamiento, redes, proceso, Security Center y supervisión.
-
	- {{cloze Azure Blueprints}} es un servicio que permite la creación rápida y repetible de suscripciones en la nube totalmente gobernadas. #flashcard
	  hl-page:: 14
	  ls-type:: annotation
	  id:: 636e3012-9ae5-4f86-ac45-869571283812
	  hl-color:: yellow
		- Además, permite a los equipos de desarrollo construir y poner en marcha nuevos entornos rápidamente. Los artefactos clave del entorno se empaquetan como plantillas de Azure Resource Manager, controles de acceso basado en el rol (RBAC) y directivas en una única definición.
		- Con Azure Blueprints se aúnan los aspectos siguientes:
			-  Grupos de recursos.
			-  Asignaciones de roles.
			-  Asignaciones de directivas.
			-  Plantillas de Azure Resource Manager.