# Administración de Sistemas para la Cloud Tema-3

deck:: [[UNI::Administración de Sistemas para la Cloud Tema-3]]\
author:: [[UNIR]]\
full-title:: "Administración de Sistemas para la Cloud Tema-3"\
category:: #books\
\
tags:: Administración-de-Sistemas-para-la-Cloud UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/d66b5b36-dfa0-4fcd-b1ef-26fce559b77f.jpg)
## Highlights
- id:: 63c669dd-268d-4c1b-b158-296c4a99ba5e
   ¿Cómo podrías definir la Shell? #flashcard 
    Dicho de un modo muy sencillo, la shell es un macroprocesador que ejecuta comandos. Esta definición indica que hay una funcionalidad donde textos y símbolos se combinan para crear expresiones más grandes. La shell es, a la vez, una intérprete de comandos y un lenguaje de programación. En su rol de intérprete de comandos, la shell ofrece al usuario una rica interfaz de utilidades o herramientas de GNU. Las características del lenguaje de programación, por su parte, permiten que estas herramientas se combinen.
  
     (Page 4)
-
- id:: 63c669dd-5eee-4de9-bded-47926a2b9dc8
   ¿Qué es la shell? #flashcard 
    La shell puede funcionar en modo interactivo y en modo no interactivo.
     En modo interactivo, la shell acepta entrada desde el teclado, ya sea el teclado local o un teclado remoto en una sesión SSH. El sistema operativo arranca una shell en el momento en el que un usuario inicia una nueva sesión (Van Vugt, 2015, pp. 1-26), ya sea una sesión local o por SSH.
     Por tanto, una shell no es sino un proceso más. En modo no interactivo, la shell lee un archivo (es decir, un script) y ejecuta los comandos contenidos en él, línea por línea. Estos scripts pueden convertirse en comandos en sí mismos. Estos nuevos comandos tienen el mismo status que comandos del sistema en directorios como /bin, permitiendo que usuarios o grupos puedan construir sus propios entornos y automatizar sus tareas comunes.
  
     (Page 5)
-
- id:: 63c669dd-1926-4b7d-9fc6-088b064e19b1
   Comandos síncronos VS asíncronos en la shell. #flashcard 
    En cuanto a los comandos GNU, la shell permite su ejecución de modo síncrono y asíncrono. En el primer caso, la shell acepta un comando, lo ejecuta y espera a que este termine antes de aceptar el siguiente comando. Por su parte, los comandos asíncronos continúan ejecutándose en paralelo con la shell, mientras lee y ejecuta comandos adicionales.
  
     (Page 6)
-
- id:: 63c669dd-f679-4855-94a3-a2c438c5003b
  
   Built-in: es un comando que se implementa internamente por la shell, en lugar de por un programa ejecutable en algún lugar en el sistema de archivos. Es decir, es un comando llevado a cabo por la shell, como cd, en lugar de interpretarlo como una solicitud para cargar y ejecutar algún otro programa, como vim. Esto tiene dos consecuencias principales. En primer lugar, por lo general, es más rápido, ya que el tiempo que toma cargar y ejecutar un programa es más prolongado. En segundo lugar, un comando built-in puede afectar el estado interno de la shell. Es por eso por lo que los comandos como cd deben ser builtin, dado que un programa externo no puede cambiar el directorio actual de la shell. Otros comandos, como echo, podrían ser built-in por un motivo de eficiencia, pero no hay ninguna otra razón intrínseca para que no puedan ser comandos externos. #flashcard 
  
  
     (Page 7)
-
- id:: 63c669dd-3f8f-4369-a48d-2124f480a74f
   ¿Qué significa el operador $? en bash? #flashcard 
    el código de salida de la orden anterior se almacena en el parámetro de shell $?. Este parámetro se utiliza para comprobar el estado de la última orden ejecutada.
     Si el valor devuelto por $? es 0, significa que el último comando acabó con éxito; de lo contrario, el comando falló.
     El valor concreto depende de cada utilidad, pero, en todo caso, es un número entero de 8 bits.
  
     (Page 8)
-
- id:: 63c669dd-33e8-4ee6-ad0a-f91788683d79
   ¿Cómo puedes mostrar $tree de otra forma, sin usar ese comando? #flashcard 
    ls –aR: lista de forma recursiva.
  
     (Page 10)
-
- id:: 63c669dd-f205-4392-91a1-e2cf9a103ca9
   ¿Cómo (des)comprimirías un .zip (o un .tar.gz) en shell? #flashcard 
    • zip arch.zip /home/usr/public/dir: comprime el directorio y su contenido en el fichero arch.zip.
     • unzip arch.zip: descomprime arch.zip.
     • unzip -v arch.zip: visualiza el contenido de arch.zip.
     • tar xvzf package.tgz: descomprime el fichero package.tgz.
  
     (Page 10)
-
- id:: 63c669dd-b183-42b0-ac0a-229f620efed7
   ¿Cómo copiarías un directorio a otro manteniendo sus permisos? #flashcard 
    • cp -a /home/usr/origen/* /home/usr/destino/: copia todos los contenidos de un directorio a otro, manteniendo sus permisos.
  
     (Page 11)
-
- id:: 63c669dd-a7d8-44f1-82b3-028c936e62c7
   ¿Cómo consultarías el espacio ocupado por la carpeta actual?, ¿y por cada fichero? #flashcard 
    • du -sh: visualiza el espacio total ocupado por la carpeta actual.
     • du -sh *: muestra el espacio ocupado de cada fichero.
  
     (Page 11)
-
- id:: 63c669dd-77df-4077-9128-0415845a6fcf
   ¿Cómo podrías obtener el nombre del usuario actual en la shell? #flashcard 
    **$ whoami**; muestra el nombre del usuario.
  
     (Page 11)
-
- id:: 63c669dd-b81e-4fa0-8d68-ecad5df8c0eb
  
  el siguiente comando muestra el contenido del fichero de configuración del servidor SSH, pero las líneas no comentadas y ordenadas por orden alfabético: $ cat sshd_config | grep -v "#" | sort | uniq #flashcard 
  
  
     (Page 13)
-
- id:: 63c669dd-ab74-46e3-8ba0-50780eb17739
  
  Para ejecutar operaciones administrativas, no hay más que iniciar sesión como root. Sin embargo, esto conlleva ciertos riesgos de seguridad, como que el usuario teclee un comando sintácticamente válido, pero que no hace lo que debe, borrando datos importantes por error.
     Es habitual que la cuenta de root esté deshabilitada por defecto y que ni siquiera tenga contraseña, por lo que no se puede iniciar sesión con ella en muchas distribuciones. La alternativa es usar el mecanismo de Sudo.
     La idea es que tareas de administración concretas pueden asignarse a usuarios específicos. Si un usuario necesita ejecutar una tarea administrativa como, por ejemplo, instalar un paquete nuevo con apt-get install, debe ejecutarlo con Sudo: sudo apt-get install openssh-server.
     El usuario root podría ejecutar el mismo comando sin Sudo, pero es obligatorio para cualquier otro usuario. #flashcard 
  
  
     (Page 14)
-
- id:: 63c669dd-cf2e-4835-ad3f-731139b6c6a9
   ¿Con qué comando debe abrirse el fichero sudoers? #flashcard 
    El fichero sudoers contiene los permisos asignados a los usuarios y grupos del sistema. Debe editarse con visudo: este comando abre el fichero sudores con el editor del sistema (por ejemplo, vi o nano) y lo valida al guardarlo. De esta manera, se evita que un usuario cometa un error de sintaxis al guardarlo, rompiendo la funcionalidad de Sudo.
  
     (Page 15)
-
- id:: 63c669dd-8385-4a85-9bf4-a2bb871346c5
   ¿Con qué comando puedes crear o cambiar variables de entorno en bash? #flashcard 
    **$ export CONFIG_FILE=/opt/app/config**
  
     (Page 16)
-
- id:: 63c669dd-a032-4c48-8434-d159bd6e40d7
   ¿Cómo ejecutarías un mensaje de varias líneas en bash? #flashcard 
    **$ cat << HEREDOC**
     Mensaje de varias lineas que no
     podria imprimirse por pantalla
     simplemente con "cat mensaje"
     **HEREDOC**
  
     (Page 17)
-
- id:: 63c669dd-5c95-4cb2-b6c7-17598d1c4ff3
   ¿Qué códigos de salida devuelve una condición verdadera?¿Qué comando puedes usar para evaluarla? #flashcard 
    El comando test evalúa una condición lógica y devuelve un código de salida cero, si la condición es verdadera, o distinto de cero, si es falsa. Este comando tiene una forma alternativa, en la que el nombre test se sustituye por corchetes, [ ], y otra forma que usa corchetes dobles, [[ ]]; esta segunda forma no aplica expansión de ruta ni división de palabras.
  
     (Page 18)
-
- id:: 63c669dd-0062-4dac-b219-5c564d5c6464
   ¿Cómo harías un bucle for en bash? #flashcard 
    $ for r in i{1..3}; echo interacion $r do done
  
     (Page 22)
-
- id:: 63c669dd-efb2-4aac-8681-c9bd568838e1
   ¿Cómo puedes recorrer en Bash la lista de parámetros pasados como argumentos en el script con un bucle y mostrarlos? #flashcard 
    for p in $@; do echo $p; done
  
     (Page 22)
-
- id:: 63c669dd-653c-4656-a1ac-9895b31379ab
  
  también se puede iterar sobre un rango de enteros, tal como en otros lenguajes. $ for ((i=1; i <= 5; i += 1)) if [[ -e file$i ]]; then echo file$i existe; echo file$i no existe do else fi done #flashcard 
  
  
     (Page 23)
-
- id:: 63c669dd-2965-4424-b6a4-15660b354425
   Define script #flashcard 
    Un script de Bash es un fichero de texto con una secuencia de comandos de shell (Van Vugt, 2015, pp. 319-351). No tiene más requisitos, así que un fichero con este contenido sería un script válido: echo "Hello World" pwd $ bash script.sh Hello World /etc/apache2 Este script se podría ejecutar invocándolo de la siguiente manera:
  
     (Page 24)
-
- id:: 63c669dd-689a-4a74-ad2b-160d006c8236
   ¿Cuál sería el shebang correcto para un script en Bash? #flashcard 
    **#!/bin/bash**
     Deben empezar con un shebang, #!, en la primera línea, indicando la ruta al ejecutable de la shell. Esta línea es un comentario especial que permite ejecutar un script como un ejecutable binario más. Para un script de Bash, la línea sería #!/bin/bash, mientras que un script de Python podría usar #!/usr/bin/python3 v.
  
     (Page 24)
-
- id:: 63c669dd-df0b-450d-bfbc-4e7ee0d5b06b
   ¿Qué valor debería devolver un script al terminar? #flashcard 
     El uso de exit indica explícitamente cuando termina el script, tanto de manera correcta con un código de salida 0 como si hay algún error.
  
     (Page 24)
-
- id:: 63c669dd-499b-4613-beb4-24662d6a0c5f
  
  se ha mostrado cómo ejecutar un script de dos maneras: como argumento del comando bash y convirtiendo el script en ejecutable e invocándolo directamente. Ambas opciones funcionan de manera similar: la shell desde la que se invoca arranca otra shell como un nuevo proceso y es esta la que se encarga de ejecutar los comandos del script. Hay una tercera opción, ligeramente diferente: ejecutar el script en el mismo proceso de la shell actual. Este caso puede ser útil si el script cambia valores de variables de entorno que son necesarias en la shell actual (por ejemplo, para configurar la shell de alguna manera concreta). No obstante, puede tener efectos contraproducentes: si el script termina proactivamente con un comando exit, la shell actual también terminará. El comando para ejecutar los scripts en la propia shell es source o . (un punto): #flashcard 
  
  
     (Page 25)
-
- id:: 63c669dd-7fd7-40bd-866c-88a0929c98a2
  
  $ source script.sh $ . script.sh #flashcard 
  
  
     (Page 26)
-