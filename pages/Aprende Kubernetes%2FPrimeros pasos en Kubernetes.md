title:: Aprende Kubernetes/Primeros pasos en Kubernetes
tags:: LinkedIn-Learning, Kubernetes

- #tags #LinkedIn-Learning #Kubernetes
-
-
- ## La herramienta kubectl
	- `$ kubectl <comando> <parámetros>`
-
-
- ## El panel de control o dashboard de Kubernetes
	- El dashboard es peligroso porque requiere permisos totales.
		- Por eso no se recomienda para entornos que sean de producción.
-
	- ### Flashcards
		- ¿Por qué se desaconseja el uso del dashboard de Kubernetes en favor de la CLI? #flashcard
			- El dashboard es peligroso porque requiere permisos totales.
				- Por eso no se recomienda para entornos que sean de producción.
-
-
- ## Crear un pod en Kubernetes
	- `$ kubectl apply -f mi-fichero.yml`
	- `$ kubectl delete -f mi-fichero.yml`
	- `$ kubectl describe pod mi-pod`
	- Un `kubectl apply` no puede añadir ni quitar contenedores.
		- Hay que hacer un `kubectl delete` y `kubectl create`
	-
	-
-