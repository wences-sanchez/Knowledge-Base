deck:: [[UNIR::Curso Azure::Microsoft Learn Course]]
tags:: Azure, Microsoft-Learn

-
- ## Describir los componentes arquitectónicos principales de Azure
	- ### Qué es Microsoft Azure #flashcard
		- Azure proporciona más de 100 servicios que permiten hacer todo tipo de cosas: desde ejecutar las aplicaciones existentes en máquinas virtuales hasta explorar nuevos paradigmas de software, como bots inteligentes y realidad mixta.
		- Muchos equipos comienzan a explorar la nube mediante la migración de sus aplicaciones existentes a máquinas virtuales (VM) que se ejecutan en Azure. Aunque este es un buen comienzo, **la nube es mucho más que un lugar diferente donde ejecutar las máquinas virtuales**.
		- Por ejemplo, Azure proporciona servicios de inteligencia artificial (IA) y aprendizaje automático (ML) que pueden comunicarse de forma natural con los usuarios mediante la vista, el oído y la voz. También facilita soluciones de almacenamiento que crecen dinámicamente para dar cabida a grandes cantidades de datos. Los servicios de Azure permiten soluciones que no son factibles sin la potencia de la nube.
	- ### Ejercicio: Exploración del espacio aislado de Learn
		- Para ejecutar bash desde PowerShell, usar {{cloze $ bash}} #flashcard
		- Para establecer una sesión de texto con Azure interactiva desde la terminal, usar {{cloze $ az interactive}} #flashcard
	- ### Descripción de la infraestructura física de Azure
		- Una {{c1 región}} es un área geográfica del planeta que contiene al menos un centro de datos, aunque podrían ser varios cercanos y conectados mediante una red de baja latencia. Azure asigna y controla los recursos de forma inteligente dentro de cada {{c1 región}} para garantizar que las cargas de trabajo están bien compensadas. #flashcard
		-
		- Las {{c1 zonas de disponibilidad}} son centros de datos separados físicamente dentro de una región de Azure. Cada {{c1 zona de disponibilidad}} consta de uno o varios centros de datos equipados con alimentación, refrigeración y redes independientes. Una {{c1 zona de disponibilidad}} se configura para constituir un límite de aislamiento. Si una zona deja de funcionar, la otra continúa trabajando. Las {{c1 zonas de disponibilidad}} están conectadas a través de redes de fibra óptica de alta velocidad privadas.
		  
		  Para garantizar la resistencia, se configuran un mínimo de tres {{c1 zonas de disponibilidad}} independientes en todas las regiones habilitadas. Pero no todas las regiones de Azure admiten actualmente las {{c1 zonas de disponibilidad}}.
		-
		- #### Pares de regiones #flashcard
			- Incluso con la resistencia adicional que proporcionan las zonas de disponibilidad, es posible que un evento pueda ser tan grande que afecte a varias zonas de disponibilidad en una sola región. Para proporcionar una mayor resistencia, Azure tiene pares de regiones.
			- La mayoría de las regiones de Azure se emparejan con otra región de la misma zona geográfica (por ejemplo, EE. UU., Europa o Asia) que se encuentre como mínimo a 500 km de distancia. Este enfoque permite la replicación de recursos en una zona geográfica que ayuda a reducir la probabilidad de que se produzcan interrupciones provocadas por eventos como desastres naturales, disturbios sociales, cortes del suministro eléctrico o interrupciones de la red física que afecten a una región completa. Por ejemplo, si una región de un par se ve afectada por un desastre natural, los servicios conmutarán por error automáticamente a la otra región de su par de regiones.
				- ![image.png](../assets/image_1668851904525_0.png)
		- #### Regiones soberanas #flashcard
			- Además de las regiones normales, Azure también tiene regiones soberanas. Las regiones soberanas son instancias de Azure que están aisladas de la instancia principal de Azure. Es posible que tenga que usar una región soberana con fines legales o de cumplimiento.
			- Entre las regiones soberanas de Azure se incluyen las siguientes:
				- US DoD (centro), US Gov Virginia, US Gov Iowa y más: Estas regiones son instancias físicas y lógicas con aislamiento de red de Azure para asociados y agencias de la administración pública de EE. UU. Estos centros de datos están operados por personal estadounidense sometido a evaluación e incluyen certificaciones de cumplimiento adicionales.
				- Este de China, Norte de China y más: Estas regiones están disponibles gracias a una asociación exclusiva entre Microsoft y 21Vianet, por la cual Microsoft no mantiene directamente los centros de datos.
		- #### Grupos de administración de Azure #flashcard
			- La última pieza es el **grupo de administración**. Los **recursos** se recopilan en grupos de recursos y los **grupos de recursos** se recopilan en **suscripciones**. Si acaba de empezar en Azure, podría parecer una jerarquía suficiente para mantener las cosas organizadas. Pero imagine que trabaja con varias aplicaciones, varios equipos de desarrollo, en varias zonas geográficas.
			- Si tiene muchas suscripciones, es posible que necesite una forma de administrar con eficacia el acceso, las directivas y el cumplimiento para esas suscripciones. Los grupos de administración de Azure proporcionan un nivel de ámbito por encima de las suscripciones. Las suscripciones se organizan en contenedores llamados grupos de administración, a los que se aplican condiciones de gobernanza. Todas las suscripciones de un grupo de administración heredan automáticamente las condiciones que tenga aplicadas, de la misma manera que los grupos de recursos heredan la configuración de las suscripciones y los recursos heredan de los grupos de recursos. Los grupos de administración proporcionan capacidad de administración de nivel empresarial a gran escala con independencia del tipo de suscripciones que tenga. Los **grupos de administración** se pueden anidar.
	-
- ## Descripción de los servicios de proceso y redes de Azure
	- ### Descripción de Azure Virtual Machines
		- Con **Azure Virtual Machines (VM)**, puede crear y usar máquinas virtuales en la nube. Estas máquinas virtuales proporcionan una infraestructura como servicio (IaaS) en forma de un servidor virtualizado y se pueden usar de muchas formas. Como sucede en un equipo físico, puede personalizar todo el software que se ejecuta en la máquina virtual. Las máquinas virtuales son una opción ideal cuando se necesita lo siguiente: #flashcard
			- Control total sobre el sistema operativo (SO).
			- Capacidad de ejecutar software personalizado.
			- Usar configuraciones de hospedaje personalizadas.
-
-
-
- ## Descripción de los servicios de almacenamiento de Azure
- ## Descripción de la identidad, el acceso y la seguridad de Azure
-