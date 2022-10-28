# Contenedores Tema-1

deck:: [[UNI::Contenedores Tema-1]]\
author:: [[UNIR]]\
full-title:: "Contenedores Tema-1"\
category:: #books\
\
tags:: Contenedores UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/97cc1d28-1745-4233-9c46-fa97ce5566b9.jpg)

## Highlights
- 
 Acerca de contenedores y Docker #flashcard 
    Un contenedor es una unidad de software estandarizada que empaqueta el código de una aplicación y todas sus dependencias para permitir su ejecución de manera rápida y consistente independientemente del entorno en el que se ejecute. Docker es una plataforma de código abierto para desarrollar, distribuir y desplegar aplicaciones en entornos aislados y seguros denominados contenedores. Los contenedores tienen la característica de ser livianos, ya que no necesitan la carga adicional de un hipervisor como ocurre con las máquinas virtuales, sino que se ejecutan directamente dentro del núcleo de la máquina host.

     (Page 5)
-
- 
 INCLUIR IMAGEN #flashcard 
    Para poder ejecutar máquinas virtuales necesitamos un hipervisor, que es una capa de software que instalamos directamente sobre un servidor físico y su infraestructura. El hipervisor permite exponer los recursos hardware (CPUs, memoria, almacenamiento, etc.) que están debajo del sistema operativo, de forma que puedan ser utilizados por los sistemas operativos de las máquinas virtuales.

     (Page 8)
-
- 
 ¿Cómo funcionan los contenedores?
   INCLUIR IMAGEN #flashcard 
    Los contenedores tienen una filosofía totalmente diferente a la de las máquinas virtuales. En lugar de tener un sistema operativo completo, los contenedores comparten el mismo kernel o núcleo del sistema operativo host sobre el que se ejecutan. El motor de Docker será el encargado de desplegar y gestionar los contenedores de nuestras aplicaciones, pero en lugar de reservar parte de los recursos de hardware de la máquina para cada contenedor, lo que hace es compartirlos entre todos los contenedores, permitiendo optimizar su uso y eliminando la necesidad de tener sistemas operativos separados para conseguir el aislamiento.

     (Page 9)
-
- 

En resumen, los contenedores comparten los recursos subyacentes del host sobre el que se ejecutan. Además, los desarrolladores construyen una imagen que incluye exactamente lo que necesitan para ejecutar su aplicación o servicio, comenzando por lo básico y agregando solo lo necesario. #flashcard 


     (Page 9)
-
- 

Las máquinas virtuales se construyen en la dirección opuesta, se empieza por un sistema operativo completo y, dependiendo de las necesidades de aplicación, se añadirán o eliminarán componentes. #flashcard 


     (Page 10)
-
- 

Podríamos resumir el proceso de esta nueva visión en tres fases:  Construir la imagen: empaquetar consistentemente todo lo que nuestra aplicación necesita para ser ejecutada.  Distribuir la imagen: haremos disponible la imagen para utilizarla en nuestro datacenter, en la nube o en la maquina local del desarrollador.  Ejecutar la imagen: desplegar contenedores a partir de la imagen de una manera rápida, sencilla y consistente. #flashcard 


     (Page 11)
-
- 

Escenarios de contenedores Veamos algunos escenarios en los que los contenedores nos ayudarán. Despliegues portables y escalables Podremos ejecutar nuestros contenedores sabiendo que tendrán el mismo comportamiento en diferentes entornos, ya sea en el portátil de un desarrollador, en máquinas físicas o virtuales de nuestro datacenter, en servidores en la nube o en una combinación de ellos. La portabilidad de los contenedores y su reducido tamaño nos permiten gestionar las distintas cargas de trabajo, escalando las aplicaciones y servicios según lo exijan las necesidades casi en tiempo real. Mejor aprovechamiento del hardware disponible Los contenedores son más ligeros y rápidos al desplegarse que las máquinas virtuales, lo que nos permite ejecutar más cargas de trabajo en el mismo hardware. Trabajando con prototipos Los contenedores nos ofrecen entornos aislados con los que podremos probar diferentes configuraciones para nuestras aplicaciones sin necesidad de desplegar nuevas máquinas virtuales ni reconfigurar los sistemas existentes. #flashcard 


     (Page 11)
-
- 

Empaquetando y versionando nuestro software Las imágenes de Docker nos aseguran que, al no tener dependencias con el sistema subyacente, nuestra aplicación se comportará de la misma manera en cualquier servidor que tenga Docker instalado. Además, podremos gestionar diferentes versiones de nuestras imágenes. Actualizando las aplicaciones Cuando lanzamos una nueva versión de nuestro software o detectamos un defecto, no es necesario parchear o actualizar las aplicaciones existentes, simplemente distribuiremos una nueva imagen con las modificaciones necesarias y desplegaremos un nuevo contenedor que reemplazará al actual. El tiempo de despliegue de un contenedor se mide en segundos. Facilitando arquitecturas basadas en microservicios Trabajar con contenedores nos ayudará a descomponer nuestros sistemas complejos en componentes más pequeños y manejables, creando imágenes para cada uno. Modelado de redes Podremos modelar grandes redes para simular escenarios de pruebas más cercanos a los entornos de producción, ya que podremos ejecutar cientos de contenedores en un mismo servidor con la configuración necesaria. Facilitando la entrega continua Los sistemas basados en contenedores son más fácilmente reproducibles y replicables que los sistemas tradicionales, lo que nos permitirá probar de manera consistente nuestro código en los diferentes entornos (stage, uat, prod). #flashcard 


     (Page 12)
-
- 
 ¿Qué hace el demonio de Docker? #flashcard 
    El demonio de Docker (proceso dockerd) escucha las solicitudes del API y es el responsable de administrar los objetos de Docker, como imágenes, contenedores, redes y volúmenes. Un demonio también puede comunicarse con otros demonios para administrar los servicios de Docker de forma distribuida.

     (Page 13)
-
- 

Entrega rápida y consistente de sus aplicaciones Se optimiza el ciclo de vida del desarrollo al permitir que los desarrolladores trabajen en entornos estandarizados utilizando contenedores locales que proporcionan sus aplicaciones y servicios. Los contenedores son excelentes para la integración continua y los flujos de trabajo de entrega continua (CI / CD). #flashcard 


     (Page 13)
-
- 
 ¿Qué hace el cliente Docker? #flashcard 
    sistema remoto. El cliente Docker (comando docker) permite a los usuarios interactuar con el demonio de Docker utilizando la línea de comandos. El cliente Docker y el demonio de Docker se comunican mediante un API REST, ya sea a través de sockets UNIX o mediante una interfaz de red. Ambos no tienen por qué ejecutarse en la misma máquina, ya que el cliente Docker podrá conectarse a un demonio de Docker de un

     (Page 14)
-
- 

Para entender mejor la diferencia entre imágenes y contenedores podemos ver su paralelismo con un fichero ejecutable y el proceso que lo ejecuta. La imagen sería el equivalente al ejecutable y el contenedor similar a los distintos procesos que hay en ejecución del ejecutable. #flashcard 


     (Page 14)
-
- 
 ¿Cómo describirías las imágenes en Docker? #flashcard 
    Las imágenes son objetos de Docker que nos servirán para empaquetar una aplicación o servicio junto a todo lo necesario para su funcionamiento: código de la aplicación, librerías dependientes, configuraciones, etcétera.

     (Page 14)
-
- 
 ¿Cómo describirías los contenedores en Docker? #flashcard 
    Los contenedores son instancias o ejecuciones de la imagen de nuestra aplicación o servicio. Los contenedores se comportan como entornos aislados y seguros, por lo que en una misma máquina podemos tener varios contenedores en ejecución de la misma imagen.

     (Page 14)
-
- 
 ¿Cómo podemos hacer para no tener que escribir sudo cada vez que lanzamos docker? #flashcard 
    Si queremos evitar tener que ejecutar el comando docker con sudo, podemos añadir nuestro usuario al grupo Docker de la siguiente manera: $ sudo groupadd docker $ sudo usermod -aG docker $USER

     (Page 22)
-
