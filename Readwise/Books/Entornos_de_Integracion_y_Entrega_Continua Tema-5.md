# Entornos_de_Integracion_y_Entrega_Continua Tema-5

deck:: [[UNI::Entornos_de_Integracion_y_Entrega_Continua Tema-5]]\
author:: [[UNIR]]\
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-5"\
category:: #books\
\
tags:: Entornos-CI-CD UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/a0ce2b0f-edc9-4ed0-9a15-89640a0a011d.jpg)
## Highlights
- id:: 63c669fb-7743-4884-8901-d88feec8c4e7
  
  Las pruebas unitarias intentan comprobar el comportamiento del código de la aplicación al nivel más básico posible. La unidad de prueba suele ser el método o la función. #flashcard 
  
  
     (Page 5)
-
- id:: 63c669fb-6395-4e9b-997c-fd61520de558
  
  En las pruebas de integración, también denominadas pruebas de sistema o de servicio, se comprueba el comportamiento de una aplicación y su interacción con otros sistemas. Al contrario de las pruebas unitarias, la aplicación debe estar arrancada y se permite el acceso a bases de datos y sistemas externos. #flashcard 
  
  
     (Page 6)
-
- id:: 63c669fb-a9cb-4b48-ab5d-cf923e977a6b
  
  ¿Debería considerarse un fallo de la aplicación, aun cuando el problema puede haber sido la existencia de una intervención manual en la base de datos? Para ello se suele hacer uso de dos técnicas:  La inicialización de la base de datos con «datos semilla», más conocidos como seed data. Estos datos son siempre los mismos y se insertan en una base de datos en blanco antes de empezar las pruebas. Si la base persiste tras las pruebas probablemente no sería razonable insertar seed data en cada ejecución de dichas pruebas.  El uso de fixtures: una fixture es una función que deja la base de datos (o cualquier otro sistema) en un estado conocido antes de iniciar la prueba y la devuelve a su estado original al terminar. Por ejemplo, puede insertar un registro conocido en la base, mantenerlo durante la prueba y borrarlo al terminar o modificar un registro, deshaciendo las modificaciones al terminar. Las fixtures no son específicas de las pruebas de integración y pueden usarse en cualquier otro tipo de pruebas. #flashcard 
  
  
     (Page 7)
-
- id:: 63c669fb-9ff0-40e0-9cdf-db283996a973
  
  El objetivo de las pruebas de aceptación es verificar el comportamiento real de la aplicación y que esta ofrezca precisamente la funcionalidad para la que se ha diseñado. A simple vista podrían parecer iguales a las pruebas de integración o de UI, pero la implementación técnica es diferente. La definición de las pruebas de aceptación se suele hacer en ficheros con sentencias en inglés que establecen, paso a paso, el objetivo de la prueba y el resultado de cada operación. #flashcard 
  
  
     (Page 8)
-