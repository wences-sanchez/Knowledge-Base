tags:: [[Feynman-Technique]], [[Azure]]

-
- # Habilidades
	- ## Describiendo los conceptos de la computación en la nube
		- ### Qué es la computación en la nube
			- La computación en la nube es un servicio por parte de los proveedores de nube sobre cómputo, almacenamiento y otros productos relacionados.
			- Lo que realmente marca la diferencia es que:
				- Todos los servicios se pagan únicamente por uso consumido
				- Estos servicios permiten consumir más (usar más) en determinados momentos, y consumir menos (usar menos) cuando no sean necesarios.
					- Esto es brutal cuando queremos escalar nuestras aplicaciones web en función de la demanda que tengamos
		- ### Describe el modelo de responsabilidad compartida
			- Cuando usamos un servicio de un proveedor de nube, esto no significa que no tengamos que ocuparnos de la seguridad del sistema. Más bien, es un gradiente en el cual:
				- Si usamos *Infraestructura-como-Servicio*, tendremos que seguir encargándonos de todo excepto de los servidores físicos y la red física.
				- Si usamos *Plataforma-como-Servicio*, el proveedor se encargará también del almacenamiento y sistema operativo. Dejándonos solo al cargo de nuestro código y nuestros tests. Todo lo demás está manejado por el proveedor de nube.
				- Si usamos *Software-como-Servicio*, tampoco tendremos que preocuparnos siquiera del despliegue de nuestra aplicación. Ya que estará administrado por el proveedor de nube.
		- ### Define los modelos de nube
			- Cuando usamos una nube pública, todos nuestros datos viajan a través de Internet (o a través de medios dedicados si pagamos por ello)