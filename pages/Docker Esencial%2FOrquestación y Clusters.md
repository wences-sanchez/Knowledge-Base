title:: Docker Esencial/Orquestación y Clusters
tags:: Docker, LinkedIn-Learning

- #tags #LinkedIn-Learning #Docker
-
- # Módulo 6: Orquestación y Clusters
	- ## 1. Qué es la orquestación
		- La orquestación es un sistema que nos ofrecen determinados tipos de software que nos permiten gestionar los despliegues, tanto de nuestro software como de nuestra infraestructura de una manera semiautomática, a partir de configuraciones.
			- Antes, había que hacerlo todo manualmente. Y había que esperar hasta semanas para poder tener el hardware y todo el software.
		- Un despliegue en la nube tarda segundos o minutos. Pero siempre tenemos esos asuntos de la configuración, la puesta en marcha, los despliegues de máquinas, etc.
		- En la orquestación lo que hacemos es definir unos ficheros de configuración. Pueden ser: YAML, XML, JSON. Que definen:
			- Qué plataforma vamos a utilizar,
			- Qué tipo de máquinas vamos a usar,
			- Qué tipo de instancias o máquinas virtuales vamos a tener,
			- Cuántas se van a lanzar,
			- Qué software van a llevar dentro,
			- Cómo se pueden instalar automática o semiautomáticamente
		- Y sólo tenemos que mantener esa definición en un fichero.
			- El sistema de orquestación será el que se encargará de comunicarse directamente con la API de ese sistema y encargarle lo necesario o también modificarlo.
	- ### Flashcards
	  collapsed:: true
		- ¿Qué se conoce como *orquestación*? #flashcard
		  id:: 6345459b-97fa-4b19-9b6d-2ce70c6b05bc
			- La orquestación es un sistema que nos ofrecen determinados tipos de software que nos permiten gestionar los despliegues, tanto de nuestro software como de nuestra infraestructura de una manera semiautomática, a partir de configuraciones.
				- Antes, había que hacerlo todo manualmente. Y había que esperar hasta semanas para poder tener el hardware y todo el software.
			- Un despliegue en la nube tarda segundos o minutos. Pero siempre tenemos esos asuntos de la configuración, la puesta en marcha, los despliegues de máquinas, etc.
			- En la orquestación lo que hacemos es definir unos ficheros de configuración. Pueden ser: YAML, XML, JSON. Que definen:
				- Qué plataforma vamos a utilizar,
				- Qué tipo de máquinas vamos a usar,
				- Qué tipo de instancias o máquinas virtuales vamos a tener,
				- Cuántas se van a lanzar,
				- Qué software van a llevar dentro,
				- Cómo se pueden instalar automática o semiautomáticamente
			- Y sólo tenemos que mantener esa definición en un fichero.
				- El sistema de orquestación será el que se encargará de comunicarse directamente con la API de ese sistema y encargarle lo necesario o también modificarlo.
	- ## 2. Docker Compose
		- **Docker Compose** es una herramienta para definir y correr aplicaciones Docker multi-contenedor.
			- Está pensado, sobre todo, para el entorno de desarrollo y para aplicaciones que empiezan a ser complejas (porque raramente tienen un solo componente).
		- **Docker Compose** se basa en un fichero YAML en el que se definen todos los contenedores y las relaciones que tienen entre ellos.
		- *Docker Compose* **NO** está pensado para producción.
		-
	- ### Flashcards
	  collapsed:: true
		- Define *Docker Compose*. #flashcard
		  id:: 6345459b-3780-4300-bf6a-98d400aad7f7
			- **Docker Compose** es una herramienta para definir y correr aplicaciones Docker multi-contenedor.
				- Está pensado, sobre todo, para el entorno de desarrollo y para aplicaciones que empiezan a ser complejas (porque raramente tienen un solo componente).
			- **Docker Compose** se basa en un fichero YAML en el que se definen todos los contenedores y las relaciones que tienen entre ellos.
			- *Docker Compose* **NO** está pensado para producción.
		-
	- ## 3. Docker Swarm
		- **Docker Swarm** se traduce como: *Modo enjambre*
		- Este modo permite, desde las herramientas de terminal, gestionar un cluster (o enjambre) de máquinas Docker, desplegar servicios y gestionar su comportamiento.
		-
	- ### Flashcards
	  collapsed:: true
		- ¿Qué es, a nivel básico, Docker Swarm? #flashcard
		  id:: 6345459b-aa45-4817-8246-7d7ec11ad3ab
			- **Docker Swarm** se traduce como: *Modo enjambre*
			- Este modo permite, desde las herramientas de terminal, gestionar un cluster (o enjambre) de máquinas Docker, desplegar servicios y gestionar su comportamiento.
		-
	- ## 4. Kubernetes
		- **Kubernetes** es un sistema de gestión, creación y orquestación de clusters de contenedores, que además es software libre.
		-
	- ## 5. Amazon Container Service
		-
		-
-