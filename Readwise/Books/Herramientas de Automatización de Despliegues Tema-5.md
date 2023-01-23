# Herramientas de Automatización de Despliegues Tema-5

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-5]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-5"\
category:: #books\
\
tags:: Herramientas-de-Automatización-de-Despliegues UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/e24dfa32-8bce-4c9c-b79d-96b8e71ec1b9.jpg)
## Highlights
- id:: 63c66a05-2023-4447-94b9-42c82cb0845c
  
  Ansible aprovecha el protocolo SSH para ejecutar sus comandos de forma remota en las máquinas que gestiona, por lo que no requiere la instalación de ningún otro protocolo o sistema de comunicación. #flashcard 
  
  
     (Page 5)
-
- id:: 63c66a05-3494-4004-987b-ec188902595c
  
  Esto supone una gran ventaja, debido a: Las máquinas gestionadas van a ejecutar exclusivamente la aplicación o aplicaciones que le correspondan, sin ningún otro proceso ejecutándose en segundo plano que compita por la CPU y memoria de la máquina. Al hacer uso de SSH, toda su funcionalidad está disponible para aprovecharla. Puedes, por ejemplo, utilizar un host como máquina de salto para alcanzar otro host. Además, #flashcard 
  
  
     (Page 5)
-
- id:: 63c66a05-621a-44b4-9c16-eee054756bc8
  
  no existe la necesidad de incluir un mecanismo de autenticación propio; puedes utilizar el que te proporciona SSH. #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a05-e387-4214-a5db-99924d5b9159
  
  Ansible, por el contrario, no necesita utilizar un servidor centralizado al que se conecten los agentes desplegados en las máquinas a gestionar, ya que no necesita el uso de agentes; es, por tanto, agentless. #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a05-695f-4425-8be6-93e6969e8dcd
  
  Este modelo tiene ventajas e inconvenientes; la ventaja principal es que, una vez que haces cambios, puedes enviarlos inmediatamente a las máquinas, sin esperar a que un proceso demonio (el agente) compruebe si hay cambios. La desventaja es que tú eres el responsable de distribuir esos cambios a tus máquinas, mientras que con Puppet y Chef basta simplemente con guardar (commit) tus cambios en el servidor centralizado, teniendo la certeza de que serán distribuidos pronto. Cabe destacar que Ansible puede configurarse para utilizar este modelo de funcionamiento pull, pero no es lo más habitual. #flashcard 
  
  
     (Page 7)
-
- id:: 63c66a05-3438-41a3-9752-c6885f7fbce9
  
  $ mkdir ansible‐test && cd ansible‐test $ vagrant init ubuntu/bionic64 A `Vagrantfile` has been placed in this directory. You are now ready to `vagrant up` your first virtual environment! Please read the comments in the Vagrantfile as well as documentation on `vagrantup.com` for more information on using Vagrant. #flashcard 
  
  
     (Page 11)
-
- id:: 63c66a05-bc2e-4eda-9f9d-587aea1af1e7
  
  por defecto las máquinas que se crean tienen asignados 489 MB de memoria RAM. Esta cantidad de memoria es escasa para nuestro cometido, por lo que vamos a aumentarla a 1024 MB de memoria para trabajar con cierta fluidez, así que edita el Vagranfile e incluye el siguiente fragmento antes de la última línea que contiene la palabra end: config.vm.provider "virtualbox" do |vb| vb.memory = "1024" end #flashcard 
  
  
     (Page 14)
-
- id:: 63c66a05-250d-45b0-972d-4d9464cb6be7
  
  Para además indicarle a Vagrant que el aprovisionamiento de esta máquina virtual lo realizaremos mediante Ansible, es necesario incluir en el archivo de configuración de Vagrant el siguiente fragmento, también antes de la última línea con end: config.vm.provision "ansible" do |ansible| ansible.playbook ="provisioning/playbook.yml" end #flashcard 
  
  
     (Page 14)
-
- id:: 63c66a05-d281-486a-a1b5-10011ab87e2d
   config.vm.provision "ansible" do |ansible|
   ansible.playbook ="provisioning/playbook.yml"
   end #flashcard 
    Esto le dice a Vagrant que utilice Ansible para aprovisionar la máquina virtual, ejecutando el playbook que se llama playbook.yml dentro de un subdirectorio provisioning que se encuentra en el directorio actual (ruta relativa).
  
     (Page 15)
-
- id:: 63c66a05-502b-46b2-af58-b9304555906f
  
  Si Ansible no está instalado en tu máquina (por ejemplo, porque utilices Windows como sistema operativo), necesitas utilizar el aprovisionamiento con ansible_local, tal como: end config.vm.provision "ansible_local" do |ansible| ansible.playbook ="provisioning/playbook.yml" #flashcard 
  
  
     (Page 15)
-
- id:: 63c66a05-6a5f-4e28-9bdd-cdd6f0d840b2
  
  La diferencia entre estos dos fragmentos de configuración de Vagrant es que uno utiliza ansible, mientras que el otro, ansible_local. Al utilizar ansible estarás ejecutando Ansible desde tu máquina host para aplicar el playbook sobre la máquina virtual, mientras que con ansible_local lo ejecutará desde dentro de la máquina virtual. Vagrant se encargará de la instalación y la configuración de Ansible dentro de la máquina virtual automáticamente para poder realizar el aprovisionamiento. #flashcard 
  
  
     (Page 15)
-
- id:: 63c66a05-c927-4f65-86f3-1eecf36b9009
  
  Los archivos YAML comienzan por definir una sección de metadatos (habitualmente conocida como asunto frontal – front matter). Dado que no es necesario añadir ningún metadato, no escribiremos nada en esta sección e iniciaremos nuestro playbook con tres guiones seguidos en una sola línea (que indican el final de la sección de metadatos, que está vacía en nuestro caso). #flashcard 
  
  
     (Page 17)
-
- id:: 63c66a05-c597-46a9-8db1-8ca90c7ee430
  
  El atributo state admite cualquier valor de una lista de posibles valores, incluyendo latest, present y absent. #flashcard 
  
  
     (Page 20)
-
- id:: 63c66a05-8183-4df8-98a8-59ef620a2349
  
  El atributo update_cache indica a Ansible que actualice la caché del gestor de paquetes primero #flashcard 
  
  
     (Page 20)
-
- id:: 63c66a05-44b5-462b-bd28-ef0429d3286a
  
  ‐ name: Install PHP become: true apt: name=php5‐cli state=present update_cache=yes #flashcard 
  
  
     (Page 21)
-
- id:: 63c66a05-c359-44bf-9c83-65c35a7b437a
  
  ‐‐‐ ‐ hosts: all become: true tasks: ‐ name: Install required packages apt: state: present update_cache: yes name: #flashcard 
  
  
     (Page 23)
-
- id:: 63c66a05-0f12-429c-a7e1-9b34c139479a
  
  ‐ php ‐ nginx ‐ mysql‐server #flashcard 
  
  
     (Page 24)
-