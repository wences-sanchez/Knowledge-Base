title:: UNIR/Curso AWS/Módulo-1/Tema 4: AWS IAM. Aspectos de seguridad
tags:: UNIR, AWS

- #tags #UNI #AWS #Tema-1
-
- ## Modelo de responsabilidad compartida de AWS
	- ![image.png](../assets/image_1665044543811_0.png)
	- Tanto el cliente como AWS tenemos (diferentes) responsabilidades
	- Como clientes, somos responsables de lo que ocurre dentro de la nube. Es decir, de que nuestras aplicaciones funcionen, de nuestros datos de clientes, de aplicaciones, de las identidades, accesos, configurar parches si tenemos máquinas virtuales, de la red, cortafuegos, etc.
	- AWS es responsable de la seguridad de la nube: de las máquinas físicas, del almacenamiento, los servidores, bases de datos, regiones, zonas de disponiblidad, etc.
-
	- ### Responsabilidades de AWS
		- AWS se encarga de la seguridad física de sus centros de datos, de la infraestructura de hadware y software, de la auditoría de sistemas operativos, de que no hay intrusiones, de la vídeo-vigilancia, de los sistemas de virtualización, etc.
	- ### Responsabilidades de los clientes
		- Del sistema operativo de las instancias de EC2, de sus parches y mantenimiento, contraseñas de aplicaciones, roles, cifrado de datos, cortafuegos, red y cuentas.
-