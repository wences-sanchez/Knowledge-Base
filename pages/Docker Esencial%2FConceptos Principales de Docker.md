title:: Docker Esencial/Conceptos Principales de Docker
tags:: Docker, LinkedIn-Learning

- #tags #Docker #LinkedIn-Learning
-
- # Conceptos Principales de Docker
	- ## 1. Imágenes en Docker
		- Un registro Docker es un repositorio de imágenes Docker
			- Podemos buscar SOs tanto como de apps específicas optimizado el contenedor
		- Docker Store empieza a tener cosas más *enterprise* como plugins o soporte extra y certificaciones.
		- Pero podemos usar el soporte y tecnología gratuitos de Docker.
	-
		- ### Flashcards
			- Define registro en Docker: #flashcard
				- Un **registro Docker** es un **repositorio** de **imágenes** Docker
					- Podemos buscar SOs tanto como de apps específicas optimizado el contenedor
				- Aparte, **Docker Store** empieza a tener cosas más *enterprise* como plugins o soporte extra y certificaciones.
					- Pero podemos usar el soporte y tecnología gratuitos de Docker.
	- ## 2. Contenedores y Capas en Docker
		- Los contenedores en Docker son el resultado de poner en marcha una imágen que hayamos tomado, ya sea de un reopositorio, o que hayamos modificado con un *Dockerfile* nosotros.
		-
		- Pueden estar: EXIT, PAUSED o RUNNING
		- Sus datos se almacenan en capas
			- DTodos los cambios que se hacen, en vez de creares