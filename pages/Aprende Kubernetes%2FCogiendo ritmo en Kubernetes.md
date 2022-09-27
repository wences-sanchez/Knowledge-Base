title:: Aprende Kubernetes/Cogiendo ritmo en Kubernetes
tags:: LinkedIn-Learning, Kubernetes

- #tags #LinkedIn-Learning #Kubernetes
-
- ## Anatomía de un fichero de definición en Kubernetes
	- Las etiquetas son opcionales.
-
-
- ## Etiquetas y anotaciones en tus objetos de Kubernetes
	- Las **anotaciones** se componen más bien de información adicional que nos puede ser útil para describir o extraer información de un objeto.
	- Y las **etiquetas (label)** por su parte tienen funciones operativas
	-
	- `$ kubectl get pods --selector environment=development`
	-
	- ### Flashcards
		- ¿Qué comando puedes usar para filtrar objetos en Kubernetes? #flashcard
			- `$ kubectl <command> --selector <key>=<value>`
-
	-
- ## Editar un recurso en vivo en Kubernetes
	-
	-
- ## Guardar configuraciones en Kubernetes
	- Los **ConfigMap**, en vez de `spec:`, tienen `data:`
	-
	-
		-
	-
-