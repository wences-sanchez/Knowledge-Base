title:: Readwise/Administración de Sistemas para la Cloud Tema-9 (highlights)
deck:: [[Across-the-Net]]
author:: [[UNIR]]
full-title:: "Administración de Sistemas para la Cloud Tema-9"
category:: #articles

tags:: Administración-de-Sistemas-para-la-Cloud UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/fae11c36-3217-4264-98f0-78802e83eb1f.jpg)
- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- ¿Qué son las directivas de grupo en Windows? #flashcard
			- Las directivas de grupo, o group policies, también denominadas GPO (group policy object),  están  diseñadas  para  proporcionar  a  los  administradores  del  sistema  la capacidad de personalizar la configuración del usuario final y establecer restricciones sobre  los  tipos  de  acciones  que  los  usuarios  pueden  realizar.  Los  administradores pueden crear directivas de grupo y luego aplicarlas a uno o más usuarios, servidores o  equipos  de  escritorio  dentro  del  entorno.  En  general,  estas  configuraciones modifican  opciones  del  registro  de  Windows,  pero  es  más  fácil  configurar  las opciones  mediante  directivas  de  grupo  que  realizar  cambios  en  el  registro manualmente.
		- (Page 5)
	- -
	- -
		- ¿Qué tres opciones de configuración pueden tener las directivas de grupo en Windows? #flashcard
			- La  mayoría  de  los  elementos  de  la  directiva  de  grupo  tienen  tres  opciones  de configuración diferentes (ver Figura 1):   Enabled:  especifica  que  se  ha  establecido  una  configuración  para  esta  GPO. Algunas  GPO  requieren  que  se  establezcan  valores  u  opciones  concretos.  Por ejemplo,  la  directiva  de  account  lockout  (bloqueo  de  cuenta)  debe  especificar cuántos intentos de inicio de sesión incorrectos pueden realizarse antes de que la cuenta se bloquee.   Disabled.  Especifica  que  esta  opción  está  desactivada,  es  decir,  que  el administrador del sistema desea no permitir ciertas funciones.
		- (Page 6)
	- -
	- -
		- CONTINUE #flashcard
			-   Not  Configured.  Especifica  que  esta  configuración  no  se  ha  habilitado  ni deshabilitado.  Simplemente  establece  que  esta directiva  de  grupo no  establece esta configuración, aunque otras GPO pueden haberla configurado.
		- (Page 7)
	- -
	- -
		- ¿Qué opciones principales se pueden configurar dentro de las directivas de grupo de Windows? #flashcard
			- Las principales opciones que puede configurar dentro de las directivas de grupo son las siguientes:   Configuración  de  software  (software  settings).  Se  aplican  a  aplicaciones  y software específicos que pueden instalarse en los equipos. Los administradores pueden  usar  esta  configuración  para  hacer  que  las  nuevas  aplicaciones  estén disponibles  para los  usuarios  finales  y  para  controlar la  configuración predeterminada de estas.   Configuración de Windows (Windows settings).  Permiten a los administradores personalizar  el  comportamiento  del  sistema  operativo.  Incluye  opciones  para configurar Internet Explorer (incluida la página de inicio predeterminada y  otras configuraciones), seguridad (como la política de cuenta) o el registro de eventos.   Plantillas administrativas (administrative templates). Se utilizan para configurar aún  más  las  configuraciones  de  usuario  y  equipo.  Además  de  las  opciones predeterminadas disponibles, los administradores del sistema pueden crear sus propias plantillas administrativas con opciones personalizadas.
		- (Page 7)
	- -
	- -
		- Las principales opciones que puede configurar dentro de las directivas de grupo son las siguientes:   Configuración  de  software  (software  settings).  Se  aplican  a  aplicaciones  y software específicos que pueden instalarse en los equipos. Los administradores pueden  usar  esta  configuración  para  hacer  que  las  nuevas  aplicaciones  estén disponibles  para los  usuarios  finales  y  para  controlar la  configuración predeterminada de estas.   Configuración de Windows (Windows settings).  Permiten a los administradores personalizar  el  comportamiento  del  sistema  operativo.  Incluye  opciones  para configurar Internet Explorer (incluida la página de inicio predeterminada y  otras configuraciones), seguridad (como la política de cuenta) o el registro de eventos.   Plantillas administrativas (administrative templates). Se utilizan para configurar aún  más  las  configuraciones  de  usuario  y  equipo.  Además  de  las  opciones predeterminadas disponibles, los administradores del sistema pueden crear sus propias plantillas administrativas con opciones personalizadas. #flashcard
		- (Page 7)
	- -
	- -
		- ¿Qué cuatro niveles jerárquicos incluyen los objetos de directiva de grupo en Windows? #flashcard
			- la  configuración  de  la  directiva  de  grupo  es jerárquica. Hay cuatro niveles que determinan la prioridad de procesamiento de GPO:   Local.  Cada  equipo  tiene  un  objeto  de  directiva  de  grupo  que  se  almacena localmente.   Sitios.  La  configuración  de  GPO  de  un  sitio  se  aplica  a  todos  los  dominios  y servidores que forman parte de este.   Dominios.  Los  dominios  son  el  tercer  nivel  al  que  los  administradores  pueden asignar GPO. La configuración de GPO ubicada en el nivel de dominio se aplicará a todos los objetos de usuario y equipo dentro del dominio.   Unidades  organizativas  (OU).  Es  el  nivel  de  configuración  más  granular.  Si  la estructura de OU está bien planificada, resultará fácil hacer asignaciones lógicas de GPO a departamentos o unidades de negocio.
		- (Page 9)
	- -
	- -
		- ¿Qué dos opciones permite la configuración de los GPO de Windows? #flashcard
			- Aunque el comportamiento predeterminado es que la configuración sea acumulativa y heredada, este comportamiento se puede modificar con dos opciones:   Bloqueo  de  herencia.  Especifica  que  las  directivas  de  grupo  para  un  objeto contenedor no se heredan de los contenedores superiores. Esto puede ser útil, por ejemplo, cuando una unidad organizativa secundaria requiere una configuración completamente diferente de una unidad organizativa principal.
		- (Page 10)
	- -
	- -
		-   Forzar  herencia  de  directivas.  Cuando  se  activa  esta  opción  en  un  GPO,  se garantiza que todos los objetos de nivel inferior hereden estas configuraciones. En algunos  casos,  los  administradores  desean  asegurarse  de  que  la  herencia  de  la directiva  de  grupo  no  esté  bloqueada  en  otros  niveles.  Por  ejemplo,  se  puede aplicar en una política corporativa de contraseña para que los administradores de OU inferiores no la bloqueen (hay que recordar que las OU permiten delegar la administración de objetos, por lo que los administradores de una OU no tienen por qué ser los mimos que se encargan del domino). #flashcard
		- (Page 11)
	- -
	- -
		- ¿Cómo te conectarías remotamente con PowerShell? #flashcard
			- se puede abrir una sesión de PowerShell interactiva, de la misma manera que se puede iniciar una sesión interactiva de SSH en Linux. La primera opción pasa por usar el parámetro -ComputerName. Muchos de los cmdlets disponibles en PowerShell, en particular los que comienzan con Get-, se pueden usar con el parámetro -ComputerName. Esto especifica que el comando en cuestión debe ejecutarse en el sistema remoto que especifique este parámetro. Por ejemplo, para comprobar  si  el  servicio  del  programador  de  tareas  está  arrancado  en  el  servidor server1, habría que ejecutar el siguiente comando: Get-Service schedule -ComputerName server1 El parámetro acepta más de un nombre de host, por lo que, en caso de especificar varios, la salida mostrará la ejecución del comando en cada uno de los equipos. Por  otro  lado,  a  veces  es  más  cómodo  usar  Enter-PSSession  e  iniciar  una  sesión interactiva en la que ejecutar los  cmdlets. Al ejecutar  Enter-PSSession, la línea de comandos pasa a ser la shell del equipo remoto. Los cmdlets  se ejecutarán en esa shell, que tiene su propio entorno y sus propias variables. Para arrancar una consola en el servidor server1, habría que ejecutar: Enter-PSSession -ComputerName server1
		- (Page 13)
	- -
	- -
		- Esto especifica que el comando en cuestión debe ejecutarse en el sistema remoto que especifique este parámetro. Por ejemplo, para comprobar  si  el  servicio  del  programador  de  tareas  está  arrancado  en  el  servidor server1, habría que ejecutar el siguiente comando: Get-Service schedule -ComputerName server1 El parámetro acepta más de un nombre de host, por lo que, en caso de especificar varios, la salida mostrará la ejecución del comando en cada uno de los equipos. Por  otro  lado,  a  veces  es  más  cómodo  usar  Enter-PSSession  e  iniciar  una  sesión interactiva en la que ejecutar los  cmdlets. Al ejecutar  Enter-PSSession, la línea de comandos pasa a ser la shell del equipo remoto. Los cmdlets  se ejecutarán en esa shell, que tiene su propio entorno y sus propias variables. Para arrancar una consola en el servidor server1, habría que ejecutar: Enter-PSSession -ComputerName server1 #flashcard
		- (Page 13)
	- -
	- -
		- Esto especifica que el comando en cuestión debe ejecutarse en el sistema remoto que especifique este parámetro. Por ejemplo, para comprobar  si  el  servicio  del  programador  de  tareas  está  arrancado  en  el  servidor server1, habría que ejecutar el siguiente comando: Get-Service schedule -ComputerName server1 El parámetro acepta más de un nombre de host, por lo que, en caso de especificar varios, la salida mostrará la ejecución del comando en cada uno de los equipos. Por  otro  lado,  a  veces  es  más  cómodo  usar  Enter-PSSession  e  iniciar  una  sesión interactiva en la que ejecutar los  cmdlets. Al ejecutar  Enter-PSSession, la línea de comandos pasa a ser la shell del equipo remoto. Los cmdlets  se ejecutarán en esa shell, que tiene su propio entorno y sus propias variables. Para arrancar una consola en el servidor server1, habría que ejecutar: Enter-PSSession -ComputerName server1 #flashcard
		- (Page 13)
	- -