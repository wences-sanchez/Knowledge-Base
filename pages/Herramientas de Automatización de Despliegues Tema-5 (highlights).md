title:: Herramientas de Automatización de Despliegues Tema-5 (highlights)
deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-5]]
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-5"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/e24dfa32-8bce-4c9c-b79d-96b8e71ec1b9.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Ansible aprovecha el protocolo SSH para ejecutar sus comandos de forma remota en las máquinas que gestiona, por lo que no requiere la instalación de ningún otro protocolo o sistema de comunicación. #flashcard
		  id:: c851941f-a58f-4297-b2d4-dba0ef4a08d4
		- (Page 5)
	- -
	- -
		- Esto supone una gran ventaja, debido a: Las máquinas gestionadas van a ejecutar exclusivamente la aplicación o aplicaciones que le correspondan, sin ningún otro proceso ejecutándose en segundo plano que compita por la CPU y memoria de la máquina. Al hacer uso de SSH, toda su funcionalidad está disponible para aprovecharla. Puedes, por ejemplo, utilizar un host como máquina de salto para alcanzar otro host. Además, #flashcard
		  id:: beeeab1d-ebae-4a66-b2ab-c3079a2b3795
		- (Page 5)
	- -
	- -
		- no  existe  la  necesidad  de  incluir  un  mecanismo  de  autenticación  propio;  puedes utilizar el que te proporciona SSH. #flashcard
		  id:: debca280-b1b9-43a5-a088-5e3757ea63a3
		- (Page 6)
	- -
	- -
		- Ansible, por el contrario, no necesita utilizar un servidor centralizado al que  se  conecten  los  agentes  desplegados  en  las  máquinas  a  gestionar,  ya  que  no necesita el uso de agentes; es, por tanto, agentless. #flashcard
		  id:: 95c06b0b-f8d2-4c97-934c-b4e962559e95
		- (Page 6)
	- -
	- -
		- Este modelo tiene ventajas e inconvenientes; la ventaja principal es que, una vez que haces cambios, puedes enviarlos inmediatamente a las máquinas, sin esperar a que un proceso demonio (el agente) compruebe si hay cambios. La desventaja es que tú eres  el  responsable  de  distribuir  esos  cambios  a  tus  máquinas,  mientras  que  con Puppet y Chef basta simplemente con guardar (commit) tus cambios en el servidor centralizado, teniendo la certeza de que serán distribuidos pronto. Cabe destacar que Ansible puede configurarse para utilizar este modelo de funcionamiento pull, pero no es lo más habitual. #flashcard
		  id:: 41cffda9-bad2-4a1a-a60b-cd32389b3554
		- (Page 7)
	- -
	- -
		- $ mkdir ansible‐test && cd ansible‐test $ vagrant init ubuntu/bionic64 A `Vagrantfile` has been placed in this directory. You are now ready to `vagrant up` your first virtual environment! Please read the comments in the Vagrantfile as well as documentation on `vagrantup.com` for more information on using Vagrant. #flashcard
		  id:: 2c3e5e4b-16c7-4aef-83be-fd1b343dc441
		- (Page 11)
	- -
	- -
		- por  defecto  las máquinas que se crean tienen asignados 489 MB de memoria RAM. Esta cantidad de memoria es escasa para nuestro cometido, por lo que vamos a aumentarla a 1024 MB de memoria para trabajar con cierta fluidez, así que edita el Vagranfile e incluye el siguiente fragmento antes de la última línea que contiene la palabra  end: config.vm.provider "virtualbox" do |vb| vb.memory = "1024" end #flashcard
		  id:: 5dc87d63-cf28-4faf-aa83-6b6aa1196ae1
		- (Page 14)
	- -
	- -
		- Para además indicarle a Vagrant que el aprovisionamiento de esta máquina virtual lo realizaremos mediante Ansible, es necesario incluir en el archivo de configuración de Vagrant el siguiente fragmento, también antes de la última línea con end: config.vm.provision "ansible" do |ansible| ansible.playbook ="provisioning/playbook.yml" end #flashcard
		  id:: 80a47aab-c3fb-4668-9a60-9ac19107c4c8
		- (Page 14)
	- -
	- -
		- config.vm.provision "ansible" do |ansible|
		  id:: 0b0ca2e9-7645-48e8-ab88-067b61c26b08
		  ansible.playbook ="provisioning/playbook.yml"
		  end #flashcard
			- Esto  le  dice  a  Vagrant  que  utilice  Ansible  para  aprovisionar  la  máquina  virtual, ejecutando  el  playbook  que  se  llama  playbook.yml  dentro  de  un  subdirectorio provisioning que se encuentra en el directorio actual (ruta relativa).
		- (Page 15)
	- -
	- -
		- Si Ansible no está instalado en tu máquina (por ejemplo, porque utilices Windows como sistema operativo), necesitas utilizar el aprovisionamiento con ansible_local, tal como: end config.vm.provision "ansible_local" do |ansible| ansible.playbook ="provisioning/playbook.yml" #flashcard
		  id:: fbfc63dc-d102-4ceb-87cb-069b3b17f0ad
		- (Page 15)
	- -
	- -
		- La  diferencia  entre  estos  dos  fragmentos  de  configuración  de  Vagrant  es  que  uno utiliza  ansible,  mientras  que  el  otro,  ansible_local.  Al  utilizar  ansible  estarás ejecutando Ansible desde tu máquina host para aplicar el playbook sobre la máquina virtual,  mientras  que  con  ansible_local  lo  ejecutará  desde  dentro  de  la  máquina virtual. Vagrant se encargará de la instalación y la configuración de Ansible dentro de la máquina virtual automáticamente para poder realizar el aprovisionamiento. #flashcard
		  id:: c9ecddc0-8c26-40fc-ac43-1c78a6aab1af
		- (Page 15)
	- -
	- -
		- Los archivos YAML comienzan por definir una sección de metadatos (habitualmente conocida  como  asunto  frontal  –  front  matter).  Dado  que  no  es  necesario  añadir ningún  metadato,  no  escribiremos  nada  en  esta  sección  e  iniciaremos  nuestro playbook con tres guiones seguidos en una sola línea (que indican el final de la sección de metadatos, que está vacía en nuestro caso). #flashcard
		  id:: 7d3069f5-3f88-4530-ae8f-f8c05b5b4f13
		- (Page 17)
	- -
	- -
		- El atributo state admite cualquier valor de una lista de posibles valores, incluyendo latest, present y absent. #flashcard
		  id:: c3782a8c-ea80-4a18-8207-f6a1f6e246c3
		- (Page 20)
	- -
	- -
		- El  atributo  update_cache  indica  a  Ansible  que  actualice  la  caché  del  gestor  de paquetes  primero #flashcard
		  id:: 69764171-d889-4486-8f82-3f7250eb80f3
		- (Page 20)
	- -
	- -
		- ‐  name: Install PHP become: true apt: name=php5‐cli state=present update_cache=yes #flashcard
		  id:: cc256811-1e0b-449b-a24a-98e8c372e5e0
		- (Page 21)
	- -
	- -
		- ‐‐‐ ‐ hosts: all become: true tasks: ‐ name: Install required packages apt: state: present update_cache: yes name: #flashcard
		  id:: 97de5b27-3d6e-4b43-9668-f11783aab494
		- (Page 23)
	- -
	- -
		- ‐ php ‐ nginx ‐ mysql‐server #flashcard
		  id:: 6199b5fd-b8db-4205-8d9b-61a0c1c69e74
		- (Page 24)
	- -