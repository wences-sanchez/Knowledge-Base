# Administración de Sistemas para la Cloud Tema-2

deck:: [[UNI::Administración de Sistemas para la Cloud Tema-2]]\
author:: [[UNIR]]\
full-title:: "Administración de Sistemas para la Cloud Tema-2"\
category:: #books\
\
tags:: Administración-de-Sistemas-para-la-Cloud UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/5b66d271-6a8e-428f-91ae-f8dfcb024839.jpg)

## Highlights
- 
 ¿A qué nos referimos normalmente como una distribución de Linux? #flashcard 
    Una distribución de Linux es un paquete que consiste en el núcleo del sistema operativo y una colección de paquetes y aplicaciones (Dulaney, 2018). Dada una misma versión del núcleo, una aplicación escrita para Linux debería ser ejecutable en cualquier distribución con ese núcleo. No obstante, dado que la colección de aplicaciones abarca desde el instalador al entorno gráfico y el gestor de paquetes, la manera de interactuar con cada distribución puede ser muy diferente. La licencia también varía de una distribución a otra: aunque Linux es de código abierto, hay distribuciones comerciales que se ofrecen con contratos de soporte. Compañías como SUSE o RedHat no cobran por el sistema operativo, sino por el soporte que ofrecen a sus clientes.

     (Page 4)
-
- 
 ¿Qué es Telnet (como acceso remoto)? #flashcard 
    Telnet es un protocolo de capa de aplicación, utilizado en Internet o redes de área local, para proporcionar acceso remoto mediante una conexión de terminal virtual. La utilización de Telnet está desaconsejada, porque el tráfico no se transmite cifrado. Este hecho permitiría a un usuario malintencionado acceder al contenido del tráfico, si fuera capaz de interceptarlo.

     (Page 6)
-
- 
 ¿Qué es SSH (como acceso remoto)? #flashcard 
    Secure Shell (SSH) es un protocolo de red de cifrado para servicios de red de operación segura a través de una red no segura. Su aplicación más habitual es la de inicio de sesión remoto a servidores Linux. SSH proporciona un canal seguro mediante una arquitectura cliente-servidor. Los sistemas operativos Linux cuentan habitualmente con un cliente de SSH. En el caso de los clientes Windows, el cliente más utilizado es el llamado Putty. Se trata de un cliente de SSH de código abierto y libre (Van Vugt, 2015). SSH es la forma más habitual de acceder a los servidores, tanto aquellos alojados en la nube como servidores tradicionales en un centro de datos propio. SSH soporta el acceso con usuario y password y el uso de certificados (también llamados pareja de claves o key pair). En muchos de los proveedores de nube pública, el uso de certificados es obligatorio.

     (Page 6)
-
- 
 Describe los pasos para establecer una conexión SSH con un servidor Ubuntu #flashcard 
     Ejecutar sudo apt-get update && sudo apt-get install -y openssh-server.  Asegurarse de que el servicio esté arrancado con sudo service ssh start.  Editar el archivo de configuración con sudo vim /etc/ssh/sshd_config o con cualquier otro editor de texto. El fichero debe contener al menos las siguientes opciones. Estas opciones no son las más seguras, pero servirán para poder hacer pruebas en entornos locales: • Port 22. • ListenAddress 0.0.0.0. • PasswordAuthentication yes.  Recargar la configuración con sudo service sshd reload.  Averiguar la IP (internet protocol) del equipo con ip address. En este punto, ya sería posible usar un cliente para conectarse y, en un entorno local, no será necesario más configuración. En un entorno de nube, será necesario haber habilitado el puerto 22 en el grupo de seguridad de la instancia.

     (Page 8)
-
- 
 ¿Cómo funciona la clave privada SSH entre servidores? #flashcard 
    es más seguro no utilizar contraseñas para los inicios de sesión. SSH soporta autenticación basada en claves: el usuario crea una pareja de claves, pública y privada, y copia la clave pública a aquellos servidores a los que se va a conectar. Al conectar, selecciona la clave privada en el cliente SSH. El servidor, al recibir la conexión, comprobará que la clave privada corresponde con la clave pública

     (Page 14)
-
- 
 Comando para crear pares clave pública-privada. #flashcard 
    **$ ssh-keygen -t rsa -b 4096 -f./security_key**

     (Page 14)
-
- 
 ¿Cómo se llaman y dónde se guardan en Linux la pareja de claves SSH pública y privada recién creadas? #flashcard 
    La clave pública se guardará en el fichero security_key.pub y la clave privada en security_key. Por defecto, las rutas serían ~/.ssh/id_rsa.pub y ~/.ssh/id_rsa.

     (Page 14)
-
- 

ssh-copy-id -i ./security_key.pub <usuario>@<equipo_remoto> #flashcard 


     (Page 14)
-
- 

A partir de ese momento, ya es posible conectarse indicando el fichero de clave privada. El cliente solicitará la clave del fichero, pero no hace falta indicar la contraseña del usuario: ssh -i ./security_key <usuario>@<equipo_remoto> #flashcard 


     (Page 15)
-
- 
 ¿Cómo harías, en bash, para ver cada línea de un script antes de que se ejecute? #flashcard 
    los scripts de shell se pueden invocar con el parámetro -v, que muestra cada línea antes de ejecutarla

     (Page 18)
-
- 
 ¿Cómo funciona la IP pública en instancias de AWS? #flashcard 
    dado que el objetivo es demostrar el acceso remoto, la opción de asignar una IP pública está habilitada. Las redes virtuales suelen tener rangos de direcciones privadas, personalizables por el usuario, pero no enrutables desde Internet. Esto no suele ser un problema, y de hecho suele ser deseable. AWS ofrece varios servicios para exponer una aplicación a Internet (por ejemplo, API Gateway), pero,en estecaso,es suficiente con que la instancia tenga una IP pública. La tarjeta de red de la instancia seguirá teniendo una IP privada y AWS configurará un NAT (network address translation) entre la IP pública y la privada

     (Page 21)
-
- 
 ¿Cómo funcionan los grupos de seguridad en AWS? #flashcard 
    Los grupos de seguridad, o security groups, son firewalls a nivel de instancia que se ejecutan a nivel de hipervisor, por lo que liberan al sistema operativo de ejecutar un firewall interno. Los grupos de seguridad de AWS bloquean todo el tráfico entrante y permiten todo el tráfico saliente por defecto. Dado que el objetivo es el acceso remoto a un equipo Linux, es necesario añadir al menos una regla para permitir el SSH desde el equipo de origen. Se puede abrir el puerto a cualquier IP, aunque es recomendable restringirlo a la IP que detecta la consola web

     (Page 23)
-
