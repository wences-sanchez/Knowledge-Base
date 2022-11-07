title:: Herramientas de Automatización de Despliegues Tema-2 (highlights)
deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-2]]
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-2"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/770418a5-40f8-49ee-9b6c-21554abd0a87.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- El comando import indica a Puppet que debe cargar un archivo llamado nodes.pp , ya
		  id:: 710b00bd-3de0-48fb-b83b-7a81fdc6bfbd
		  que este comando nos permite importar otro manifiesto de Puppet dentro de
		  nuestro archivo. #flashcard
			- Import 'nodes.pp' $servidorpuppet = 'puppet.ejemplo.edu'
		- (Page 5)
	- -
	- -
		- Cabe señalar que en los manifiestos de Puppet, tal como ocurre en muchos sistemas operativos, las cadenas de caracteres entre comillas dobles permiten la sustitución de las variables, mientras que las cadenas entre comillas simples, no. Si deseas utilizar el valor de una variable dentro de la cadena, debes declarar la cadena entre comillas, como por ejemplo: “Esto es una cadena $variable”. También se puede encerrar el nombre de la variable entre llaves, ${variable}, para definirla más claramente. #flashcard
		  id:: 658fa21c-5ee8-4a60-8461-486ddc3d3367
		- (Page 6)
	- -
	- -
		- Un módulo consta de una estructura de directorios concreta y un archivo principal llamado init.pp, que será el punto de entrada. Esta estructura permite que Puppet pueda  cargar  módulos  de  forma  automática,  para  lo  cual  Puppet  revisará  los directorios que se hayan especificado mediante las rutas de módulos. Estas rutas de módulos  se  configuran  en  el  fichero  puppet.conf  mediante la  opción  de configuración  modulepath  dentro  de  la  sección  [main].  Por  defecto,  Puppet comprobará los directorios  /etc/puppet/modules  y  /var/lib/puppet/modules  en busca  de  módulos,  pero  se  pueden  personalizar  las  rutas  mediante  la  opción  de configuración: [main] moduledir = /etc/puppet/modules:/var/lib/puppet/modules:/opt/modules Esta carga automática de módulos nos permite no tener que incluirlos explícitamente mediante la directiva import, a diferencia de lo que pasa con el fichero nodes.pp. #flashcard
		  id:: 45ad205e-9490-4dd9-9c8e-1c700d9b951a
		- (Page 9)
	- -
	- -
		- # mkdir -p /etc/puppet/modules/sudo/{files,templates,manifests} # touch /etc/puppet/modules/sudo/manifests/init.pp #flashcard
		  id:: 0fa82e2f-bf5d-4528-b457-b7b57618e119
		- (Page 10)
	- -
	- -
		- los  módulos  son  colecciones  portables  y reutilizables, que permiten encapsular las configuraciones y compartirlas. Puppet  Forge  es  el  repositorio  que  proporciona  Puppet  para  tal  fin,  en  el  que podremos encontrar miles de módulos compartidos por desarrolladores de Puppet y por la propia comunidad. Todos estos módulos están disponibles para  descargar e instalar en nuestro entorno Puppet y aprovechar sus funcionalidades. También  puedes  compartir  en  Puppet  Forge  tus  propios  módulos,  sobre  los  que podrás recibir contribuciones, y podrás mantener y liberar versiones sucesivas. #flashcard
		  id:: 635faaa9-a142-4297-b4c1-68486de4fc3c
		- (Page 12)
	- -
	- -
		- class sudo { package {sudo: ensure => present, } if $operatingsystem == "Ubuntu" { package {"sudo-ldap": ensure => present, require => Package["sudo"], } } file {"/etc/sudoers": owner  =>"root", group =>"root", #flashcard
		  id:: 0dc7e3b1-fe36-4280-b995-7c10a0bac1d2
		- (Page 12)
	- -
	- -
		- CONTINUE #flashcard
		  id:: 635faaa9-afe4-4843-9fbe-b1f147134601
			- mode => 0440, source =>"puppet://$servidorpuppet/modules/sudo/etc/sudoers", require => Package["sudo"], } }
		- (Page 13)
	- -
	- -
		- El  metaparámetro  require,  en  nuestro  caso,  sirve  para  definir  una  relación  de dependencia entre el recurso  Package[“sudo-ldap”] y el recurso  Package[“sudo”], por  lo  que  le  decimos  a  Puppet que el  recurso Package[“sudo”]  es prerrequisito (requerido)  por  Package[“sudo-ldap”  y,  por  ello,  el  recurso  Package[“sudo”]  se debe  instalar  en  primer  lugar.  La  utilización  del  metaparámetro  require  nos  sirve para  definir  el  flujo  y  precedencia  de  ejecución  de  los  diferentes  recursos  que hayamos definido. #flashcard
		  id:: d986fc26-bc89-4624-a199-1d8d3acc81cd
		- (Page 14)
	- -
	- -
		- puppet:///modules/sudo/etc/sudoers La siguiente parte del valor source  indica a Puppet cuál es la ubicación del fichero dentro del servidor, que equivale a la ruta de acceso a un recurso compartido en un servidor de ficheros de red. El primer directorio de la ruta es modules, que indica que el fichero en cuestión pertenece a un módulo, cuyo nombre será lo que aparece a continuación en la ruta, que en nuestro caso es sudo, para finalmente especificar la ubicación dentro del módulo donde se encuentra el fichero. #flashcard
		  id:: b5227bc5-00fa-4073-b20f-03097745f9d5
		- (Page 15)
	- -
	- -
		- config.vm.provision "shell", inline: <<-SHELL wget https://apt.puppetlabs.com/puppet6-release-bionic.deb sudo dpkg -i puppet6-release-bionic.deb sudo apt-get update sudo apt-get install -y puppet-agent SHELL #flashcard
		  id:: 8c472524-9165-4091-acbf-ce88f3d7c7fa
		- (Page 21)
	- -
	- -
		- config.vm.provision "puppet" do |puppet| puppet.module_path = "modules" puppet.manifests_path = "manifests"   # Default puppet.manifest_file = "default.pp"   # Default end El  primer  parámetro  del  provisionador  Puppet  indica  la  ruta  local  donde  están almacenados nuestros módulos, para poder hacer uso desde el fichero de manifiesto que se ejecute. Los valores establecidos para los dos siguientes parámetros son los #flashcard
		  id:: 30dfe888-ecd9-41fd-9180-c7921f470179
		- (Page 21)
	- -
	- -
		- CONTINUE #flashcard
		  id:: bfb557cd-5371-4617-908e-f0a69477277e
			- valores  por  defecto,  pero  hemos  querido  incluirlos  para  mostrar  las  opciones  más comunes de configuración a la hora de establecer un aprovisionamiento con Puppet.
		- (Page 22)
	- -
	- -
		- Vagrant.configure(2) do |config| config.vm.box = "ubuntu/bionic64" config.vm.network "private_network", ip: "192.168.33.10" config.vm.provider "virtualbox" do |vb| vb.memory = "1024" end config.vm.provision "shell", inline: <<-SHELL wget https://apt.puppetlabs.com/puppet6-release-bionic.deb sudo dpkg -i puppet6-release-bionic.deb sudo apt-get update sudo apt-get install -y puppet-agent SHELL config.vm.provision "puppet" do |puppet| puppet.module_path = "modules"        # Default puppet.manifests_path = "manifests"   # Default puppet.manifest_file = "default.pp"   # Default end end #flashcard
		  id:: e79cf27f-4d74-4f7f-ba8f-447b73f8b662
		- (Page 22)
	- -
	- -
		- Tal como hemos especificado en el fichero de configuración de Vagrant, necesitamos crear las rutas y ficheros que Vagrant va a buscar para aprovisionar mediante Puppet. Ejecuta los siguientes comandos desde el directorio de tu Vagranfile: Ahora vamos a editar el manifiesto con nuestro editor favorito en incluir lo siguiente: mkdir manifests && mkdir modules touch manifests/default.pp $document_root = '/vagrant' include apache Hemos definido una variable denominada document_root con el valor ‘/vagrant’ y a continuación  hemos  incluido  el  módulo  apache,  que  será  el  que  definamos  a continuación. Ya tenemos creado el directorio de los módulos, por lo que ahora tenemos que crear el  subdirectorio  correspondiente  a  nuestro  nuevo  módulo  apache,  y  ubicar  su manifiesto en la ruta apropiada del módulo: mkdir -p modules/apache/manifests cd modules/apache touch manifests/init.pp Aparte del directorio del módulo, hemos creado el directorio manifests e incluido ahí el fichero init.pp, que será el punto de entrada al módulo #flashcard
		  id:: d736ddcb-efca-45de-a492-5e9f530525fa
		- (Page 23)
	- -
	- -
		- class apache { exec { 'apt-update': command => '/usr/bin/apt-get update' Exec["apt-update"] -> Package <| |> package { 'apache2': ensure => installed, } } } #flashcard
		  id:: 096af339-7595-4435-ab72-feac140e3ec4
		- (Page 24)
	- -
	- -
		- file { '/etc/apache2/sites-enabled/000-default.conf': ensure => absent, require => Package['apache2'], file { '/etc/apache2/sites-available/vagrant.conf': content => template('apache/virtual-hosts.conf.erb'), require => File['/etc/apache2/sites-enabled/000-default.conf'], file { "/etc/apache2/sites-enabled/vagrant.conf": ensure  => link, target  => "/etc/apache2/sites-available/vagrant.conf", require => File['/etc/apache2/sites-available/vagrant.conf'], file { "${document_root}/index.html": ensure  => present, source => 'puppet:///modules/apache/index.html', require => File['/etc/apache2/sites-enabled/vagrant.conf'], } } } } #flashcard
		  id:: a012269a-8024-4281-9df0-f979e0617b44
		- (Page 25)
	- -
	- -
		- Como  podemos  apreciar,  aparece  un  par  de  veces  la  referencia  a  la  variable document_root que habíamos definido, mediante la sintaxis de plantillas Ruby: <%= @document_root %> Esto le indica a Puppet que debe sustituir esa referencia por el valor de la variable definida. Cabe señalar que en este caso también podemos ver otro tipo de referencia de variables, tal como ${APACHE_LOG_DIR}, pero esta sintaxis está referenciando una variable de entorno. Puppet no lo interpretará y lo copiará tal cual al fichero destino #flashcard
		  id:: 255c0621-bd50-4ef1-8a8f-4a81059faf31
		- (Page 27)
	- -
	- -
		- service { 'apache2': ensure => running, enable => true, hasstatus  => true, apache2 reload", } restart => "/usr/sbin/apachectl configtest && /usr/sbin/service #flashcard
		  id:: 93228b6a-6163-475e-9ab5-a8f015a09e1b
		- (Page 28)
	- -
	- -
		- file { "${document_root}/index.html": ensure  => present, source => 'puppet:///modules/apache/index.html', require => File['/etc/apache2/sites-enabled/vagrant.conf'], notify  => Service['apache2'], restart => "/usr/sbin/apachectl configtest && /usr/sbin/service } } service { 'apache2': ensure => running, enable => true, hasstatus  => true, apache2 reload", #flashcard
		  id:: 8f866713-0945-4f57-b7a3-13c8602cce19
		- (Page 30)
	- -