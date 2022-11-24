title:: Administración de Sistemas para la Cloud Tema-5 (highlights)
author:: [[UNIR]]
full-title:: "Administración de Sistemas para la Cloud Tema-5"
category:: #books

tags:: Administración-de-Sistemas-para-la-Cloud UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/dad4eef0-4646-4392-abe6-cb7908390c3d.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- la ruta  /media  suele  alojan  las  unidades  del  CD  (disco  duro)  y  las  unidades  de  USB externas, una vez montadas. #flashcard
		  id:: 34cf231e-da8e-4072-9499-7c933ac03d33
		- (Page 5)
	- -
	- -
		- Como su propio nombre indica, el flag de lectura permite leer o ver un archivo normal o leer los nombres, pero no los detalles, del contenido de un directorio. El  flag de escritura  permite  hacer  cambios  sobre  un  archivo  o,  si  se  trata  de  un  directorio, permite  crear,  borrar  y  renombrar  los  ficheros  del  directorio.  El  flag  de  ejecución permite, efectivamente, la ejecución de un archivo. Los binarios de /bin deben tener el flag activo para que se puedan ejecutar. Un script, aunque sea un fichero de texto, puede tener el flag activo para poder ejecutarlo. Si el flag de ejecución se activa en un directorio, es posible «entrar» dentro del directorio usando el comando cd. #flashcard
		  id:: ec163943-4819-4c90-b4d5-f7c670869449
		- (Page 9)
	- -
	- -
		- ¿Cuál es el patrón de sintaxis de chmod? #flashcard
		  id:: d441212c-9667-41c3-ae39-d0931c47b4f4
			-   Clase|activar/desactivar|permiso.   Representación binaria.
		- (Page 10)
	- -
	- -
		- chmod u+x,g-x,o+r file chmod 764 file #flashcard
		  id:: 6ca2da82-34a7-4e9e-a48b-d5eae973681b
		- (Page 10)
	- -
	- -
		- Hay dos tipos de enlaces: enlaces fuertes  y  enlaces  débiles  o  simbólicos.  Los  enlaces  fuertes,  o  hard  links,  son referencias reales al archivo. Si se borran todos los enlaces fuertes a un archivo, el archivo se borra también. Un enlace fuerte solo se puede crear en la misma partición que el archivo al que referencia. Los enlaces simbólicos se pueden borrar sin afectar al fichero al que referencian. Es habitual que los archivos binarios tengan enlaces simbólicos, para poder acceder a ellos con varios nombres o para poder cambiar la versión de un binario sin cambiar el nombre con el que se accede. Por ejemplo, la Figura 5 muestra los ejecutables de Python en la carpeta /usr/bin. La versión instalada de Python es la 3.6, tal como se indica en el binario python3.6. Sin embargo, es posible ejecutarlo tanto con python como  con  python3.  Una  actualización  a  Python  3.8  cambiaría  estos  enlaces simbólicos,  para  que  apunten  al  nuevo  binario,  pero  manteniendo  los  nombres python y python3. #flashcard
		  id:: aad2a6bf-bbc7-4636-80c0-31b040329569
		- (Page 11)
	- -
	- -
		- ¿Cómo se puede crear un enlace simbólico? #flashcard
		  id:: 46de5a84-e4b0-49d4-83df-cefe68097078
			- Los  enlaces  se  crean  con  el  comando  ln.  Los  enlaces  serán  fuertes  por  defecto  y simbólicos con el flag -s. La manera más sencilla de crear un enlace simbólico en la ruta actual es simplemente indicando la ruta del archivo enlazado
		- (Page 12)
	- -
	- -
		- Linux es un sistema operativo multiusuario (Matotek et al., 2017). Esto significa que permite el inicio de sesión de múltiples usuarios simultáneamente, ya sea por la línea de comandos o en una sesión de escritorio. También hay usuarios específicos para ciertos componentes del sistema operativo. #flashcard
		  id:: bd858b3d-6209-48f6-ad81-06949bbb9c1c
		- (Page 12)
	- -
	- -
		- la ruta /home. Esta carpeta ofrece un lugar en el que los usuarios pueden guardar sus ficheros, además de ser la ubicación por defecto que muchas aplicaciones usan para guardar las configuraciones específicas de cada usuario. Por ejemplo, las claves para  las  conexiones  SSH  se  guardan en  la  carpeta  ~/.ssh  y el  histórico  de  Bash  se guarda  en  ~/.bash_profile. #flashcard
		  id:: b9d3d9f6-0d30-43db-869f-f42ef011d8e0
		- (Page 13)
	- -
	- -
		- **$ id ubuntu**
		  id:: 31bbb147-2f03-41c2-9f29-d18afb440be4
		  
		  uid=1000(ubuntu) gid=1000(ubuntu) min),126(sambashare) groups=1000(ubuntu),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),116(lpad #flashcard
		- (Page 17)
	- -
	- -
		- $ sudo useradd -m -G sudo,cdrom ubuntu_sudo
		  id:: b905a404-546f-456f-9664-336cd08ec2b7
		  $ id ubuntu_sudo uid=1002(ubuntu_sudo) gid=1002(ubuntu_sudo) groups=1002(ubuntu_sudo),24(cdrom),27(sudo) #flashcard
		- (Page 17)
	- -
	- -
		- $ sudo usermod -a -G plugdev ubuntu_sudo $ id ubuntu_sudo uid=1002(ubuntu_sudo) gid=1002(ubuntu_sudo) groups=1002(ubuntu_sudo),24(cdrom),27(sudo),46(plugdev) #flashcard
		  id:: 3bf69dae-cdd7-4d3a-8629-3b8d19d06f28
		- (Page 17)
	- -
	- -
		- Al  igual  que  otros  sistemas  operativos,  en  Linux  existe  el  concepto  de  servicio, también llamado  daemon.  Los  serviciosson  procesos  que  no  terminan inmediatamente  tras  la  ejecución,  como  el  comando  pwd,  sino  que  se  ejecutan continuamente,  ofreciendo  ciertas  funcionalidades  al  sistema  operativo  o  a  los usuarios. Algunos ejemplos de servicios son, por ejemplo, el  daemonde SSH, cuyo proceso se llama sshd, o el servidor web Apache, cuyo proceso es httpd. El comando ps auxmuestra todos los procesos en ejecución, tanto servicios como otros procesos. #flashcard
		  id:: 544acdbe-fbd9-44f5-a724-3ff86e840d1d
		- (Page 18)
	- -
	- -
		- Se puede hacer uso de la sustitución al vuelo de comandos de Bash para obtener el PID del proceso con pidof e insertarlo en kill en una sola línea:
		  id:: 5bc6de58-279a-47a3-b670-0d409a61c00b
		  
		  **$ sudo kill -9 `pidof top`** #flashcard
		- (Page 20)
	- -
	- -
		- killallterminará todos los  procesos  con  ese  nombre.  También  permite  especificar  un  usuario,  por  lo  que terminará los procesos de ese usuario. #flashcard
		  id:: 1adf4b96-2e98-48c6-8dc2-929c9332fc2d
		- (Page 20)
	- -
	- -
		- killall terminará también el proceso de consola y, por tanto, terminará la sesión del usuario. $ killall -u username $ killall -r httpd #flashcard
		  id:: b8f92880-bff0-4d87-9ef5-41faf085aeca
		- (Page 21)
	- -
	- -
		- **$ pkill [-P] pid**
		  id:: 121fca0c-2d94-4120-8084-c4f1ac67845a
		  
		  Finalmente, pkill permite terminar procesos con el nombre del proceso.
		  Es también capaz de terminar los procesos hijos de un proceso padre con el flag -P. #flashcard
		- (Page 21)
	- -
	- -
		- El comando uptime muestra por consola un resumen del estado del sistema:
		  id:: 1605966c-e725-4f87-b9df-1001d9f34b4f
		  la hora actual,
		  el tiempo que el sistema ha estado arrancado,
		  el número de usuarios conectados
		  y el uso medio del CPU en el último minuto, últimos cinco últimos quinceminutos.
		  
		  **$ uptime**
		  *23:32:56 up 37 min, 2 users, load average: 0.00, 0.00, 0.05* #flashcard
		- (Page 26)
	- -
	- -
		- **$ df -h** muestra el espacio disponible en los sistemas de ficheros montados. En la Figura20se muestra la salida de dfen una instalación de Ubuntu con escritorio. El modificador -h imprime los valores en unidades más legibles para un usuario, como KB, MB, etc. #flashcard
		  id:: 41d4d344-4e39-4f8d-a173-35167f176a5c
		- (Page 28)
	- -
	- -
		- El directorio /proc es un directorio especial, ya que contiene archivos con información del sistema operativo. De hecho, no solo se puede obtener información, sino que es posible cambiar los parámetros del núcleo de Linux editando los archivos contenidos de /proc, modificando así el comportamiento del sistema.
		  id:: 2c910ac0-a4a0-4f7b-803e-18a36dbeb295
		  
		  El sistema de archivos /proc no es un directorio real en el disco duro, sino una colección de estructuras de datos en la memoria, administrada por el núcleo, que aparece como un conjunto de directorios y archivos. El propósito de /proc (también llamado sistema de archivos de procesos) es ofrecer acceso a la información sobre el sistema operativo y sobre todos los procesos que se encuentran en ejecución. Los archivos de /proc son accesibles,como cualquier otro, pero es necesario conocer el significado y la sintaxis de ellos para interpretar la información. #flashcard
		- (Page 29)
	- -
	- -
		- Fuente: elaboración propia. Otro  archivo  interesante  es  /proc/cpuinfo.  Este contiene  las  características  de  los procesadores del equipo: fabricante, modelo, conjuntos de instrucciones, frecuencia, etc. #flashcard
		  id:: 45fde17c-b882-4eb6-9565-9957172336cb
		- (Page 30)
	- -