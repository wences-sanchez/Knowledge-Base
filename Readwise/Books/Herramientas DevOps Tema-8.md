# Herramientas DevOps Tema-8

deck:: [[UNI::Herramientas DevOps Tema-8]]\
author:: [[UNIR]]\
full-title:: "Herramientas DevOps Tema-8"\
category:: #books\
\
tags:: UNI Herramientas-DevOps  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/422bbcda-c225-4b1b-bec0-f28c0c448c44.png)

## Highlights
- 
 ¿Qué es logstash? #flashcard 
    Logstash es un motor de recopilación de datos de código abierto con capacidades de procesamiento en tiempo real.Puede unificar dinámicamente datos de fuentes dispares y normalizar los datos en los destinos que indique el usuario. Permite limpiar y unificar todos los datos para casos de uso avanzados de análisis y visualización. Logstash tiene capacidades para ingestar directamente algunas fuentes de datos como pueden ser los ficheros o ciertas bases de datos. Para algunas aplicaciones es posible utilizar Logstash exclusivamente, sin embargo, para aplicaciones de monitorización como las que estamos analizando nosotros, las diferentes piezas de Beats permiten la recolección y enriquecimiento de datos en las fuentes, y presentan un menor consumo de recursos, por lo que suelen ser la solución preferida. Además suele requerir muy poco mantenimiento frente a Logstash I ) R N U i j ( a o R a L e d l a n o i c a n r e t n I d a d i s r e v i n U ©

     (Page 6)
-
- 
 Ejemplos de Yaml con listas y dicts #flashcard 
    index: 'beat-%{[agent.version]}-%{+yyyy.MM.dd}' output.elasticsearch.index: 'beat-%{[agent.version]}-%{+yyyy.MM.dd}' output: elasticsearch: Será guardado como: En el caso de listas: filebeat: inputs: - type: log Se almacena como: filebeat.inputs.0.type: log

     (Page 10)
-
- 

En YAML los strings se soportan cerrados por comillas dobles (“string”), comillas simples (‘string’) y sin poner comillas. Las comillas dobles permiten escapar caracteres mediante la barra invertida: \. Es necesario tener cuidado si no utilizamos comillas de que el texto no haga conflicto con ningún otro significado en YAML. #flashcard 


     (Page 11)
-
- 

es posible mostrar un error específico cuando la variable no está presente como: ${VAR:?texto_de_error}. #flashcard 


     (Page 12)
-
- 
 ¿Cómo funciona Filebeat? #flashcard 
    Así es como funciona Filebeat: cuando inicia Filebeat, inicia una o más entradas que se leen en las ubicaciones que ha especificado. Para cada fichero o registro que Filebeat localiza, Filebeat inicia un recolector. Cada recolector lee el contenido nuevo de un único logy envía los nuevos datos de registro a libbeat, que agrega los eventos y envía los datos agregados a la salida que ha configurado para Filebeat

     (Page 14)
-
- 
 ¿Qué dos componentes tiene Filebeat? #flashcard 
    Filebeat consta de dos componentes principales: entradas y recolectores. Estos componentes trabajan juntos para crear una cola de registros y enviar datos de eventos a la salida que especifique.

     (Page 15)
-
- 
 ¿Qué hacen los recolectores de Filebeat? #flashcard 
    Un recolector es responsable de leer el contenido de un solo archivo. El recolector lee cada archivo, línea por línea, y envía el contenido a la salida. Se inicia un recolector para cada archivo. El recolector es responsable de abrir y cerrar el archivo, lo que significa que el descriptor del archivo permanece abierto mientras el recolector se está ejecutando. Si un archivo se elimina o cambia de nombre mientras se está monitorizando, Filebeat continúa leyendo el archivo. Esto tiene el efecto secundario de que el espacio en su disco está reservado hasta que la recolección se cierre. Por defecto, Filebeat mantiene el archivo abierto hasta que close_inactive se alcanza. Esto es útil ya que cuando rotamos un fichero de logs con alguna herramienta como logrotate1 es posible terminar de leer las últimas líneas del fichero.

     (Page 15)
-
- 

Es importante entender cómo mantiene el estado de cada archivo Filebeat para poder entender qué está ocurriendo cuando un comportamiento nos sorprende. Filebeat mantiene el estado de cada archivo y frecuentemente guarda el estado en el disco en el archivo de registro. El estado se utiliza para recordar el último offset o lugar desde el que estaba leyendo para garantizar que se envíen todas las líneas del fichero. Si no se puede acceder a la salida, como ElasticSearch o Logstash, Filebeat realiza un seguimiento de las últimas líneas enviadas y continuará leyendo los archivos tan pronto como la salida vuelva a estar disponible. Mientras Filebeat se está ejecutando, la información de estado también se guarda en la memoria para cada entrada. Cuando se reinicia Filebeat, los datos del archivo de registro se utilizan para reconstruir el estado, y Filebeat continúa cada recolector en la última posición conocida. #flashcard 


     (Page 16)
-
