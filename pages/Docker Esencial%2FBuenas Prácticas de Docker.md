title:: Docker Esencial/Buenas Prácticas de Docker
tags:: Docker, LinkedIn-Learning

- #tags #Docker #LinkedIn-Learning
-
- # Buenas Prácticas de Docker
	- ## 1. Lo efímero y lo permanente
		- Podríamos lanzar un contenedor con el comando **-v**, que es para montar un volumen, darle una ruta y decirle que dentro del contenedor (en la ruta dicha) monte el volumen que tengo.
			- `$ docker run -it --rm -v $(pwd)/my-subdir:/my-mount nginx:alpine`
		- La ruta tiene que ser absoluta. La del host y por supuesto la del contenedor
		- Es importante NO depender de esta funcionalidad. Y limitarla a entornos de desarrollo.
			- En Producción, se usarían: almacenamiento de objetos, sistema de ficheros de red o cluster para el almacenamiento o bases de datos, etc.
		- **Sin estado** quiere decir que no almacenan la configuración y ficheros que utilizan sino que son totalmente ajenos a ello.
	- ### Flashcards
	  collapsed:: true
		- ¿Cómo puedo montar un volumen en un contenedor Docker? #flashcard
			- Podríamos lanzar un contenedor con el comando **-v**, que es para montar un volumen, darle una ruta y decirle que dentro del contenedor (en la ruta dicha) monte el volumen que tengo.
				- `$ docker run -it --rm -v $(pwd)/my-subdir:/my-mount nginx:alpine`
			- La ruta tiene que ser absoluta. La del host y por supuesto la del contenedor
			- Es importante NO depender de esta funcionalidad. Y limitarla a entornos de desarrollo.
				- En Producción, se usarían: almacenamiento de objetos, sistema de ficheros de red o cluster para el almacenamiento o bases de datos, etc.
		- ¿Qué quiere decir que un contenedor no tenga estado (sea *stateless*)? #flashcard
			- **Sin estado** quiere decir que no almacenan la configuración y ficheros que utilizan sino que son totalmente ajenos a ello.
	- ## 2. Usar un fichero Dockerignore
		- La función de un fichero gitignore es evitar que algunos ficheros o directorios acaben versionados
		- Dockerignore es muy parecido. Nos permite evitar que deternimados ficheros que tenemos en la ruta del proyecto acaben, tanto en el espacio de trabajo de Docker como en el contenedor o imagen que estamos creando.
		- Es para que no suban a Docker
		- **.dockerignore**
			- ```
			  # Este es un ejemplo de .dockerignore
			  cache/
			  downloads/
			  */temp
			  ```
	- ### Flashcards
	  collapsed:: true
		- ¿Cómo uso un fichero en Docker para no llenar la imagen de contenedor de elementos innecesarios? #flashcard
			- Con el fichero .dockerignore
			- La función de un fichero gitignore es evitar que algunos ficheros o directorios acaben versionados
			- Dockerignore es muy parecido. Nos permite evitar que deternimados ficheros que tenemos en la ruta del proyecto acaben, tanto en el espacio de trabajo de Docker como en el contenedor o imagen que estamos creando.
			- Es para que no suban a Docker
			- **.dockerignore**
				- ```
				  # Este es un ejemplo de .dockerignore
				  cache/
				  downloads/
				  */temp
				  ```
	- ## 3. Evitar paquetes innecesarios
		- Debemos instalar el mínimo de paquetes posible
			- No instalar editores de texto ni paquetesSSH
		- No solo por eficiencia de espacio y tiempo, sino por seguridad y mantenimiento.
		- Probar primero la imágenes *alpine* antes de usarlas en Producción
	- ## 4. Un contenedor, una función
		- No es buena idea usar un contenedor como una máquina virtual :(
		- Cada uno de los contenedores se tiene que ocupar de una sola aplicación --> **Debe correr un único proceso**
			- Aunque a veces se puedan escalar horizontalmente (una misma aplicación)
	- ### Flashcards
	  collapsed:: true
		- Sobre paquetes y usos de contenedores. #flashcard
			- Debemos instalar el mínimo de paquetes posible
				- No instalar editores de texto ni paquetesSSH
			- No solo por eficiencia de espacio y tiempo, sino por seguridad y mantenimiento.
			- Probar primero la imágenes *alpine* antes de usarlas en Producción
			- **No es buena idea** usar un contenedor como una máquina virtual :(
			- Cada uno de los contenedores se tiene que ocupar de una sola aplicación --> **Debe correr un único proceso**
				- Aunque a veces se puedan escalar horizontalmente (una misma aplicación)
	- ## 5. Reducir la cantidad de capas
		- Podemos ver las capas de una imagen con el comando `$ docker history`
		- Si construimos una imagen con muchas capas y luego intentamos borralas, no funciona así Docker.
			- Porque se almacenan todos los cambios que hacemos y aunque la borremos, siempre estará disponible su contenido. Como en *Git*.
		- La solución es hacer todos estos pasos en un único comando RUN. En una única capa.
			- Por ejemplo, clonamos y borramos el contenido innecesario en una única línea o instrucción.
	- ### Flashcards
	  collapsed:: true
		- ¿Cómo podemos ver las capas de una imagen en Docker?¿Cómo funcionan las capas y su borrado? #flashcard
			- Podemos ver las capas de una imagen con el comando `$ docker history`
			- Si construimos una imagen con muchas capas y luego intentamos borralas, no funciona así Docker.
				- Porque se almacenan todos los cambios que hacemos y aunque la borremos, siempre estará disponible su contenido. Como en *Git*.
			- La solución es hacer todos estos pasos en un único comando RUN. En una única capa.
				- Por ejemplo, clonamos y borramos el contenido innecesario en una única línea o instrucción.
	- ## 6. Ordenar los comandos de múltiples líneas
		- Podemos poner cada paquete único en una única línea
		- Y ordenarlos por orden alfabético para no duplicarla por error.
		- Agregar `rm -rf /var/lib/apt/lists/` para borrar la caché de los paquetes de los repositorios apt o yum.
	-
		-
		-