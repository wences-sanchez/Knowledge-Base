# Entornos_de_Integracion_y_Entrega_Continua Tema-7

deck:: [[UNI::Entornos_de_Integracion_y_Entrega_Continua Tema-7]]\
author:: [[UNIR]]\
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-7"\
category:: #books\
\
tags:: UNI Entornos-CI-CD  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/5360dc73-d287-4d6f-8309-e6ddfbb2ce3e.jpg)
## Highlights
- id:: 63639919-fdc6-449b-a196-77143b2caffa
   ¿Qué es Jenkins? #flashcard 
    Jenkins es un sistema de integración y entrega continuas. Es una herramienta de código abierto disponible para múltiples arquitecturas que puede manejar cualquier tipo de construcción, pruebas y despliegues gracias a su formato de plugins.
  
     (Page 4)
-
- id:: 63639919-e2f0-4a9c-97c1-d72672c34429
  
  Jenkins se basa en una arquitectura de ejecución distribuida, con un servidor principal y varios agentes. El servidor principal, o master, es el controlador del sistema y aloja toda la configuración, definición de trabajos, historial de ejecuciones, etc. Puede ejecutar trabajos, pero en entornos profesionales se recomienda que el master se limite a distribuir las tareas entre los agentes. Los agentes (también denominados esclavos en versiones anteriores) son nodos dependientes del master. Están encargados de ejecutar cualquier tarea que este les delegue. El software de Jenkins que se ejecuta en estos es bastante sencillo en comparación al master ya que no necesita interfaz gráfica ni historial. Los agentes pueden ser nodos estáticos, es decir, servidores desplegados y conectados al master de forma ajena a Jenkins (manual o automáticamente), o dinámicos, de forma que Jenkins los despliega bajo demanda en una nube pública o privada. #flashcard 
  
  
     (Page 5)
-
- id:: 63639919-fe5c-48e8-a654-e10be17b9858
  
  Cada agente tiene uno o varios ejecutores. Estos son procesos iniciados por el agente para un trabajo de Jenkins concreto. Así, es posible ejecutar varios trabajos en paralelo en cada agente. #flashcard 
  
  
     (Page 6)
-
- id:: 63639919-cdca-46ee-8d4f-9e227e5c15ef
  
  de: Estructura de un trabajo El elemento central de Jenkins es el trabajo, que está compuesto, a grandes rasgos,  Uno o varios triggers (o disparadores) que inician la ejecución.  Una lista de agentes en los que se permite ejecutar el trabajo.  Parámetros de entrada, sin aplica.  Tareas que se ejecutarán (que pueden arrancar otros trabajos).  Tareas de finalización (post-processing).  Artefactos archivados. Los triggers arrancan la ejecución de un trabajo. Pueden ser periódicos (al estilo de las tareas de cron), manuales (es decir, iniciados por un usuario), desde otro trabajo o a partir de un webhook. Los triggers periódicos pueden estar condicionados a que existan cambios en un repositorio. Por ejemplo, Jenkins puede comprobar periódicamente un repositorio e iniciar el trabajo solo si han aparecido commits nuevos en una rama concreta. Este modelo síncrono añade demasiada carga tanto a Jenkins como al sistema de control de cambios, por lo que se pueden aprovechar los webhooks para arrancar los trabajos asíncronamente. Por ejemplo, GitHub puede lanzar un webhook cuando se abre una pull request o cuando aparecen commits nuevos en una rama. Jenkins puede arrancar el trabajo al recibir el webhook, evitando así las comprobaciones periódicas. #flashcard 
  
  
     (Page 7)
-
- id:: 63639919-c92a-4e5a-b847-226a9a733c31
  
  Los Jenkinsfiles admiten dos tipos de sintaxis: declarativa y en script. La sintaxis en script es imperativa, es decir, el usuario debe definir el control de flujo y de errores y depende de expresiones propias de Groovy. La sintaxis declarativa, introducida en Jenkins 2, define secciones propias de Jenkins (es decir, no usa expresiones generales de Groovy) y delega el control de flujo y de errores en el propio motor de Jenkins. La sintaxis en script es más versátil, pero suele requerir más código. #flashcard 
  
  
     (Page 13)
-
- id:: 63639919-351b-4fc6-a22b-079f9779bccc
   INCLUIR IMAGEN #flashcard 
    Estructura de un Jenkinsfile El código de un Jenkinsfile con sintaxis declarativa está formado por un bloque pipeline inicial, directivas iniciales de configuración, un bloque stage para para fase y unas directivas post al terminar. El siguiente ejemplo contiene algunas de estas opciones.
  
     (Page 14)
-
- id:: 63639919-eb8a-4878-9de4-621da82b7ae7
  
  Figura 21. Código de pipeline. #flashcard 
  
  
     (Page 28)
-