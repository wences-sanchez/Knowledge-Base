title:: Docker Esencial/Creación y Mantenimiento de Imágenes
tags:: Docker, LinkedIn-Learning

- #tags #Docker #LinkedIn-Learning
- # Creación y Mantenimiento de Imágenes
	- ## 1. Anatomía básica de un Dockerfile
		- Un Dockerfile no es otra cosa que un fichero de texto donde se encuentra la definición de cómo Docker tiene que crear y construir esta imagen.
		- `$ docker build -t <mi-nombre[:mi-tag]> .`
	- ## 2. Partiendo de una imagen base
		- Tendremos normalmente que empezar desde una versión Linux estándar.
		- Se indica en el Dockerfile con: **FROM** <image>
			- Con esto se heredará todo. Todos los metadatos, los datos, los comandos...
		- El Dockerfile está en un directorio y se llama siempre Dockerfile.
		- Nosotros le especificamos el nombre y tag de la imágen resultante con `$ docker build -t nombre:tag .`
			- Con el `.` le indicamos la ruta del Dockerfile
		-
-