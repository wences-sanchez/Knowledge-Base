title:: Administración de Sistemas para la Cloud Tema-3 (highlights)
author:: [[UNIR]]
full-title:: "Administración de Sistemas para la Cloud Tema-3"
category:: #books

tags:: Administración-de-Sistemas-para-la-Cloud UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/d66b5b36-dfa0-4fcd-b1ef-26fce559b77f.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Cómo podrías definir la Shell? #flashcard
		  id:: 7dd5b2fa-b061-49f3-8800-bd142db0650a
			- Dicho  de  un  modo  muy  sencillo,  la  shell  es  un  macroprocesador  que  ejecuta comandos. Esta definición indica que hay una funcionalidad donde textos y símbolos se combinan para crear expresiones más grandes. La shell es, a la vez, una intérprete de comandos y un lenguaje de programación. En su  rol  de  intérprete  de  comandos,  la  shell  ofrece  al  usuario  una  rica  interfaz  de utilidades o herramientas de GNU. Las características del lenguaje de programación, por su parte, permiten que estas herramientas se combinen.
		- (Page 4)
	- -
	- -
		- ¿Qué es la shell? #flashcard
		  id:: 96baddd5-c3ec-4398-8cd1-d66e4d9b804c
			- La shell puede funcionar en modo interactivo y en modo no interactivo.
			  
			  En modo interactivo, la shell acepta entrada desde el teclado, ya sea el teclado local o un teclado remoto en una sesión SSH. El sistema operativo arranca una shell en el momento en el que un usuario inicia una nueva sesión (Van Vugt, 2015, pp. 1-26), ya sea una sesión local o por SSH.
			  
			  Por tanto, una shell no es sino un proceso más. En modo no interactivo, la shell lee un archivo (es decir, un script) y ejecuta los comandos contenidos en él, línea por línea. Estos scripts pueden convertirse en comandos en sí mismos. Estos nuevos comandos tienen el mismo status que comandos del sistema en directorios como /bin, permitiendo que usuarios o grupos puedan construir sus propios entornos y automatizar sus tareas comunes.
		- (Page 5)
	- -
	- -
		- Comandos síncronos VS asíncronos en la shell. #flashcard
		  id:: 4377cd2a-7d08-42a0-b2f6-652a1a12805f
			- En cuanto a los  comandos GNU, la shell permite su ejecución de modo síncrono y asíncrono. En el primer caso, la shell acepta un comando, lo ejecuta y espera a que este  termine  antes  de  aceptar  el  siguiente  comando.  Por  su  parte,  los  comandos asíncronos continúan ejecutándose en paralelo con la  shell, mientras lee y ejecuta comandos adicionales.
		- (Page 6)
	- -
	- -
		-   Built-in: es un comando que se implementa internamente por la shell, en lugar de por un programa ejecutable en algún lugar en el sistema de archivos. Es decir, es un comando llevado a cabo por la shell, como cd, en lugar de interpretarlo como una solicitud para cargar y ejecutar algún otro programa, como vim.  Esto tiene dos consecuencias principales. En primer lugar, por lo general, es más rápido,  ya  que  el  tiempo  que  toma  cargar  y  ejecutar  un  programa  es  más prolongado.  En  segundo  lugar,  un  comando  built-in  puede  afectar  el  estado interno de la shell. Es por eso por lo que los comandos como cd deben ser builtin,  dado  que  un  programa  externo  no  puede  cambiar  el  directorio  actual  de  la shell. Otros comandos, como echo, podrían ser built-in por un motivo de eficiencia, pero  no  hay  ninguna  otra  razón  intrínseca  para  que  no  puedan  ser  comandos externos. #flashcard
		  id:: 3700f255-e01c-48f6-b361-5dd8afbf26fb
		- (Page 7)
	- -
	- -
		- ¿Qué significa el operador $? en bash? #flashcard
		  id:: 4bc562ff-2601-4974-b8b2-b718d0c40a98
			- el código de salida de la orden anterior se almacena en el parámetro de shell $?. Este parámetro se utiliza para comprobar el estado de la última orden ejecutada.
			  
			  Si el valor devuelto por $? es 0, significa que el último comando acabó con éxito; de lo contrario, el comando falló.
			  
			  El valor concreto depende de cada utilidad, pero, en todo caso, es un número entero de 8 bits.
		- (Page 8)
	- -
	- -
		- ¿Cómo puedes mostrar $tree de otra forma, sin usar ese comando? #flashcard
		  id:: eb15e52e-8c0e-443e-9388-a86bb6c56295
			- ls –aR: lista de forma recursiva.
		- (Page 10)
	- -
	- -
		- ¿Cómo (des)comprimirías un .zip (o un .tar.gz) en shell? #flashcard
		  id:: 0fcb7342-1d90-43d3-a90f-3ddeff37a3cd
			- • zip arch.zip /home/usr/public/dir: comprime el directorio y su contenido en el fichero arch.zip.
			  • unzip arch.zip: descomprime arch.zip.
			  • unzip -v arch.zip: visualiza el contenido de arch.zip.
			  • tar xvzf package.tgz: descomprime el fichero package.tgz.
		- (Page 10)
	- -
	- -
		- ¿Cómo copiarías un directorio a otro manteniendo sus permisos? #flashcard
		  id:: 63c38340-7035-4ede-89f3-40f6fa49edc9
			- •  cp  -a  /home/usr/origen/*  /home/usr/destino/: copia todos los contenidos de un directorio a otro, manteniendo sus permisos.
		- (Page 11)
	- -
	- -
		- ¿Cómo consultarías el espacio ocupado por la carpeta actual?, ¿y por cada fichero? #flashcard
		  id:: aa7ba8e2-34d9-4793-a33d-17531311763b
			- • du -sh: visualiza el espacio total ocupado por la carpeta actual.
			  
			  • du -sh *: muestra el espacio ocupado de cada fichero.
		- (Page 11)
	- -
	- -
		- ¿Cómo podrías obtener el nombre del usuario actual en la shell? #flashcard
		  id:: 45800210-7dca-46ad-be97-cc8e59216d4c
			- **$ whoami**; muestra el nombre del usuario.
		- (Page 11)
	- -
	- -
		- el  siguiente  comando muestra el contenido del fichero de configuración del servidor SSH, pero las líneas no comentadas y ordenadas por orden alfabético: $ cat sshd_config | grep -v "#" | sort | uniq #flashcard
		  id:: c6064fa3-d151-458a-bc40-da7b35ab7143
		- (Page 13)
	- -
	- -
		- Para ejecutar operaciones administrativas, no hay más que iniciar sesión como root. Sin embargo, esto conlleva ciertos riesgos de seguridad, como que el usuario teclee un comando sintácticamente válido, pero que no hace lo que debe, borrando datos importantes por error.
		  id:: 93e1688e-2e53-4d09-9b56-cf1f1103e5c5
		  
		  Es habitual que la cuenta de root esté deshabilitada por defecto y que ni siquiera tenga contraseña, por lo que no se puede iniciar sesión con ella en muchas distribuciones. La alternativa es usar el mecanismo de Sudo.
		  
		  La idea es que tareas de administración concretas pueden asignarse a usuarios específicos. Si un usuario necesita ejecutar una tarea administrativa como, por ejemplo, instalar un paquete nuevo con apt-get install, debe ejecutarlo con Sudo: sudo apt-get install openssh-server.
		  
		  El usuario root podría ejecutar el mismo comando sin Sudo, pero es obligatorio para cualquier otro usuario. #flashcard
		- (Page 14)
	- -
	- -
		- ¿Con qué comando debe abrirse el fichero sudoers? #flashcard
		  id:: 954e9eeb-1ffd-4d74-a3b4-874935153b25
			- El  fichero  sudoers  contiene  los permisos asignados a los usuarios y grupos del sistema. Debe editarse con  visudo: este comando abre el fichero  sudores con el editor del sistema (por ejemplo,  vi o nano) y lo valida al guardarlo. De esta manera, se evita que un usuario cometa un error de sintaxis al guardarlo, rompiendo la funcionalidad de Sudo.
		- (Page 15)
	- -
	- -
		- ¿Con qué comando puedes crear o cambiar variables de entorno en bash? #flashcard
		  id:: b7e72ae7-6b13-458c-9477-ab8b5d5310f3
			- **$ export CONFIG_FILE=/opt/app/config**
		- (Page 16)
	- -
	- -
		- ¿Cómo ejecutarías un mensaje de varias líneas en bash? #flashcard
		  id:: 9cf0bdd0-960c-40e8-a18c-30eae370f16f
			- **$ cat << HEREDOC**
			  Mensaje de varias lineas que no
			  podria imprimirse por pantalla
			  simplemente con "cat mensaje"
			  **HEREDOC**
		- (Page 17)
	- -
	- -
		- ¿Qué códigos de salida devuelve una condición verdadera?¿Qué comando puedes usar para evaluarla? #flashcard
		  id:: d7c67c51-da1f-4864-93d3-19710331255c
			- El comando test evalúa una condición lógica y devuelve un código de salida cero, si la  condición  es  verdadera,  o  distinto  de  cero,  si  es  falsa.  Este  comando  tiene  una forma  alternativa,  en  la  que  el  nombre  test  se  sustituye  por  corchetes,  [  ],  y  otra forma que usa corchetes dobles, [[ ]]; esta segunda forma no aplica expansión de ruta ni  división  de  palabras.
		- (Page 18)
	- -
	- -
		- ¿Cómo harías un bucle for en bash? #flashcard
		  id:: 5bd04d30-b582-4b26-9297-de429cdf5139
			- $ for r in i{1..3}; echo interacion $r do done
		- (Page 22)
	- -
	- -
		- ¿Cómo puedes recorrer en Bash la lista de parámetros pasados como argumentos en el script con un bucle y mostrarlos? #flashcard
		  id:: a9953c3b-0bca-40f7-baed-542b20af5199
			- for p in $@; do echo $p; done
		- (Page 22)
	- -
	- -
		- también se puede iterar sobre un rango de enteros, tal como en otros  lenguajes. $ for ((i=1; i <= 5; i += 1))   if [[ -e file$i ]]; then     echo file$i existe;     echo file$i no existe do   else   fi done #flashcard
		  id:: 755d857a-7611-4398-a372-276ca5a17512
		- (Page 23)
	- -
	- -
		- Define script #flashcard
		  id:: 441072f4-115e-4139-ad78-4d67d1595a37
			- Un script de Bash es un fichero de texto con una secuencia de comandos de shell (Van Vugt,  2015,  pp.  319-351).  No  tiene  más  requisitos,  así  que  un  fichero  con  este contenido sería un script válido: echo "Hello World" pwd $ bash script.sh Hello World /etc/apache2 Este script se podría ejecutar invocándolo de la siguiente manera:
		- (Page 24)
	- -
	- -
		- ¿Cuál sería el shebang correcto para un script en Bash? #flashcard
		  id:: 94e4a160-3bd0-4cf7-9d34-3473eeaba944
			- **#!/bin/bash**
			  Deben empezar con un shebang, #!, en la primera línea, indicando la ruta al ejecutable de la shell. Esta línea es un comentario especial que permite ejecutar un script como un ejecutable binario más. Para un script de Bash, la línea sería #!/bin/bash, mientras que un script de Python podría usar #!/usr/bin/python3 v.
		- (Page 24)
	- -
	- -
		- ¿Qué valor debería devolver un script al terminar? #flashcard
		  id:: 14f3a446-e238-40bb-abfd-5dcb13a1c977
			-   El uso de  exit indica explícitamente cuando termina el  script, tanto de manera correcta con un código de salida 0 como si hay algún error.
		- (Page 24)
	- -
	- -
		- se  ha  mostrado  cómo  ejecutar  un  script  de  dos  maneras:  como argumento  del  comando  bash  y  convirtiendo el  script  en  ejecutable  e  invocándolo directamente. Ambas opciones funcionan de manera similar: la shell desde la que se invoca  arranca  otra  shell  como  un  nuevo  proceso  y  es  esta  la  que  se  encarga  de ejecutar los comandos del script. Hay una tercera opción, ligeramente diferente: ejecutar el script en el mismo proceso de la shell actual. Este caso puede ser útil si el script cambia valores de variables de entorno que son necesarias en la shell actual (por ejemplo, para configurar la shell de alguna manera concreta). No obstante, puede tener efectos contraproducentes: si el script  termina  proactivamente  con  un  comando  exit,  la  shell  actual  también terminará. El comando para ejecutar los scripts en la propia shell es source o . (un punto): #flashcard
		  id:: 917741b6-abb5-45c6-bfa4-136c5e95424a
		- (Page 25)
	- -
	- -
		- $ source script.sh $ . script.sh #flashcard
		  id:: 2836e8ab-e9c7-487f-aed0-ed5a993bfe52
		- (Page 26)
	- -