# Herramientas de Automatización de Despliegues Tema-2

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-2]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-2"\
category:: #books\
\
tags:: Herramientas-de-Automatización-de-Despliegues UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/770418a5-40f8-49ee-9b6c-21554abd0a87.jpg)
## Highlights
- id:: 63c66a04-cfdd-4557-a94d-169a23f71783
   El comando import indica a Puppet que debe cargar un archivo llamado nodes.pp , ya
   que este comando nos permite importar otro manifiesto de Puppet dentro de
   nuestro archivo. #flashcard 
    Import 'nodes.pp' $servidorpuppet = 'puppet.ejemplo.edu'
  
     (Page 5)
-
- id:: 63c66a04-4d2a-4230-aa90-6bcf089e55ab
  
  Cabe señalar que en los manifiestos de Puppet, tal como ocurre en muchos sistemas operativos, las cadenas de caracteres entre comillas dobles permiten la sustitución de las variables, mientras que las cadenas entre comillas simples, no. Si deseas utilizar el valor de una variable dentro de la cadena, debes declarar la cadena entre comillas, como por ejemplo: “Esto es una cadena $variable”. También se puede encerrar el nombre de la variable entre llaves, ${variable}, para definirla más claramente. #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a04-975c-45af-aac5-cce151991960
  
  Un módulo consta de una estructura de directorios concreta y un archivo principal llamado init.pp, que será el punto de entrada. Esta estructura permite que Puppet pueda cargar módulos de forma automática, para lo cual Puppet revisará los directorios que se hayan especificado mediante las rutas de módulos. Estas rutas de módulos se configuran en el fichero puppet.conf mediante la opción de configuración modulepath dentro de la sección [main]. Por defecto, Puppet comprobará los directorios /etc/puppet/modules y /var/lib/puppet/modules en busca de módulos, pero se pueden personalizar las rutas mediante la opción de configuración: [main] moduledir = /etc/puppet/modules:/var/lib/puppet/modules:/opt/modules Esta carga automática de módulos nos permite no tener que incluirlos explícitamente mediante la directiva import, a diferencia de lo que pasa con el fichero nodes.pp. #flashcard 
  
  
     (Page 9)
-
-
# mkdir -p /etc/puppet/modules/sudo/{files,templates,manifests} # touch /etc/puppet/modules/sudo/manifests/init.pp #flashcard 
id:: 63c66a04-c413-403a-bba7-66197eb44fb9


   (Page 10)
-
- id:: 63c66a04-72d4-4ead-b52d-aa7284469a1f
  
  los módulos son colecciones portables y reutilizables, que permiten encapsular las configuraciones y compartirlas. Puppet Forge es el repositorio que proporciona Puppet para tal fin, en el que podremos encontrar miles de módulos compartidos por desarrolladores de Puppet y por la propia comunidad. Todos estos módulos están disponibles para descargar e instalar en nuestro entorno Puppet y aprovechar sus funcionalidades. También puedes compartir en Puppet Forge tus propios módulos, sobre los que podrás recibir contribuciones, y podrás mantener y liberar versiones sucesivas. #flashcard 
  
  
     (Page 12)
-
- id:: 63c66a04-1b8e-4462-8bd9-2dd6c03fc052
  
  class sudo { package {sudo: ensure => present, } if $operatingsystem == "Ubuntu" { package {"sudo-ldap": ensure => present, require => Package["sudo"], } } file {"/etc/sudoers": owner =>"root", group =>"root", #flashcard 
  
  
     (Page 12)
-
- id:: 63c66a04-f65f-4545-87c3-b68c5c3dc044
   CONTINUE #flashcard 
    mode => 0440, source =>"puppet://$servidorpuppet/modules/sudo/etc/sudoers", require => Package["sudo"], } }
  
     (Page 13)
-
- id:: 63c66a04-6720-47f7-b5c2-d2127f21cbee
  
  El metaparámetro require, en nuestro caso, sirve para definir una relación de dependencia entre el recurso Package[“sudo-ldap”] y el recurso Package[“sudo”], por lo que le decimos a Puppet que el recurso Package[“sudo”] es prerrequisito (requerido) por Package[“sudo-ldap” y, por ello, el recurso Package[“sudo”] se debe instalar en primer lugar. La utilización del metaparámetro require nos sirve para definir el flujo y precedencia de ejecución de los diferentes recursos que hayamos definido. #flashcard 
  
  
     (Page 14)
-
- id:: 63c66a04-d4ef-4731-bbb2-74cbe8f26200
  
  puppet:///modules/sudo/etc/sudoers La siguiente parte del valor source indica a Puppet cuál es la ubicación del fichero dentro del servidor, que equivale a la ruta de acceso a un recurso compartido en un servidor de ficheros de red. El primer directorio de la ruta es modules, que indica que el fichero en cuestión pertenece a un módulo, cuyo nombre será lo que aparece a continuación en la ruta, que en nuestro caso es sudo, para finalmente especificar la ubicación dentro del módulo donde se encuentra el fichero. #flashcard 
  
  
     (Page 15)
-
- id:: 63c66a04-635c-483b-9774-97a92c2ef887
  
  config.vm.provision "shell", inline: <<-SHELL wget https://apt.puppetlabs.com/puppet6-release-bionic.deb sudo dpkg -i puppet6-release-bionic.deb sudo apt-get update sudo apt-get install -y puppet-agent SHELL #flashcard 
  
  
     (Page 21)
-
- id:: 63c66a04-1881-4d95-b031-6dda476a693c
  
  config.vm.provision "puppet" do |puppet| puppet.module_path = "modules" puppet.manifests_path = "manifests" # Default puppet.manifest_file = "default.pp" # Default end El primer parámetro del provisionador Puppet indica la ruta local donde están almacenados nuestros módulos, para poder hacer uso desde el fichero de manifiesto que se ejecute. Los valores establecidos para los dos siguientes parámetros son los #flashcard 
  
  
     (Page 21)
-
- id:: 63c66a04-753e-4a8c-9888-4499f37226ab
   CONTINUE #flashcard 
    valores por defecto, pero hemos querido incluirlos para mostrar las opciones más comunes de configuración a la hora de establecer un aprovisionamiento con Puppet.
  
     (Page 22)
-
- id:: 63c66a04-a650-4e00-b4e4-2cf8e450d528
  
  Vagrant.configure(2) do |config| config.vm.box = "ubuntu/bionic64" config.vm.network "private_network", ip: "192.168.33.10" config.vm.provider "virtualbox" do |vb| vb.memory = "1024" end config.vm.provision "shell", inline: <<-SHELL wget https://apt.puppetlabs.com/puppet6-release-bionic.deb sudo dpkg -i puppet6-release-bionic.deb sudo apt-get update sudo apt-get install -y puppet-agent SHELL config.vm.provision "puppet" do |puppet| puppet.module_path = "modules" # Default puppet.manifests_path = "manifests" # Default puppet.manifest_file = "default.pp" # Default end end #flashcard 
  
  
     (Page 22)
-
- id:: 63c66a04-5ffa-43a5-b24b-e9dd729ee1c5
  
  Tal como hemos especificado en el fichero de configuración de Vagrant, necesitamos crear las rutas y ficheros que Vagrant va a buscar para aprovisionar mediante Puppet. Ejecuta los siguientes comandos desde el directorio de tu Vagranfile: Ahora vamos a editar el manifiesto con nuestro editor favorito en incluir lo siguiente: mkdir manifests && mkdir modules touch manifests/default.pp $document_root = '/vagrant' include apache Hemos definido una variable denominada document_root con el valor ‘/vagrant’ y a continuación hemos incluido el módulo apache, que será el que definamos a continuación. Ya tenemos creado el directorio de los módulos, por lo que ahora tenemos que crear el subdirectorio correspondiente a nuestro nuevo módulo apache, y ubicar su manifiesto en la ruta apropiada del módulo: mkdir -p modules/apache/manifests cd modules/apache touch manifests/init.pp Aparte del directorio del módulo, hemos creado el directorio manifests e incluido ahí el fichero init.pp, que será el punto de entrada al módulo #flashcard 
  
  
     (Page 23)
-
- id:: 63c66a04-c0df-424a-a230-c63d5e3d6c2d
  
  class apache { exec { 'apt-update': command => '/usr/bin/apt-get update' Exec["apt-update"] -> Package <| |> package { 'apache2': ensure => installed, } } } #flashcard 
  
  
     (Page 24)
-
- id:: 63c66a04-31ee-4d52-b55e-ef2a135e230f
  
  file { '/etc/apache2/sites-enabled/000-default.conf': ensure => absent, require => Package['apache2'], file { '/etc/apache2/sites-available/vagrant.conf': content => template('apache/virtual-hosts.conf.erb'), require => File['/etc/apache2/sites-enabled/000-default.conf'], file { "/etc/apache2/sites-enabled/vagrant.conf": ensure => link, target => "/etc/apache2/sites-available/vagrant.conf", require => File['/etc/apache2/sites-available/vagrant.conf'], file { "${document_root}/index.html": ensure => present, source => 'puppet:///modules/apache/index.html', require => File['/etc/apache2/sites-enabled/vagrant.conf'], } } } } #flashcard 
  
  
     (Page 25)
-
- id:: 63c66a04-0839-4624-bb23-cf43cf3e37b6
  
  Como podemos apreciar, aparece un par de veces la referencia a la variable document_root que habíamos definido, mediante la sintaxis de plantillas Ruby: <%= @document_root %> Esto le indica a Puppet que debe sustituir esa referencia por el valor de la variable definida. Cabe señalar que en este caso también podemos ver otro tipo de referencia de variables, tal como ${APACHE_LOG_DIR}, pero esta sintaxis está referenciando una variable de entorno. Puppet no lo interpretará y lo copiará tal cual al fichero destino #flashcard 
  
  
     (Page 27)
-
- id:: 63c66a04-8575-452a-a715-83c6a7458529
  
  service { 'apache2': ensure => running, enable => true, hasstatus => true, apache2 reload", } restart => "/usr/sbin/apachectl configtest && /usr/sbin/service #flashcard 
  
  
     (Page 28)
-
- id:: 63c66a04-ac4e-4f75-a8fa-368518d55ee3
  
  file { "${document_root}/index.html": ensure => present, source => 'puppet:///modules/apache/index.html', require => File['/etc/apache2/sites-enabled/vagrant.conf'], notify => Service['apache2'], restart => "/usr/sbin/apachectl configtest && /usr/sbin/service } } service { 'apache2': ensure => running, enable => true, hasstatus => true, apache2 reload", #flashcard 
  
  
     (Page 30)
-