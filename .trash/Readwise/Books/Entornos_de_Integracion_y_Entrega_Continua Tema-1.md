# Entornos_de_Integracion_y_Entrega_Continua Tema-1

deck:: [[UNI::Entornos_de_Integracion_y_Entrega_Continua Tema-1]]\
author:: [[UNIR]]\
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-1"\
category:: #books\
\
tags:: Entornos-CI-CD UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/ed1ff853-1da7-4f47-a3a7-6f588b221213.jpg)

## Highlights
- 
 ¿Qué tres áreas cubre _ALM_?
   AÑADIR IMAGEN #flashcard 
    ALM se puede dividir en tres áreas distintas: gobierno, desarrollo y operaciones. En la Figura 1 se puede ver cada uno de estos aspectos en su propia línea horizontal.

     (Page 6)
-
- 
 Mínimos pasos necesarios para una tarea de *pipeline* automatizada #flashcard 
    La alternativa a este antipatrón es tender a los despliegues completamente automatizados. La intervención humana se debe limitar a tres operaciones: seleccionar el entorno (desarrollo, prueba o producción), seleccionar la versión (o el ID del commit, o cualquier otra manera de identificar el código) y presionar el botón de Ok.

     (Page 12)
-
- 

La integración continua, según Fowler (2007) es: «Una metodología de desarrollo de software en la que los miembros de un equipo integran su trabajo de manera frecuente, incluso varias veces al día, por lo que el trabajo de todo el equipo se integra múltiples veces al día. Cada integración se verifica con una construcción y pruebas automáticas para detectar errores tan pronto como sea posible». #flashcard 


     (Page 15)
-
- 
 ¿Qué cuatro cosas hacen falta para aplicar integración continua en un proyecto? #flashcard 
    Hacen falta cuatro cosas para aplicar integración continua en un proyecto:  Control de versiones. Todo debe estar versionado en un repositorio: código, pruebas, scripts de base de datos, scripts de construcción y despliegue, etc. Da igual el tamaño del proyecto y el número de individuos involucrados: cualquier proyecto de software debe usar un sistema de control de versiones.  Una construcción automática. Aunque los IDES facilitan la construcción de un proyecto sencillo, la situación se complica con aplicaciones profesionales que se ofrecen como servicio. En cualquier caso, la construcción del proyecto (que puede implicar compilación, empaquetado de recursos y almacenamiento en un repositorio) debe estar automatizada de principio a fin. Si el lenguaje de programación o el sistema de despliegue ofrecen utilidades de compilación, empaquetado, etc., hay que aprovecharlas. Además, todos los scripts de esta tarea deben estar también versionados.

     (Page 18)
-
- 
 <<<<<<< #flashcard 
     Batería de pruebas completa. Si la batería de pruebas no es lo suficientemente completa, una ejecución satisfactoria realmente no dice nada sobre la fiabilidad de los cambios. Las pruebas deben cubrir suficientes casos como para ser capaces de detectar alteraciones en el comportamiento del código y en las funcionalidades de la aplicación. Al igual que la fase de construcción, las pruebas deben ejecutarse de manera automática y deben estar versionadas junto al código.  Aceptación del equipo. Los conceptos de integración, entrega y despliegue continuos son una metodología, no una herramienta. Requiere un cierto nivel de implicación y disciplina por parte del equipo. Si uno de los desarrolladores (acostumbrado a trabajar en largas iteraciones y a reportar sus tareas cada mes) no se adapta a integrar sus cambios habitualmente, no recibirá valor alguno del sistema de CICD, por muy avanzada que sea la implementación del pipeline. El objetivo final no es integrar rápido, sino aumentar la calidad del producto final. Los equipos deben empezar por asimilar este objetivo, hacer suyos los procesos, y la calidad aumentará por sí sola.

     (Page 19)
-
