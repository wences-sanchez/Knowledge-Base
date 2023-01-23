# Herramientas de Automatización de Despliegues Tema-1

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-1]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-1"\
category:: #books\
\
tags:: Herramientas-de-Automatización-de-Despliegues UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/1b21e990-d0c5-4240-b8e6-78a06a29ea4d.jpg)
## Highlights
- id:: 63c66a04-4077-4163-b4ae-e592c17d8427
  
  El diseño de Puppet está pensado para estar en continua interacción con las máquinas que gestiona, al contrario que otras herramientas de aprovisionamiento que únicamente se encargan de la etapa de construcción de las máquinas. #flashcard 
  
  
     (Page 5)
-
- id:: 63c66a04-0357-4c4b-af58-568bac75578c
    Lenguaje de configuración y capa de abstracción de recursos.  Capa transaccional. #flashcard 
    Puppet tiene un modelo de funcionamiento sencillo, fácil de entender y de aplicar, que se compone de tres componentes básicos:
	- Despliegue.
	- Lenguaje de configuración y capa de abstracción de recursos.
	- Capa transaccional.
	  
	       (Page 5)
-
- id:: 63c66a04-0b78-44cc-9926-05261a9b836b
  
  El proceso de Puppet Master se ejecuta como un daemon en el servidor, donde se almacena la configuración necesaria de todo el entorno gestionado. Los agentes se identifican con el servidor Puppet Master al conectarse y utilizan el estándar SSL para establecer un canal de comunicación cifrado, a través del cual se obtiene la configuración que se va a aplicar. #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a04-3a7c-452a-9c8d-bbe2a4d4a932
   ¿Cuál es la plantilla de un resource en Puppet? #flashcard 
    type { title :
     attribute => value,
     }
  
     (Page 9)
-
- id:: 63c66a04-09a8-415d-9112-4ad28042383f
  
  package {"vim": ensure => present, } #flashcard 
  
  
     (Page 9)
-
- id:: 63c66a04-3ac4-47b5-a385-2c189d6dfa3a
  
  Para utilizar el tipo y el título del recurso como referencia, Puppet nos permite unir el tipo de recurso con la primera letra en mayúscula seguido del nombre entre conchetes, como, por ejemplo: Package["vim"]. #flashcard 
  
  
     (Page 9)
-
- id:: 63c66a04-709a-4ea2-8e83-8404ef3e458f
   ¿Cómo se puede deshacer una transacción en Puppet? #flashcard 
    En Puppet, las transacciones no se registran (más allá de los registros informativos) y, por lo tanto, no se pueden deshacer como se hace con algunas bases de datos.
     Lo que sí podemos hacer es configurar estas transacciones en modo NOOP (del inglés no operation mode), lo que nos posibilita el probar la ejecución de la configuración sin realmente realizar ningún cambio
  
     (Page 11)
-
- id:: 63c66a04-2f66-4e30-afc1-82e8c67f6526
   ¿Cómo podemos ver los facts de Puppet para una máquina? #flashcard 
    Para ver los facts que están disponibles en cada máquina, podemos ejecutar directamente en ella el comando facter desde la línea de comandos.
  
     (Page 12)
-
- id:: 63c66a04-15b5-4775-86de-6280070fa560
  
  El directorio /etc/puppet es donde se guarda la configuración del Puppet Master, en la mayor parte de las plataformas. El fichero principal de configuración de Puppet se puede encontrar en la siguiente ruta: /etc/puppet/puppet.conf. Este fichero se crea habitualmente durante la instalación de Puppet, pero, si no es el caso, el siguiente comando nos permite crear el fichero: # puppetmasterd --genconfig > puppet.conf #flashcard 
  
  
     (Page 17)
-
- id:: 63c66a04-1e7d-4d82-9bdb-67230fc40db7
  
  El fichero puppet.conf tiene una estructura muy similar a los ficheros de configuración de formato INI, ya que está dividido en diferentes secciones. Cada una de las secciones se centra en configurar un aspecto concreto de Puppet. Por ejemplo, tenemos la sección del agente [agent] para establecer la configuración del agente y la sección de Puppet Master [master] para configura el servidor Master. También se encuentra una sección llamada [main] para configuración general. En esta sección se configuran opciones generales para todos los componentes de Puppet. Por ahora, no añadiremos en el fichero de puppet.conf nada más que una entrada, certname, para especificar el nombre del Puppet Master. Para ello, tenemos que añadir la entrada certname a la sección [master], que habrá que crearla en caso de que no exista todavía: [master] certname=puppet.ejemplo.edu #flashcard 
  
  
     (Page 18)
-
- id:: 63c66a04-c989-4db8-ac17-c58ff503e6a0
  
  El fichero site.pp es el que contiene las máquinas que se van a gestionar y la configuración que debe aplicar a estas.
     Este archivo suele almacenarse en el subdirectorio manifests dentro del directorio /etc/puppet/. #flashcard 
  
  
     (Page 19)
-
- id:: 63c66a04-24dd-46af-954f-9970751ba3c3
  
  Nota: los ficheros que Puppet maneja para la definición de la configuración de los recursos se denominan ficheros manifests (manifiestos). Un fichero manifest de Puppet tiene la extensión .pp. #flashcard 
  
  
     (Page 19)
-
- id:: 63c66a04-a77b-4f3c-87c4-014dd5255cfd
  
  mkdir/etc/puppet/manifests touch/etc/puppet/manifests/site.pp #flashcard 
  
  
     (Page 19)
-
- id:: 63c66a04-8df8-4cd3-8e8b-81d75312844f
  
  El Puppet Master puede iniciarse en la mayoría de las distribuciones de Linux mediante un script init de inicio de servicio. En Red Hat, ejecutaríamos el script de inicio con el comando service de esta forma: # service puppetmaster start En Debian o Ubuntu, lo ejecutamos con el comando invoke-rc.d: # invoke-rc.d puppetmaster start Si inicias el Daemon, se iniciará el entorno Puppet, se creará una autoridad de certificados locales (local Certificate Authority), certificados y claves para el master, y se abrirá el socket de red adecuado para recibir las conexiones del cliente #flashcard 
  
  
     (Page 20)
-
- Toda la funcionalidad de Puppet está disponible a partir de un único fichero binario, como ocurre en otras herramientas como GIT, en lugar de los binarios individuales para cada función utilizados en las versiones iniciales de Puppet.
     Por ello, es posible arrancar el Puppet Master de esta forma:
# puppet master
   Y para iniciar la funcionalidad del agente:
# puppet agent #flashcard 
id:: 63c66a04-62de-43da-9bfd-894c9aa5a8ed


   (Page 21)
-
- id:: 63c66a04-f155-4ef5-810c-6e779d581902
  
  El daemon del agente de Puppet es ejecutado utilizando el comando puppet agent y se puede ver la conexión iniciada con el Master en el siguiente listado (también se puede ejecutar el cliente Puppet en el propio Puppet Master, pero vamos a comenzar con la forma más tradicional cliente-servidor): verbose node1# puppet agent --server=puppet.ejemplo.edu --no-daemonize info: Creating a new certificate request for nodo1.ejemplo.edu info: Creating a new SSL key at /var/lib/puppet/ssl/private_keys/nodo1.ejemplo.edu .pem warning: peer certificate won't be verified in this SSL session notice: Did not receive certificate Nota: Si no se especifica el servidor, Puppet buscará por defecto un host llamado puppet. Por lo general es recomendable definir un CNAME para el Puppet Master, tal como: puppet.ejemplo.edu #flashcard 
  
  
     (Page 22)
-
- id:: 63c66a04-e25c-42f8-850e-75ddb0742f30
  
  Para autenticar las conexiones entre el Master y los agentes, Puppet hace uso de certificados SSL.
     En las últimas versiones de Puppet se soporta tanto una arquitectura de CA (autoridad certificadora) simple, con un certificado raíz autofirmado que también se utiliza para firmar, como una arquitectura de CA intermedia, con un certificado raíz autofirmado que emite un certificado CA intermedio que se utiliza para firmar las peticiones entrantes de certificado.
     La arquitectura con CA intermedia es la recomendada, ya que es más segura y facilita la regeneración de certificados. #flashcard 
  
  
     (Page 23)
-
- id:: 63c66a04-7dd1-4d96-beb0-7e3b025c463c
  
  Podemos definir esto mismo en el fichero /etc/puppet/puppet.conf de configuración del agente, en la sección principal: [main] server=puppet.ejemplo.edu #flashcard 
  
  
     (Page 23)
-
- id:: 63c66a04-f3f8-46e9-a25e-7fbaada15ab4
  
  Para generar una CA intermedia para el servidor Puppet se debe ejecutar el siguiente comando antes de iniciar el servidor por primera vez: puppetserver ca setup #flashcard 
  
  
     (Page 23)
-
- id:: 63c66a04-c21f-4c8e-b49c-b4e9e6202523
  
  firmar el certificado que el agente envió al Master. Esto se hace mediante puppet cert en el Master: puppet# puppetserver ca list nodo1.ejemplo.edu La acción list muestra todos los certificados que están a la espera de ser firmados, tras lo que procederemos a firmarlo mediante la acción sign. puppet# puppetserver ca sign --certname nodo1.ejemplo.edu Signed nodo1.ejemplo.edu Puppet también permite activar el modo autosign, en el que, en lugar de firmar cada certificado individualmente, todos los certificados provenientes de direcciones IP o rangos de direcciones especificadas se firmarán automáticamente #flashcard 
  
  
     (Page 24)
-