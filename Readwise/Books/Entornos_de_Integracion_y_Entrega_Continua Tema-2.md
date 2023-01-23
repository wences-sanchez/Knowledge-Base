# Entornos_de_Integracion_y_Entrega_Continua Tema-2

deck:: [[UNI::Entornos_de_Integracion_y_Entrega_Continua Tema-2]]\
author:: [[UNIR]]\
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-2"\
category:: #books\
\
tags:: Entornos-CI-CD UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/a1db0259-1f1c-43a7-8ee2-ddcb17940e9c.jpg)
## Highlights
- id:: 63c669fa-f206-475f-8095-ab07780588a9
   Define **Repositorio** #flashcard 
     Repositorio: es el almacenamiento maestro de todos los archivos y su historial de cambios. Se almacena en el servidor de control de versiones. Cada proyecto autónomo debe tener su propio repositorio, aunque un único proyecto puede estar repartido en más de un repositorio.
  
     (Page 6)
-
- id:: 63c669fa-1fd0-4ada-8906-727a26d6c9fb
   Define **Sandbox** #flashcard 
     Sandbox: también se conoce como copia de trabajo. Contiene una copia de todos los archivos del repositorio de un punto en particular. Cada desarrollador mantiene su propia copia de trabajo a partir del contenido del repositorio.
  
     (Page 6)
-
- Define **Check-out** #flashcard 
     Check-out: es el proceso de inicializar una copia de trabajo a partir de un punto concreto de un repositorio. En algunos sistemas de control de versiones este proceso se define con el término update and lock o actualizar y bloquear.
  
     (Page 6)
-
- id:: 63c669fa-3e3e-4e79-8c5d-4db0e8bf1d25
   Define **Update** #flashcard 
     Update: actualización de la sandbox para obtener los últimos cambios desde el repositorio. También se puede actualizar a un punto en particular en el pasado.
  
     (Page 6)
-
- id:: 63c669fa-502a-410c-b195-07b5c44c511f
   Define **Lock** #flashcard 
     Lock: un bloqueo hace posible que nadie pueda editar un archivo sin el desarrollador que lo ha bloqueado.
  
     (Page 6)
-
- id:: 63c669fa-72d8-4d48-8853-88352b1e7af8
   Define **commit** #flashcard 
     Check-in o commit: registro de los cambios efectuados en la copia de trabajo. Es el proceso fundamental para guardar los cambios en el repositorio. Estos son efímeros desde el punto de vista del repositorio; es decir, aunque los archivos estén guardados en el disco duro, los cambios entre el último commit y el estado actual no están registrados en el repositorio y, por tanto, no existen en el histórico del control de versiones a menos que se registren en un commit.
  
     (Page 6)
-
- id:: 63c669fa-e118-4bed-bb4a-50848dd30ddd
   Define **Revert** #flashcard 
     Revert: destruye la sandbox para descartar los cambios y volver al punto de la última actualización. Esto es útil cuando el código de la copia de trabajo actual se ha vuelvo inestable y no es posible hacerlo funcionar de nuevo. A veces revertir es más rápido que depurar, especialmente, si hay commits recientes.
  
     (Page 7)
-
- id:: 63c669fa-287a-4a43-96e9-d7b3080c0229
   Define **Head** #flashcard 
     Tip o Head: la cabecera del repositorio contiene los cambios más recientes que se han registrado. Al actualizar la copia de trabajo los archivos quedan en el estado de la cabecera. El sistema de control de versiones soporta ramas, cada rama tiene su propia cabecera, por lo que la copia de trabajo se puede actualizar en la cabecera de cada una de las ramas.
  
     (Page 7)
-
-  Tag o label: una etiqueta marca un commit determinado en el historial del repositorio, lo que permite acceder fácilmente a él de nuevo. Pueden usarse para indicar una versión liberada (release) o un punto de pase a producción. Aunque es posible borrarlas, no deberían ser modificadas. #flashcard 
  
  
     (Page 7)
-
- id:: 63c669fa-5c80-453c-a192-c0a3cc829169
   Define **Rollback** #flashcard 
     Rollback: es el proceso en el que se deshace un commit para que los cambios introducidos desaparezcan de la cabecera del repositorio. El mecanismo para hacerlo varía dependiendo del sistema de control de versiones: en unos casos se genera un segundo commit B que anula los cambios del anterior commit A, por lo que los archivos vuelven al estado anterior (commit A). En otros casos, se puede eliminar el commit A completamente.
  
     (Page 7)
-
- id:: 63c669fa-0879-405b-ae63-837fe55a1bc2
  
   Rama: las ramas permiten dividir el repositorio en distintos historiales alternativos. Suelen partir de un commit común, pero a partir de ese momento los cambios registrados en cada rama pueden divergir tanto como sea necesario. Es habitual, por ejemplo, separar en ramas el trabajo, en diferentes características nuevas, en arreglos o en entornos de trabajo. Las ramas apuntan a un commit, al igual que las etiquetas, pero se actualizan cada vez que hay uno nuevo (las etiquetas no se modifican una vez asignadas a un commit). #flashcard 
  
  
     (Page 7)
-
- id:: 63c669fa-1360-4d72-a1cc-fd874b7cb3ab
  
   Fusión o merge: es el proceso de combinar cambios de dos ramas. Si dos programadores le hacen un cambio a uno o varios archivos (cada uno en una rama por separado) y ambos hacen un check-in de los cambios, el segundo programador tendrá que fusionar los cambios de la primera persona. Las herramientas más modernas ayudan en este proceso e incluso lo hacen automáticamente si los cambios no afectan a las mismas líneas de código. #flashcard 
  
  
     (Page 8)
-
- id:: 63c669fa-0f23-45d8-a1ca-b50dd6c8f8d3
  
   Resolución de conflictos: una fusión se puede llevar a cabo automáticamente si los cambios de dos commits afectan a archivos diferentes o a diferentes partes de uno. Sin embargo, si los cambios afectan a la misma sección de un archivo, las herramientas no son capaces de resolverlo y el desarrollador debe encargarse de identificar el estado original del fichero, los cambios introducidos por el otro desarrollador y sus propios cambios, y decidir cómo resolverlo. Los sistemas de control de versiones suelen resaltar los conflictos y muestran, en un mismo editor, los cambios de ambos commits con el objetivo de facilitarle la vida al desarrollador. #flashcard 
  
  
     (Page 8)
-
- id:: 63c669fa-5478-4ba8-a367-209f1e324c3d
  
  Uno de los usos más potentes de un sistema de control de versiones es la capacidad de retroceder en el tiempo. Un desarrollador puede actualizar su copia de trabajo con todos los archivos a un punto en particular en el pasado. Por ejemplo, si se ha detectado un error en una versión ya publicada de la aplicación, pero no se encuentra la causa, el desarrollador puede aplicar diff debugging:  Actualiza la copia de trabajo a un punto en el que el error no existía.  A continuación, actualiza la copia de trabajo con los siguientes cambios por orden histórico hasta que logra aislar el commit exacto que introdujo el error.  En ese punto, el desarrollador solo tiene que revisar los cambios de ese commit para localizar el error. Si se trabaja con integración continua y el número de cambios es pequeño, el error será fácil de corregir. #flashcard 
  
  
     (Page 10)
-
- id:: 63c669fa-d0c5-4d4f-b2f7-e93964d24560
  
  Siempre que sea posible, es recomendable mantener en el control de versiones todas las herramientas, librerías, documentación y cualquier elemento con el proyecto. Las herramientas y librerías son particularmente importantes ya que, si se dejan fuera, en algún momento se actualizará una de ellas y ya no se podrá volver a un punto anterior a la actualización, salvo manualmente (con la posibilidad de fallo humano que esto implica). #flashcard 
  
  
     (Page 11)
-
- id:: 63c669fa-9b50-44cb-a684-be665c793ea3
  
  Lo único relacionado con el proyecto que no debería guardarse en el control de versiones es el código generado, es decir, binarios compilados o ficheros autogenerados #flashcard 
  
  
     (Page 12)
-
- id:: 63c669fa-79ec-4512-8ee5-bce0d02cd7bb
  
  La información de usuario también debe ir al repositorio. Esto incluye la documentación, notas sobre requisitos, escritura técnica (como manuales y guías) y pruebas de usuario. Hay una excepción adicional en cuanto a lo que no debe almacenar en control de versiones: un código que se va a desechar. Estos son los experimentos, test, proyectos de investigación que permanecen sin integrarse, etcétera. Algunos desarrolladores mantienen repositorios propios para almacenar este tipo de información. #flashcard 
  
  
     (Page 12)
-
- id:: 63c669fa-1f59-43c2-9d36-ce960f3f5c38
  
  sistemas como Git permiten usar herramientas externas para extraer contenido de texto de un fichero binario y guardar los cambios sobre este texto. El control de versiones almacenará los cambios sobre el fichero binario, pero las herramientas de comparación de cambios podrán trabajar con ficheros de texto. Por ejemplo, se puede versionar un fichero PDF y usar la herramienta pdfinfo para comparar detalles del contenido entre dos versiones. #flashcard 
  
  
     (Page 13)
-
- id:: 63c669fa-32c6-4259-a2e7-e1975c2381ce
   INCLUIR IMAGEN #flashcard 
    A grandes rasgos, el código atraviesa cuatro niveles de completitud que veremos en la Figura 1:
  
     (Page 14)
-
- id:: 63c669fa-7bc8-402e-95f1-6d6bbc1c6a18
  
  Otra opción es incluir la aplicación del repositorio externo como una dependencia. En este caso, tan solo hay que modificar la referencia a la librería cuando se libere una nueva versión, los cambios de la versión sean interesantes y hayan sido validados con el código local. Muchos sistemas de control de versiones soportan la integración entre repositorios. Al actualizar una copia de trabajo, el sistema recuperará automáticamente los cambios más recientes del repositorio principal y de sus dependientes. Por ejemplo, Git soporta la funcionalidad de submódulos: un repositorio externo configurado como submódulo que aparece como un directorio dentro del repositorio local. #flashcard 
  
  
     (Page 20)
-
- id:: 63c669fa-3c0a-45d5-b8fc-e3893e828e41
  
   Si no está en control de versiones, no existe. • El código que reside en la máquina de un desarrollador no le vale a nadie más • Se recomienda habitualmente subir el código al control de versiones al final del día (siempre que no rompa la construcción, o en cualquier caso si se trata de y se puede perder. ramas privadas). #flashcard 
  
  
     (Page 21)
-
- id:: 63c669fa-dee4-4be3-bc1f-b946122340f1
  
  Las ramas de desarrollo son, por norma general, consideradas efímeras. Los cambios ya se han incorporado en la rama principal y, eventualmente, serán parte de una versión liberada. Por tanto, las ramas de desarrollo se pueden borrar sin que por ello desaparezcan los commits. Se puede pensar en las ramas como punteros a commits concretos, pero el hecho de borrar el puntero no borra el commit. #flashcard 
  
  
     (Page 33)
-