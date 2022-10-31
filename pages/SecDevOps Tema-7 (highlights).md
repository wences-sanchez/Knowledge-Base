title:: SecDevOps Tema-7 (highlights)
deck:: [[UNI::SecDevOps Tema-7]]
author:: [[UNIR]]
full-title:: "SecDevOps Tema-7"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/63fa058f-dfb0-4855-8aa0-8ab56f3d5df5.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Qué es IAM? #flashcard
		  id:: cb0ee63e-2f53-4322-b4e4-90348395c4a6
			- IAM  (Identity  and  Access  Management)  es  el  servicio  de  AWS  que  permite administrar quién puede acceder a las API y qué acciones puede ejecutar (Lucifredi y Ryan, 2018). Tener una política de IAM bien planificada es una parte importante de la seguridad de AWS. IAM distingue entre autenticación, que está basada en usuarios y grupos; y autorización, que se basa en las directivas de IAM.
		- (Page 4)
	- -
	- -
		- ¿Qué significa ARN en AWS? INPUT.... #flashcard
		  id:: a185011e-fcd0-4b25-a809-2870419c1e9f
			- Para identificar los recursos, entre ellos a los usuarios de IAM, AWS usa los Amazon Resource Names o ARN. Un ARN es un identificador único global que hace referencia a objetos de AWS. La mayoría de los tipos de recursos de AWS tienen ARN, incluidos los objetos de S3 y los roles, usuarios y directivas de IAM. Tienen el siguiente formato: arn:partition:service:region:account-id:resource-type/resource-id
		- (Page 5)
	- -
	- -
		- ¿Qué es una directiva de IAM? #flashcard
		  id:: 70484cc2-563a-4161-bf8e-38a95a706f55
			- La idea detrás de IAM es separar a los usuarios y grupos de las acciones que necesitan realizar.  Para  ello,  se  crean  directivas  de  IAM,  que  son  documentos  JSON  que describen qué acciones puede realizar un usuario. Esta política se aplica a los usuarios o grupos, dándoles acceso solo a los servicios que especifica el documento.
		- (Page 5)
	- -
	- -
		- ¿Qué es un permiso en IAM? #flashcard
		  id:: fba7d31a-6da6-4087-a5e1-093b0b64aec5
			- Un  permiso  es  una  combinación  de  dos  elementos:  una  acción  y  una  lista  de recursos. AWS verificará si el usuario autenticado puede realizar la acción solicitada en un recurso específico, por ejemplo, ¿se le permite al usuario reiniciar (la acción) una instancia EC2 (el recurso)?
		- (Page 6)
	- -
	- -
		- Ejemplo de acciones y permisos sobre recursos de AWS #flashcard
		  id:: 57397fb5-9bdf-47ff-a6a6-77827b489970
			- Las acciones se definen como  cadenas de texto con el formato  servicio:permiso. Por ejemplo, la acción de reinicio de instancias se define como ec2:RebootInstances. Las directivas hacen referencia a permisos dinámicos muy granulares en todos los servicios  de  AWS.  El  siguiente  documento  JSON  hace  uso  de  esta  acción  y  de ec2:DescribeInstances sobre todos los recursos. "Version": "2012-10-17", "Statement": [{ "Sid": "VisualEditor0", "Effect": "Allow", "Action": [ "ec2:RebootInstances", "ec2:DescribeInstances" ], "Resource": "*" { }] }
		- (Page 6)
	- -
	- -
		- Este ejemplo sirve para describir algunas de las características de las directivas de   Las directivas contienen  statements, o declaraciones. La declaración es la pieza elemental de una directiva, ya que enlaza acciones y recursos.   El  campo  statement  es  realmente una  lista  de  subdocumentos, por  lo  que  una única directiva puede tener varias declaraciones. IAM: #flashcard
		  id:: 39fd9f41-9a7a-4a69-b8bf-4b1fccf7b970
		- (Page 6)
	- -
	- -
		-   El campo effect indica si se habilitan las acciones sobre los recursos, con Allow, o si se deniegan explícitamente, con Deny. Por defecto, un usuario al que no se le aplica  ninguna  directiva  no  tendrá  permiso  para  ejecutar  ninguna  acción  sobre ningún recurso. El valor  Deny en  effect sirve, por tanto, para denegar permisos específicos que pueden haber sido habilitados por otra directiva.   El  campo  action  especifica  las  acciones  permitidas  o  denegadas  sobre  los recursos. Puede ser un campo de texto, en cuyo caso, especifica una única acción, o una lista. texto o una lista.   El campo resource especifica el recurso o recursos, identificados con ARN, sobre los que hace efecto la declaración. Al igual que  action, puede ser un campo de #flashcard
		  id:: 86312ded-29b1-48f7-b8fb-a22b21da601c
		- (Page 7)
	- -
	- -
		- ¿Cuál es el proceso de rotación de claves en AWS? #flashcard
		  id:: 27d531de-3e5e-4e74-a92a-c3aa5c5e43da
			- Este  proceso  de  rotación consiste en los siguientes pasos:   Se crea una pareja de clave y secreto para una cuenta de servicio.   Se configura la aplicación, script, etc. para usar esta clave. Puede ocurrir que la clave  esté  en  uso  en  varios  sitios,  por  ejemplo,  en  varios  procesos  de  una aplicación configurada en alta disponibilidad.   Tras el tiempo estipulado por la política de seguridad de la empresa (por ejemplo, a los treinta días), se genera una nueva clave.   Se sustituye la clave original por la nueva en todos los sitios donde se configuró. En  este  intervalo  de  tiempo  ambas  claves  son  válidas;  de  lo  contrario,  unos procesos dejarían de funcionar hasta recibir la nueva clave.   Una vez distribuida la clave nueva se puede desactivar y borrar la clave antigua.
		- (Page 10)
	- -
	- -
		- El proceso entre una cuenta PROD y una cuenta TEST para dar permiso de lectura, sobre instancias de EC2, a un equipo de control de calidad sería el siguiente:   En la cuenta PROD, un administrador crea el rol ReadEC2 y asigna al rol una directiva con las acciones ec2:Describe* y ec2:Get* sobre todas las instancias. En el rol se indica el ID de la cuenta TEST, sin identificar nombres de usuarios concretos. El rol puede requerir opciones adicionales, como que el usuario haya iniciado sesión con Multi-Factor Authentication (MFA) para poder asumir el rol. #flashcard
		  id:: e3fa11ca-df6c-47b0-a7eb-6651f6beb1e7
		- (Page 12)
	- -
	- -
		-   El administrador comparte el nombre y el ARN del rol y el número de cuenta con los usuarios de la cuenta TEST. Para asumir el rol desde la consola web, hay que indicar el nombre del rol y el ID de la cuenta, mientras que, para asumirlo desde awscli o desde un SDK, hay que indicar el ARN.   En  la  cuenta  TEST,  un  administrador  crea  una  directiva  con  el  permiso sts:AssumeRole  y  el  ARN  del  rol  ReadEC20  de  la  cuenta  PROD  como  recurso  y  la asigna a un grupo. A partir de ese momento, los usuarios del grupo pueden asumir el rol. Esta directiva no incluye los permisos sobre las instancias de la cuenta PROD, ya que estos están incluidos en la directiva del rol ReadEC2.   El usuario de la cuenta TEST solicita el cambio al rol ReadEC2: •Para acciones en la consola de AWS, el usuario inicia sesión con su usuario y contraseña habituales y selecciona la opción Switch Role del menú de usuario. A continuación, indica el nombre del rol y el ID de la cuenta PROD. •Para acceder programáticamente, el usuario configura el SDK o awscli con la clave  y  secreto  (no  su  contraseña)  y,  a  continuación,  ejecuta  la  función AssumeRole con el ARN del rol ReadEC2.   El servicio AWS STS devuelve credenciales temporales. Este paso es transparente tanto para el usuario en la consola web como si usa un SDK.   A partir de este momento, el usuario puede ejecutar las acciones permitidas por la directiva del rol ReadEC2 en la cuenta PROD. En todo este proceso, el administrador de la cuenta  PROD no ha facilitado ninguna credencial a los usuarios de la cuenta TEST. Esto es especialmente relevante cuando las dos cuentas implicadas pertenecen a organizaciones diferentes. Puede servir, por ejemplo, para dar control sobre una cuenta a una herramienta de gestión de ciclo de vida de aplicaciones o de copias de seguridad ofrecida como servicio. #flashcard
		  id:: 3766f23b-ec5a-490c-90ef-41a28d477f96
		- (Page 13)
	- -
	- -
		- ¿Qué es CloudTrail? #flashcard
		  id:: dced9a5c-39b3-463d-9a28-509d3c111cad
			- y Ryan, 2018). CloudTrail es una herramienta de auditoría que registra todas las llamadas a la API en una región específica, o globalmente, independientemente de la herramienta que origina la llamada: awscli, SDKs, consola e, incluso, otros servicios de AWS (Lucifredi Estos registros mejoran la capacidad para determinar qué usuario realizó qué acción en  un  momento dado,  y  es  esencial  para  reconstruir  lo que realmente  sucedió en caso  de  un  incidente  de  seguridad.  CloudTrail  incluirá  en  sus  registros  todas  las llamadas a la API generadas por cualquier servicio de AWS en nombre del usuario. Algunas  de  estas  llamadas  pueden  haberse  realizado  automáticamente  por  otro servicio,  bien  como  respuesta  a  una  llamada  de  usuario  o  como  parte  del funcionamiento habitual. Los registros de CloudTrail indican si una llamada API fue generada automáticamente por otro servicio.
		- (Page 14)
	- -
	- -
		- ¿Qué es Amazon Inspector? #flashcard
		  id:: 791fd8f0-294e-4ba9-bbfa-fc88c21ec8a7
			- Amazon  Inspector  es  un  escáner  de  vulnerabilidad  de  bajo  impacto.  Reúne información sobre la red y los procesos de los servidores, la analiza y presenta un informe, al usuario, con los resultados. Permite analizar el comportamiento de los recursos y ayuda a identificar posibles problemas de seguridad. Inspector funciona ejecutando evaluaciones sobre conjuntos de recursos. Los datos que recopila de los recursos objetivo incluyen detalles de la comunicación con los servicios  de  AWS,  uso  de  canales  seguros,  procesos  en  ejecución  y  tráfico  de  red entre los procesos, entre otros. Estos datos se analizan y comparan con un conjunto de  reglas  de  seguridad.  El  informe  contiene  una  lista  de  posibles  problemas  de seguridad, con un indicador de gravedad.
		- (Page 15)
	- -
	- -
		- ¿Qué es Amazon Detective? #flashcard
		  id:: 554fa22d-1ab4-4d3a-8619-0152eb6ef6b1
			- Amazon Detective es un servicio administrado por AWS que permite a los usuarios analizar y procesar cantidades ingentes de logs, con el objetivo de buscar causas e impactos  de  incidentes  de  seguridad.  Se  alimenta  de  logs  generados  por  otros servicios de AWS, como GuardDuty (Amazon Web Services, s. f.e), CloudTrail y VPC Flow  Logs,  por  lo  que  puede  activarse  sin  perjuicio  de  rendimiento  de  la infraestructura existente. Según AWS, Detective: «Utiliza modelos de aprendizaje automático para producir representaciones gráficas del comportamiento de su cuenta y lo ayuda a responder preguntas como "¿es esta una llamada API inusual para este rol?" o "¿se espera este aumento  en  el  tráfico  de  esta  instancia?".  No  necesita  escribir  código, configurar o ajustar sus propias consultas»
		- (Page 17)
	- -
	- -
		- ¿Cuáles son las fases que sigue Amazon Detective? #flashcard
		  id:: 81402537-9613-4175-8b26-d45ba857150d
			- A alto nivel, una investigación general, y de Amazon Detective en particular, seguirá estas fases:   Triaje.  El  proceso  comienza  con  un  aviso  de  posible  actividad  maliciosa.  Esta información se hace llegar a un analista o ingeniero de seguridad. Uno de estos puntos  de  entrada  puede  ser  una  alerta  generada  por  Amazon  GuardDuty,  o, simplemente, el ID de la VPC de la que proviene la alerta. El ingeniero determinará si la actividad es genuinamente un riesgo de seguridad o un falso positivo. En caso de considerar la alerta un verdadero positivo, seguirá con la siguiente fase.   Alcance.  En  este  caso,  el  ingeniero  considera  el  alcance  y  posible  causa  del incidente.  Por  ejemplo,  deberá  averiguar  qué  sistemas  y  recursos  han  sido afectados, dónde se originó el ataque, cuándo empezó, si ya ha terminado y si hay actividades  relacionadas  con  el  ataque  (si  un  atacante  toma  el  control  de  una máquina, es probable que intente extraer datos confidenciales hacia el exterior).   Respuesta. Finalmente, el ingeniero intentará detener el ataque y minimizar el daño. Además, establecerá medidas y procedimientos para impedir que un ataque similar pueda volver a ocurrir. En la segunda etapa es donde más valor se puede obtener de Detective. A partir del elemento encontrado en la etapa de triaje, Detective muestra información enlazada. Por  ejemplo,  puede  mostrar  llamadas  API  sobre  un  recurso  con  errores  de autenticación, o el origen geográfico de dichas llamadas. Además, permite comparar el  comportamiento  que  reflejan  los  registros  actuales  con  el  comportamiento habitual. de SDK. Al igual que Inspector, Detective se puede automatizar a través de llamadas de API y
		- (Page 18)
	- -