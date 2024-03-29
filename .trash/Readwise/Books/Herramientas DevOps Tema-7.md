# Herramientas DevOps Tema-7

deck:: [[UNI::Herramientas DevOps Tema-7]]\
author:: [[UNIR]]\
full-title:: "Herramientas DevOps Tema-7"\
category:: #books\
\
tags:: Herramientas-DevOps UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/a21c72f6-f305-4921-be4a-23a000473eae.png)

## Highlights
- 
 ¿Qué guardarías en ElasticSearch? #flashcard 
    Es importante resaltar que ElasticSearch se puede considerar una base de datos de búsqueda. Pero, sin embargo, no es conveniente guardar información que requiera una alta durabilidad (datos de transacciones de clientes) sin una copia de seguridad. Por ejemplo, en una web de e-commerce podrían guardarse los datos del inventario y de productos, pero no sería conveniente guardar la información de los pedidos únicamente en ElasticSearch.

     (Page 5)
-
- 
 ¿Qué es, básicamente, ElasticSearch? #flashcard 
    ElasticSearch es un almacén de documentos distribuidos. En lugar de almacenar información como filas de datos en columnas, ElasticSearch almacena estructuras de datos complejas que se han serializado como documentos JSON. Cuando tienes varios nodos ElasticSearch en un clúster, los documentos almacenados se distribuyen a través del clúster y se puede acceder a ellos inmediatamente desde cualquier nodo.

     (Page 7)
-
- 
 ¿Cómo funciona el concepto de índice invertido en ElasticSearch? #flashcard 
    ElasticSearch utiliza una estructura de datos llamada índice invertido, que admite búsquedas de texto completo muy rápidas. Un índice invertido enumera cada palabra única que aparece en cualquier documento, e identifica todos los documentos en los que aparece dicha palabra.

     (Page 7)
-
- 
 Define índice y documento en ElasticSearch. #flashcard 
    Un índice puede considerarse como una colección optimizada de documentos, y cada documento es una colección de campos, que son los pares clave-valor que contienen sus datos. Por defecto, ElasticSearch indexa todos los datos en cada campo y cada campo indexado tiene una estructura de datos optimizada y dedicada. Por ejemplo, los campos de texto se almacenan en índices invertidos, y los campos numéricos y geográficos se almacenan en árboles BKD. La capacidad de usar las estructuras de datos por campo para ensamblar y devolver resultados de búsqueda es lo que hace que ElasticSearch sea tan rápido.

     (Page 7)
-
- 
 Ejemplo de inserción de datos en ElasticSearch #flashcard 
    Los índices de ElasticSearch pueden crearse de múltiples formas, pero finalmente lo que harán será incluir documentos JSON en un índice. Es posible hacer esto directamente con una solicitud PUT, que especifica el índice al que desea agregar el documento, un ID de documento único y uno o más pares "field": "value" en el cuerpo de la solicitud. Por ejemplo, si ejecutamos el código que aparece debajo en un clúster nuevo, esta solicitud crea automáticamente el índice customer si aún no existe, agrega un nuevo documento que tiene un ID 1 y almacena e indexa el campo name. PUT /customer/_doc/1 "name": "John Doe" { }

     (Page 9)
-
- 
 Ejemplo de recuperación de documento en ElasticSearch #flashcard 
    documento: GET /customer/_doc/1 Puedes recuperarlo con una solicitud GET que especifique su ID de

     (Page 10)
-
- 
 Habla acerca de los índices congelados en ElasticSearch #flashcard 
    es preferible liberar memoria y reconstruir estas estructuras de datos en cada búsqueda si los índices se utilizan con poca frecuencia. Por ejemplo, si estás utilizando índices basados en eltiempo para almacenar mensajes de registro o datos de series de tiempo, es probable que los índices más antiguos se busquen con mucha menos frecuencia que los más recientes. Los índices más antiguos tampoco reciben solicitudes de indexación. Además, sueledarse el caso de que las búsquedas de índices más antiguos se utilicen para realizar análisis a más largo plazo, para los cuales una respuesta más lenta es aceptable. Esta funcionalidad es muy frecuentemente utilizada en los casos de uso que estamos cubriendo, y es conveniente conocerla cuando nuestro clúster de ElasticSearch empieza a crecer, a fin de disminuir el consumo de memoria. Estos índices, son buenos candidatos para convertirse en índices congelados (frozen indices). ElasticSearchconstruye las estructuras de datos transitorios de cada fragmento de un índice congelado cada vez que se busca ese fragmento, y descarta estas estructuras de datos tan pronto como se completa la búsqueda. Debido a que ElasticSearch no mantiene estas estructuras de datos transitorios en la memoria, los índices congelados consumen mucho menos memoria en normales.

     (Page 12)
-
- 
 ¿Cómo congelarías un índice en ElasticSearch? #flashcard 
    Es posible congelar un índice utilizando la API Freeze Index: POST /<index>/_freeze

     (Page 12)
-
- 
 ¿Cómo descongelarías un índice en ElasticSearch? #flashcard 
    Para “descongelar” un índice, puedes usar la API de índice Unfreeze: POST /<index>/_unfreeze

     (Page 13)
-
- 
 ¿Dónde y cómo guarda los datos ElasticSearch? #flashcard 
    También es posible optar por almacenar datos en otro sistema. ElasticSearch (a no ser que se utilicen los índices congelados) almacena datos en la memoria RAM de los servidores. El coste de memoria es mucho mayor al coste de disco, por tanto, congelar índices puede ser una forma de reducir el consumo monetario sin perder información. Otra opción menos costosa es la de guardar los datos en un almacenamiento separado e independiente de ElasticSearch. Esta solución es la más frecuente cuando los logs deben almacenarse por motivos regulatorios, pero no se espera que se vayan a consultar más tarde.

     (Page 14)
-
- 
 Define Rollup en ElasticSearch. #flashcard 
    Si deseamos analizar los datos (por ejemplo, sacar métricas de evolución de tiempo de respuesta, o comparar cuantas peticiones ha habido en el mes de abril en diferentes años), necesitaremos almacenarlos de una forma en que la consulta no sea tan costosa. Ahí es donde entra en juego Rollup. Esta funcionalidad resume los datos antiguos de alta granularidad y los dispone en un formato más reducido (con menor detalle) para el almacenamiento a largo plazo. Al "enrollar" los datos en un único documento (resumen), los datos históricos se pueden comprimir en gran medida, en comparación con los datos sin procesar.

     (Page 15)
-
- 
 ¿Cómo trabaja Rollup con los datos (procesados y sin procesar) en ElasticSearch? #flashcard 
    El hecho de tener un punto de entrada separado habilita una característica útil de Rollup que es la capacidad de consultar datos “en vivo” (en tiempo real), además de datos históricos “enrollados” en una sola consulta. Por ejemplo, el sistema puede mantener un mes de datos sin procesar. Transcurrido ese plazo, se acumula en resúmenes históricos utilizando Rollup y se eliminan los datos sin procesar. Si consultaras los datos sin procesar, solo verías el mes más reciente. Y si consultaras los datos acumulados, solo verías datos anteriores a un mes. Endpoint RollupSearch, sin embargo, admite ambas consultas al mismo tiempo. Tomará los resultados de ambas fuentes de datos y los fusionará. Si hay una superposición entre los datos “en vivo” y “enrollados”, dará preferencia a los datos “en vivo” para aumentar la precisión. Rollup es capaz de utilizar, de manera inteligente, el mejor intervalo disponible.

     (Page 17)
-
- 

Las API REST de ElasticSearch admiten consultas estructuradas, libres y complejas (combinación de las dos anteriores). #flashcard 


     (Page 18)
-
- 
 Ejemplo de búsqueda en ElasticSearch Query DSL #flashcard 
    Una vez que hayas metido datos en un índice de ElasticSearch, puedes buscarlos enviando solicitudes al endpoint de _search. Utilizaremos el ElasticSearch Query DSL para especificar los criterios de búsqueda en el cuerpo de la solicitud. Para ello debes especificar el nombre del índice que deseas buscar en el URI de solicitud. Por ejemplo, la siguiente solicitud recupera todos los documentos en el índice de bank ordenados por número de cuenta: GET /bank/_search "query": { "match_all": {} }, "sort": [ { "account_number": "asc" } { ] }

     (Page 19)
-
- 
 Campos de respuesta a una consulta en ElasticSearch #flashcard 
    La respuesta también incluye información adicional sobre la solicitud de búsqueda:  took: cuánto tiempo tardó ElasticSearch en ejecutar la consulta, en milisegundos.  timed_out: si la solicitud de búsqueda expiró o no.  _shards: cuántos fragmentos se buscaron y un desglose de cuántos fragmentos tuvieron éxito, fallaron o se omitieron.  max_score: la puntuación del documento más relevante encontrado.  hits.total.value: cuántos documentos coincidentes se encontraron.  hits.sort: la posición de clasificación del documento (cuando no se clasifica por puntuación de relevancia).  hits._score: la puntuación de relevancia del documento (no aplicable cuando se usa match_all).

     (Page 21)
-
- 
 Ejemplo de consulta match sencilla en ElasticSearch #flashcard 
    Para buscar términos específicos dentro de un campo, puedes usar una matchconsulta. Por ejemplo, la siguiente solicitud busca en el campo address aquellos clientes cuyas direcciones contengan “Calle de la Universidad de la Rioja”: GET /bank/_search "query": { "match": { "address": "Calle de la Universidad de la Rioja" } } { }

     (Page 22)
-
- 
 Ejemplo de consulta match de frase en ElasticSearch #flashcard 
    GET /bank/_search Rioja" } } "query": { "match_phrase": { "address": "Calle de la Universidad de la { }

     (Page 22)
-
- 
 ¿Cómo podrías construir consultas más complejas en ElasticSearch? #flashcard 
    Para construir consultas más complejas, puedes usar una consulta booleana para combinar varios criterios de consulta. Se puede designar los criterios como obligatorios (deben coincidir con must), deseables (deberían coincidir con should) o indeseables (no deben coincidir con must_not).

     (Page 22)
-
- 
 ¿Cómo buscarías en ElasticSearch personas que tengan 40 años y que no vivan en La Rioja? #flashcard 
    Por ejemplo, la siguiente solicitud busca en el índice bank las cuentas que pertenecen a clientes que tienen 40 años, pero excluye a cualquier persona que viva en la Rioja (ES-RI): GET /bank/_search "query": { "bool": { "must": [ { "match": { "age": "40" } } "must_not": [ { "match": { "region": "ES-RI" } } { ], ] } } }

     (Page 23)
-
- 
 ¿Qué es, básicamente, una agregación en ElasticSearch? #flashcard 
    El marco de agregación ayuda a proporcionar datos agregados basados en una consulta de búsqueda. Se basa en bloques de construcción simples llamados agregaciones, que se pueden componer para crear resúmenes complejos de los datos. Una agregación puede verse como una unidad de trabajo que construye información analítica sobre un conjunto de documentos. El contexto de la ejecución define qué es este conjunto de documentos (por ejemplo, una agregación de nivel superior se ejecuta dentro del contexto de la consulta / filtros ejecutados de la solicitud de búsqueda)

     (Page 28)
-
- 
 Menciona los cuatro tipos de agregaciones en ElasticSearch. #flashcard 
    dividiremos en cuatro familias principales:  De agrupación o bucket. Son una familia de agregaciones que crean agrupaciones, donde cada grupo está asociado con una clave y un criterio del documento. Cuando se ejecuta la agregación, todos los criterios de los grupos se evalúan en cada documento en el contexto y cuando un criterio coincide, se considera que el documento “cae” en la agrupación correspondiente. Al final del proceso de agregación, terminaremos con una lista de grupos o categorías, cada uno con un conjunto de documentos que “pertenecen” a él.  De métricas o metric. Son agregaciones que realizan un seguimiento y calculan métricas sobre un conjunto de documentos.  Matriz. Son una familia de agregaciones que operan en múltiples campos y producen un resultado de matriz basado en los valores extraídos de los campos del documento solicitado.  De pipeline o línea de procesamiento. Son agregaciones que agregan la salida de otras agregaciones y sus métricas asociadas.

     (Page 29)
-
- 
 Sobre las agregaciones de tipo métricas en ElasticSearch. #flashcard 
    Las agregaciones de esta familia calculan métricas basadas en valores extraídos de los documentos que se están agregando. Los valores generalmente se extraen de los campos del documento (utilizando los datos del campo), pero también se pueden generar mediante scripts. Las agregaciones de métricas numéricas son un tipo especial de agregación de métricas que generan valores numéricos. Algunas agregaciones generan una sola métrica numérica (por ejemplo, avg) y se llaman métricas de un único valor (del inglés single-value numeric metrics aggregation); otras generan múltiples métricas (por ejemplo, stats) y se llaman métricas numéricas de valores múltiples (del inglés multi value numeric metrics aggregation).

     (Page 32)
-
- 
 Acerca de las agregaciones de tipo de agrupación en ElasticSearch. #flashcard 
    Las agregaciones de agrupación (del inglés bucket aggregations) no calculan métricas sobre campos como lo hacen las agregaciones de métricas, sino que crean grupos de documentos. Cada grupo está asociado con un criterio (dependiendo del tipo de agregación) que determina si un documento en el contexto actual “cae” en él. Los depósitos definen efectivamente conjuntos de documentos, y también calculan y devuelven el número de documentos que “cayeron” en cada depósito. Las agregaciones de grupo, a diferencia de las agregaciones métricas, pueden contener subagregaciones. Estas subagregaciones se agregarán para los grupos creados por la agregación de grupo “principal”.

     (Page 34)
-
- 
 Acerca de las agregaciones de tipo de pipeline en ElasticSearch. #flashcard 
    Las agregaciones de pipeline funcionan en las salidas producidas a partir de otras agregaciones (en lugar de conjuntos de documentos), y agregan información conjuntamente en el árbol de salida. Existen muchos tipos diferentes de agregación de pipeline, cada uno de los cuales calcula información diferente de otras agregaciones. Estos tipos se pueden dividir en dos grandes familias:  Padre. Es una familia de agregaciones de pipeline que se proporciona junto con la salida de la agregación principal y puede calcular nuevos grupos o nuevas agregaciones para agregar a los grupos existentes.  Mismo nivel. Es una de las agregaciones de pipeline que se proporciona con la salida de una agregación de mismo nivel y pueden calcular una nueva agregación que estará en el mismo nivel que la agregación de este tipo.

     (Page 36)
-
