title:: Aprende Kubernetes/Kubernetes avanzado
tags:: LinkedIn-Learning, Kubernetes

- #tags #LinkedIn-Learning #Kubernetes
-
- ## DaemonSets en Kubernetes
	- Un "daemonset" es un tipo de despliegue de Kubernetes que hace que siempre se esté ejecutando un POD determinado en cada uno de los nodos de nuestro clúster.
	- En algunas ocasiones como, por ejemplo, para la monitorización del sistema nos puede interesar este formato
	-
	- Su estructura es idéntica a la de un Deployment
		- Pero sin el campo **replicas** (obviamente)
		-
	- Se pueden usar para, por ejemplo, recolectar logs
		-
	- ### Flashcards
		- ¿Qué es un **daemonSet** en *Kubernetes*? #flashcard
		  id:: 6345458a-0081-447e-8d70-21e1f45cbe60
			- Un "daemonset" es un tipo de despliegue de Kubernetes que hace que siempre se esté ejecutando un POD determinado en cada uno de los nodos de nuestro clúster.
			- En algunas ocasiones como, por ejemplo, para la monitorización del sistema nos puede interesar este formato
			-
			- Su estructura es idéntica a la de un Deployment
				- Pero sin el campo **replicas** (obviamente)
				-
			- Se pueden usar para, por ejemplo, recolectar logs
				-
		-
		-
- ## Jobs en Kubernetes
	- Son para tareas que tienen un inicio y un final definidos.
	- No es como un servidor web que está ejecutándose continuamente.
	- No tiene promesa de continuidad
	- No tienen **selector** porque no tienen nada que vigilar
	- Se intentará ejecutarlo el sistema un número **N** de veces y si falla, ya no se volverá a intentar ejecutarse nunca más.
	- No se puede lanzar dos veces.
		- Solo tiene un nombre
	-
	- ### Flashcards
		- Acerca de los **Jobs** en *Kubernetes*. #flashcard
		  id:: 6345458a-7a75-4c00-a63d-db1b8630e64e
			- Son para tareas que tienen un inicio y un final definidos.
			- No es como un servidor web que está ejecutándose continuamente.
			- No tiene promesa de continuidad
			- No tienen **selector** porque no tienen nada que vigilar
			- Se intentará ejecutarlo el sistema un número **N** de veces y si falla, ya no se volverá a intentar ejecutarse nunca más.
			- No se puede lanzar dos veces.
				- Solo tiene un nombre
	-
- ## CronJobs en Kubernetes
	- También se pueden ejecutar jobs en Kubernetes de forma periódica
	- minuto; hora; dia; mes; dia_semana;
		- El `*` es igual a todos
		- El día de la semana empieza en 0 = domingo
	- Se genera un job para cada ejecución, que generan a su vez un pod para cada tarea
	-
	- ### Flashcards
		- ¿Cómo se pueden usar y configurar los **CronJobs** en Kubernetes? #flashcard
		  id:: 6345458a-e5fc-471c-b27b-dfa327d0d7f8
			- También se pueden ejecutar jobs en Kubernetes de forma periódica --> **CronJobs**
			- `minuto; hora; dia; mes; dia_semana;`
				- El `*` es igual a todos
				- El día de la semana empieza en 0 = domingo
			- Se genera un job para cada ejecución, que generan a su vez un pod para cada tarea
	-
	-
- ## Reservando espacio de disco en Kubernetes
	- Un volumen persistente de Kubernetes es un almacenamiento al que se conecta Kubernetes que permanece en el tiempo hasta que lo borremos, pase lo que pase con los pods que se conecten a él.
	- hemos visto que si necesitamos almacenamiento permanente en Kubernetes, lo que vamos a hacer es una petición de volumen persistente.
	- Estos volúmenes persistentes, aunque la definición sea siempre la misma, por detrás van a ser asignados por Kubernetes.
		- Que, dependiendo de cómo sea nuestro clúster, ese almacenamiento estará en un sitio o en otro y gracias a los "driver" CSI que podemos instalar en nuestros clústeres podemos gestionar transparentemente ese almacenamiento.
	-
	- ### Flashcards
		- Acerca de los volúmenes persistentes en Kubernetes. #flashcard
		  id:: 6345458a-9313-4318-87fe-c6b18c0fd5b6
			- Un volumen persistente de Kubernetes es un almacenamiento al que se conecta Kubernetes que permanece en el tiempo hasta que lo borremos, pase lo que pase con los pods que se conecten a él.
			- hemos visto que si necesitamos almacenamiento permanente en Kubernetes, lo que vamos a hacer es una petición de volumen persistente.
			- Estos volúmenes persistentes, aunque la definición sea siempre la misma, por detrás van a ser asignados por Kubernetes.
				- Que, dependiendo de cómo sea nuestro clúster, ese almacenamiento estará en un sitio o en otro y gracias a los "driver" CSI que podemos instalar en nuestros clústeres podemos gestionar transparentemente ese almacenamiento.
	-
	-
- ## StatefulSets en Kubernetes
	- Para mantener el estado en componentes como bases de datos que necesitan persistencia.
	- Necesitan un servicio (en el YAML) para hacerles un seguimiento
	- Si borramos los pods, los volume van a seguir persistiendo
	-
	-
- ## Ingress en Kubernetes
	- Un 'Ingress' es un tipo de objeto de Kubernetes para el acceso a un servicio desde el exterior del clúster.
	- Provee de una interfaz de nivel más alto que NodePort, con funciones específicas para protocolos HTTP o HTTPS y se integra directamente con el proveedor de "cloud" que estés usando.
	-
	-
-