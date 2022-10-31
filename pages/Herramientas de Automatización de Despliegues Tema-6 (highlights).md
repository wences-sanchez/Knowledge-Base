title:: Herramientas de Automatización de Despliegues Tema-6 (highlights)
deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-6]]
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-6"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/83b0bea9-fcb6-4213-86c3-82153ce20f55.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Si  no  se  le  indica  de  otro  modo,  Ansible  leerá  el  fichero  de  inventario  de  la  ruta etc/ansible/hosts.  Sin  embargo,  el  definir  tu  inventario  en  este  fichero  no  está recomendado. Lo más conveniente es mantener un fichero de inventario distinto por cada proyecto que tengas y pasarlo como parámetro al comando ansible o ansible‐ playbook mediante  la  opción  ‐i #flashcard
		- (Page 5)
	- -
	- -
		- El  fichero  de  inventario  en  Ansible  puede  implementarse  en  un  fichero  INI,  o mediante  un  JSON.  Los  ejemplos  más  habituales  en  la  web  utilizan  un  fichero  INI, mientras  que  el  fichero  JSON  se  utiliza  típicamente  para  generar  el  inventario dinámicamente.  Usar  el  formato  INI  hace  que  los  ficheros  de  inventario  sean normalmente bastante simples. Pueden ser tan sencillos como una simple lista de nombres  de  hosts  en  los  que  ejecutar.  A  continuación,  se  muestra  un  fichero  de inventario sencillo: host1.example.com host2.example.com host3.example.com 192.168.9.29 En este ejemplo se define una lista de cuatro hosts sobre los que se quiere ejecutar. Ansible ejecutará sobre cada uno de ellos por turnos, siguiendo el orden establecido, desde  host1.example.com  hasta  192.168.9.29.  Esta  es  la  forma  más  sencilla  de fichero de inventario que puedes usar, en la que no hay información adicional para ningún  host  ni  agrupaciones,  sino  sencillamente  una  lista  de  hosts  sobre  la  que queremos ejecutar Ansible. #flashcard
		  id:: e00546c0-4d5d-4167-b2da-412d3ece1c21
		- (Page 5)
	- -
	- -
		- En  lugar  de especificar cada host uno por uno, puedes usar esta funcionalidad de expansión de rangos para definirlos todos de una vez, tal como, por ejemplo: host[1:3].example.com Esta expresión equivale a: host1.example.com host2.example.com host3.example.com #flashcard
		- (Page 6)
	- -
	- -
		- Para  poder  probar  la  ejecución  manual  de  Ansible,  necesitas  habilitar  en  tu Vagrantfile la gestión de red privada para poder así acceder por SSH a la máquina virtual. Esto se hace editando el fichero Vagrantfile y descomentando o añadiendo la siguiente línea: config.vm.network "private_network", ip: "192.168.33.10" Una vez guardados los cambios en el fichero, ejecuta vagrant  halt && vagrant up para reiniciar tu máquina y habilitar esta red. Esto proporcionará a la máquina virtual creada una IP que podrás utilizar para conectar con ella. Una vez que tengas dirección IP, puedes manejarla como si no fuera una máquina gestionada por Vagrant, sino otra máquina accesible en la red en la que necesitas ejecutar Ansible. Esto podría ser una máquina virtual que se encuentra alojada en tu mismo equipo, o en algún lugar de la nube. #flashcard
		- (Page 7)
	- -
	- -
		- ansible‐playbook –i <inventory_file> provisioning/playbook.yml #flashcard
		  id:: c0b6f6ac-9fbd-448e-81e0-35e2d061444a
		- (Page 7)
	- -
	- -
		- 192.168.33.10 ansible_user=vagrant ansible_ssh_private_key_file=.vagrant/machines/default/virtualbox/pr ivate_key #flashcard
		- (Page 8)
	- -
	- -
		- ansible‐playbook ‐i inventory provisioning/playbook.yml #flashcard
		- (Page 8)
	- -
	- -
		- El ejemplo de fichero de inventario a continuación utiliza alguna de estas opciones: alpha.example.com ansible_user=bob ansible_port=50022 bravo.example.com ansible_user=mary ansible_ssh_private_key_file=/path/to/mary.key frontend.example.com ansible_port=50022 yellow.example.com ansible_host=192.168.33.10 Con  esto  se  establece  un  puerto  alternativo  para  las  máquinas  alpha  y  frontend, usuarios específicos con los que accede a  alpha y  bravo, proporciona el fichero de clave privada para bravo y por último define que el nombre yellow.example.com es realmente la dirección IP 192.168.33.10 #flashcard
		- (Page 10)
	- -
	- -
		- Por ejemplo, para aplicar el playbook en el entorno de producción, usaremos: ansible‐playbook –i production‐inventory playbook.yml #flashcard
		- (Page 13)
	- -
	- -
		- solemos tener balanceadores de carga, servidores web, servidores de aplicaciones, bases de datos, etc. Se hace necesario poder agrupar estos conjuntos de servidores por tipo y poder  referenciarlos  como  a  un  único  grupo.  Ansible  permite  definir  grupos  de inventario para dar soporte a este caso de uso. Para  definir  un  grupo  de  servidores  en  el  fichero  de  inventario  se  utilizan  las cabeceras de sección INI, incluyendo su nombre entre corchetes, tal como especifica el formato de archivos INI: [web] host1.example.com host2.example.com [database] db.example.com #flashcard
		- (Page 13)
	- -
	- -
		- El siguiente comando ejecutará el módulo ping únicamente en el grupo web: ansible web –i /path/to/inventory –m ping También  puedes  establecerlo  en  un  playbook  cambiando  simplemente  el  valor  de hosts: al principio de tu playbook, tal como: - hosts: web tasks: ‐ ping: #flashcard
		- (Page 14)
	- -
	- -
		- De  la  misma  manera  que  puedes  establecer  variables  para  máquinas  específicas, también puedes establecer variables para los grupos. Para ello, utiliza una cabecera especial con el nombre de grupo y el sufijo :vars en tu fichero de inventario: [web:vars] apache_version=2.4 engage_flibbit=true Las variables así definidas estarán disponibles en la ejecución Ansible para cualquier máquina del grupo web #flashcard
		  id:: eec0bd95-487d-4c68-ac63-fb150ae9215f
		- (Page 14)
	- -
	- -
		- El fichero de inventario podría parecerse al siguiente: [web_centos6] host1.example.com host2.example.com [web_centos7] shinynewthing.example.com [database_centos] database.example.com [reporting_centos7] reporting.example.com [centos6:children] web_centos6 database_centos6 [centos7:children] web_centos7 reporting_centos7 [centos6:vars] apache_version=2.2 Si  necesitas  ejecutar  algo  únicamente  en  las  máquinas  CentOS  6,  típicamente tendrías que hacerlo sobre ambos grupos, webcentos6 y database_centos6. En lugar de ello, puedes crear un grupo de grupos utilizando el sufijo :children en tu nombre de grupo: Con este grupo de grupos ya solo tendrás que apuntar a los  hosts  centos6  si solo necesitas  ejecutar  en  los  servidores  CentOS  6.  Es  más,  puedes  también  definir variables para este nuevo grupo, como harías con cualquier otro grupo: #flashcard
		- (Page 15)
	- -
	- -
		- Un fichero de inventario bien escrito no debe ser simplemente algo que Ansible debe usar, sino que debe servir también como documentación propia del entorno, para cuando necesites referirte a ella, o mostrárselo a alguien. #flashcard
		- (Page 17)
	- -
	- -
		- Cuando se ejecuta Ansible, este comprobará si el fichero pasado como parámetro del inventario es un archivo ejecutable. En caso de serlo, lo ejecutará y Ansible utilizará su analizador JSON para leer los datos resultantes. Si no es ejecutable, Ansible lo leerá suponiendo que está en formato de fichero INI y fallará en el análisis si es un archivo JSON estático. #flashcard
		- (Page 18)
	- -