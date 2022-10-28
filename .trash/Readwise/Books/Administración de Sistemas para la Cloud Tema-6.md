# Administración de Sistemas para la Cloud Tema-6

deck:: [[UNI::Administración de Sistemas para la Cloud Tema-6]]\
author:: [[UNIR]]\
full-title:: "Administración de Sistemas para la Cloud Tema-6"\
category:: #books\
\
tags:: Administración-de-Sistemas-para-la-Cloud UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/f0b7705f-2058-4ff4-b2c6-eba91a7415cc.png)

## Highlights
- 

Windows Server 2019 está disponible en dos ediciones, también conocidas como SKU: Standard y Datacenter. Las ediciones se diferencian por su precio y las funcionalidades que soportan. La edición Datacenter está enfocada principalmente a entornos de virtualización y puede alojar un número ilimitado de máquinas virtuales (siempre que el servidor sea capaz de servir los requisitos de hardware virtual), mientras que la edición Standard solo puede ejecutar dos máquinas. Además de algunas diferencias específicas de Hyper-V (el hipervisor de virtualización de Windows), Datacenter soporta software defined networking (SDN, redes definidas por software), #flashcard 


     (Page 5)
-
- 

Ambas ediciones soportan, además, varios modos de ejecución:  Escritorio o Server with Desktop Experience.  Server Core.  Nano Server. El modo de escritorio es el más familiar, ya que convierte al servidor en un host similar a cualquier máquina Windows: tiene botón de inicio, ventanas y consolas de #flashcard 


     (Page 5)
-
- 

configuración. El modo Core, sin embargo, no tiene escritorio. Mantiene las funcionalidades para soportar aplicaciones tradicionales y permite la activación de cualquier rol, pero no tiene el entorno de escritorio tradicional. Está pensando para ser administrado remotamente a través de la línea de comandos, con PowerShell o con consolas MMC remotas. Hay otras diferencias, como que Server Core no incluye las herramientas de accesibilidad, soporte de audio o Internet Explorer. La Tabla 1 lista algunas de las diferencias en cuanto a disponibilidad de aplicaciones entre ambos modos. Administración de Sistemas en la Cloud Tema 6. Ideas clave 6 I ) R N U i j ( a o R a L e d l a n o i c a n r e t n I d a d i s r e v i n U © #flashcard 


     (Page 6)
-
- 

El tercer modo de ejecución mencionado anteriormente, Nano Server, no es un modo de instalación y, de hecho, no es posible instalarlo sobre hardware físico o virtual. Esta opción era posible con Windows Server 2016, pero no lo es con Windows Server 2019. Nano Server solo está disponible para ser ejecutado como un contenedor y, por tanto, Microsoft no ofrece un disco de instalación, sino una imagen base de contenedor. Nano Server es aún más limitado que Server Core, pero, al ser más ligero, está más indicado para entornos de virtualización. #flashcard 


     (Page 8)
-
- 

Remote Desktop Protocol (RDP) es un protocolo propietario, desarrollado por Microsoft, que proporciona al usuario una interfaz gráfica para conectarse a otro ordenador a través de una conexión de red. El usuario necesita un cliente RDP mientras que el otro equipo debe tener habilitada la funcionalidad de acceso remoto. #flashcard 


     (Page 9)
-
- 

La consola nativa de Windows, PowerShell, permite ejecutar comandos al iniciar sesiones de consola en hosts remotos. Está disponible tanto en el servidor con escritorio como en Server Core y puede habilitarse en Nano Server si se instala PowerShell Core. #flashcard 


     (Page 10)
-
- 

La herramienta de Administración de Servidor, o Server Manager, ofrece una interfaz gráfica para ejecutar tareas de configuración, tanto en el equipo local como en equipos remotos. Ofrece acceso a consolas de administración de roles de Windows, como DNS o Directorio Activo, desde un único punto, instalación de roles, escritorio remoto, etc. La Figura 6 muestra una instancia de Server Manager #flashcard 


     (Page 11)
-
- 

La consola tradicional de administración de Windows, MMC (Microsoft Management Console), es otra herramienta gráfica de configuración. Mientras que Server Manager es una herramienta centralizada, MMC ofrece múltiples snapins para cada funcionalidad y solo permite administrar un equipo con cada snapin. De hecho, parte de la funcionalidad de Server Manager es abrir la consola MMC con el snapin correcto en un equipo concreto, ahorrando tiempo al administrador. MMC soporta servidores con escritorio, Server Core y Nano Server. #flashcard 


     (Page 12)
-
- 

RSAT no es más que una colección de herramientas de administración remotas, listas para ser instaladas en un equipo Windows cliente (por ejemplo, Windows 10) con un único paquete. Incluye Server Manager, la consola MMC con múltiples snapins y commandlets de PowerShell que solo las versiones de Windows Server incorporan por defecto. #flashcard 


     (Page 13)
-
- 

Directorio Activo, o AD (Active Directory), es un servicio de directorio para redes de equipos Windows. Cualquier versión de Windows Server puede actuar como controlador de dominio, desde Windows Server 2000. AD se usa para tareas de administración centralizada, aparte de integrar otras funcionalidades, como servicios de certificados. #flashcard 


     (Page 14)
-
- 

Un controlador de dominio es un servidor Windows que ejecuta el servicio Active Directory Domain Service. Autentica y autoriza todos los usuarios y equipos de un dominio y les aplica políticas de seguridad. Por ejemplo, cuando un usuario inicia sesión en un ordenador que es parte de un dominio Windows, un controlador de dominio, y no el equipo local, comprueba que la contraseña sea válida. #flashcard 


     (Page 14)
-
- 

A nivel de protocolos, AD se sirve de múltiples tecnologías:  DNS para localizar servicios (gracias a entradas SRV) y para identificar tanto dominios como los equipos miembros del dominio.  LDAP es el servicio de directorio como tal. Sirve de base de datos para alojar información de las cuentas de máquinas y de usuario. Es extensible, por lo que sistemas como Exchange pueden alojar datos adicionales de cada usuario, como los datos de la cuenta de correo, sin necesidad de crear otro repositorio de datos.  Kerberos es el sistema de autenticación y autorización entre equipos. #flashcard 


     (Page 14)
-
- 

AD funciona esencialmente como una base de datos administrativa. Usa una estructura jerárquica formada por objetos, dominio, árboles y bosques #flashcard 


     (Page 14)
-
- 

Los objetos son los elementos básicos del dominio. Representan los ordenadores cliente (por ejemplo, los equipos ofimáticos de escritorio, que actúan como clientes de AD), los servidores de aplicaciones (que, a efectos del directorio, son también clientes de AD), carpetas compartidas y cuentas de usuario. Cada objeto tiene un identificador único y un conjunto de atributos. #flashcard 


     (Page 15)
-
- 

Los objetos se pueden organizar en objetos contenedores, como carpetas y unidades organizativas, o OU. Las carpetas son similares a las de un sistema de ficheros, pero las unidades organizativas permiten, además, aplicar políticas de seguridad a los objetos de la OU y delegar la administración a otros usuarios. #flashcard 


     (Page 15)
-
- 

Un dominio es un área de la red con una única base de datos de autenticación. A efectos prácticos, sirve para establecer límites administrativos entre diferentes grupos de red. Cualquier objeto pertenece a un único dominio y los objetos de un mismo dominio pueden estar dispersos en diferentes ubicaciones físicas. Por ejemplo, una organización puede establecer un dominio para cada departamento, pero en una misma oficina pueden convivir usuarios y equipos de departamentos diferentes sin que eso rompa la estructura del dominio. #flashcard 


     (Page 16)
-
- 

Cada dominio tendrá al menos un controlador de dominio, o DC, que actúa como autoridad de aquel; es decir, es responsable de los permisos de los objetos, la autenticación y las modificaciones de objetos. Es habitual que un dominio disponga de más de un DC. Esta disposición es posible porque los DC pueden trabajar de manera distribuida y es necesaria porque la caída del único DC de un dominio colapsaría todas las máquinas del dominio, ya que nadie podría iniciar sesión ni acceder a carpetas compartidas. Los controladores de dominio suelen alojar el servicio DNS, que también puede funcionar en modo distribuido. #flashcard 


     (Page 16)
-
- 
 ¿Cómo se organizan en árboles el Directorio Activo? #flashcard 
    Cada dominio tiene una estructura de árbol de contenedores. Estos contenedores pueden ser carpetas normales o unidades organizativas. La Figura 9 muestra el árbol de carpetas de un dominio y el contenido de una de las carpetas.

     (Page 16)
-
- 

Los dominios se identifican con un nombre DNS. De hecho, la creación de un dominio requiere la presencia de un servicio DNS asociado, bien externo o integrado en el propio dominio. Al ser un nombre DNS, las cuentas de máquina reciben un nombre de dominio completo (o FQDN, fully qualified domain name) en el que se une el nombre del host con el nombre del dominio. Un equipo con nombre member en el dominio demo.loc tendrá un registro DNS member.demo.loc. La integración de AD con DNS es tan fuerte que los dominios siguen una estructura de árbol, de manera que un dominio padre puede ser demo.loc y un dominio hijo podría ser, a su vez, child.demo.loc. #flashcard 


     (Page 17)
-
- 
 ¿Qué son los bosques dentro del Directorio Activo? #flashcard 
    Las empresas con cientos o miles de usuarios pueden disponer de varios árboles de directorios. Los administradores podrán organizar los árboles en bosques. Los bosques son el límite administrativo y de seguridad más amplio en una estructura AD. Una organización puede decidir tener no ya varios dominios, sino varios bosques. Esta situación es habitual, por ejemplo, cuando hay uniones y adquisiciones de organizaciones. En estos casos, es posible conectar los bosques con una relación de confianza. Estas relaciones extienden la accesibilidad de los recursos de los dominios, de manera que centraliza la administración a nivel lógico.

     (Page 18)
-
