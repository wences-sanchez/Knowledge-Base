# Herramientas DevOps Tema-6

deck:: [[UNI::Herramientas DevOps Tema-6]]\
author:: [[UNIR]]\
full-title:: "Herramientas DevOps Tema-6"\
category:: #books\
\
tags:: Herramientas-DevOps UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/841e10b1-50a8-4574-a5e9-6993f36fce49.jpg)

## Highlights
- 
 Ejemplo de código en Terraform #flashcard 
    resource "aws_instance" "example" { ami = "ami‐b374d5a5" instance_type = "t2.micro" provisioner "local‐exec" { command = "echo ${aws_instance.example.public_ip} > ip_address.txt" } }

     (Page 6)
-
- 

Los aprovisionadores solo se ejecutan cuando se crea un recurso. No son un reemplazo para la administración de la configuración y el cambio del software de un servidor que ya se está ejecutando, y en su lugar, solo están pensados como una forma de arrancar un servidor. Para la administración de configuración, debes usar el aprovisionamiento de Terraform para invocar una solución de administración de configuración real. Un ejemplo de esto es utilizarlo para instalar un agente Chef o Puppet. #flashcard 


     (Page 6)
-
- 
 ¿Cómo gestiona Terraform los recursos que fallan en tiempo de aprovisionamiento? #flashcard 
    Si un recurso se crea correctamente, pero falla durante el aprovisionamiento, Terraform generará un error y marcará el recurso como “contaminado”. Un recurso que está contaminado, aunque se haya creado físicamente, no se puede considerar seguro para usar, dado que el suministro ha fallado. Cuando generes tu próximo plan de ejecución, Terraform no intentará reiniciar el aprovisionamiento en el mismo recurso porque no se garantiza que sea seguro (podría haber quedado en un estado inconsistente). En su lugar, Terraform eliminará los recursos contaminados y creará nuevos recursos, intentando aprovisionarlos nuevamente después de la creación. Terraform tampoco destruye automáticamente el recurso cuando el aprovisionamiento falla, ya que eso iría en contra del plan de ejecución.

     (Page 7)
-
- 
 Ejemplo de código en Terraform (usando variables) #flashcard 
    provider "aws" { access_key = var.access_key secret_key = "var.secret_key region = var.region }

     (Page 9)
-
- 

Todos los archivos que coincidan con terraform.tfvars o *.auto.tfvars presentes en el directorio actual son cargados automáticamente por Terraform para rellenar variables. Si el archivo tiene otro nombre, puedes usar el flag ‐var‐file. Estos archivos tienen la misma sintaxis que Terraform, y como todos los archivos de Terraform, también pueden ser JSON. #flashcard 


     (Page 10)
-
- 

Para usarla, reemplaza aws_instance con lo siguiente: resource "aws_instance" "example" { ami = "${lookup(var.amis, var.region)}" instance_type = "t2.micro" } Esto introduce un nuevo tipo de interpolación: llamada a función. La función lookup hace una búsqueda dinámica en un mapa a partir de una clave. La clave es var.region, que especifica que el valor var.region es la clave. También puedes hacer una búsqueda estática de un mapa directamente con: ${var.amis [" us‐east‐1 "]}. #flashcard 


     (Page 13)
-
- 

Los resultados son una forma de decirle a Terraform qué datos son importantes. Esta información se emite cuando se llama apply, y puede ser consultada usando el comando terraform output. #flashcard 


     (Page 15)
-
- 
 ¿Qué son los módulos en Terraform? #flashcard 
    Los módulos en Terraform son paquetes independientes de configuraciones Terraform que se manejan como un grupo. Los módulos se usan para crear componentes reutilizables, organizarlos más fácilmente y tratar las piezas de infraestructura como una caja negra.

     (Page 16)
-
