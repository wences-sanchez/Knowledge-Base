title:: Herramientas DevOps Tema-5 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas DevOps Tema-5"
category:: #books

tags:: #[[Herramientas-DevOps]] #[[UNI]]

- #tags #[[Herramientas-DevOps]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/936d2bf0-976b-448c-89a2-1b0daff285b9.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- objetivos Terraformes  una  herramientautilizada  para  gestionar  desplieguesen  diferentes entornos. Su foco no es el ciclo de vida del código de una aplicación individual, sino de toda la infraestructura alrededor de ella #ñspace
		- (Page 4)
	- -
	- -
	- Terraform es una herramienta que se utiliza para la construcción, el cambio y el versionado de infraestructura, de manera segura y eficiente. Esta puede administrar tanto servicios existentes como nubes públicas o soluciones internas personalizadas. #ñspace
		- (Page 5)
	- -
	- -
	- Ejemplo de Terraform #car
		- provider "aws" {  access_key = "ACCESS_KEY_HERE"  secret_key = "SECRET_KEY_HERE"  region = "us-east-1" resource "aws_instance" "example" {  ami = "ami-2757f631"  instance_type = "t2.micro" }  }
		- (Page 14)
	- -
	- -
	- El  comando  terraform  init descarga  e  instala  de  forma  automática  el Provider binario para los proveedores en uso dentro de la configuración. En este caso, es solo el proveedor de AWS #ñspace
		- (Page 16)
	- -
	- -
	- Es  importante  que  sepas  que  Terraform  ha  escrito  datos  en  el  archivo  de  estado terraform.tfstate. Ten en cuenta que este archivo es sumamente relevante porque lleva a cabo un seguimiento de los ID de aquellos recursos que fueron creados para que la herramienta Terraform tenga conocimiento sobre lo que está gestionando. Por ello,  deberás  guardarlo  y  compartirlo  con  aquellas  personas  dentro  de  la organización que deban ejecutar Terraform. #ñspace
		- (Page 19)
	- -
	- -
	- asignaremos  una  IP  elástica  a  la instancia  de  EC2.  Para  ello,  vamos  a  Modificar  el  example.tf  y  agregaremos  lo siguiente: } resource "aws_eip" "ip" { instance = "${aws_instance.example.id}"   Esto es similar a lo que hemos hecho en el ejemplo anterior (cuando agregamos un recurso de  instancia  EC2), excepto que  esta  vez estamos  construyendo un  tipo de recurso aws_eip. Lo que hace este tipo de recursos es asignar y asociar una IP elástica #ñspace
		- (Page 25)
	- -
	- -
	- En algunos casos hay dependencias entre recursos que no resultan visibles para Terraform. El argumento depends_on es aceptado por cualquier recurso y acepta una lista de recursos para crear dependencias explícitas. #ñspace
		- (Page 28)
	- -
	- -
	- Cuando  necesites  realizar  cambios  en  la  infraestructura,  en  lugar  de  actualizar  la infraestructura de forma manual en los servidores, puedes directamente realizar los cambios en  los  archivos de  configuración de  Terraform.  Esos  cambios  se validarán mediante  pruebas  automáticas  y  revisiones  de  códigos,  se  confirmará  el  código actualizado control de versiones, y luego se ejecutará el comando terraform apply para  que  Terraform  realice  las  llamadas  API  necesarias  para  implementar  los cambios. #ñspace
		- (Page 31)
	- -