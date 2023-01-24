# Herramientas de Automatización de Despliegues Tema-8

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-8]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-8"\
category:: #books\
\
tags:: Herramientas-de-Automatización-de-Despliegues UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/e3359d36-b8eb-40cb-9801-7103ac0b8eab.jpg)
## Highlights
- id:: 63c66a06-66de-4657-8f85-d825d5031514
  
  Los playbooks y los roles son similares en cierto sentido, pero a la vez muy diferentes entre sí. Un playbook es un archivo independiente que Ansible puede ejecutar y contiene toda la información necesaria para establecer el estado de la máquina a lo que se desea. Esto quiere decir que un playbook puede incluir variables, tareas, manejadores, roles e incluso otros playbooks, todo en un mismo archivo. Un rol podría considerarse como un playbook que se separa en diferentes archivos. En vez de tener un único archivo que contenga todo lo que necesitamos, vamos a tener un archivo para variables, otro para las tareas y otro para los manejadores. Sin embargo, no se puede ejecutar un rol por sí mismo; es necesario incluirlo dentro de un playbook junto con la información de los hosts donde ejecutarlo. #flashcard 
  
  
     (Page 4)
-
- id:: 63c66a06-a93c-4811-98a0-d84535af5d20
  
  Para descargar un rol del repositorio, utiliza el comando ansible-galaxy proporcionando el parámetro -p roles para que el rol se instale en un directorio denominado roles. Debes ejecutar ansible-galaxy desde el mismo directorio donde se encuentra el archivo playbook.yml. #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a06-bd86-4f16-97c5-93fbf566b7c8
  
  ansible-galaxy install geerlingguy.git –p roles Esta línea creará la carpeta roles en caso de que no exista y descargará el rol en ella. Para usar este rol, debes incluirlo desde un playbook. Como ya sabemos, primero le indicamos a Ansible en qué servidores se va a ejecutar, y ahora, a continuación, también le proporcionaremos una lista de roles para que Ansible los incluya: -- hosts: all roles: - geerlingguy.git #flashcard 
  
  
     (Page 6)
-
- id:: 63c66a06-989e-4dda-8145-20092944497d
  
  mkdir -p provisioning/roles cd provisioning/roles ansible-galaxy init ansibleunir.php El comando ansible-galaxy init habrá creado un subdirectorio llamado ansibleunir.php bajo el directorio roles que contendrá la estructura y los ficheros básicos de un rol de Ansible: #flashcard 
  
  
     (Page 8)
-
- IMAGEN #flashcard 
  id:: 63cfbccc-f345-4893-8603-800fedc11d82
    a
  
     (Page 8)
-
- id:: 63c66a06-7681-4737-bfe2-a661ec91e916
  
   El archivo defaults/main.yml puede contener los valores por defecto que utilizarán las variables que maneja el rol, en caso de no haber proporcionado otro valor personalizado. También es posible definir variables en otras ubicaciones tales como vars/main.yml que actualizará cualquier variable que ya estuviera definida en defaults/main.yml, ya que tiene mayor prioridad.  El directorio files es en el que se colocan los ficheros necesarios para la ejecución del rol. Podrá contener tanto elementos estáticos, ficheros de configuración, como cualquier otro tipo de fichero. Ten en cuenta que estos archivos no pueden ser manipulados de ninguna manera, solo se pueden copiar.  handlers/main.yml es donde defines manejadores como restart nginx. El contar con todos los manejadores disponibles en un único lugar común es muy útil para cualquiera que utilice el módulo, para poder ver de un vistazo las acciones que están disponibles. Los manejadores se pueden invocar tanto desde el mismo rol, como desde otros roles y desde el playbook que incluye al rol.  El archivo meta/main.yml contiene los metadatos del rol. Este archivo va a incorporar los metadatos que utiliza Ansible Galaxy si publicas el rol. También se pueden definir algunos parámetros, como la versión mínima de Ansible requerida, plataformas soportadas y cualquier otra dependencia de este rol.  El archivo tasks/main.yml es el punto de entrada del rol. Incorpora la sección de tareas que está contenida en tu playbook. Las acciones que están definidas en este archivo son las que procesará Ansible cuando se ejecute el rol.  El directorio templates contiene todas las plantillas que necesitan ser procesadas por el procesador de plantillas jinja2 para así sustituir las variables necesarias en el archivo (y cualquier otro procesamiento soportado por Jinja) antes de copiarlo en el sistema de destino. #flashcard 
  
  
     (Page 9)
-
- id:: 63c66a06-0d83-4153-a6bc-fbbe42152700
  
   El directorio tests es donde debes incluir los playbooks de prueba que usan el rol. Esto se utiliza para definir pruebas automatizadas del rol, que podrán ejecutarse mediante un sistema de integración continua, tal como Jenkins o Travis CI. Este tipo de sistemas (de integración continua) son herramientas que detectan cuándo realizas modificaciones en el código fuente de un programa y desencadenan acciones relacionadas; típicamente, la compilación o construcción de ese código fuente, la ejecución de pruebas para el proyecto, empaquetado de los binarios o cualquier otra cosa que se pueda expresar en un script. #flashcard 
  
  
     (Page 10)
-
- id:: 63c66a06-5e31-4688-9e6d-96ad8a9eba91
   IMAGEN. Hace falta para indicar otros ficheros que no sean main.yml #flashcard 
    -- include: 'php.yml' - include: 'extensions.yml' Esto utiliza la sintaxis include de YAML, que incorpora un archivo YAML dentro de otro. Cuando Ansible se ejecuta, todos estos archivos se fusionarán, pero mientras estés desarrollando el playbook, conseguirás una clara separación de las responsabilidades.
  
     (Page 11)
-
- id:: 63c66a06-cfb9-4a66-9616-7c1064cfa52a
  
  existe la opción de dependencias en meta/main.yml que fue mencionada al explicar la estructura de directorios de un rol. Pues bien, puedes usarla para especificar las dependencias de un rol y hacer que Ansible las incluya de forma automática, en lugar de tenerlo que incluir tú en el playbook #flashcard 
  
  
     (Page 20)
-
- dependencies: - ansibleunir.common - ansibleunir.php - ansibleunir.mysql - ansibleunir.nginx Esto es la lista de roles requeridos para ejecutar este rol. Después, modifica playbook.yml para que solo ansibleunir.wordpress esté en la lista de roles. Si ejecutas nuevamente vagrant provision, podrás apreciar que todas las dependencias se ejecutan antes de que se ejecute el rol ansibleunir.wordpress. #flashcard 
  id:: 63cfbccc-1bee-43f3-8299-0c67c96f28b9
  
  
     (Page 20)
-
-
# main.yml -- include_vars:"{{ansible_os_family}}.yml" - include: install-debian.yml when: ansible_os_family =='Debian' - include: install-redhat.yml when: ansible_os_family =='RedHat' En vez de condicionar las tareas con when, se podía haber simplificado: include:"install-{{ansible_os_family}}.yml" Sin embargo, es preferible usar when en vez de incluir el fichero basado en la variable ansible_os_family para así ver claramente qué familias de sistemas operativos están soportados por el rol. También se incluye el fichero de variables correcto automáticamente. #flashcard 
id:: 63c66a06-4bbb-4fff-b99b-cef8b11d63b7


 (Page 23)
-
- id:: 63c66a06-c1d7-41b2-a667-f946939a98fc
  
  Los módulos, también denominados plugins de tareas (o plugins de biblioteca), son fragmentos de código que se pueden usar desde la línea de comandos o desde una tarea de un playbook. Ansible ejecuta cada módulo habitualmente en el nodo remoto destino de la ejecución y recolecta los valores de retorno. #flashcard 
  
  
     (Page 25)
-
- id:: 63c66a06-e97c-418e-8de0-82808bff76e6
  
  Todos los módulos básicos de Ansible están desarrollados en Python. Hay dos grupos de módulos: ansible-modules-core y ansible-modules-extras. #flashcard 
  
  
     (Page 26)
-