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
		-
		-