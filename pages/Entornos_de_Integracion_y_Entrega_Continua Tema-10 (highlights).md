title:: Entornos_de_Integracion_y_Entrega_Continua Tema-10 (highlights)
author:: [[UNIR]]
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-10"
category:: #books

tags:: #[[Entornos-CI-CD]] #[[UNI]]

- #tags #[[Entornos-CI-CD]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/2f569712-df1a-413e-bcba-54aa4aa1618c.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- Llevar cada commit a producción tan pronto como se valida el código es un cambio de paradigma que afecta no solo el aspecto técnico, sino también a la forma en la que se entregan funcionalidades a los usuarios.  Explicaremos también el concepto de feature flag y cómo pueden ayudar en aplicaciones con un ciclo de despliegues rápido. #space
		- (Page 4)
	- -
	- -
	- un  despliegue  continuo  real: sobre el código de master siempre se ejecutan las pruebas, se construye el paquete (es  decir,  se  aplican  integración  y  entrega  continuas)  y,  en  caso  de  subida  de versión, esta se publica en el registro de paquetes. #space
		- (Page 5)
	- -
	- -
	- cada nuevo cambio en master debe iniciar un despliegue en un entorno de staging. Cuando  se  sigue  este  proceso,  los  despliegues  en  producción  tienen  muy  poco riesgo  porque  ya  se  han  probado  los  mismos  cambios  anteriormente.  Cada despliegue en staging debe ser validado con la batería de pruebas automática. Si no pasa las pruebas, el cambio debe ser anulado. #space
		- (Page 6)
	- -
	- -
	- Disponer  de  un  entorno  de  staging  no  impide  que  se  puedan  desplegar  otros entornos de pruebas, como un entorno de control de calidad o uno para pruebas de rendimiento. El primero podría no actualizarse con cada cambio de master, sino desplegarse con la próxima versión candidata para permitir la ejecución de pruebas de  aceptación  manuales  (si  fueran  necesarias).  El  segundo  podría  ser  efímero  y desplegarse para ejecutar las pruebas de rendimiento puntualmente. #space
		- (Page 7)
	- -
	- -
	- Explica el despliegue blue/green #card
		- Este  tipo  de  despliegue,  a  veces  denominado  black/white,  consiste  en  desplegar dos entornos de producción y dirigir el tráfico a uno u otro, ya sea a través de un balanceador de carga o mediante el nombre DNS. En un momento dado, el entorno azul  sirve  la  versión  de  producción  y  recibe  todo  el  tráfico  (tal  como  muestra  la Figura 1 en el paso a). Durante un despliegue, se crea un entorno nuevo, al que se denomina verde, idéntico en cuanto a infraestructura, a partir de la nueva versión (paso  b).  Cuando  el  entorno  verde  está  listo,  se  modifica  el  balanceador  de  carga para que dirija todo el tráfico a este (paso c). Una vez validado el nuevo entorno de producción, el azul se podría desmantelar.
		- (Page 9)
	- -
	- -
	- Sobre Kubernetes en despliegues continuos #card
		- Una  de  las  características  de  estos  despliegues  es  que  solo  se  continúa  con  la sustitución  de  servidores  si  los  desplegados  hasta  el  momento  se  consideran válidos.  Por  ejemplo,  Kubernetes  ofrece  este  tipo  de  despliegues  a  partir  de  dos parámetros de un Deployment:   El  parámetro  maxUnavailable  indica  el  número  máximo  de  contenedores  que pueden  estar  no  disponibles.  En  el  ejemplo  de  la  Figura  3,  el  valor  sería  de  2 (también  se  podría  especificar  con  un  porcentaje).  Los  dos  nodos  con  la  v2  del paso b tardan un tiempo en crearse y arrancar el proceso, por lo que de manera efectiva hay dos contenedores no disponibles.   La  configuración  de  una  sonda  con  readinessProbe  define  un  comando  o  una petición  HTTP  que  se  ejecuta  contra  el  contenedor,  una  vez  creado.  Cuando  el resultado es positivo, el contenedor se considera disponible.
		- (Page 14)
	- -