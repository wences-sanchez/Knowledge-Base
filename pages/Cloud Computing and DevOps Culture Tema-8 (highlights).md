title:: Cloud Computing and DevOps Culture Tema-8 (highlights)
author:: [[UNIR]]
full-title:: "Cloud Computing and DevOps Culture Tema-8"
category:: #books

tags:: Cloud-Computing-and-DevOps-Culture UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/9fe9ff3c-7718-4510-96c8-8e89dcd7233b.png)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Acerca de IaC y DevOps. #flashcard
		  id:: da27bda9-20d8-41e7-be81-bfa15bb0c075
			- La infraestructura  como  código  (en  siglas,  IaC)  trata la infraestructura  de configuración  de  sistemas  como  un  software  de  programación.  Esto  genera  una delgada línea entre los límites de la escritura de aplicaciones y la creación de entornos en los que se ejecutan. Se trata de una parte fundamental de la computación en la nube y esencial para DevOps. La IaC es el marco que ha dado origen a DevOps.
		- (Page 6)
	- -
	- -
		- ¿Cuáles son las cinco etapas del ciclo de vida de los recursos de infraestructura? #flashcard
		  id:: adf3b62d-d9ba-43f1-9905-4cd19c27e62c
			-   Aprovisionamiento de recursos. Etapa en la que los administradores utilizan este principio de la IaC para aprovisionar recursos de acuerdo con sus especificaciones y necesidades. AWS CloudFormation puede ser un claro ejemplo para aplicar.   Gestión de configuración. Los recursos se vuelven componentes de un sistema de gestión  de  configuración  que  soportan  actividades  tales  como  optimización  y actualización.   Supervisión y rendimiento. Herramientas de supervisión y rendimiento validan el estado  operacional  de los  recursos  examinando ítems  como  métricas, transacciones sintéticas y archivos de registro.
		- (Page 7)
	- -
	- -
		- BORRAR #flashcard
		  id:: 2031710f-8c47-43a4-bca0-452ad8799443
			-   Gobierno  y  conformidad.  Los  marcos  de  trabajo  de  conformidad  y  gobierno gestionan la validación adicional a fin de asegurar la relación y consonancia con la corporación y los estándares de la industria, así como requerimientos regulatorios.   Optimización  de  recursos.  Los  administradores  revisan  datos  de  rendimiento  e identifican  cambios  necesarios  para  optimizar  el  ambiente  alrededor  de  los criterios tales como rendimiento y los costes. Cloud Computing, DevOps and DevOps Culture Tema 8. Ideas clave 8 I  ) R N U i j (  a o R a L  e d   l a n o i c a n r e t n I  d a d i s r e v i n U ©
		- (Page 8)
	- -
	- -
		- Plantillas Son los ficheros donde se describen las infraestructuras en sí mismas. Nombraremos algunas de las características fundamentales:   Son susceptibles de ser anidadas e importadas por otras plantillas.   El  motor  de  plantillas  ofrece  funciones  auxiliares  similares  a  las  de  cualquier lenguaje de programación.   Permiten  definir  parámetros  y,  a  través  de  estos,  se  pueden  escribir  plantillas reutilizables  para  distintos  entornos.  Se  pueden  definir  condiciones  y  utilizarlas para crear un recurso u otro en base a una condición. #flashcard
		  id:: ac420c83-b184-4667-8ce3-c4801cbb7453
		- (Page 13)
	- -
	- -
		- Es la implementación de una plantilla combinada con los parámetros necesarios. Una vez creada, permite comprobar y acceder a la información sobre: qué plantilla se ha Stacks #flashcard
		  id:: 84466ec8-5390-44ed-836f-e7a24f8dacb7
		- (Page 13)
	- -
	- -
		- usado,  qué  parámetros  tenía,  cuáles  son  los  recursos  creados  y  la  información  de salida que proporciona. AWS CloudFormation es un servicio para modelar y configurar los recursos de AWS de  forma  sencilla,  mediante  la  creación  de  una  plantilla  que  describa  todos  los recursos  de  AWS  que  se  necesiten  (como  las  instancias  de  Amazon  EC2  o  DB  de Amazon RDS), y AWS CloudFormation se encarga de aprovisionar y configurar esos recursos automáticamente. Cloud Computing, DevOps and DevOps Culture Tema 8. Ideas clave 14 I  ) R N U i j (  a o R a L  e d   l a n o i c a n r e t n I  d a d i s r e v i n U © #flashcard
		  id:: 0e2dd54c-4ae7-4b66-b00d-a46152e53177
		- (Page 14)
	- -
	- -
		- id:: c1649482-c0da-4b96-a781-798b3a8bdd29
		  1.  Crea una plantilla de AWS CloudFormation (un documento con formato JSON o YAML)  en  AWS  CloudFormation  Designer  o  escribe  una  en  un  editor  de  texto. También podemos elegir una plantilla proporcionada por AWS CloudFormation. La plantilla describe los recursos que queremos y su configuración. Figura 7. Ejemplo en JSON usando plantillas para crear una instancia EC2. Fuente: Amazon Web Services, s.f. 2.  Guarda la plantilla localmente o en Amazon S3. Si es una creación desde cero, se guardará con cualquiera de las siguientes extensiones: .json, . yaml, o .txt. 3.  Crea una pila de AWS CloudFormation especificando la ubicación de la plantilla como ruta local o URL de Amazon S3. Si la plantilla contiene parámetros, es posible especificar  valores  de  entrada  en  el  momento  de  crear  la  pila.  Los  parámetros permiten pasar valores a la plantilla para personalizar los recursos cada vez que cree una pila. Adicionalmente, es posible crear pilas usando AWS CloudFormation, API o AWS CLI. #flashcard
		- (Page 15)
	- -
	- -
		- Una vez que los recursos hayan sido creados, AWS CloudFormation informa que la pila ha sido creada. Posteriormente, será posible empezar a utilizar los recursos de la pila  creada.  Si  en  el  momento  de  la  creación  hubiese  algún  problema,  AWS CloudFormation realizaría un rollback y eliminaría los recursos que se hayan creado. Cloud Computing, DevOps and DevOps Culture Tema 8. Ideas clave 16 I  ) R N U i j (  a o R a L  e d   l a n o i c a n r e t n I  d a d i s r e v i n U © #flashcard
		  id:: ed0077b7-7ae6-4e20-ad66-646464437a81
		- (Page 16)
	- -