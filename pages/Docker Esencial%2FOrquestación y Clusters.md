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
	- ## 2. Docker Compose
		- Docker Compose
		-
-