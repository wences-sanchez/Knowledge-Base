title:: Herramientas de Automatización de Despliegues Tema-1 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-1"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/1b21e990-d0c5-4240-b8e6-78a06a29ea4d.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- El diseño de Puppet está pensado para estar en continua interacción con las máquinas que gestiona, al contrario que otras herramientas de aprovisionamiento que únicamente se encargan de la etapa de construcción de las máquinas. #flashcard
		  id:: d34ae422-fa3f-4d13-b63a-4a3f01623b4f
		- (Page 5)
	- -
	- -
		-  Lenguaje de configuración y capa de abstracción de recursos.  Capa transaccional. #flashcard
		  id:: ed33ae4f-ae7c-4114-ab5b-cf4fd5cc9cf0
			- Puppet tiene un modelo de funcionamiento sencillo, fácil de entender y de aplicar, que se compone de tres componentes básicos:
		- (Page 5)
	- -
	- -
		- El proceso de Puppet Master se ejecuta como un daemon en el servidor, donde se almacena la configuración necesaria de todo el entorno gestionado. Los agentes se identifican con el servidor Puppet Master al conectarse y utilizan el estándar SSL para establecer un canal de comunicación cifrado, a través del cual se obtiene la configuración que se va a aplicar. #flashcard
		  id:: 7dfe0766-af52-40ee-b046-2f5e5351baf3
		- (Page 6)
	- -
	- -
		- ¿Cuál es la plantilla de un resource en Puppet? #flashcard
		  id:: 7c44725d-c9b5-47d2-90f1-8c894cb32075
			- type { title :
			  attribute => value,
			  }
		- (Page 9)
	- -
	- -
		- package {"vim": ensure => present, } #flashcard
		  id:: c096e934-29cb-4106-95c7-62aa572d5932
		- (Page 9)
	- -
	- -
		- Para utilizar el tipo y el título del recurso como referencia, Puppet nos permite unir el tipo de recurso con la primera letra  en  mayúscula  seguido  del  nombre  entre  conchetes,  como,  por  ejemplo: Package["vim"]. #flashcard
		  id:: 5b4144a4-606e-4318-a74c-baa033227fb0
		- (Page 9)
	- -
	- -
		- ¿Cómo se puede deshacer una transacción en Puppet? #flashcard
		  id:: 711ec0e7-46e5-4784-b2f0-7dc67ace0f4b
			- En Puppet, las transacciones no se registran (más allá de los registros informativos) y, por lo tanto, no se pueden deshacer como se hace con algunas bases de datos.
			  
			  Lo que sí podemos hacer es configurar estas transacciones en modo NOOP (del inglés no operation mode), lo que nos posibilita el probar la ejecución de la configuración sin realmente realizar ningún cambio
		- (Page 11)
	- -
	- -
		- ¿Cómo podemos ver los facts de Puppet para una máquina? #flashcard
		  id:: 9cb6788c-a63d-4e40-b43c-70bc06c72c6b
			- Para  ver  los  facts  que  están  disponibles  en  cada  máquina,  podemos  ejecutar directamente en ella el comando facter desde la línea de comandos.
		- (Page 12)
	- -
	- -
		- El directorio /etc/puppet es donde se guarda la configuración del Puppet Master, en la mayor parte de las plataformas. El fichero principal de configuración de Puppet se  puede encontrar en la siguiente ruta:  /etc/puppet/puppet.conf.  Este  fichero  se  crea  habitualmente  durante  la instalación de Puppet, pero, si no es el caso, el siguiente comando nos permite crear el fichero: # puppetmasterd --genconfig > puppet.conf #flashcard
		  id:: 91d59bbb-c291-4728-9cd2-9b6589923c48
		- (Page 17)
	- -
	- -
		- El  fichero  puppet.conf  tiene  una  estructura  muy  similar  a  los  ficheros  de configuración de formato INI, ya que está dividido en diferentes secciones. Cada una de las secciones se centra en configurar un aspecto concreto de Puppet. Por ejemplo, tenemos la sección del agente [agent] para establecer la configuración del agente y la sección de Puppet Master [master] para configura el servidor Master. También se encuentra una sección llamada [main] para configuración general. En esta sección se configuran opciones generales para todos los componentes de Puppet. Por ahora, no añadiremos en el fichero de puppet.conf nada más que una entrada, certname,  para  especificar  el  nombre  del  Puppet  Master.  Para  ello,  tenemos  que añadir la entrada certname a la sección [master], que habrá que crearla en caso de que no exista todavía: [master] certname=puppet.ejemplo.edu #flashcard
		  id:: 0b0981c8-5caf-4691-a682-9873dd4fbd76
		- (Page 18)
	- -
	- -
		- El fichero site.pp es el que contiene las máquinas que se van a gestionar y la configuración que debe aplicar a estas.
		  id:: 6e9f5198-62e3-4517-910b-ed18d6810da0
		  
		  Este archivo suele almacenarse en el subdirectorio manifests dentro del directorio /etc/puppet/. #flashcard
		- (Page 19)
	- -
	- -
		- Nota: los ficheros que Puppet maneja para la definición de la configuración de los recursos se denominan ficheros manifests (manifiestos). Un fichero manifest de Puppet tiene la extensión .pp. #flashcard
		  id:: cea2aa22-a6f2-42e7-9e4f-a437897838b4
		- (Page 19)
	- -
	- -
		- mkdir/etc/puppet/manifests touch/etc/puppet/manifests/site.pp #flashcard
		  id:: d432f6cf-d641-4489-aad7-e08c33225b22
		- (Page 19)
	- -
	- -
		- El  Puppet  Master  puede  iniciarse  en  la  mayoría  de  las  distribuciones  de  Linux mediante un script init de inicio de servicio. En Red Hat, ejecutaríamos el script de inicio con el comando service de esta forma: # service puppetmaster start En Debian o Ubuntu, lo ejecutamos con el comando invoke-rc.d: # invoke-rc.d puppetmaster start Si  inicias  el  Daemon,  se  iniciará  el  entorno  Puppet,  se  creará  una  autoridad  de certificados locales (local Certificate Authority), certificados y claves para el master, y se abrirá el socket de red adecuado para recibir las conexiones del cliente #flashcard
		  id:: bee7efbe-8a7d-4876-9e42-e34b2e19e7a7
		- (Page 20)
	- -
	- -
		- Toda la funcionalidad de Puppet está disponible a partir de un único fichero binario, como ocurre en otras herramientas como GIT, en lugar de los binarios individuales para cada función utilizados en las versiones iniciales de Puppet.
		  
		  Por ello, es posible arrancar el Puppet Master de esta forma:
		- (Page 21)
	- -
	- -
		- El  daemon  del  agente  de Puppet es ejecutado utilizando el comando puppet agent y se puede ver la conexión iniciada con el Master en el siguiente listado (también se puede ejecutar el  cliente Puppet  en  el  propio  Puppet  Master,  pero  vamos  a  comenzar  con  la  forma  más tradicional cliente-servidor): verbose node1# puppet agent --server=puppet.ejemplo.edu --no-daemonize info: Creating a new certificate request for nodo1.ejemplo.edu info: Creating a new SSL key at /var/lib/puppet/ssl/private_keys/nodo1.ejemplo.edu .pem warning: peer certificate won't be verified in this SSL session notice: Did not receive certificate Nota: Si no se especifica el servidor, Puppet buscará por defecto un host llamado puppet. Por lo general es recomendable definir un CNAME para el Puppet Master, tal como:  puppet.ejemplo.edu #flashcard
		  id:: e9dabb19-c893-4fdd-a307-8642b37abbb2
		- (Page 22)
	- -
	- -
		- Para autenticar las conexiones entre el Master y los agentes, Puppet hace uso de certificados SSL.
		  id:: 656ef86d-5bef-489c-bc54-739a364c367f
		  
		  En las últimas versiones de Puppet se soporta tanto una arquitectura de CA (autoridad certificadora) simple, con un certificado raíz autofirmado que también se utiliza para firmar, como una arquitectura de CA intermedia, con un certificado raíz autofirmado que emite un certificado CA intermedio que se utiliza para firmar las peticiones entrantes de certificado.
		  
		  La arquitectura con CA intermedia es la recomendada, ya que es más segura y facilita la regeneración de certificados. #flashcard
		- (Page 23)
	- -
	- -
		- Podemos definir esto mismo en el fichero /etc/puppet/puppet.conf de configuración del agente, en la sección principal: [main] server=puppet.ejemplo.edu #flashcard
		  id:: 8dcc483b-2b51-417c-a3ea-78d1526005b1
		- (Page 23)
	- -
	- -
		- Para generar una CA intermedia para el servidor Puppet se debe ejecutar el siguiente comando antes de iniciar el servidor por primera vez: puppetserver ca setup #flashcard
		  id:: 76ad8446-d0b0-4629-bffe-18ede90fbb73
		- (Page 23)
	- -
	- -
		- firmar el certificado que el agente envió al Master. Esto se hace mediante puppet cert   en el Master: puppet# puppetserver ca list nodo1.ejemplo.edu La acción list muestra todos los certificados que están a la espera de ser firmados, tras lo que procederemos a firmarlo mediante la acción sign. puppet# puppetserver ca sign --certname nodo1.ejemplo.edu Signed nodo1.ejemplo.edu Puppet también permite activar el modo autosign, en el que, en lugar de firmar cada certificado individualmente, todos los certificados provenientes de direcciones IP o rangos  de  direcciones  especificadas  se  firmarán  automáticamente #flashcard
		  id:: 5c8c2284-1a15-4564-b72b-6a4acd01b442
		- (Page 24)
	- -