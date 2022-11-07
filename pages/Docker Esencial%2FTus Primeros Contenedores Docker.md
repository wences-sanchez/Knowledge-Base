title:: Docker Esencial/Tus Primeros Contenedores Docker
tags:: Docker, LinkedIn-Learning

- #tags #Docker #LinkedIn-Learning
-
- # Tus Primeros Contenedores Docker
	- ## 1. Instalación de Docker en Windows
		- Ahora, se puede instalar Docker en Windows usando Hyper-V =)
	- ## 2. Instalación de Docker en Mac
	- ## 3. Instalación de Docker en GNU/Linux
		- Hay que asegurarse siempre de que instalamos la aplicación desde cero.
	- ## 4. Descarga tu Primera imagen
		- Para mostrar las imágenes, hacemos: `$ docker images`
		- Si no decimos ningún tag, usará el *por defecto*, que es *latest*.
		- Si queremos alguna otra versión, se la podemos especificar.
	- ## 5. Crear un Contenedor y ejecutar comandos en él
		- Podemos ejecutar `$ docker run <nombre-imagen>`.
			- Pero si lo ejecutamos así, no veremos nada
			- Si no ejecutamos el contenedor de manera interactiva, el contenedor ejecuta el proceso y sale después (sin interacción)
			- Así, ejecutamos **-i** para interacción y **-t** para que abra una terminal
		- Para borrar automáticamente contenedores, usamos **--rm**
			- Hay que tener cuidado porque si encontramos algo útil, se borrará todo inmediatamente al salir
	- ## 6. Ejecutar diferentes versiones de Docker al mismo tiempo
		- Podemos usar, con Docker, versiones diferentes del software que estamos ejecutando
		- Así, podemos coger un software para hacerle pruebas y testearlo con diferentes versiones del Sistema Operativo.
			- Y testear si el fallo de un dev es a causa de su versión
		- También podemos probar con distintas veriones de un software mismo (como por ejemplo **Python**)
	- ## 7. Parar y borrar contenedores
		- Se pueden dejar corriendo en el background contenedores cuando añadimos **-d** al `$ docker run`
		- Para deshacernos de los contenedores, hacemos:
			- `$ docker rm <id-del-contenedor>`
		- Hay que pararlos siempre los contenedores antes de borrarlos.
	- ## 8. Borrado de imágenes y tags
		- Las imágenes que creamos también ocupan espacio en disco (no solo los conenedores)
		- Para borrar imágenes, usamos:
			- `$ docker rmi <nombre-imagen>`
		- Si queremos borrar una imagen de la cual ya existen sus capas, no se borra. Simplemente elimina el puntero *tag* de la tabla.
		- Solo se borran las capas cuando se borra la útlima imagen que las usa.
- ## Flashcards
	- ¿Cómo relacionas Docker con el testeo de aplicaciones? #flashcard
	  id:: 6345459c-8a0d-47ca-baf3-1ac41d12f3ea
		- Podemos usar, con Docker, versiones diferentes del software que estamos ejecutando
		- Así, podemos coger un software para hacerle pruebas y testearlo con diferentes versiones del Sistema Operativo.
			- Y testear si el fallo de un dev es a causa de su versión
		- También podemos probar con distintas veriones de un software mismo (como por ejemplo **Python**)
	- ¿Cómo puedes borrar un contenedor en Docker? #flashcard
	  id:: 6345459c-3d31-4e4f-8475-92b947c3c039
		- Para deshacernos de los contenedores, hacemos:
			- `$ docker rm <id-del-contenedor>`
		- Hay que pararlos siempre los contenedores antes de borrarlos.
	- ¿Cómo puedes borrar una imagen en Docker? #flashcard
	  id:: 6345459c-1d8f-4582-b37f-c239188249ee
		- Las imágenes que creamos también ocupan espacio en disco (no solo los conenedores)
		- Para borrar imágenes, usamos:
			- `$ docker rmi <nombre-imagen>`
		- Si queremos borrar una imagen de la cual ya existen sus capas, no se borra. Simplemente elimina el puntero *tag* de la tabla.
		- Solo se borran las capas cuando se borra la útlima imagen que las usa.
	- ¿Dónde pondrías el argumento `--name` en un `$ docker run ...`? #flashcard
	  id:: 6345459c-e66a-4c68-aff9-041e7af33294
		- Antes del nombre del contenedor. Si no, fallará en el argumento opcional de salida especificado
		-