# Administración de Sistemas para la Cloud Tema-4

deck:: [[UNI::Administración de Sistemas para la Cloud Tema-4]]\
author:: [[UNIR]]\
full-title:: "Administración de Sistemas para la Cloud Tema-4"\
category:: #books\
\
tags:: Administración-de-Sistemas-para-la-Cloud UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/078b3e08-d0f7-4a89-a8d3-db59beea9618.jpg)
## Highlights
- id:: 6363990b-e8ca-4d1d-91ef-e8d1c5d25a46
   ¿Qué es MongoDB? #flashcard 
    MongoDB es una base de datos de propósito general basada en documentos. Soporta alta disponibilidad gracias a su funcionalidad de réplicas y consultas distribuidas en las instalaciones en modo shard.
  
     (Page 4)
-
- id:: 6363990b-e5dd-443d-a7a5-d3cd02e71b2f
   ¿Qué hace el comando de Bash: set -e? #flashcard 
    Concretamente, set -e saldrá del script si cualquiera de los comandos falla.
  
     (Page 9)
-
- id:: 6363990b-de8a-4a00-998d-fd935ecf6739
   ¿Cómo puedes accede a los paámetos pasados a un scipt dento de este? #flashcard 
    r
  
     (Page 10)
-
- id:: 6363990b-b676-4a77-a2f5-640e71acf7af
  
  Los parámetros están normalmente disponibles en las variables $1, $2, $3, etc. o en el array $@ #flashcard 
  
  
     (Page 10)
-
- id:: 6363990b-fa10-4142-aaa0-2e5cf7a8a93d
  
  se usa una expresión if-else en la misma línea: si el comando id -u nginx termina satisfactoriamente, se ejecuta el comando a continuación de &&. Si termina en error, se ejecuta el comando a continuación de ||. El comando id devuelve el identificador del nombre de usuario y falla si el usuario id -u nginx && chown -R nginx:nginx /var/www || chown -R www-data:www-data no existe. /var/www #flashcard  #code 
  
  
     (Page 23)
-
- id:: 6363990b-2b6e-4f98-8dd5-36b3a4dd733d
   ¿Cómo puedes comprobar, mediante comandos en Bash, que estás en una u otra distribución de Linux? #flashcard 
    if [[ -e /etc/redhat-release || -e /etc/system-release ]]; then Más adelante, sin embargo, aprovecha otra diferencia entre las distribuciones: la existencia del fichero /usr/bin/yum. if [[ -x /usr/bin/yum ]]; then
  
     (Page 29)
-