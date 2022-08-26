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
			- Desde la primera imagen que partimos (que es la que crea la base del contendor). Todos los cambios que se hacen, en vez de crearse sobre el fichero original, (es decir, modificar el almacenamiento que tenemos) van creando una capa encima que indica los cambios que se han realizado.
			- Así, siempre tenemos acceso al estado anterior del fichero, parecido a *GIT*. --> Una capa se crea sobre la otra haciendo (mismo nombre) commits a la imagen base (la primera obligatoria del FROM).
			- Las capas que son iguales entre contenedores, Docker es suficientemente inteligente como para no duplicarlas. Las mantiene en una única referencia.
			-