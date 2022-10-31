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
		- (Page 5)
	- -
	- -
	- ‐‐‐ ‐ hosts: all become: true tasks: ‐ name: Make sure we can connect ping: #flashcard
		- (Page 6)
	- -
	- -
	- ‐ name: Generate new root password command: openssl rand ‐hex 7 register: mysql_new_root_pass Aquí, hemos utilizado una característica de Ansible que no se había visto hasta ahora, que es el registro (register). Al usar register en una tarea, le decimos a Ansible que queremos guardar el valor de retorno de la ejecución de la tarea como una variable para poder utilizarlo posteriormente en un playbook. #flashcard
		- (Page 9)
	- -
	- -
	- La siguiente acción que vamos a realizar es la de quitar las bases de datos de prueba y  los  usuarios  anónimos.  Esto  es  fácil  de  hacer  en  Ansible  gracias  a  los  módulos mysql_db y mysql_user. Se debe hacer esto antes de cambiar la contraseña de root para que Ansible pueda realizar los cambios. Añade lo siguiente al playbook: ‐ name: Remove anonymous users mysql_user: name="" state=absent ‐ name: Remove test database mysql_db: name=test state=absent #flashcard
		- (Page 9)
	- -
	- -
	- ‐ "{{ansible_hostname}}" loop: ‐ 127.0.0.1 ‐ ::1 ‐ localhost ‐ name: Output new root password debug: msg="New root password is {{mysql_new_root_pass.stdout}}" Sería posible en MySQL tener una contraseña diferente por cada usuario y lugar de conexión  distinto.  Hemos  utilizado  loop  para  establecer  la  contraseña  de  cada nombre  de  host  que  se  refiere  a  la  propia  máquina  iterando  con  cada  uno  de  los valores  de la lista  de loop  y  sustituyéndolos  en  {{item}}, incluyendo ansible_hostname, una variable que se rellena automáticamente con el nombre de host  de  la  máquina  actual. #flashcard
		- (Page 10)
	- -
	- -
	- También es necesario indicarle a Ansible que procese esta plantilla y la copie en tu máquina  virtual;  esto  se  hace  mediante  el  módulo  template.  Para  ello,  añade  lo siguiente al playbook: ‐ name: Create my.cnf template: src=templates/mysql/my.cnf dest=/root/.my.cnf #flashcard
		- (Page 11)
	- -
	- -
	- Aunque es conveniente cambiar las contraseñas de root con cierta frecuencia, es probable que no desees hacerlo cada vez que ejecutas. Para  inhibir  este  comportamiento,  puedes  indicarle  a  Ansible  que  no  ejecute determinados comandos cuando exista un archivo específico. Ansible proporciona la opción creates para determinar si ya existe un archivo antes de ejecutar el módulo: ‐ name: Generate new root password command: openssl rand ‐hex 7 creates=/root/.my.cnf register: mysql_new_root_pass #flashcard
		- (Page 11)
	- -
	- -
	- ‐ name: Generate new root password command: openssl rand ‐hex 7 creates=/root/.my.cnf register: mysql_new_root_pass # If /root/.my.cnf doesn't exist and the command is run - debug: msg="New root password is {{mysql_new_root_pass.stdout}}" when: mysql_new_root_pass.changed # If /root/.my.cnf exists and the command is not run - debug: msg="No change to root password" when: not mysql_new_root_pass.changed #flashcard
		- (Page 12)
	- -
	- -
	- # nginx ‐ name: Install nginx apt: name=nginx state=present ‐ name: Start nginx service: name=nginx state=started #flashcard
		- (Page 14)
	- -
	- -
	- Podrías añadir la siguiente tarea para reiniciar NginX al final del playbook: ‐ name: Restart nginx service: name=nginx state=restarted #flashcard
		- (Page 17)
	- -
	- -
	- Sin embargo, esto haría que se reiniciase NginX cada vez que ejecutes el playbook. La mejor manera de trabajar en Ansible con procesos que necesitan un reinicio cuando cambia algún parámetro de su configuración es usar un manejador. Los manejadores son iguales que las tareas, pero no se ejecutan por orden de aparición en el playbook, sino  que  pueden  ser  invocados  desde  cualquier  otro  lugar.  Elimina  ahora  la  tarea Restart  nginx  si  la  habías  añadido  y  agrega  el  siguiente  fragmento  al  final  del playbook, al mismo nivel y sangría que tasks: handlers: ‐ name: restart nginx service: name=nginx state=restarted Este  código  usará  el  módulo  service  para  reiniciar  NginX  cuando  se  active  el manejador.  Puede  activarse  cada  vez  que  haya  cambios  en  el  archivo  de configuración, modificando la tarea de la configuración de esta forma: template: src=templates/nginx/default dest=/etc/nginx/sites ‐ name: Create nginx config available/default notify: restart nginx #flashcard
		- (Page 18)
	- -
	- -
	- Lo  siguiente  será  copiarlo  en  la  máquina  virtual  y,  dado  que  solo  lo  necesitas temporalmente, lo puedes copiar en el directorio /tmp mediante la siguiente tarea: # Wordpress ‐ name: Copy wordpress.zip into tmp copy: src=files/wordpress.zip dest=/tmp/wordpress.zip #flashcard
		- (Page 20)
	- -
	- -
	- Ansible proporciona un módulo denominado unarchive que sabe cómo extraer los formatos de archivo comprimido más comunes: ‐ name: Unzip WordPress unarchive: src=/tmp/wordpress.zip dest=/tmp copy=no creates=/tmp/wordpress/wp‐settings.php #flashcard
		- (Page 22)
	- -
	- -
	- ‐ name: Install required tools apt: name={{item}} state=present loop: ‐ unzip #flashcard
		- (Page 23)
	- -
	- -
	- ‐ name: Create project folder file: dest=/var/www/book.example.com state=directory ‐ name: Copy WordPress files copy: source=/tmp/wordpress/. dest=/var/www/book.example.com #flashcard
		- (Page 24)
	- -
	- -
	- ‐ name: Create WordPress MySQL database mysql_db: name=wordpress state=present ‐ name: Create WordPress MySQL user mysql_user: name=wordpress host=localhost password=bananas priv=wordpress.*:ALL #flashcard
		- (Page 24)
	- -