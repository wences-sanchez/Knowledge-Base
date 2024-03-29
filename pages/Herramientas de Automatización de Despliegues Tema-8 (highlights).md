title:: Herramientas de Automatización de Despliegues Tema-8 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-8"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/e3359d36-b8eb-40cb-9801-7103ac0b8eab.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Los playbooks y los roles son similares en cierto sentido, pero a la vez muy diferentes entre  sí.  Un playbook  es  un  archivo  independiente  que  Ansible  puede  ejecutar  y contiene toda la información necesaria para establecer el estado de la máquina a lo que  se  desea.  Esto  quiere  decir  que  un  playbook  puede  incluir  variables,  tareas, manejadores, roles e incluso otros playbooks, todo en un mismo archivo. Un rol podría considerarse como un playbook que se separa en diferentes archivos. En vez de tener un único archivo que contenga todo lo que necesitamos, vamos a tener un  archivo  para  variables,  otro  para  las  tareas  y  otro  para  los  manejadores.  Sin embargo, no se puede ejecutar un rol por sí mismo; es necesario incluirlo dentro de un playbook junto con la información de los hosts donde ejecutarlo. #flashcard
		  id:: 4531a1b7-f8b3-4ccf-9a8c-f73105d00381
		- (Page 4)
	- -
	- -
		- Para descargar un rol  del  repositorio, utiliza  el comando ansible-galaxy proporcionando el parámetro  -p  roles  para que el rol se instale en un directorio denominado roles. Debes ejecutar ansible-galaxy desde el mismo directorio donde se encuentra el archivo playbook.yml. #flashcard
		  id:: 3c0cb23f-0cc4-4110-aec0-4cdce607499f
		- (Page 6)
	- -
	- -
		- ansible-galaxy install geerlingguy.git –p roles Esta línea creará la carpeta roles en caso de que no exista y descargará el rol en ella. Para usar este rol, debes incluirlo desde un playbook. Como ya sabemos, primero le indicamos  a  Ansible  en  qué  servidores  se  va  a  ejecutar,  y  ahora,  a  continuación, también le proporcionaremos una lista de roles para que Ansible los incluya: -- hosts: all roles: - geerlingguy.git #flashcard
		  id:: eebf31dc-2d95-42c8-9f60-d3589f62816a
		- (Page 6)
	- -
	- -
		- mkdir -p provisioning/roles cd provisioning/roles ansible-galaxy init ansibleunir.php El  comando  ansible-galaxy  init  habrá  creado  un  subdirectorio llamado ansibleunir.php bajo el directorio roles que contendrá la estructura y los ficheros básicos de un rol de Ansible: #flashcard
		  id:: ce00e867-55a4-46dd-8336-446770df12a8
		- (Page 8)
	- -
	- -
		- IMAGEN #flashcard
		  id:: 2c07ebe9-18d5-40a5-8ef9-4414cf161621
			- a
		- (Page 8)
	- -
	- -
		-   El  archivo  defaults/main.yml  puede  contener  los  valores  por  defecto  que utilizarán las variables que maneja el rol, en caso de no haber proporcionado otro valor personalizado. También es posible definir variables en otras ubicaciones tales como vars/main.yml que actualizará cualquier variable que ya estuviera definida en defaults/main.yml, ya que tiene mayor prioridad.   El directorio files es en el que se colocan los ficheros necesarios para la ejecución del  rol.  Podrá  contener  tanto  elementos  estáticos,  ficheros  de  configuración, como cualquier otro tipo de fichero. Ten en cuenta que estos archivos no pueden ser manipulados de ninguna manera, solo se pueden copiar.   handlers/main.yml es donde defines manejadores como restart nginx. El contar con todos los manejadores disponibles en un único lugar común es muy útil para cualquiera que utilice el módulo, para poder ver de un vistazo las acciones que están disponibles. Los manejadores se pueden invocar tanto desde el mismo rol, como desde otros roles y desde el playbook que incluye al rol.   El  archivo  meta/main.yml  contiene  los  metadatos  del  rol.  Este  archivo  va  a incorporar los metadatos que utiliza Ansible Galaxy si publicas el rol. También se pueden definir algunos parámetros, como la versión mínima de Ansible requerida, plataformas soportadas y cualquier otra dependencia de este rol.   El archivo tasks/main.yml es el punto de entrada del rol. Incorpora la sección de tareas que está contenida en tu playbook. Las acciones que están definidas en este archivo son las que procesará Ansible cuando se ejecute el rol.   El directorio templates contiene todas las plantillas que necesitan ser procesadas por el procesador de plantillas jinja2 para así sustituir las variables necesarias en el archivo (y cualquier otro procesamiento soportado por Jinja) antes de copiarlo en el sistema de destino. #flashcard
		  id:: af80a4c2-36e3-4795-9db7-76d33eec5557
		- (Page 9)
	- -
	- -
		-   El directorio tests es donde debes incluir los playbooks de prueba que usan el rol. Esto  se utiliza para definir pruebas automatizadas del rol,  que  podrán ejecutarse mediante un sistema de integración continua, tal como Jenkins o Travis CI. Este tipo de sistemas (de integración continua) son herramientas que detectan cuándo realizas  modificaciones  en  el  código  fuente  de  un  programa  y  desencadenan acciones relacionadas; típicamente, la compilación o construcción de ese código fuente, la ejecución de pruebas para el proyecto, empaquetado de los binarios o cualquier otra cosa que se pueda expresar en un script. #flashcard
		  id:: f18df5d3-cf67-4e8c-a2fe-99acbd67235e
		- (Page 10)
	- -
	- -
		- IMAGEN. Hace falta para indicar otros ficheros que no sean main.yml #flashcard
		  id:: 60c7b26e-fe0c-4f31-948e-a469293bd282
			- -- include: 'php.yml' - include: 'extensions.yml' Esto utiliza la sintaxis  include de YAML, que incorpora un archivo YAML dentro de otro. Cuando Ansible se ejecuta, todos estos archivos se fusionarán, pero mientras estés  desarrollando  el  playbook,  conseguirás  una  clara  separación  de las responsabilidades.
		- (Page 11)
	- -
	- -
		- existe  la  opción  de  dependencias  en  meta/main.yml  que  fue mencionada al explicar la estructura de directorios de un rol. Pues bien, puedes usarla para especificar las dependencias de un rol y hacer que Ansible las incluya de forma automática,  en  lugar  de  tenerlo  que  incluir  tú  en  el  playbook #flashcard
		  id:: 59156289-74ba-42ee-b4f9-5912553c4b93
		- (Page 20)
	- -
	- -
		- dependencies: - ansibleunir.common - ansibleunir.php - ansibleunir.mysql - ansibleunir.nginx Esto  es  la  lista  de  roles  requeridos  para  ejecutar  este  rol.  Después,  modifica playbook.yml  para  que  solo  ansibleunir.wordpress  esté  en  la  lista  de  roles.  Si ejecutas nuevamente vagrant provision, podrás apreciar que todas las dependencias se ejecutan antes de que se ejecute el rol ansibleunir.wordpress. #flashcard
		  id:: ad1298c2-a0b2-481c-930e-938d928046f0
		- (Page 20)
	- -
	- -
		- # main.yml -- include_vars:"{{ansible_os_family}}.yml" - include: install-debian.yml when: ansible_os_family =='Debian' - include: install-redhat.yml when: ansible_os_family =='RedHat' En vez de condicionar las tareas con when, se podía haber simplificado: include:"install-{{ansible_os_family}}.yml" Sin embargo, es preferible usar when en vez de incluir el fichero basado en la variable ansible_os_family para así ver claramente qué familias de sistemas operativos están soportados  por  el  rol.  También  se  incluye  el  fichero  de  variables  correcto automáticamente. #flashcard
		  id:: db6dd473-f382-4f6b-9d0f-16ae8fd0aecd
		- (Page 23)
	- -
	- -
		- Los módulos, también denominados plugins de tareas (o plugins de biblioteca), son fragmentos de código que se pueden usar desde la línea de comandos o desde una tarea de un playbook. Ansible ejecuta cada módulo habitualmente en el nodo remoto destino de la ejecución y recolecta los valores de retorno. #flashcard
		  id:: 7ea98491-5367-4a88-b3a8-daff1b9416dd
		- (Page 25)
	- -
	- -
		- Todos  los  módulos  básicos  de  Ansible  están desarrollados  en  Python.  Hay  dos  grupos  de  módulos:  ansible-modules-core  y ansible-modules-extras. #flashcard
		  id:: f1cbbed2-68c6-4223-aad2-6181be0fd612
		- (Page 26)
	- -