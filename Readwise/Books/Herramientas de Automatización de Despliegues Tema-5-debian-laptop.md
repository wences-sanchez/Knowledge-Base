# Herramientas de Automatización de Despliegues Tema-5

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-5]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-5"\
category:: #books\
\
tags:: UNI Herramientas-de-Automatización-de-Despliegues  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/e24dfa32-8bce-4c9c-b79d-96b8e71ec1b9.jpg)
## Highlights
- id:: 6363991c-e1f8-4f98-998c-9f1c56f52be7
  
  Ansible aprovecha el protocolo SSH para ejecutar sus comandos de forma remota en las máquinas que gestiona, por lo que no requiere la instalación de ningún otro protocolo o sistema de comunicación. #flashcard 
  
  
     (Page 5)
-
- id:: 6363991c-0250-4ba2-80f2-50e8a8847e8d
  
  Esto supone una gran ventaja, debido a: Las máquinas gestionadas van a ejecutar exclusivamente la aplicación o aplicaciones que le correspondan, sin ningún otro proceso ejecutándose en segundo plano que compita por la CPU y memoria de la máquina. Al hacer uso de SSH, toda su funcionalidad está disponible para aprovecharla. Puedes, por ejemplo, utilizar un host como máquina de salto para alcanzar otro host. Además, #flashcard 
  
  
     (Page 5)
-
- id:: 6363991c-b525-456f-83d7-64b48cc64cc0
  
  no existe la necesidad de incluir un mecanismo de autenticación propio; puedes utilizar el que te proporciona SSH. #flashcard 
  
  
     (Page 6)
-
- id:: 6363991c-406c-40a8-9ae6-6f22189cacd5
  
  Ansible, por el contrario, no necesita utilizar un servidor centralizado al que se conecten los agentes desplegados en las máquinas a gestionar, ya que no necesita el uso de agentes; es, por tanto, agentless. #flashcard 
  
  
     (Page 6)
-
- id:: 6363991c-2398-415a-87a8-f061c688d76a
  
  Este modelo tiene ventajas e inconvenientes; la ventaja principal es que, una vez que haces cambios, puedes enviarlos inmediatamente a las máquinas, sin esperar a que un proceso demonio (el agente) compruebe si hay cambios. La desventaja es que tú eres el responsable de distribuir esos cambios a tus máquinas, mientras que con Puppet y Chef basta simplemente con guardar (commit) tus cambios en el servidor centralizado, teniendo la certeza de que serán distribuidos pronto. Cabe destacar que Ansible puede configurarse para utilizar este modelo de funcionamiento pull, pero no es lo más habitual. #flashcard 
  
  
     (Page 7)
-
- id:: 6363991c-22c2-4363-85ba-fad84455cde4
  
  $ mkdir ansible‐test && cd ansible‐test $ vagrant init ubuntu/bionic64 A `Vagrantfile` has been placed in this directory. You are now ready to `vagrant up` your first virtual environment! Please read the comments in the Vagrantfile as well as documentation on `vagrantup.com` for more information on using Vagrant. #flashcard 
  
  
     (Page 11)
-
- id:: 6363991c-c6c2-470b-a099-8fbfe7ceb314
  
  por defecto las máquinas que se crean tienen asignados 489 MB de memoria RAM. Esta cantidad de memoria es escasa para nuestro cometido, por lo que vamos a aumentarla a 1024 MB de memoria para trabajar con cierta fluidez, así que edita el Vagranfile e incluye el siguiente fragmento antes de la última línea que contiene la palabra end: config.vm.provider "virtualbox" do |vb| vb.memory = "1024" end #flashcard 
  
  
     (Page 14)
-
- id:: 6363991c-b82e-4ecb-8236-02013ee5e8c9
  
  Para además indicarle a Vagrant que el aprovisionamiento de esta máquina virtual lo realizaremos mediante Ansible, es necesario incluir en el archivo de configuración de Vagrant el siguiente fragmento, también antes de la última línea con end: config.vm.provision "ansible" do |ansible| ansible.playbook ="provisioning/playbook.yml" end #flashcard 
  
  
     (Page 14)
-
- id:: 6363991c-4596-437f-84d8-475561babfbc
   config.vm.provision "ansible" do |ansible|
   ansible.playbook ="provisioning/playbook.yml"
   end #flashcard 
    Esto le dice a Vagrant que utilice Ansible para aprovisionar la máquina virtual, ejecutando el playbook que se llama playbook.yml dentro de un subdirectorio provisioning que se encuentra en el directorio actual (ruta relativa).
  
     (Page 15)
-
- id:: 6363991c-1804-43c6-a7df-9752179d2a06
  
  Si Ansible no está instalado en tu máquina (por ejemplo, porque utilices Windows como sistema operativo), necesitas utilizar el aprovisionamiento con ansible_local, tal como: end config.vm.provision "ansible_local" do |ansible| ansible.playbook ="provisioning/playbook.yml" #flashcard 
  
  
     (Page 15)
-
- id:: 6363991c-b1de-497b-b8f1-f89bd321a525
  
  La diferencia entre estos dos fragmentos de configuración de Vagrant es que uno utiliza ansible, mientras que el otro, ansible_local. Al utilizar ansible estarás ejecutando Ansible desde tu máquina host para aplicar el playbook sobre la máquina virtual, mientras que con ansible_local lo ejecutará desde dentro de la máquina virtual. Vagrant se encargará de la instalación y la configuración de Ansible dentro de la máquina virtual automáticamente para poder realizar el aprovisionamiento. #flashcard 
  
  
     (Page 15)
-
- id:: 6363991c-3ea5-40d3-a937-e9c93d0c7e14
  
  Los archivos YAML comienzan por definir una sección de metadatos (habitualmente conocida como asunto frontal – front matter). Dado que no es necesario añadir ningún metadato, no escribiremos nada en esta sección e iniciaremos nuestro playbook con tres guiones seguidos en una sola línea (que indican el final de la sección de metadatos, que está vacía en nuestro caso). #flashcard 
  
  
     (Page 17)
-
- id:: 6363991c-acad-490a-be42-8baf971077f9
  
  El atributo state admite cualquier valor de una lista de posibles valores, incluyendo latest, present y absent. #flashcard 
  
  
     (Page 20)
-
- id:: 6363991c-0424-4dbf-8476-0f89b0c2342b
  
  El atributo update_cache indica a Ansible que actualice la caché del gestor de paquetes primero #flashcard 
  
  
     (Page 20)
-
- id:: 6363991c-327d-4b45-a793-5018bb6fd040
  
  ‐ name: Install PHP become: true apt: name=php5‐cli state=present update_cache=yes #flashcard 
  
  
     (Page 21)
-
- id:: 6363991c-4ba0-44d5-9ed1-ccf5061231a6
  
  ‐‐‐ ‐ hosts: all become: true tasks: ‐ name: Install required packages apt: state: present update_cache: yes name: #flashcard 
  
  
     (Page 23)
-
- id:: 6363991c-9f9f-4a90-8e7a-3486eaa2e5d1
  
  ‐ php ‐ nginx ‐ mysql‐server #flashcard 
  
  
     (Page 24)
-