deck:: [[Cloud Learning::Azure::Microsoft Learn Course]] 
tags:: Azure, Microsoft-Learn

-
- ## Describir los componentes arquitectónicos principales de Azure
  collapsed:: true
	- ### Qué es Microsoft Azure #flashcard
	  id:: 637ddaaa-d959-4a98-ae2d-3e27c6b62cad
		- Azure proporciona más de 100 servicios que permiten hacer todo tipo de cosas: desde ejecutar las aplicaciones existentes en máquinas virtuales hasta explorar nuevos paradigmas de software, como bots inteligentes y realidad mixta.
		- Muchos equipos comienzan a explorar la nube mediante la migración de sus aplicaciones existentes a máquinas virtuales (VM) que se ejecutan en Azure. Aunque este es un buen comienzo, **la nube es mucho más que un lugar diferente donde ejecutar las máquinas virtuales**.
		- Por ejemplo, Azure proporciona servicios de inteligencia artificial (IA) y aprendizaje automático (ML) que pueden comunicarse de forma natural con los usuarios mediante la vista, el oído y la voz. También facilita soluciones de almacenamiento que crecen dinámicamente para dar cabida a grandes cantidades de datos. Los servicios de Azure permiten soluciones que no son factibles sin la potencia de la nube.
	- ### Ejercicio: Exploración del espacio aislado de Learn
		- Para ejecutar bash desde PowerShell, usar {{cloze $ bash}} #flashcard
		  id:: 637ddaaa-2392-4c13-8a9a-91d9ed226a47
		- Para establecer una sesión de texto con Azure interactiva desde la terminal, usar {{cloze $ az interactive}} #flashcard
		  id:: 637ddaaa-ba17-4403-8096-dd716d599525
	- ### Descripción de la infraestructura física de Azure
		- Una {{c1 región}} es un área geográfica del planeta que contiene al menos un centro de datos, aunque podrían ser varios cercanos y conectados mediante una red de baja latencia. Azure asigna y controla los recursos de forma inteligente dentro de cada {{c1 región}} para garantizar que las cargas de trabajo están bien compensadas. #flashcard
		  id:: 637ddaaa-a296-4d37-8b85-aefab3d01ff5
		-
		- Las {{c1 zonas de disponibilidad}} son centros de datos separados físicamente dentro de una región de Azure. Cada {{c1 zona de disponibilidad}} consta de uno o varios centros de datos equipados con alimentación, refrigeración y redes independientes. Una {{c1 zona de disponibilidad}} se configura para constituir un límite de aislamiento. Si una zona deja de funcionar, la otra continúa trabajando. Las {{c1 zonas de disponibilidad}} están conectadas a través de redes de fibra óptica de alta velocidad privadas.
		  id:: 637ddaaa-95af-4f2f-aca5-2cf39d44b2e5
		  
		  Para garantizar la resistencia, se configuran un mínimo de tres {{c1 zonas de disponibilidad}} independientes en todas las regiones habilitadas. Pero no todas las regiones de Azure admiten actualmente las {{c1 zonas de disponibilidad}}.
		-
		- #### Pares de regiones #flashcard
		  id:: 637ddaaa-e164-42cd-a02a-f74e2fe7e051
			- Incluso con la resistencia adicional que proporcionan las zonas de disponibilidad, es posible que un evento pueda ser tan grande que afecte a varias zonas de disponibilidad en una sola región. Para proporcionar una mayor resistencia, Azure tiene pares de regiones.
			- La mayoría de las regiones de Azure se emparejan con otra región de la misma zona geográfica (por ejemplo, EE. UU., Europa o Asia) que se encuentre como mínimo a 500 km de distancia. Este enfoque permite la replicación de recursos en una zona geográfica que ayuda a reducir la probabilidad de que se produzcan interrupciones provocadas por eventos como desastres naturales, disturbios sociales, cortes del suministro eléctrico o interrupciones de la red física que afecten a una región completa. Por ejemplo, si una región de un par se ve afectada por un desastre natural, los servicios conmutarán por error automáticamente a la otra región de su par de regiones.
				- ![image.png](../assets/image_1668851904525_0.png)
		- #### Regiones soberanas #flashcard
		  id:: 637ddaaa-86a2-4b63-8615-0c93900f99f7
			- Además de las regiones normales, Azure también tiene regiones soberanas. Las regiones soberanas son instancias de Azure que están aisladas de la instancia principal de Azure. Es posible que tenga que usar una región soberana con fines legales o de cumplimiento.
			- Entre las regiones soberanas de Azure se incluyen las siguientes:
				- US DoD (centro), US Gov Virginia, US Gov Iowa y más: Estas regiones son instancias físicas y lógicas con aislamiento de red de Azure para asociados y agencias de la administración pública de EE. UU. Estos centros de datos están operados por personal estadounidense sometido a evaluación e incluyen certificaciones de cumplimiento adicionales.
				- Este de China, Norte de China y más: Estas regiones están disponibles gracias a una asociación exclusiva entre Microsoft y 21Vianet, por la cual Microsoft no mantiene directamente los centros de datos.
		- #### Grupos de administración de Azure #flashcard
		  id:: 637ddaaa-45ba-4749-be9a-8a79cab90385
			- La última pieza es el **grupo de administración**. Los **recursos** se recopilan en grupos de recursos y los **grupos de recursos** se recopilan en **suscripciones**. Si acaba de empezar en Azure, podría parecer una jerarquía suficiente para mantener las cosas organizadas. Pero imagine que trabaja con varias aplicaciones, varios equipos de desarrollo, en varias zonas geográficas.
			- Si tiene muchas suscripciones, es posible que necesite una forma de administrar con eficacia el acceso, las directivas y el cumplimiento para esas suscripciones. Los grupos de administración de Azure proporcionan un nivel de ámbito por encima de las suscripciones. Las suscripciones se organizan en contenedores llamados grupos de administración, a los que se aplican condiciones de gobernanza. Todas las suscripciones de un grupo de administración heredan automáticamente las condiciones que tenga aplicadas, de la misma manera que los grupos de recursos heredan la configuración de las suscripciones y los recursos heredan de los grupos de recursos. Los grupos de administración proporcionan capacidad de administración de nivel empresarial a gran escala con independencia del tipo de suscripciones que tenga. Los **grupos de administración** se pueden anidar.
	-
- ## Descripción de los servicios de proceso y redes de Azure
  collapsed:: true
	- ### Descripción de Azure Virtual Machines
		- #### Introducción
			- Con **Azure Virtual Machines (VM)**, puede crear y usar máquinas virtuales en la nube. Estas máquinas virtuales proporcionan una infraestructura como servicio (IaaS) en forma de un servidor virtualizado y se pueden usar de muchas formas. Como sucede en un equipo físico, puede personalizar todo el software que se ejecuta en la máquina virtual. Las máquinas virtuales son una opción ideal cuando se necesita lo siguiente: #flashcard
			  id:: 637ddaaa-3c82-45f4-a255-df8830d1e62e
				- Control total sobre el sistema operativo (SO).
				- Capacidad de ejecutar software personalizado.
				- Usar configuraciones de hospedaje personalizadas.
		- #### Conjuntos de escalado de máquinas virtuales #flashcard
		  id:: 637ddaaa-5e04-444f-a998-ddc2242326c7
			- Los conjuntos de escalado de máquinas virtuales permiten crear y administrar un grupo de máquinas virtuales idénticas de carga equilibrada. De manera que permite automatizar y gestionar la tarea de crear máquinas idénticas para reducir nuestro esfuerzo manual.
		- #### Conjuntos de disponibilidad de máquinas virtuales #flashcard
		  id:: 637ddaaa-a132-4b0e-9cce-da6d9232f17d
			- Los conjuntos de disponibilidad de máquinas virtuales son otra herramienta que nos ayuda a crear un entorno más resistente y de alta disponibilidad. Están diseñados para garantizar que las máquinas virtuales escalen pero además, que sean resistentes a un fallo de energía o de red de manera que tengan una conectividad de red y potencia variadas.
			-
			- Los **conjuntos de disponiblidad** agrupan las máquinas virtuales de dos maneras:
				- **Dominio de actualización:** Agrupa las máquinas virtuales que se pueden reiniciar al mismo tiempo. Esto le permite aplicar actualizaciones en distintas ventanas (de 30 minutos) a nuestras instancias.
				- **Dominio de error:** Agrupa las máquinas virtuales por fuente de alimentación común y conmutador de red. Por defecto, un conjunto de disponiblidad dividirá las máquinas virtuales en un máximo de tres dominios de error. Esto ayuda frente a cortes de alimentación y/o de red.
			-
			- Los conjuntos de disponibilidad no llevan asociado **ningún coste adicional** salvo las instancias que se estén ejecutando.
			-
		- #### Ejemplos de cuándo usar máquinas virtuales #flashcard
		  id:: 637ddaaa-3758-48d9-9007-6800ce77b3d4
			- **Durante las pruebas y el desarrollo:** Para construir entornos de prueba y desarrollo específicos a nuestros requerimientos.
			- **Para ejecutar aplicaciones en la nube:** Para ahorrar costes y tener escalabilidad.
			- **Para ampliar el centro de datos a la nube:** Es más simple que implementar un servidor de manera local.
			- **Para recuperarnos frente a desastres naturales**
	-
	- ### Descripción de contenedores de Azure
		- #### ¿Qué son los contenedores? #flashcard
		  id:: 637ddaaa-a089-4ff4-ad81-46a31a842d93
			- Los contenedores son un entorno de virtualización.
			- Igual que las máquinas virtuales, nos permiten ejecutar varios contenedores en un solo host.
			- A diferencia de las máquinas virtuales, no se administra el sistema operativo de un contenedor. Los contenedores son ligeros y se han diseñado para crearse, escalarse horizontalmentet y detenerse de forma dinámica. De manera mucho más agil que con máquinas virtuales.
			- **Las máquinas virtuales virtualizan el hardware, mientras que los contenedores virtualizan el Sistema Operativo.**
			- Las máquins virtuales son apropiadas para cuando queremos control total sobre nuestra instancia.
	-
	- ### Descripción de las opciones de hospedaje de aplicaciones
		- **Azure App Service** es tu opción para implementar tu Proyecto Final de Master. 😉
		-
	- ### Descripción de las redes virtuales de Azure
		- #### Comunicación con recursos locales
			- Las **redes virtuales** de Azure permiten vincular entre sí los recursos del entorno local y dentro de la suscripción de Azure. De hecho, puede crear una red que abarque tanto el entorno local como el entorno en la nube. Existen tres mecanismos para lograr esta conectividad: #flashcard
			  id:: 637ddaaa-d7d6-46e9-9f0b-9c022287d176
				- Las conexiones de red privada virtual de {{cloze punto a sitio}} se establecen desde un equipo ajeno a la organización a la red corporativa. En este caso, el equipo cliente inicia una conexión VPN cifrada para conectarse a la red virtual de Azure.
				  id:: 637ddaaa-c5f7-433d-9ee1-dab05a789387
				- Las redes virtuales privadas de {{cloze sitio a sitio}} vinculan el dispositivo o puerta de enlace de VPN local con la puerta de enlace de VPN de Azure en una red virtual. De hecho, puede parecer que los dispositivos de Azure están en la red local. La conexión se cifra y funciona a través de Internet.
				  id:: 637ddaaa-ca52-43a5-9687-a6b7bfe3e258
				- {{cloze Azure ExpressRoute}} proporciona una conectividad privada dedicada a Azure que no se desplaza por Internet. ExpressRoute es útil para los entornos donde se necesita más ancho de banda e incluso mayores niveles de seguridad.
				  id:: 637ddaaa-5f89-46dc-b45e-bff8311b37be
	- ### Descripción de las redes privadas virtuales de Azure
		- #### Puertas de enlace de VPN
			- Al implementar una instancia de VPN Gateway, especifique el tipo de red privada virtual, es decir, **basada en directivas** o **basada en rutas**. La principal diferencia entre estos dos tipos de VPN es cómo se especifica el tráfico que se va a cifrar. En Azure, ambos tipos de puertas de enlace de VPN usan una clave previamente compartida como único método de autenticación. #flashcard
			  id:: 637ddaaa-d482-4b94-8f0b-9548f6cb8a3c
				- Las **instancias de VPN Gateway basadas en directivas** especifican de forma estática la dirección IP de los paquetes que se deben cifrar a través de cada túnel. Este tipo de dispositivo evalúa cada paquete de datos en función de los conjuntos de direcciones IP para elegir el túnel a través del cual se va a enviar el paquete.
				- En las **puertas de enlace basadas en rutas**, los túneles IPSec se modelan como una interfaz de red o una interfaz de túnel virtual. El enrutamiento IP (ya sean rutas estáticas o protocolos de enrutamiento dinámico) decide cuál de estas interfaces de túnel se va a usar al enviar cada paquete. Las redes privadas virtuales basadas en rutas son el método preferido para conectar dispositivos locales. Son más resistentes a los cambios de la topología, como la creación de subredes.
	- ### Describir Azure ExpressRoute
		- #### Modelos de conectividad de ExpressRoute
			- ExpressRoute admite cuatro modelos que puede usar para conectar la red local con la nube de Microsoft: #flashcard
			  id:: 637ddaaa-3d60-463d-aa1e-af3012d29f32
				- **Ubicación de CloudExchange**
					- La ubicación conjunta hace referencia al centro de datos, la oficina u otras instalaciones que se encuentran físicamente en un intercambio en la nube, como un ISP. Si la instalación tiene la ubicación compartida en un intercambio en la nube, puede solicitar una conexión cruzada virtual a la nube de Microsoft.
				- **Conexión Ethernet de punto a punto**
					- La conexión Ethernet de punto a punto hace referencia al uso de una conexión punto a punto para conectar la instalación a la nube de Microsoft.
				- **Conexión universal**
					- Con la conectividad universal, puede integrar la red de área extensa (WAN) con Azure si proporciona conexiones a las oficinas y los centros de datos. Azure se integra con la conexión WAN para proporcionarle una conexión, como la que tendría entre el centro de datos y las sucursales.
				- **Directamente desde sitios de ExpressRoute**
					- Puede conectarse directamente a la red global de Microsoft en una ubicación de emparejamiento distribuida estratégicamente por todo el mundo. ExpressRoute Direct proporciona conectividad dual de 100 Gbps o 10 Gbps, que es compatible con la conectividad activa/activa a escala.
-
- ## Descripción de los servicios de almacenamiento de Azure
  id:: 637cc071-e79b-4fc3-aee0-144bf2dff0c1
	- ### Descripción de la redundancia de almacenamiento de Azure
		- #### Almacenamiento con redundancia local #flashcard
		  id:: 637ddaaa-71f1-45fb-ac38-77f22af08b41
			- El **almacenamiento con redundancia local (LRS)** replica los datos tres veces dentro de **un único** centro de datos en la región primaria. LRS ofrece una durabilidad mínima de **11 nueves** (99,999999999 %) de los objetos en un año determinado.
			- **LRS** es la opción de redundancia de costo más bajo y ofrece la menor durabilidad en comparación con otras opciones. **LRS** protege los datos frente a errores en la **estantería** de servidores y en la **unidad**. No obstante, si se produce un **desastre** como un incendio o una inundación en el **centro de datos**, es posible que todas las réplicas de una cuenta de almacenamiento con LRS se pierdan o no se puedan recuperar. Para mitigar este riesgo, Microsoft **recomienda** el uso del almacenamiento con redundancia de zona (**ZRS**), el almacenamiento con redundancia geográfica (**GRS**) o el almacenamiento con redundancia de zona geográfica (**GZRS**).
				- ![Diagrama en el que se muestra la estructura usada para el almacenamiento con redundancia local.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-azure-storage-services/media/locally-redundant-storage-37247957.png)
		- #### Almacenamiento con redundancia de zona #flashcard
		  id:: 637ddaaa-1fdf-4225-9856-31919dc8920c
			- Para las regiones con zona de disponibilidad habilitada, el **almacenamiento con redundancia de zona (ZRS)** replica los datos de Azure Storage sincrónicamente en **tres** zonas de disponibilidad de Azure en la región primaria. ZRS proporciona a los objetos de datos de Azure Storage una durabilidad de al menos **12 nueves** (99,9999999999 %) durante un año determinado.
			- Con **ZRS**, los datos son accesibles para las operaciones de **escritura y lectura** incluso si una **zona** deja de estar disponible. No es necesario volver a montar los recursos compartidos de archivos de Azure de los clientes conectados. Si alguna zona deja de estar disponible, Azure realiza las actualizaciones de la red, como el redireccionamiento de DNS. Estas actualizaciones pueden afectar a la aplicación si se accede a los datos antes de que se completen dichas actualizaciones.
			- Microsoft recomienda usar ZRS en la región primaria para escenarios que requieren de **alta disponibilidad**. También se recomienda ZRS para restringir la replicación de datos dentro de un país o **región** para cumplir los requisitos de **gobernanza** de datos.
				- ![Diagrama en el que se muestra ZRS, con una copia de los datos almacenados en cada una de las tres zonas de disponibilidad.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-azure-storage-services/media/zone-redundant-storage-6dd46d22.png)
			-
		- #### Redundancia en una región secundaria #flashcard
		  id:: 637ddaaa-16ad-410c-81bf-7e927447c698
			- En el caso de las aplicaciones que requieren de alta durabilidad, puede optar por copiar los datos de la cuenta de almacenamiento en una **región secundaria** que esté a cientos de kilómetros de distancia de la **región primaria**. Si los datos de la cuenta de almacenamiento se copian en una región secundaria, los datos serán duraderos incluso en caso de un error catastrófico que impida que se recuperen los datos de la región primaria.
			- Al crear una cuenta de almacenamiento, seleccione la región **principal** de la cuenta. La región secundaria emparejada **se determina en función de los Pares de regiones** de Azure y **no se puede cambiar**.
			- Azure Storage ofrece dos opciones para copiar los datos en una región secundaria:
				- almacenamiento con redundancia geográfica (**GRS**) y
				- almacenamiento con redundancia de zona geográfica (**GZRS**).
			- GRS es similar a ejecutar LRS en dos regiones, y GZRS es similar a ejecutar ZRS en la región primaria y LRS en la región secundaria.
		- #### Almacenamiento con redundancia geográfica #flashcard
		  id:: 637ddaaa-6369-40c2-bfaa-3654bd52cbed
			- GRS copia los datos de manera sincrónica **tres veces** dentro de una ubicación física única en la **región primaria** mediante LRS. Luego copia los datos de forma asincrónica en **una única ubicación física en la región secundaria** (el par de regiones) mediante LRS. GRS proporciona a los objetos de datos de Azure Storage una durabilidad de al menos **16 nueves** (99,99999999999999 %) durante un año determinado.
			- ![image.png](../assets/image_1669123089295_0.png)
			-
		- #### Almacenamiento con redundancia de zona geográfica #flashcard
		  id:: 637ddaaa-88ad-4044-bb12-5b2e1cf53f82
			- **GZRS** combina la alta disponibilidad que proporciona la redundancia entre zonas de disponibilidad con la protección frente a interrupciones regionales que proporciona la replicación geográfica. Los datos de una cuenta de almacenamiento de GZRS se almacenan en **tres zonas de disponibilidad** de Azure en la región **primaria** (de manera similar a ZRS) y también se replican en una **región geográfica secundaria** para protegerlos frente a **desastres** regionales.
			- ![Diagrama en el que se muestra GZRS, con el ZRS de la región primaria replicando datos al LRS en una segunda región.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-azure-storage-services/media/geo-zone-redundant-storage-138ab5af.png)
			-
	- ### Descripción de los servicios de almacenamiento de Azure
		- La plataforma de Azure Storage incluye los servicios de datos siguientes: #flashcard
		  id:: 637ddaaa-8965-4baf-878f-591156e640d2
			- **Blobs de Azure**: un almacén de objetos que se puede escalar de forma masiva para datos de texto y binarios. También incluye compatibilidad con el análisis de macrodatos a través de Data Lake Storage Gen2.
			- **Azure Files**: recursos compartidos de archivos administrados para implementaciones locales y en la nube.
			- **Colas de Azure**: un almacén de mensajería para mensajería confiable entre componentes de aplicación.
			- **Azure Disks**: volúmenes de almacenamiento en el nivel de bloque para máquinas virtuales de Azure.
		- #### Blob Storage #flashcard
		  id:: 637ddaaa-691c-40a1-94a7-98651a2af3de
			- **Azure Blob Storage** es una solución de almacenamiento de **objetos** para la nube. Puede almacenar grandes cantidades de datos, como **datos de texto o binarios**. Azure Blob Storage es **no estructurado**, lo que significa que no hay ninguna restricción en cuanto a los tipos de datos que puede contener. Blob Storage puede administrar miles de cargas simultáneas, cantidades enormes de datos de vídeo, archivos de registro en constante crecimiento y es accesible desde cualquier lugar con conexión a Internet.
			- Una ventaja del almacenamiento en **blobs** con respecto al almacenamiento en **disco** es que no requiere que los desarrolladores piensen en discos o los administren. Los datos se cargan como **blobs** y **Azure** se encarga de las necesidades de almacenamiento físico.
			- Usos:
				- Visualización de imágenes o documentos directamente en un explorador.
				- Almacenamiento de archivos para acceso distribuido.
				- Streaming de audio y vídeo.
				- Almacenamiento de datos para copia de seguridad y restauración, recuperación ante desastres y archivado.
				- Almacenamiento de datos para el análisis en local o en un servicio hospedado de Azure.
		- #### Niveles de Blob Storage #flashcard
		  id:: 637ddaaa-5940-487c-ab2c-0f6ab340fbc8
			- Entre los niveles de acceso disponibles se incluyen:
				- **Nivel de acceso frecuente**: optimizado para almacenar datos a los que se accede con frecuencia (por ejemplo, imágenes para el sitio web).
				- **Nivel de acceso esporádico**: optimizado para datos a los que se accede con poca frecuencia y que se almacenan al menos durante 30 días (por ejemplo, las facturas de los clientes).
				- **Nivel de acceso de archivo**: conveniente para datos a los que raramente se accede y que se almacenan durante al menos 180 días con requisitos de latencia flexibles (por ejemplo, copias de seguridad a largo plazo).
		- #### Azure Files #flashcard
		  id:: 637ddaaa-1938-401d-be9a-89bb80982f18
			- **Azure Files** ofrece recursos compartidos de archivos totalmente administrados en la nube a los que se puede acceder mediante los protocolos **SMB (Bloque de mensajes del servidor)** o **NFS (Network File System)** estándar del sector. Los recursos compartidos de archivos de Azure Files se pueden montar simultáneamente mediante implementaciones locales o en la nube. A los recursos compartidos de archivos SMB de Azure se puede acceder desde clientes Windows, Linux y macOS. A los recursos compartidos de archivos NFS de Azure Files se puede acceder desde clientes Linux y macOS. Además, los recursos compartidos de archivos SMB de Azure Files se pueden almacenar en la caché de los servidores de Windows Server con Azure File Sync, lo que permite un acceso rápido allí donde se utilizan los datos.
		- #### Queue Storage #flashcard
		  id:: 637ddaaa-07bc-4a8a-b4bb-0f909276d7ca
			- **Azure Queue Storage** es un servicio para almacenar grandes cantidades de **mensajes**. Una vez que están almacenados, se puede acceder a los mensajes desde cualquier lugar del mundo mediante llamadas autenticadas con HTTP o HTTPS. Una cola puede contener tantos mensajes como el **espacio que tenga la cuenta de almacenamiento** (pueden ser **millones**). Cada mensaje individual de la cola puede llegar a tener un tamaño **máximo** de 64 KB. Las colas se utilizan normalmente para crear un trabajo pendiente del trabajo que se va a procesar de forma **asíncrona**.
		- #### Disk Storage #flashcard
		  id:: 637ddaaa-ad05-4977-b2c7-9f10ff1a1e93
			- El **almacenamiento en disco** o los discos administrados de Azure son **volúmenes** de almacenamiento de nivel de **bloque** que administra Azure para su uso con **máquinas virtuales** de Azure. Conceptualmente, son iguales que un disco físico, pero están **virtualizados**, lo que ofrece mayor resistencia y disponibilidad que un disco físico. Con los discos administrados, lo único que debe hacer es aprovisionar el disco; Azure se encargará del resto.
		-
	- ### Identificación de las opciones de migración de datos de Azure
		- #### Azure Migrate #flashcard
		  id:: 637ddaaa-0c02-463e-9a75-6a12787cbf52
			- Azure Migrate es un servicio que le ayuda a migrar desde un entorno local a la nube. Azure Migrate funciona como centro para ayudarle a administrar la valoración y la migración del centro de datos local a Azure. Ofrece lo siguiente:
				- **Plataforma de migración unificada**: un único portal para iniciar, ejecutar y realizar un seguimiento de la migración a Azure.
				- **Rango de herramientas**: Rango de herramientas para la evaluación y migración Las herramientas de Azure Migrate incluyen Azure Migrate: Discovery y assessment y Azure Migrate: Server Migration.
				   Azure Migrate también se integra con otros servicios y herramientas de Azure, así como con ofertas de proveedores de software independientes (ISV).
				- **Assessment and migration** (Evaluación y migración): en el centro de Azure Migrate, puede evaluar y migrar la infraestructura local a Azure.
		- #### Herramientas integradas #flashcard
		  id:: 637ddaaa-fc94-492a-ade9-cc20fdbe0740
			- Además de trabajar con herramientas de ISV, el centro de Azure Migrate también incluye las siguientes herramientas para ayudar con la migración:
			- **Azure Migrate: Discovery and assessment** (Azure Migrate: detección y evaluación). Detecte y evalúe servidores locales que se ejecutan en VMware, Hyper-V y servidores físicos para preparar la migración a Azure.
			- **Azure Migrate: Server Migration** (Azure Migrate: migración del servidor). Migre máquinas virtuales de VMware, máquinas virtuales de Hyper-V, servidores físicos, otros servidores virtualizados y máquinas virtuales de la nube pública a Azure.
			- **Data Migration Assistant**. Data Migration Assistant es una herramienta independiente para evaluar servidores de SQL Server. Ayuda a identificar posibles problemas que bloquean la migración. Identifica características no admitidas, nuevas características que puede aprovechar después de la migración y la ruta de acceso correcta para la migración de la base de datos.
			- **Azure Database Migration Service**. Migre bases de datos locales a máquinas virtuales de Azure en las que se ejecutan SQL Server, Azure SQL Database o instancias administradas de SQL.
			- **Web app migration assistant** (Asistente de migración de aplicación web). Azure App Service Migration Assistant es una herramienta independiente para evaluar sitios web locales para la migración a Azure App Service. Use Migration Assistant para migrar aplicaciones web de .NET y PHP a Azure.
			- **Azure Data Box**. Use los productos de Azure Data Box para trasladar grandes cantidades de datos sin conexión a Azure.
		- #### Azure Data Box #flashcard
		  id:: 637ddaaa-e4bf-46f7-a1ab-3cb0e7627bff
			- Azure Data Box es un servicio de **migración física** que ayuda a transferir grandes cantidades de datos de forma rápida, económica y confiable. La transferencia de datos segura se acelera mediante el envío de un dispositivo de almacenamiento propietario de Data Box que tiene una capacidad de almacenamiento utilizable máxima de 80 terabytes. **Data Box se transporta hacia y desde el centro de datos a través de un transportista regional**. Una caja resistente asegura y protege Data Box de daños durante el trayecto.
			- **Data Box** es ideal para transferir tamaños de datos con **más de 40 TB** en escenarios sin conectividad de red limitada. El movimiento de datos puede ser único, periódico o una transferencia de datos masiva inicial seguida de transferencias periódicas.
	- ### Identificación de las opciones de movimiento de archivos de Azure
		- Además de la migración a gran escala mediante servicios como Azure Migrate y Azure Data Box, Azure también tiene herramientas diseñadas para ayudarle a mover o interactuar con archivos individuales o grupos de archivos pequeños. Entre esas herramientas se encuentran AzCopy, Explorador de Azure Storage y Azure File Sync. #flashcard
		  id:: 637ddaaa-f188-47b1-aa30-037c8c785bf6
		- #### AzCopy #flashcard
		  id:: 637ddaaa-d2d1-46d7-a35b-1be6c2e60361
			- **AzCopy** es una utilidad de línea de comandos que puede usar para copiar blobs o archivos a una cuenta de almacenamiento o desde una cuenta de almacenamiento. Con AzCopy, puede copiar archivos entre cuentas de almacenamiento, cargarlos, descargarlos e incluso sincronizarlos. AzCopy incluso se puede configurar para trabajar con otros proveedores de nube para ayudar a mover archivos entre nubes.
		- #### Azure File Sync #flashcard
		  id:: 637ddaaa-0a89-4bd8-b976-f0c41c857ceb
			- **Azure File Sync** es una herramienta que permite centralizar los archivos compartidos en Azure Files y mantener la flexibilidad, el rendimiento y la compatibilidad de un servidor de archivos de Windows. Es casi como convertir el servidor de archivos de Windows en una **red de entrega de contenido en miniatura**. Una vez que instale Azure File Sync en el servidor local de Windows, se mantendrá sincronizado bidireccionalmente con los archivos en Azure de forma automática.
			-
-
- ## Descripción de la identidad, el acceso y la seguridad de Azure
  id:: 637ddaaa-df19-435c-9626-ca9b2e70fe3c
	- ### Descripción de los servicios de directorio de Azure #flashcard
	  id:: 637ddbd4-b574-46ad-ab1b-544aa1680a97
		- {{c1 Azure Active Directory (Azure AD)}} es un servicio de directorio que le permite iniciar sesión y acceder tanto a las aplicaciones en la nube de Microsoft como a las aplicaciones en la nube que desarrolle. {{c1 Azure AD}} también puede ayudarle a mantener la implementación de Active Directory local. #flashcard
		  id:: 637ddc95-d0d2-4c00-8487-6e6308d49eae
	- ### Descripción del control de acceso basado en roles de Azure #flashcard
	  id:: 637de45a-64c4-491b-9eec-1c538fcccbb5
		- El control de acceso basado en roles se aplica a un ámbito, que es un recurso o un conjunto de recursos en los que este acceso se permite. Los ámbitos pueden ser lo siguiente: #flashcard
		  id:: 637ddeb3-c52c-44db-8ea5-c06cb12e3c44
			- Un grupo de administración (una colección de varias suscripciones)
			- Una sola suscripción
			- Un grupo de recursos.
			- Un solo recurso
	- ### Descripción del modelo de Confianza cero #flashcard
	  id:: 637de48b-9929-44da-a168-b2ff0391ab0d
		- **Confianza cero** es un modelo de seguridad que supone el peor de los escenarios posibles y protege los recursos con esa expectativa. Confianza cero presupone que hay una vulneración y comprueba todas las solicitudes como si provinieran de una red no controlada.
		- Para abordar este nuevo mundo informático, Microsoft recomienda encarecidamente el modelo de seguridad de Confianza cero, que se basa en estos principios rectores:
			- **Comprobar explícitamente**: realice siempre las operaciones de autorización y autenticación en función de todos los puntos de datos disponibles.
			- **Usar el acceso de privilegios mínimos**: limite el acceso de los usuarios con Just-in-Time y Just-Enough-Access (JIT/JEA), directivas que se adaptan al nivel de riesgo y protección de datos.
			- **Asumir que hay brechas**: minimice el radio de expansión y el acceso a los segmentos. Comprobación del cifrado de un extremo a otro. Utilice el análisis para obtener visibilidad, impulsar la detección de amenazas y mejorar las defensas.
		- ![Diagrama en el que se compara la autenticación de todos los usuarios por parte de Confianza cero con la opción clásica de la ubicación de red.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-azure-identity-access-security/media/zero-trust-cf9202be.png)
	- ### Descripción de defensa en profundidad #flashcard
	  id:: 637de60f-dc72-407d-9900-cea766226110
		- ![Un diagrama de las capas de defensa en profundidad. Desde el centro, estas capas son: datos, aplicación, proceso, red, perímetro, identidad y acceso, y seguridad física.](https://learn.microsoft.com/es-es/training/wwl-azure/describe-azure-identity-access-security/media/defense-depth-486afc12.png)
		-
		- Aquí tiene una breve descripción del rol de cada capa:
			- La capa de seguridad física es la primera línea de defensa para proteger el hardware informático del centro de datos.
			- La capa de identidad y acceso controla el acceso a la infraestructura y al control de cambios.
			- La capa perimetral usa protección frente a ataques de denegación de servicio distribuido (DDoS) para filtrar los ataques a gran escala antes de que puedan causar una denegación de servicio para los usuarios.
			- La capa de red limita la comunicación entre los recursos a través de controles de acceso y segmentación.
			- La capa de proceso protege el acceso a las máquinas virtuales.
			- La capa de aplicación ayuda a garantizar que las aplicaciones sean seguras y estén libres de vulnerabilidades de seguridad.
			- La capa de datos controla el acceso a los datos empresariales y de clientes que es necesario proteger.
		-
		- #### Seguridad física
			- La protección física del acceso a los edificios y el control del acceso al hardware de proceso del centro de datos son la primera línea de defensa.
			- La intención de la seguridad física es proporcionar medidas de seguridad físicas contra el acceso a los recursos. Estas medidas garantizan que no se puedan omitir otras capas y se controle apropiadamente la pérdida o el robo. Microsoft usa varios mecanismos de seguridad físicos en sus centros de datos de la nube.
		- #### Perímetro
			- El perímetro de la red protege frente a ataques basados en red contra los recursos. Identificar estos ataques, eliminar sus repercusiones y recibir alertas sobre ellos cuando suceden son formas importantes de proteger la red.
			  
			  En esta capa, es importante que realice lo siguiente:
				- Use protección contra DDoS para filtrar los ataques a gran escala antes de que puedan afectar a la disponibilidad de un sistema para los usuarios.
				- Use firewalls perimetrales para identificar los ataques malintencionados contra la red y alertar sobre ellos.
		- #### Red
			- En esta capa, el enfoque está en limitar la conectividad de la red en todos los recursos para permitir solo la necesaria. Al limitar esta comunicación, se reduce el riesgo de que se propaguen los ataques a otros sistemas de la red.
			- En esta capa, es importante que realice lo siguiente:
				- Limite la comunicación entre los recursos.
				- Deniegue de forma predeterminada.
				- Restrinja el acceso entrante de Internet y limite el saliente cuando sea apropiado.
				- Implemente conectividad segura a las redes locales.
		- #### Procesos
			- El software malintencionado, los sistemas sin revisiones aplicadas y los sistemas protegidos inadecuadamente abren el entorno a los ataques. El enfoque en esta capa es asegurarse de que sus recursos de proceso estén seguros y de que cuenta con los controles adecuados para minimizar los problemas de seguridad.
			- En esta capa, es importante que realice lo siguiente:
				- Proteja el acceso a las máquinas virtuales.
				- Implemente la protección del punto de conexión de los dispositivos y mantenga los sistemas revisados y actualizados.
		- #### Aplicación
		- #### Datos
			- Los que almacenan y controlan el acceso a los datos son responsables de asegurarse de que están protegidos correctamente. A menudo, los requisitos legales dictan los controles y procesos que deben cumplirse para garantizar la confidencialidad, la integridad y la disponibilidad de los datos.
			- En casi todos los casos, los atacantes intentan conseguir datos:
				- Almacenados en una base de datos.
				- Almacenados en discos en máquinas virtuales.
				- Almacenados en aplicaciones de software como servicio (SaaS), como Office 365.
				- Administrados mediante el almacenamiento en la nube.
	- ### Descripción de Microsoft Defender for Cloud #flashcard
	  id:: 637de904-fa04-485c-9846-208587cfa3ed
		- Microsoft Defender for Cloud es una herramienta de supervisión para la administración de la posición de seguridad y la protección contra amenazas. Supervisa los entornos en la nube, locales, híbridos y multinube para ofrecer instrucciones y notificaciones destinadas a reforzar la posición de seguridad.
		-