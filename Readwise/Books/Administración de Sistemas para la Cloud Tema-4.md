# Administración de Sistemas para la Cloud Tema-4

deck:: [[UNI::Administración de Sistemas para la Cloud Tema-4]]\
author:: [[UNIR]]\
full-title:: "Administración de Sistemas para la Cloud Tema-4"\
category:: #books\
\
tags:: Administración-de-Sistemas-para-la-Cloud UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/078b3e08-d0f7-4a89-a8d3-db59beea9618.jpg)
## Highlights
- id:: 63c669dd-7e38-4384-8ecc-70f74b2e4e3a
   ¿Qué es MongoDB? #flashcard 
    MongoDB es una base de datos de propósito general basada en documentos. Soporta alta disponibilidad gracias a su funcionalidad de réplicas y consultas distribuidas en las instalaciones en modo shard.
  
     (Page 4)
-
- id:: 63c669dd-4419-4d68-846e-bec58cc4dfef
   ¿Qué hace el comando de Bash: set -e? #flashcard 
    Concretamente, set -e saldrá del script si cualquiera de los comandos falla.
  
     (Page 9)
-
- id:: 63c669dd-854d-4872-9919-073e604c39cf
   ¿Cómo puedes accede a los paámetos pasados a un scipt dento de este? #flashcard 
    r
  
     (Page 10)
-
- id:: 63c669dd-375a-44ed-ba81-c1d8efd45461
  
  Los parámetros están normalmente disponibles en las variables $1, $2, $3, etc. o en el array $@ #flashcard 
  
  
     (Page 10)
-
- id:: 63c669dd-0f07-4438-a290-e15ce58b644c
  
  se usa una expresión if-else en la misma línea: si el comando id -u nginx termina satisfactoriamente, se ejecuta el comando a continuación de &&. Si termina en error, se ejecuta el comando a continuación de ||. El comando id devuelve el identificador del nombre de usuario y falla si el usuario id -u nginx && chown -R nginx:nginx /var/www || chown -R www-data:www-data no existe. /var/www #flashcard  #code 
  
  
     (Page 23)
-
- id:: 63c669dd-4c71-4c59-ade8-6aa7f2da4da8
   ¿Cómo puedes comprobar, mediante comandos en Bash, que estás en una u otra distribución de Linux? #flashcard 
    if [[ -e /etc/redhat-release || -e /etc/system-release ]]; then Más adelante, sin embargo, aprovecha otra diferencia entre las distribuciones: la existencia del fichero /usr/bin/yum. if [[ -x /usr/bin/yum ]]; then
  
     (Page 29)
-