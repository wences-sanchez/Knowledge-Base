title:: Docker Esencial/Buenas Prácticas de Docker
tags:: Docker, LinkedIn-Learning

- #tags #Docker #LinkedIn-Learning
-
- # Buenas Prácticas de Docker
	- ## 1. Lo efímero y lo permanente
		- Podríamos lanzar un contenedor con el comando **-v**, que es para montar un volumen, darle una ruta y decirle que dentro del contenedor (en la ruta dicha) monte el volumen que tengo.
			- `$ docker run -it --rm -v $(pwd)/my-subdir:/my-mount nginx:alpine`
-