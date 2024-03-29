tags:: [[Feynman-Technique]], [[InMyOwnWords]] ,[[Azure]]

-
- # Describiendo los conceptos de la computación en la nube {{renderer :wordcount_iijpmxuii}}
	- ## Describiendo la computación en la nube
		- ### Qué es la computación en la nube
			- La computación en la nube es un servicio por parte de los proveedores de nube sobre cómputo, almacenamiento y otros productos relacionados.
			- Lo que realmente marca la diferencia es que:
				- Todos los servicios se pagan únicamente por uso consumido
				- Estos servicios permiten consumir más (usar más) en determinados momentos, y consumir menos (usar menos) cuando no sean necesarios.
					- Esto es brutal cuando queremos escalar nuestras aplicaciones web en función de la demanda que tengamos
		- ### Describe el modelo de responsabilidad compartida
			- Cuando usamos un servicio de un proveedor de nube, esto no significa que no tengamos que ocuparnos de la seguridad del sistema. Más bien, es un gradiente en el cual:
				- Si usamos *Infraestructura-como-Servicio*, tendremos que seguir encargándonos de todo excepto de los servidores físicos y la red física.
				- Si usamos *Plataforma-como-Servicio*, el proveedor se encargará también del almacenamiento y sistema operativo. Dejándonos solo al cargo de nuestro código y nuestros tests. Todo lo demás está manejado por el proveedor de nube.
				- Si usamos *Software-como-Servicio*, tampoco tendremos que preocuparnos siquiera del despliegue de nuestra aplicación. Ya que estará administrado por el proveedor de nube.
		- ### Define los modelos de nube
			- Cuando usamos una nube **pública**, todos nuestros datos viajan a través de Internet (o a través de medios dedicados si queremos y pagamos por ello) hacia los centros de datos del proveedor de nube. Los servidores de dichos centros de datos, no son nuestros. Estas son las principales características de este tipo de nube.
			- Cuando usamos una nube **privada**, los servidores son nuestros y los datos no salen de nuestros dominios. Es mucho más cara ya que tenemos que pagar los servidores y hacer frente a los costes de su mantenimiento como su ubicación y refrigeración. Además de manejar los picos de demanda por nuestra cuenta.
			- Una nube **híbrida** es una mezcla de las dos anteriores juntas usadas en una empresa. De manera que puedan tener los datos en una nube privada y la aplicación en una nube pública.
	- ## Describiendo los beneficios de usar los servicios de la nube
		- ### Beneficios de alta disponibilidad y escalabilidad en la nube
			- Es bastante costoso (y requiere una redundancia de la que no siempre podemos aprovechar su coste) el implementar una alta disponibilidad en nuestras instalaciones físicas.
			- Supone tener los servidores duplicados, con su consiguiente mantenimiento.
			- Escalarlos supone añadir más dinero, con el consiguiente problema de que, si la demanda baja, no podemos devolver el dinero que nos ha costado para no tener dichos recursos ociosos.
			- En la nube, como solo pagamos por uso, podemos tener varios servidores para conseguir alta disponibilidad. Así, aunque la carga sea alta o baja, nunca pagaremos costes por recursos *ociosos* (de hecho, podemos configurar nuestro servicio para que escale automáticamente, despreocupándonos de casi todo lo demás).
	- ## Describiendo los tipos de servicios de nube
		- ### Describe *Infraestructura-como-Servicio*
			- En este tipo de nube, básicamente lo que tenemos son servidores virtuales, que podremos  escalar vertical y horizontalmente, pero que tendremos que mantener aunque sus aspectos físicos los hayamos externalizado hacia el proveedor de nube.
			- Cuando queremos tener control total sobre nuestra infraestructura aunque usemos un modelo de nube.
		- ### Describe *Plataforma-como-Servicio*
			- El proveedor de nube nos administra todo solo para que nosotros pongamos nuestro código y pensemos en cómo será su despliegue en las máquinas de nuestros usuarios.
			- Cuando nos interesa pagar un poco más para no tener que preocuparnos de la infraestructura subyacente. Así, nos podemos centrar en lo que más valor aporta a nuestra empresa.
		- ### Describe *Software-como-Servicio*
			- Todo está administrado salvo nuestro código. Incluso el despliegue de nuestra aplicación, que se realiza a través de la Internet como una página web con un navegador.
			- Cuando queramos usar una interfaz web como único punto de contacto con el usuario.
- # Describe los servicios y arquitectura de Azure
	- ## Describe los componentes principales de la arquitectura de Azure
	  collapsed:: true
		- ### Describe las regiones de Azure, los pares de regiones y las regiones soberanas
			- Las regiones de Azure son una zona geográfica que contiene un conjunto de centros de datos. La mayoría de las regiones están estructuradas en zonas de disponibilidad y éstas a su vez en centros de datos, pero no todas las regiones incluyen zonas de disponibilidad.
			- Casi todas las regiones tienen una *region par* que se utiliza para tener redundancia más allá de sus zonas de disponibilidad. Para, por ejemplo, desastres naturales; ya que hay más de 500 km como mínimo de una region a otra.
			- Las regiones soberanas, también llamadas geografías, son un conjunto de una o más regiones en las cuales Azure nos garantiza que nuestros datos no van a salir.
		- ### Describe las zonas de disponibilidad
			- Son un conjunto de centros de datos dentro de una misma región.
			- Están diseñadas para ofrecer al usuario una alta disponiblidad mediante el diseño mismo de la red de Azure. De manera que dichas zonas de disponibilidad están aisladas unas de otras respecto de red física y electricidad. Por otra parte, están conectadas todas juntas a través de fibra de baja latencia y redundante.
		- ### Describe los centros de datos
			- Son ubicaciones físicas en las cuales están los servidores que, en su conjunto global, sostienten toda la infraestructura de Azure. No se conocen sus ubicaciones por motivos de seguridad.
		- ### Describe los recursos de Azure y los grupos de recursos
			- Los recursos de Azure representan a todos los componentes que están a nuestro alcance para contratar.
			- Los grupos de recursos son una forma de agruparlos para facilitarnos su gestión.
		- ### Describe las suscripciones
			- Una suscripción es la manera que tiene Azure de llamar a nuestras cuentas individuales de pago.
		- ### Describe los grupos de gestión
			- Los grupos de gestión son una opción que nos ofrece Azure para agrupar distintas suscripciones y así manejarlas como un solo grupo (o varios unidos).
			- Es muy útil por ejemplo para una compañía que tenga varias suscripciones en varios departamentos.
	- ## Describe los servicios de cómputo y red de Azure
	  collapsed:: true
		- ### Compara los tipos de cómputo, incluídos *Azure Container Instances*, *Virtual Machines* y *Functions*
			- *Azure Container Instances* es un servicio que ofrece contenedores como método de cómputo. Más allá de explicar lo que son los contenedores, diremos que podemos agrupar sus dependencias y aislarlos unos de otros por si fallan, además de desplegarlos más fácilmente y sin intervención humana.
			- *Virtual Machines* nos ofrece máquinas virtuales. Las cuales podemos gestionar como servidores. Nos ofrecen una potencia de cómputo mucho mayor porque tienen más recursos. En las máquinas virtuales, si queremos, podemos ejecutar contenedores. Aunque es recomendado usar un servicio manejado por Azure en vez de ello.
			- Las Funciones, o *Functions*, entendiendo éstas como *Azure Functions*, son parte de lo que se llama **informática sin servidor**. Llamamos así a las funciones que no se ejecutan en un servidor definido ni administrado ni ejecutado por nosotros, sino que es Azure quien se encarga de absolutamente todo lo relativo a la ejecución del código en uno de sus servidores y simplemente lo ejecuta por nosotros.
			- No es que no haya servidores, sino que lo manejan por nosotros.
			- La función se ejecuta a través de eventos o, por ejemplo, cuando se llama a una URL.
			- *Azure Functions* es un servicio de tipo *Plataforma-como-Servicio*.
		- ### Describe las opciones de máquinas virtuales, incluídas Azure Virtual Machines, Azure Virtual Machine Scale Stes, Availability Sets y Azure Virtual Desktop
			- **Azure Virtual Machines** es un servicio de Azure que ofrece alquilar máquinas virtuales dentro de sus centros de datos para dar un acceso mediante internet a ellas. Hay muchos tipos, desde las más básicas a las más exigentes. El precio es pago-por-uso aunque también hay una opción de reserva por 1 o 3 años con un 70% de descuento mediante pago por adelantado del servicio.
			- **Azure Virtual Machines Scale Set** es un grupo de máquinas virtuales clonadas iguales que podemos definir sin coste adicional para que sean usadas cuando la aplicación necesite ser escalada horizontalmente.
			- **Availability Sets**, o conjuntos de disponibilidad, son grupos donde se pueden asignar las máquinas virtuales de manera que hay:
				- Dominios de actualización (o update domains) en los que nos asegura Azure que no va a reiniciar nuestras máquinas asignadas en menos de 30 minutos unas de otras. Así, nos aseguran de que cuando se actualicen (al reinicio) nunca se actualizarán juntas. Por lo que siempre habrá otra disponible en otro dominio de actualización.
				- Dominios de error (o fault domains) en los que las máquinas están aisladas unas de otras respecto de conexión a red y alimentación y refrigeración.
			- **Azure Virtual Desktop** es un servicio que nos ofrece un Sistema Operativo Windows virtualizado el cual es multi-usuario y está totalmente integrado con Windows local en nuestro PC
		- ### Describe los recursos requeridos por las máquinas virtuales
			- Son:
				- Cómputo: CPU
				- Memoria: RAM
				- y Disco: *Azure Disk Storage* o *Azure Blob Storage Pages*
		- ### Describe las redes virtuales, incluyendo el objetivo de Azure Virtual Networks, Azure Virtual Subnets, peering, Azure DNS, Azure VPN Gateway y Azure ExpressRoute
			- El objetivo de **Azure Virtual Networks** (o VNet) es comunicar nuestros dispositivos que tenemos en nuestras instalaciones a través de una red (virtual porque no es física, sino que está virtualizada). Así, podemos tener una red (como si fuera nuestra LAN) para comunicar y enlazar nuestros ordenadores sin problemas.
			- **Azure Virtual Subnets** se usa para descomponer una VNet que tengamos para nuestra empresa en, por ejemplo, distintas subredes para distintos departamentos.
			- **VNet peering** es una manera de conectar dos VNets entre sí.
			- **Azure DNS** es un servicio de *Domain Name Service* administrado por Azure. También ofrece opciones de comprobación de estado de instancias.
			- **Azure VPN Gateway** es un servicio que permite encriptar una conexión de extremo a extremo para que viaje a través de internet de manera segura. Se usa para conectar redes físicamente separadas de una empresa, por ejemplo.
			- **Azure ExpressRoute** es una manera de conectar las instalaciones de una empresa con Azure sin pasar los datos por Internet, sino que viajan a través de medios dedicados por Azure.
				- Existe también la opción de la nube con CloudExchange o por ethernet de punto-a-punto
		- ### Define los endpoints público y privado
			- Un endpoint público es uno creado normalmente.
			- Un endpoint de tipo *service* está entre público y privado
				- Concretamente, se consigue configurando Azure para que el endpoint de nuestra parte sea privado. Es decir, que no esté expuesto a Internet. Porque está en una subred privada que previamente hemos indicado.
				- Aunque seguimos teniendo uno de los dos enpoints público: el que conecta con el servicio de Azure
			- Un endpoint privado es uno que tiene una interfaz de red virtual administrada que le permite establecer una conexión privada, no con el servicio de Azure sino con una instancia específica ligada a nuestra cuenta del servicio, no accesible desde el resto de Internet.
	- ## Describe los servicios de almacenamiento de Azure
		- ### Compara los servicios de almacenamiento de Azure
			- **Azure Disks Storage** es un servicio administrado por Azure que gestiona todos los discos de nuestras máquinas virtuales en un único lugar. Está formado por los tipos:
				- HDD
				- Standard SSD
				- Premium SSD
				- Ultra Disk
			- **Azure Blob Storage** permite guardar cualquier tipo de contenido, ya que se fundamenta en datos binarios. Se usa para imágenes o backups, pero no tiene restricciones. Está formado por los tipos:
				- Block: El estándard para almacenamiento
				- Page: Optimizado para lectura/escritura por su eficiencia. Por ejemplo, discos.
				- Append: Optimizado para añadir contenido. Por ejemplo, ficheros de logs.
			- **Azure Files** es como un CDN en miniatura. Es decir, nos permite disponer de nuestros ficheros en nuestras instalaciones como si fuera un servidor de SMB o NFS.
			- **Azure Queue Storage** almacena mensajes encolados para conectar aplicaciones entre sí mediante colas de trabajo.
		- ### Describe las capas de almacenamiento
			- **Hot tier:** Para acceso frecuente. Es el más caro
			- **Cool tier:** Para acceso poco frecuente. Como mínimo un mes
			- **Archive tier:** Para guardar a largo plazo. Ideal para guardar datos para cumplir las normativas que obliguen a guardarlos. Como mínimo medio año. Es el más barato
		- ### Describe las opciones de redundancia
			- Almacenamiento de Redundancia Local (LRS):
				- Se guarda el contenido en tres discos distintos y separados dentro de un mismo centro de datos
			- Almacenamiento de Redundancia de Zona (ZRS):
				- Se guarda el contenido en tres zonas de disponibilidad distintas dentro de una misma región. De manera que en cada zona hay una copia independiente de nuestros datos.
			- Almacenamiento de Redundancia Geográfica (GRS):
				- Se guarda el contenido de nuestros datos en tres discos distintos dentro de un mismo centro de datos. Pero se guardan además otras tres copias en tres discos de otro centro de datos de la región par dada.
			- Almacenamiento con Redundancia de Zona Geográfica (GZRS):
				- Se guardan los contenidos en tres zonas distintas dentro de una misma región. Separadamente. Pero además se guardan tres copias más en tres discos distintos de un centro de datos en la región par determinada.
	- ## Describe la identidad, seguridad y acceso en Azure
		- ### TODO Describe Azure AD
		- ### Describe los métodos de autenticación en Azure, incluyendo SSO, MFA y passwordless
			- Los métodos de autenticación de Azure de Single Sign-On (SSO) consisten en aprovechar cuentas de usuarios de otras organizaciones dentro de Azure
			- Con el método de Multi-Factor Authentication lo que hacemos es añadir una (o dos) capas más de seguridad. De manera que podemos crear una regla condicional para que haya que ingresar un PIN en un dispositivo, para que haya que usar biometría de un dispositivo (táctil o facial) o que simplemente tengamos que acceder a dicho dispositivo y verificarlo; además de introducir nuestra contraseña.
			- Passwordless se refiere a usar el punto anterior para eliminar el paso de introducir una contraseña. Pues una contraseña es sólo *algo que se sabe* y que se puede robar.
				- Por otra parte,  MFA incluye *algo que se tiene*, como un teléfono móvil, y *algo que se es*, como una huella dactilar o una retina ocular.
				- Este último punto es el más difícil de falsificar. Por lo cual se puede establecer como passwordless y eliminar el paso de introducir la contraseña, incluso manteniendo un incremento de seguridad con respecto a una simple contraseña.
		- ### Describe el acceso de invitado en Azure
			- El acceso de invitado en Azure consiste en usar las cuentas que tengan dichos invitados en Microsoft, Google, Facebook, etc. para crear un acceso condicional y permitir y confiar en dichas credenciales para darles un acceso (siguiendo el permiso de Least Privilege) y no tener que crearles una cuenta específica que después (supuestamente) habría que encargarse de eliminar.
		- ### TODO Describe el acceso condicional en Azure AD
		- ### Describe el Control de Acceso Basado en Roles (RBAC)
			- En este modelo, se usan roles para ayudarnos con las tareas de otorgar acceso a los usuarios de Azure.
		- ### Describe el concepto de Confianza Cero
			- El modelo de Confianza Cero (o Zero Trust) hace referencia a tratar los distintos componentes de la red como si fueran totalmente externos. Esto choca con lo que se estaba haciendo hasta ahora: confiar en los dispositivos de la red principal y no confiar en cualquiera que fuese externo.
			- Esto ha tenido que cambiar debido al cambio de paradigma en el cual la mayoría de dispositivos están fuera de las instalaciones por tema de teletrabajo.
			- Mediante este modelo, aplicamos todas las reglas a todos los equipos. Así, ningún usuario que no esté en las instalaciones podrá conseguir nada.
		- ### Describe el propósito de la defensa en profundidad de Azure
			- La defensa en profundidad supone estructurar nuestros sistemas en capas sucesivas, de manera que si un atacante quiere entrar, tenga que encontrarse con distintas *fronteras*. Las capas son:
				- Acceso físico (los centros de datos de Azure)
				- Identidad y autenticación (Azure AD)
				- Perimetral (nos protege de ataques de DDoS y otros parecidos)
				- Red (nuestras redes virtuales)
				- Cómputo (nuestras instancias, deberían estar con security groups)
				- Aplicación y balanceado de carga (las aplicaciones deben ser seguras)
				- Datos (deberían estar cifrados, si es responsabilidad nuestra)
		- ### TODO Describe el propósito de Microsoft Defender for Cloud
- # Describe la gestión y la gobernanza en Azure
	- ## Describe la gestión del coste en Azure
		- ### Describe los factores que pueden afectar a los costes en Azure
			- Los datos salientes (no exclusivamente) de los servicios de Azure que vayan a otras regiones
			- El tipo de las instancias, es decir, su tamaño
			- El tiempo que consuman las instancias (como máquinas virtuales u otros, si aplican)
		- ### Compara la calculadora de precios con la calculadora del Coste Total de la Propiedad
			- La calculadora **Pricing Calculator** está incluída dentro de Azure Portal y sirve para calcular el coste de los recursos que allí le especificamos. Tiene en cuenta recursos, regiones, planes de soporte,...
			- La calculadora **Total Cost of Ownership (TCO)** calcula cuánto dinero costaría el conjunto de una infraestructura en la nube. Es útil para las empresas que quieran migrar las suyas a Azure. Esta página está disponible para todo el mundo, no solo para los suscritos a Azure.
		- ### Describe *Azure Cost Management and Billing tool*
			- Es un servicio para gestionar los pagos a Azure
			- También nos permite gestionar lo que estamos usando (o gastando) con gráficas y información detallada que nos ayuda a ahorrar de manera que nos damos cuenta de recursos sobreutilizados (o invertir más en recursos importantes e infrautilizados)
		- ### Describe el propósito de las etiquetas
			- Categorizarlo todo de manera que cuando queramos investigar algo todos los recursos estarán claramente indicados de dónde vienen y a qué sirven.
	- ## Describe las funcionalidades y herramientas en Azure para la gobernanza y cumplimiento
		- ### Describe el propósito de Azure Blueprints
			- Es una herramienta que nos permite recrear entornos completos exhaustivamente.
			- Incluye no solo máquinas virtuales sino policies, plantillas de ARM, recursos o roles
			- Puede contener dentro plantillas ARM que, a diferencia de las blueprints, no tienen relación nativa con Azure
		- ### Describe el proósito de Azure Policy
			- Sirve para controlar, por ejemplo, los recursos que los empleados de una organización puedan gastar.
			- Si tenemos muchos recursos en nuestra suscripción, lo más normal es que también tengamos muchas *policies*
		- ### Describe el propósito de *Resource locks*
			- Su propósito es asegurarnos de que no borramos o modificamos por error o sin querer los recursos que marquemos.
			- Los dos tipos de bloqueo de recursos son:
				- ReadOnly: Para marcar de solo lectura, no se puede modificar ni eliminar.
				- CanNotDelete: Para habilitar la lectura y escritura pero impedir su eliminación.
			- Podemos aplicar bloqueos a cualquier recurso como una suscripción o un grupo de recursos
		- ### Describe el propósito del *Service Trust Portal*
			- El portal *Service Trust* expone al público todos los estándares que Azure cumple para que los (futuros) usuarios puedan comprobar cómo serán tratados sus datos allí.
			- Es el lugar donde revisar todos los informes de auditoría de Azure
	- ## Describe las funcionalidades y herramientas para manejar y desplegar recursos de Azure
		- ### Describe el portal de Azure
			- Es una interfaz web donde podemos administrar todos los recursos y servicios de Azure de manera gráfica. Es actualizada con el paso de cierto tiempo.
		- ### Describe Azure Cloud Shell, incluyendo Azure CLI y Azure PowerShell
			- **Azure Cloud Shell** es parte de la interfaz de Azure que permite ejecutar comandos tanto de Bash como de PowerShell mediante un menú en el que podemos elegir uno de los dos.
			- **Azure CLI** es un producto software basado en línea de comandos que está disponible para descargar tanto en Windows como en Linux or MacOS. Con él podemos administrar nuestros recursos como en la interfaz gráfica pero con comandos de CLI.
			- **Azure PowerShell** es una colección de módulos para administrar recursos de Azure desde PowerShell.
		- ### Describe el propósito de Azure Arc
			- Azure Arc es un agente que se instala en los sistemas de otras nubes o de nuestras instalaciones y que sirve para poder administrar todos nuestros recursos (ya sean de Azure, AWS, GCP, on-premises...) desde un único dashboard.
		- ### Describe Azure Resource Manager y Azure Resource Manager Templates
			- Azure Resource Manager es el backend que lo maneja todo y que lo hace todo.
			- Las distintas formas de interactuar con Azure (Azure portal, Azure CLI, app, PowerShell...) no son sino medios para llegar a ARM, que es al final el que lo hace todo
			- Las templates de ARM son ficheros JSON que contienen de forma declarativa la configuración que queremos.
	- ## Describe las herramientas de monitorización de Azure
		- ### Describe el propósito de Azure Advisor
			- El propósito de Azure Advisor es ofrecer recomendaciones de buenas prácticas y de análisis de nuestras aplicaciones para mejorar su rendimiento, seguridad, confiabilidad, cose y excelencia operacional.
		- ### Describe Azure Service Health
			- Es el primer sitio al que hay que ir para comprobar el estado de los servicios cuando algo falla.
			- Es el portal en el cual Azure actualiza el estado de todos sus servicios.
		- ### Describe Azure Monitor, incluyendo Log Analytics, Azure Monitor Alerts y Application Insights
			- Azure Monitor es donde están toda la información recolectada mediante telemetría de todos nuestros recursos.
			- Log Analytics nos muestra todos los logs de nuestras aplicaciones y servicios
			- Con Azure Monitor Alerts podemos crear alertas mediante reglas y parámetros para que nos avise si algo ocurre.
			- Application Insights nos da información muy valiosa de nuestras aplicaciones, como datos de nuestros usuarios, de páginas vistas, de métricas, etc.
			-
		-
		-
		-
		-
	-
	-
	-