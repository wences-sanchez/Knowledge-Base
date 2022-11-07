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
		  id:: 6345458a-ac97-406c-af6e-8eaa82070d83
			- `$ kubectl <command> --selector <key>=<value>`
-
	-
- ## Editar un recurso en vivo en Kubernetes
	-
	-
- ## Guardar configuraciones en Kubernetes
	- Los **ConfigMap**, en vez de `spec:`, tienen `data:`
	- No se pueden poner números como valor.
		- Tienen que estar entrecomillados
	-
	- ### Flashcards
		- Sobre los configMap en Kubernetes: #flashcard
		  id:: 6345458a-eaac-46d8-bbd4-75c3e9de690b
			- Los **ConfigMap**, en vez de `spec:`, tienen `data:`
			- No se pueden poner números como valor.
				- Tienen que estar entrecomillados
	-
- ## Guardar secretos en Kubernetes
	- NO son secretos, solo están codificados en base64 en otros caracteres.
	- Estos secretos están disponibles para cualquiera con acceso a la API. O cualquiera que pueda leer el fichero de configuración.
	-
	- ### Flashcards
		- Sobre los **secret**s en Kubernetes: #flashcard
		  id:: 6345458a-8bf7-4548-8248-7e49928813e0
			- NO son secretos, solo están codificados en base64 en otros caracteres.
			- Estos secretos están disponibles para cualquiera con acceso a la API. O cualquiera que pueda leer el fichero de configuración.
	-
	-
		-
	-
-