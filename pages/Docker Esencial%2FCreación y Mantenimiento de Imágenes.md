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
	- ## 3. Ejecutar comandos en una imagen
		- El primer comando útil que aprenderemos es **RUN**.
		- Con este comando lo que hacemos es durante la construcción de nuestra futura imagen ejecutar lo que nosotros queramos.
			- Por ejemplo:
			- ```
			  FROM alpine:latest
			  RUN echo Hola Mundo > /root/saludo
			  ```
			- Luego:
			- `$ docker build -t imagen-para-saludar .`
			- `$ docker run --rm --name contenedor-que-saluda imagen-para-saludar cat /root/saludo`
			- `$ > Hola Mundo`
		- Todo lo que se ejecuta con RUN se ejecuta como superusuario
	- ## 4. Instalando paquetes en una imagen
		- Podemos hacer `RUN apt-get install -y <paquetes>`
		- Pero no podremos encontrar ningún paquete.
			- Borran todas las caches de los repositorios **apt-get**
			- Hay que hacer `$ apt-get update` antes!
		- Docker guarda la información de las caches. Así que si organizamos bien nuestras capas, será mucho más eficiente.
			- La cache, si no cambiamos las capas, no las ejecuta (si no cambian las líneas)
			- Si volvemos a reutilizar el Dockerfile y no hemos modificado la línea del install, el Docker no será capaz de ejecutarla antes (para actualizar las dependencias).
			- Así que lo mejor es incluir el *apt-get update -y* en la misma línea del *apt-get install -y* que vayamos a usar
	- ## 5. Agregando ficheros en una imagen
		- El comando **ADD** lo que hace es agregar un fichero que le digamos de una ruta que tiene que ser por lo menos comenzando en el sitio donde está el Dockerfile; y entonces la copia a la ruta que le digamos dentro de la imagen que estamos creando personalizada.
			- Por ejemplo: `ADD ficheros/index.html /var/www/curso/index.html`
	- ## 6. Configurando variables de entorno en la imagen
		- Lo podemos hacer con **ENV** *variable1 valor1*
			- También, con ENV variable2="valor2" variable3="valor3"
	- ## 7. Ejecutar un comando al arrancar el contenedor
		- Podemos hacer en el Dockerfile `CMD["uname"]`
			- Entonces, al arrancar el contenedor, si no le especificamos nada, imprimirá *Linux* (si es un Linux)
		- Podemos añadirle parámetros de la siguiente manera:
			- `CMD ["uname", "-a"]`
		- Más avanzado, podemos usar:
			- `CMD ["nginx", "-g", "daemon off;]`
		-
		-
		-
- ## Flashcards
	- Ejemplo completo (del flujo) de creación de Dockerfile y posterior despliegue en contenedor: #flashcard
		- Por ejemplo:
		- ```
		  FROM alpine:latest
		  RUN echo Hola Mundo > /tmp/saludo
		  ```
		- Luego:
		- `$ docker build -t imagen-para-saludar .`
		- `$ docker run --rm --name contenedor-que-saluda imagen-para-saludar cat /tmp/saludo`
		- `$ > Hola Mundo`