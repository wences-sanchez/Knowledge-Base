# Administración de Sistemas para la Cloud Tema-7

deck:: [[UNI::Administración de Sistemas para la Cloud Tema-7]]\
author:: [[UNIR]]\
full-title:: "Administración de Sistemas para la Cloud Tema-7"\
category:: #books\
\
tags:: Administración-de-Sistemas-para-la-Cloud UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/1dbf92cc-b832-4536-a289-926d4bfcb3b4.png)
## Highlights
- id:: 63c669de-0925-4f3a-a82d-78ff55ff63d2
   ¿En qué tipo de flujo está basada PowerShell? #flashcard 
    A diferencia de otras shells, cuyos comandos devuelven y aceptan texto, PowerShell está basada en el framework .NET y, como tal, devuelve y acepta objetos de .NET. Este cambio de paradigma ofrece funcionalidades muy útiles para tareas administrativas.
  
     (Page 4)
-
- id:: 63c669de-8788-4ebe-8c3c-8f2f28edee73
   ¿Qué hace el comando Get-Member? #flashcard 
    Uno de los conceptos que más cuesta asumir es que prácticamente todo lo que manipulan los cmdlets son objetos .NET. Esto significa que, al enviar la salida en una tubería de un comando a otro, el segundo comando recibirá un objeto. El tipo de los objetos o su formato no tienen por qué ser siempre conocidos, y aquí es donde Get-Member aporta su valor: mostrará el detalle de los métodos y atributos del objeto que haya recibido. Por ejemplo, en la Figura 2, Get-Member recibe un objeto de tipo ApplicationInfo.
  
     (Page 7)
-
- id:: 63c669de-ba2c-433c-b5a2-3909be804bd6
   ¿Cómo podrías acceder a un item dentro de un bucle en PowerShell? #flashcard 
    es posible acceder al contenido de la lista con otras expresiones nativas de PowerShell, como foreach. Esta expresión aplica un bucle sobre una lista. En cada iteración, la variable $_ contiene el objeto correspondiente y es posible acceder a él, como en el caso anterior.
  
     (Page 8)
-
- id:: 63c669de-93e8-4c21-83bd-98d5c2cff76c
   ¿Cómo puedes obtener información de las unidades de almacenamiento disponibles en PowerShell? #flashcard 
    En PowerShell, el sistema de ficheros es solo uno de los tipos de unidades que se pueden manipular. Las unidades disponibles se pueden obtener con Get-PSDrive, sin parámetros (ver Figura 5).
  
     (Page 9)
-
- id:: 63c669de-d83f-4922-bf40-1cc38fe96df2
   Algunos ejemplos de alias en PowerShell. #flashcard 
    PowerShell soporta alias, que son nombres alternativos de comandos y cmdlets (Shepard, 2015). Por ejemplo, dir y ls son alias de Get-ChildItem y cd es un alias de Set-Location. Hay alias disponibles para muchos cmdlets con funcionalidad similar en entornos DOS o Linux. El objetivo es doble: hacer el código más conciso en la línea de comandos y facilitar la transición de los usuarios habituales de otras shell. Para obtener una lista de los alias definidos en una sesión, se puede hacer uso de Get-Alias. Con el parámetro por defecto, Get-Alias <alias>, se obtiene el comando al que un alias hace referencia y con Get-Alias -Definition <cmdlet> se obtienen los alias definidos para ese cmdlet (ver Figura 8).
  
     (Page 10)
-
- id:: 63c669de-da6c-41ab-ac13-609d10bd6c48
   ¿Cómo usarías, exportarías e importarías alias en PowerShell? #flashcard 
    El cmdlet New-Alias crea un alias en la sesión actual. Los alias no son permanentes y desparecen al cerrar la consola, pero es posible guardarlos con Export-Alias. Al iniciar sesión, se pueden importar con Import-Alias.
  
     (Page 11)
-
- id:: 63c669de-0fc1-4aa3-9e29-2656d7e30c32
   ¿Qué extensión tienen los scripts de PowerShell? #flashcard 
    Como se ha mencionado anteriormente, PowerShell ofrece no solo una herramienta interactiva, sino también un entorno de programación. Los scripts en PowerShell tienen la extensión .ps1, independientemente de la versión de PowerShell (Shepard, 2015).
  
     (Page 11)
-
- id:: 63c669de-04bb-4837-bf8f-59c60f8b0701
   CONTINÚA #flashcard 
    La política de ejecución es una medida de seguridad de PowerShell que ofrece control a los administradores sobre qué scripts se pueden ejecutar. Las políticas de ejecución posibles son:  Restricted: no permite la ejecución de scripts en ningún caso. Fue la política por defecto para las versiones anteriores a Windows Server 2012 R2.  All signed: solo los scripts con una firma digital válida se pueden ejecutar.
  
     (Page 12)
-
- id:: 63c669de-2978-40b0-af35-ee4db71a85f4
   ¿Cuáles son las políticas de ejecución, de medidas de seguridad, posibles en PowerShell? #flashcard 
     Remote signed: los scripts de ubicaciones remotas deben tener una firma digital válida para ejecutarlos, pero los scripts locales se pueden ejecutar sin restricciones. Es la política por defecto desde Windows Server 2012 R2.  Unrestricted: cualquier script se puede ejecutar sin restricciones. El comando Get-ExecutionPolicy muestra la política actual, mientras que Set ExecutionPolicy permite cambiar de una política a otra (ver Figura 12). Administración de Sistemas en la Cloud Tema 7. Ideas clave 13 I ) R N U i j ( a o R a L e d l a n o i c a n r e t n I d a d i s r e v i n U ©
  
     (Page 13)
-
- ¿Cómo se especifican los comentarios en PowerShell? #flashcard 
  id:: 63cfbca9-5d0a-4734-85dc-1a8637d81df4
    Los scripts de PowerShell aceptan comentarios de una línea precedidos por el carácter # y de varias líneas rodeados con los delimitadores <# y #>. # comentario en una linea Write-Host Hello World <# #> comentario en multiples lineas Write-Host Bye bye
  
     (Page 14)
-
- id:: 63c669de-e6e2-4cb8-883d-cf606fa96170
   Manera de llamar a un script sin sobreescribir variables en PowerShell. #flashcard 
    PS C:\> Get-Content .\hello-world.ps1 $var = "Hello World" Write-Host "La variable contiene:" $var PS C:\> .\hello-world.ps1 La variable contiene: Hello World PS C:\> Write-Host $var PS C:\>
  
     (Page 14)
-
- id:: 63c669de-8742-40bb-8f51-acfad12343ea
   ¿Cómo podrías ejecutar un script en PowerShell de manera que tenga el mismo efecto que llamar a todos sus comandos en la CLI? #flashcard 
    PowerShell usa la misma técnica que Bash para ejecutar un script en el ámbito de la shell actual para mantener todos los objetos creados durante la ejecución: en vez invocar el script como cualquier otro ejecutable, se invoca el script con el comando «.» (punto). En Bash, el punto era equivalente al comando source, esta herramienta suele llamarse dot-sourcing. Este método tiene el mismo efecto que ejecutar todos los comandos del script en la línea de comandos, uno tras otro. El resultado del ejemplo anterior, usando esta técnica, sería el siguiente: PS C:\> . .\hello-world.ps1 La variable contiene: Hello World PS C:\> echo $var Hello World PS C:\>
  
     (Page 15)
-
- id:: 63c669de-95b9-4aa5-bea5-f04fc44c5561
   Ejemplo de documentación de función en PowerShell #flashcard 
    <# .Synopsis Funcion de ejemplo .DESCRIPTION Esta funcion imprime los valores de dos parametros, Var1, que es una cadena de texto y es obligatorio, y Var2, que es un entero y su valor por defecto es 42. Write-Vars -Var1 "Hello World" Write-Vars -Var1 "Hello World" -Var2 53 No espera datos por la entrada estandar. Emite el parametro Var2 por la salida estandar. function Write-Vars { .EXAMPLE .EXAMPLE .INPUTS .OUTPUTS #>
  
     (Page 19)
-
- id:: 63c669de-a460-4370-9064-733792949d36
   Ejemplo de IfElse en PowerShell #flashcard 
    } If ($Var1 -eq $Var2) { Write-Host "Iguales" } ElseIf ($Var1 -gt $Var2) { Write-Host "Mayor" } Else { Write-Host "Menor"
  
     (Page 20)
-
- id:: 63c669de-6f4e-4f87-9d63-b20c109f2952
   Ejemplo de ForEach en PowerShell #flashcard 
    La expresión más habitual para recorrer un bucle es ForEach. Esta expresión ejecuta un bloque de código para todos los valores de una colección. Por ejemplo, el siguiente bloque imprime el nombre de todos los ficheros de una carpeta: ForEach ($file in (Get-ChildItem -Path C:\Users\Administrator -File)) { Write-Host $file.Name } No es necesario inicializar la variable si ForEach recibe la colección a través de una tubería. En ese caso, la variable $_ contiene el valor de cada iteración (ya se vio en un ejemplo similar en la sección sobre Get-Member). Esta funcionalidad es especialmente útil en modo interactivo.
  
     (Page 21)
-
- id:: 63c669de-c25a-4eb1-84ae-7d779cd16496
   Ejemplo de uso de ForEach en una tubería. #flashcard 
    Get-ChildItem -Path C:\Users\Administrator -File | ForEach { Write-Host $_.Name }
  
     (Page 22)
-
- id:: 63c669de-9ca3-4f3a-baf7-7739cad8d971
   ¿Cómo ordenarías los contenidos de una carpeta por extensión y tamaño de manera descendente? .code #flashcard 
    PS C:\> Get-ChildItem -Path C:\Users\Administrator -File | Sort-Object Property Extension,Length -Descending
  
     (Page 22)
-
- id:: 63c669de-b8d9-43c9-8980-a4a914c59c3a
   Ejemplo de para qué sirve el comando Where-Object. #flashcard 
    El comando Where-Object, que ya ha aparecido en algunos ejemplos, se usa para filtrar listas a partir de los atributos de los objetos. PS C:\> Get-ChildItem -Path C:\Users\Administrator -File | Where-Object {$_.Length -gt 100 -and $_.CreationTime -gt '5/1/2020'}
  
     (Page 23)
-
- ¿Cómo usarías el comando Select-Object en PowerShell? #flashcard 
  id:: 63cfbca9-8181-4cf0-b709-ee97752c2a5e
    El comando Select-Object se puede usar con dos objetivos: limitar el número de objetos de la colección y limitar las propiedades de estos objetos. La limitación en el número de objetos no es un filtrado como el de Where-Object, sino un truncado de la lista para obtener los primeros diez elementos, o los diez últimos, por ejemplo. PS C:\> Get-ChildItem -Path C:\Users\Administrator -File | Sort-Object Property Length -Descending | Select-Object -First 2 -Skip 1
  
     (Page 23)
-