title:: Administacion de Sistemas para la Cloud Tema-1 (highlights)
deck:: [[UNI::Administacion de Sistemas para la Cloud Tema-1]]
author:: [[UNIR]]
full-title:: "Administacion de Sistemas para la Cloud Tema-1"
category:: #books

tags:: Administración-de-Sistemas-para-la-Cloud UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/341d7308-ccc7-45c6-aeca-19807120d9fa.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Explica la diferencia entre un entorno onsite y uno offsite #flashcard
		  id:: 6619399d-0c1b-406d-8603-a68ae4b6244d
			- Onsite tiende a referirse a una localización propia de la organización, frente a una ubicación offsite, a la que la organización tiene acceso por red. Un entorno offsite tradicional podía ser un centro de datos o una parte de un centro de datos subalquilado a un proveedor. En estos casos,  la  organización  cliente  podía  llegar  a  optar  por  administrar  los  servidores físicos y subcontratar el espacio y la electricidad.
		- (Page 5)
	- -
	- -
		- ¿Es necesario que un devops tenga conocimientos de networking? #flashcard
		  id:: 8565009b-998f-48fc-8e91-6e7ad34800d0
			- Un  DevOps tendrá  que  combinar  sus  conocimientos  de  desarrollo  y  administración  con conocimientos de red, para establecer las conexiones adecuadas. Estos recursos de red  serán  en  muchos  casos  virtuales  y,  por lo  tanto,  también  deben  ser automatizados.
		- (Page 6)
	- -
	- -
		- ¿Cómo podríamos tener la máxima disponibilidad de recursos en la nube? #flashcard
		  id:: 72e89a95-0100-400a-a585-05772b382b29
			- Esto  no  es  algo  que  pueda  lograrse  de forma automática por el mero hecho de utilizar la nube. Si bien es cierto que se podría pensar que al usar la nube no habrá caídas en los sistemas por fallos de hardware, no es  menos  cierto  que  las  máquinas  en  la  nube  a  veces  necesitan  ser  movidas  para tareas  de  mantenimiento  o  incluso  apagadas  por  parte  del  proveedor.  En  este escenario, muy cercano a la realidad, la única forma de garantizar el uptime es contar con mecanismos que permitan desplegar flotas de servidores autogestionados.
		- (Page 7)
	- -
	- -
		- Define flota. #flashcard
		  id:: 7cf0637b-42e3-4853-bff8-404f03ac6840
			- El concepto de flota se puede concretar en un grupo de autoescalado en AWS (Amazon Web Services) o en un despliegue en Kubernetes, por citar algunos.
			  
			  Los objetivos detrás de un grupo de servidores autogestionados son:
		- (Page 8)
	- -
	- -
		- Un servidor,
		  id:: 9c0864f8-4910-475d-a8b8-bf8ec20ce49c
		  * ¿en qué se diferencia de un cliente?
		  * ¿debería dicho servidor tener interfaz gráfica? #flashcard
			- Los  sistemas  operativos  usados  como  servidores  no  son  muy diferente  de  los  que ejecutan  los  ordenadores  de  sobremesa  o  los  portátiles.  Ambos  tipos  tienen  un núcleo,  una  arquitectura  de  procesador  habitualmente  compatible  (por  ejemplo, x86), controladores de hardware y utilidades de software. Muchos de los ejemplos descritos pueden ejecutarse también en un entorno de escritorio sin cambio alguno. Sin embargo, una instalación de servidor suele tener dos características relevantes: solo  es  posible  interactuar  con  él  por  red  y  no  tiene  entorno  gráfico.  Un  DevOps deberá  escoger  herramientas  que  le  permitan  adaptarse  a  ambas  características. Como normal general, cuantas menos piezas tenga un sistema, menos pueden fallar. Si  los  servidores  no  tienen  una  pantalla  conectada,  ¿por  qué  no  obviar  el  sistema gráfico totalmente?
		- (Page 9)
	- -
	- -
		- Menciona las tareas propias de un administrador de sistema y también cómo éstas están divididas en sus respectivos roles. #flashcard
		  id:: 16f00f21-1c8c-4a82-9c45-ed24ce522f96
			- Muchos grupos de soporte de IT (information technology) dividen las tareas en roles. Esto facilita que cada rol cree una base de conocimiento profunda para resolver problemas y ejecutar tareas. Una separación de tareas en roles podría ser la siguiente:
			  
			  Servicios de usuario:
			  • Nivel 2 de soporte a usuario.
			  • Instalación de periféricos.
			  • Instalación y mantenimiento de aplicaciones.
			  • Instalación de equipos de usuario.
			  
			  Administración de servidores:
			  • Instalación de servidores.
			  • Creación de usuarios y grupos.
			  • Copias de seguridad y recuperación frente a desastres.
			  • Automatización de tareas.
			  
			  Seguridad IT:
			  • Soporte de red.
			  • Gestión de cambios.
		- (Page 11)
	- -
	- -
		- ¿Qué representa la regla 90-8-2? #flashcard
		  id:: 9fa21045-d704-47ac-8b7a-7855cf908168
			- Un objetivo de los departamentos es tener una política 90-8-2:
			  
			  Los usuarios resuelven por sí mismos el 90 % de las incidencias.
			  
			  Los grupos de soporte intermedios se encargan de resolver un 8 %, que serán situaciones más complicadas, pero normalmente documentadas y en las que no hay que involucrar a un experto.
			  
			  Los administradores solo reciben un 2 % de los problemas. Así se pueden dedicar a tareas en las que añaden valor a la organización.
		- (Page 13)
	- -
	- -
		- Define knowledge base. #flashcard
		  id:: dd933fb2-123e-46d6-88b1-9e1592b082c4
			- Tanto  la  comunicación  con  otros  equipos  como  la  interna  benefician  a  todas  las partes. Internamente, estar al tanto de lo que ocurre o de cómo se ha solucionado un  problema  puede  ayudar  en  futuros  problemas.  La  documentación  de  estas soluciones se suele llevar a cabo en un knowledge base (KB), o base o biblioteca de conocimiento.  Incluso,  algunas  organizaciones  publican  estos  KB  al  exterior  (bien públicamente o al menos a un sector interno más amplio que el propio equipo de IT), para facilitar la resolución proactiva de problemas.
		- (Page 13)
	- -