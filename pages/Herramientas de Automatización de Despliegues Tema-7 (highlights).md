title:: Herramientas de Automatización de Despliegues Tema-7 (highlights)
deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-7]]
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-7"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/07c80289-0eec-4d82-a65b-43554716fbac.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- el archivo Vagrantfile contendrá lo que sigue: Vagrant.configure(2) do |config| config.vm.box = "ubuntu/bionic64" config.vm.network "private_network", ip: "192.168.33.20" config.vm.provider "virtualbox" do |vb| vb.memory = "1024" end config.vm.provision "ansible_local" do |ansible| ansible.playbook ="provisioning/playbook.yml" end end #flashcard
		  id:: 369b0059-4819-4da7-8231-dcd107079593
		- (Page 5)
	- -
	- -
		- ‐‐‐ ‐ hosts: all become: true tasks: ‐ name: Make sure we can connect ping: #flashcard
		  id:: 841fbfb2-5045-4e38-8954-2f717e0836ae
		- (Page 6)
	- -
	- -
		- ‐ name: Generate new root password command: openssl rand ‐hex 7 register: mysql_new_root_pass Aquí, hemos utilizado una característica de Ansible que no se había visto hasta ahora, que es el registro (register). Al usar register en una tarea, le decimos a Ansible que queremos guardar el valor de retorno de la ejecución de la tarea como una variable para poder utilizarlo posteriormente en un playbook. #flashcard
		  id:: 69ee1196-3a31-424e-9120-5bcac128d78b
		- (Page 9)
	- -
	- -
		- La siguiente acción que vamos a realizar es la de quitar las bases de datos de prueba y  los  usuarios  anónimos.  Esto  es  fácil  de  hacer  en  Ansible  gracias  a  los  módulos mysql_db y mysql_user. Se debe hacer esto antes de cambiar la contraseña de root para que Ansible pueda realizar los cambios. Añade lo siguiente al playbook: ‐ name: Remove anonymous users mysql_user: name="" state=absent ‐ name: Remove test database mysql_db: name=test state=absent #flashcard
		  id:: d39c70d2-5893-4bf1-b3b1-c91b77a3067c
		- (Page 9)
	- -
	- -
		- ‐ "{{ansible_hostname}}" loop: ‐ 127.0.0.1 ‐ ::1 ‐ localhost ‐ name: Output new root password debug: msg="New root password is {{mysql_new_root_pass.stdout}}" Sería posible en MySQL tener una contraseña diferente por cada usuario y lugar de conexión  distinto.  Hemos  utilizado  loop  para  establecer  la  contraseña  de  cada nombre  de  host  que  se  refiere  a  la  propia  máquina  iterando  con  cada  uno  de  los valores  de la lista  de loop  y  sustituyéndolos  en  {{item}}, incluyendo ansible_hostname, una variable que se rellena automáticamente con el nombre de host  de  la  máquina  actual. #flashcard
		  id:: 7e3a9d2f-718d-4603-8379-5561aab2be88
		- (Page 10)
	- -
	- -
		- También es necesario indicarle a Ansible que procese esta plantilla y la copie en tu máquina  virtual;  esto  se  hace  mediante  el  módulo  template.  Para  ello,  añade  lo siguiente al playbook: ‐ name: Create my.cnf template: src=templates/mysql/my.cnf dest=/root/.my.cnf #flashcard
		  id:: 3717c51d-6de2-4065-9219-9a1648c450e6
		- (Page 11)
	- -
	- -
		- Aunque es conveniente cambiar las contraseñas de root con cierta frecuencia, es probable que no desees hacerlo cada vez que ejecutas. Para  inhibir  este  comportamiento,  puedes  indicarle  a  Ansible  que  no  ejecute determinados comandos cuando exista un archivo específico. Ansible proporciona la opción creates para determinar si ya existe un archivo antes de ejecutar el módulo: ‐ name: Generate new root password command: openssl rand ‐hex 7 creates=/root/.my.cnf register: mysql_new_root_pass #flashcard
		  id:: f6d84c45-0f71-46cc-aa82-8b57cc72bb54
		- (Page 11)
	- -
	- -
		- ‐ name: Generate new root password command: openssl rand ‐hex 7 creates=/root/.my.cnf register: mysql_new_root_pass # If /root/.my.cnf doesn't exist and the command is run - debug: msg="New root password is {{mysql_new_root_pass.stdout}}" when: mysql_new_root_pass.changed # If /root/.my.cnf exists and the command is not run - debug: msg="No change to root password" when: not mysql_new_root_pass.changed #flashcard
		  id:: d1c87eb8-3b80-4dd5-95a8-7c4b6d4c4b23
		- (Page 12)
	- -
	- -
		- # nginx ‐ name: Install nginx apt: name=nginx state=present ‐ name: Start nginx service: name=nginx state=started #flashcard
		  id:: 5549ad7e-4e06-49d3-8ba7-e5c7c94542cc
		- (Page 14)
	- -
	- -
		- Podrías añadir la siguiente tarea para reiniciar NginX al final del playbook: ‐ name: Restart nginx service: name=nginx state=restarted #flashcard
		  id:: c928ce8e-debc-4937-9ff1-634d86b294f8
		- (Page 17)
	- -
	- -
		- Sin embargo, esto haría que se reiniciase NginX cada vez que ejecutes el playbook. La mejor manera de trabajar en Ansible con procesos que necesitan un reinicio cuando cambia algún parámetro de su configuración es usar un manejador. Los manejadores son iguales que las tareas, pero no se ejecutan por orden de aparición en el playbook, sino  que  pueden  ser  invocados  desde  cualquier  otro  lugar.  Elimina  ahora  la  tarea Restart  nginx  si  la  habías  añadido  y  agrega  el  siguiente  fragmento  al  final  del playbook, al mismo nivel y sangría que tasks: handlers: ‐ name: restart nginx service: name=nginx state=restarted Este  código  usará  el  módulo  service  para  reiniciar  NginX  cuando  se  active  el manejador.  Puede  activarse  cada  vez  que  haya  cambios  en  el  archivo  de configuración, modificando la tarea de la configuración de esta forma: template: src=templates/nginx/default dest=/etc/nginx/sites ‐ name: Create nginx config available/default notify: restart nginx #flashcard
		  id:: 60c959f5-3411-4227-a4b6-97a5b41f9bb1
		- (Page 18)
	- -
	- -
		- Lo  siguiente  será  copiarlo  en  la  máquina  virtual  y,  dado  que  solo  lo  necesitas temporalmente, lo puedes copiar en el directorio /tmp mediante la siguiente tarea: # Wordpress ‐ name: Copy wordpress.zip into tmp copy: src=files/wordpress.zip dest=/tmp/wordpress.zip #flashcard
		  id:: 4848b4de-40c2-47bd-aa0c-4f5548a23beb
		- (Page 20)
	- -
	- -
		- Ansible proporciona un módulo denominado unarchive que sabe cómo extraer los formatos de archivo comprimido más comunes: ‐ name: Unzip WordPress unarchive: src=/tmp/wordpress.zip dest=/tmp copy=no creates=/tmp/wordpress/wp‐settings.php #flashcard
		  id:: 44f19ca5-8013-41e2-8593-ee78d7347411
		- (Page 22)
	- -
	- -
		- ‐ name: Install required tools apt: name={{item}} state=present loop: ‐ unzip #flashcard
		  id:: 5c24c34b-4a85-4d30-a125-e655ed160c67
		- (Page 23)
	- -
	- -
		- ‐ name: Create project folder file: dest=/var/www/book.example.com state=directory ‐ name: Copy WordPress files copy: source=/tmp/wordpress/. dest=/var/www/book.example.com #flashcard
		  id:: 320974bf-3e40-41ee-940b-180620fbc7cc
		- (Page 24)
	- -
	- -
		- ‐ name: Create WordPress MySQL database mysql_db: name=wordpress state=present ‐ name: Create WordPress MySQL user mysql_user: name=wordpress host=localhost password=bananas priv=wordpress.*:ALL #flashcard
		  id:: 9716f94f-7511-474c-86e5-7dad8a3cbd13
		- (Page 24)
	- -