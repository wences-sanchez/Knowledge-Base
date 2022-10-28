# Cloud Computing and DevOps Culture Tema-10

deck:: [[UNI::Cloud Computing and DevOps Culture Tema-10]]\
author:: [[UNIR]]\
full-title:: "Cloud Computing and DevOps Culture Tema-10"\
category:: #books\
\
tags:: Cloud-Computing-and-DevOps-Culture UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/50d861c7-ab8d-47b1-9775-08a7c1456145.jpg)

## Highlights
- 
 ¿Cómo definirías las alertas y las visualizaciones? #flashcard 
    Las alertas son, básicamente, una selección de salidas negativas del sistema y las visualizaciones son representaciones estructuradas desambiguadas, enfocadas en facilitar la comprensión al usuario.

     (Page 4)
-
- 
 ¿Cuándo y por qué establecerías una alerta en un entorno de trabajo? #flashcard 
    Las alertas no deben usarse como un flujo constante de información o una actualización de estado. Están destinadas a notificar un determinado problema sobre el que el sistema no puede recuperarse de forma automática y se deben enviar solo a la persona que tenga la capacidad de poder recuperar el sistema. Aquello que quede fuera de esta definición no es una alerta y solo perjudicará a los empleados y a la cultura de la empresa.

     (Page 5)
-
- 
 Sobre los mapas de calor #flashcard 
    Este tipo de visualización resulta extremadamente útil para representar la información que proviene de histogramas. Es similar a un gráfico de barras, pero más enriquecido: puede mostrar gradientes dentro de las barras, que representan los diferentes percentiles respecto a la métrica general. Por ejemplo, si necesitas buscar latencias de solicitud y comprender rápidamente la tendencia general, así como la distribución de todas las solicitudes, el mapa de calor resulta un gran aliado. Además, permite usar colores para desambiguar la cantidad de cada sección de las barras.

     (Page 6)
-
- 
 ¿Qué es Bosun? #flashcard 
    Al igual que Prometheus, Bosun está escrito en Go y tiene más funcionalidad que Prometheus, ya que puede interactuar con muchos sistemas en contextos más complejos que la agregación de métricas (es compatible con Graphite, InfluxDB, OpenTSDB y Elasticsearch) y, adicionalmente, también puede consumir datos de sistemas de agregación de registros y eventos. La arquitectura de Bosun consiste en: un único servidor, un backend como OpenTSDB, Redis y sus agentes recolectores. Estos últimos detectan automáticamente los servicios en un host e informan sobre las métricas para esos procesos y otras métricas adicionales que pueda originar el sistema. El servidor de Bosun consulta los backends para determinar si existe alguna situación que requiera el disparar una alerta. Bosun también puede ser utilizado por herramientas como Grafana para facilitar las consultas a los backends subyacentes a través de una única interfaz.

     (Page 7)
-
- 
 Acerca de Cabot #flashcard 
    Cabot fue creado por una compañía llamada Arachnys con el objetivo de poder monitorizar servicios y no solo las máquinas. Parece un concepto simple, pero es de una importancia crucial, ya que en los entornos actuales de nada nos sirve saber que una máquina está funcionando si los contenedores, servicios web o microservicios que aloja, han dejado de responder de forma correcta.

     (Page 8)
-
- 
 ¿Qué es Grafana? #flashcard 
    El objetivo de Grafana es representar los datos de monitorización de una forma más usable y agradable. Una de sus ventajas más notables es que puede recopilar datos nativos de Graphite, Elasticsearch, OpenTSDB, Prometheus y InfluxDB. También existe una versión Enterprise que incluye complementos para que soporte más fuentes de datos, pero no hay razón por la que estos complementos no puedan ser también open source

     (Page 10)
-
