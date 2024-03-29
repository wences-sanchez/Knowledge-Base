title:: Readwise/Administración de Sistemas para la Cloud Tema-4 (highlights)
deck:: [[Across-the-Net]]
author:: [[UNIR]]
full-title:: "Administración de Sistemas para la Cloud Tema-4"
category:: #articles

tags:: Administración-de-Sistemas-para-la-Cloud UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/078b3e08-d0f7-4a89-a8d3-db59beea9618.jpg)
- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- ¿Qué es MongoDB? #flashcard
			- MongoDB es una base de datos de propósito general basada en documentos. Soporta alta disponibilidad gracias a su funcionalidad de réplicas y consultas distribuidas en las  instalaciones  en  modo  shard.
		- (Page 4)
	- -
	- -
		- ¿Qué hace el comando de Bash: set -e? #flashcard
			- Concretamente, set -e saldrá del script si cualquiera de los comandos falla.
		- (Page 9)
	- -
	- -
		- ¿Cómo puedes accede a los paámetos pasados a un scipt dento de este? #flashcard
			- r
		- (Page 10)
	- -
	- -
		- Los parámetros están normalmente disponibles en las variables $1, $2, $3, etc. o en el array $@ #flashcard
		- (Page 10)
	- -
	- -
		- se usa una expresión if-else en la misma línea: si el comando id -u nginx termina satisfactoriamente, se ejecuta el comando a continuación de &&. Si termina en error, se ejecuta el comando a continuación de ||. El comando id devuelve el identificador del nombre de usuario y falla si el usuario id -u nginx && chown -R nginx:nginx /var/www || chown -R www-data:www-data no existe. /var/www #flashcard
		- tags:: [[code]]
		- (Page 23)
	- -
	- -
		- ¿Cómo puedes comprobar, mediante comandos en Bash, que estás en una u otra distribución de Linux? #flashcard
			- if [[ -e /etc/redhat-release || -e /etc/system-release ]]; then Más  adelante,  sin  embargo,  aprovecha  otra  diferencia  entre  las  distribuciones:  la existencia del fichero /usr/bin/yum. if [[ -x /usr/bin/yum ]]; then
		- (Page 29)
	- -