title:: Herramientas de Automatización de Despliegues Tema-9 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-9"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/4973ab6c-aee6-4f19-ba05-d87b0c77b79e.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Las variables en Ansible son  siempre globales, lo  que significa que,  al declarar una variable en un  rol, en un playbook o en cualquiera de las ubicaciones posibles (que veremos en este tema), se hace disponible para todos los playbooks y plantillas que se procesan durante la ejecución de Ansible. Esto tiene como consecuencia que las variables de un rol generalmente se prefijan con el nombre del rol. #flashcard
		  id:: 61cb5026-b975-4e25-bb7a-651a78848c41
		- (Page 4)
	- -
	- -
		- La manera de referenciar variables en Ansible es incluyendo su nombre entre llaves dobles, tal como {{variable_name}}, dado que es la sintaxis que define Jinja2 para la sustitución  de  variables. #flashcard
		  id:: 13ed4322-3e07-4b19-a5ef-fe5b6ffbfef1
		- (Page 6)
	- -
	- -
		- Valores por defecto de los roles (se usan habitualmente) Se definen en el archivo defaults/main.yml dentro del rol. Estas variables tienen la precedencia más baja, por lo que una variable declarada en cualquier otra ubicación las  sobrescribirá  y,  por  ello,  son  muy  adecuadas  para  establecer  valores predeterminados. En mi_rol/defaults/main.yml: nombre_usuario: Caracola #flashcard
		  id:: 7f36c578-5e4b-49c0-bd58-08e0a049e499
		- (Page 12)
	- -
	- -
		- Variables de grupo de playbook (se usan habitualmente) Otra  ubicación  donde  se  pueden  definir  variables  de  grupo  es  en  el  subdirectorio group_vars pero situado a nivel de playbook. Su funcionalidad es la misma que las definidas  a  nivel  inventario,  pero  esta  vez  el  subdirectorio  cuelga  del  mismo directorio  en  el  que  se  encuentra  el  fichero  playbook.yml,  y  su  precedencia  es también superior. #flashcard
		  id:: 59074bf8-0223-48b9-ac82-6b86e9e1c701
		- (Page 15)
	- -
	- -
		- Variables de host de playbook (se usan habitualmente) Análogamente  a  las  variables  de  grupo,  las  de  host  también  pueden  definirse  al mismo  nivel  que  el  playbook.  Nuevamente  tienen  la  misma  funcionalidad  que  las definidas a nivel inventario, pero esta vez el subdirectorio  host_vars se encuentra ubicado en el mismo directorio en el que se encuentra el fichero playbook.yml, y su precedencia es también superior. #flashcard
		  id:: 720f3e62-8eb5-433a-94fd-1d4b8ecd40d9
		- (Page 16)
	- -
	- -
		- Variables registradas (se usan habitualmente) Cuando trabajas dentro de un playbook, puedes guardar la salida de los módulos para usarla más adelante. Por ejemplo, para almacenar en la variable hosts_info toda la información del sistema de archivos sobre el fichero /etc/hosts, utiliza el siguiente fragmento de tarea: - stat: path=/etc/hosts register: hosts_info - debug: var=hosts_info En caso de que la variable hosts_info estuviera definida en cualquier otra ubicación con una precedencia más baja que la de las variables registradas, se sobrescribiría su valor. Esto podría llegar a provocar errores difíciles de detectar, dado que la variable tenía  un  valor  hasta  ejecutar  esta  tarea,  pero  una  vez  ejecutada  el  valor  ahora  es diferente. El uso de prefijos en las variables puede ayudar a evitar esto. #flashcard
		  id:: 00dfd0ba-d32d-45e7-ade5-f8a382be1f3e
		- (Page 17)
	- -
	- -
		- Este tipo de variables se declaran en su propia sección vars,que se encuentraal mismo nivel que las de tareas: -- hosts: all gather_facts: false vars: tasks: nombre_usuario: Caracola - debug: msg="Hello {{nombre_usuario}}" #flashcard
		  id:: e38ce7de-ee70-47e7-aaf8-6e8a8a47bc2e
		- (Page 18)
	- -
	- -
		- Variables de rol (se usan habitualmente) Cuando utilizas un rol en tu playbook, se pueden especificar las variables que quieres emplear en el rol, como si le pasaras parámetros. Este tipo de variables ya lo hemos utilizado cuando hemos establecido los valores a utilizar para las variables necesarias en nuestro rol de WordPress: -- hosts: all become: true roles: - role: ansibleunir.wordpress vars: nombre_bd: mywordpressdb usuario_bd: mywordpressusr password_bd: Aproba2to2 #flashcard
		  id:: 317ee3c4-0946-44e5-aeaa-ea50df76c650
		- (Page 23)
	- -