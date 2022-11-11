title:: Herramientas DevOps Tema-5 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas DevOps Tema-5"
category:: #books

tags:: Herramientas-DevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/936d2bf0-976b-448c-89a2-1b0daff285b9.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- objetivos Terraformes  una  herramientautilizada  para  gestionar  desplieguesen  diferentes entornos. Su foco no es el ciclo de vida del código de una aplicación individual, sino de toda la infraestructura alrededor de ella #flashcard
		  id:: 7c5d77d4-5b9d-4ff4-8428-d0ee9e9ed1b1
		- (Page 4)
	- -
	- -
		- Terraform es una herramienta que se utiliza para la construcción, el cambio y el versionado de infraestructura, de manera segura y eficiente. Esta puede administrar tanto servicios existentes como nubes públicas o soluciones internas personalizadas. #flashcard
		  id:: 68051759-c118-4c36-80b9-b2cf5f7c1e47
		- (Page 5)
	- -
	- -
		- Ejemplo de Terraform #flashcard
		  id:: 1fe0b6e1-b7bb-4187-9218-94c2e30c192d
			- provider "aws" {  access_key = "ACCESS_KEY_HERE"  secret_key = "SECRET_KEY_HERE"  region = "us-east-1" resource "aws_instance" "example" {  ami = "ami-2757f631"  instance_type = "t2.micro" }  }
		- (Page 14)
	- -
	- -
		- El  comando  terraform  init descarga  e  instala  de  forma  automática  el Provider binario para los proveedores en uso dentro de la configuración. En este caso, es solo el proveedor de AWS #flashcard
		  id:: 3e3d2cd0-2b20-4444-bfc2-90056d08710b
		- (Page 16)
	- -
	- -
		- Es  importante  que  sepas  que  Terraform  ha  escrito  datos  en  el  archivo  de  estado terraform.tfstate. Ten en cuenta que este archivo es sumamente relevante porque lleva a cabo un seguimiento de los ID de aquellos recursos que fueron creados para que la herramienta Terraform tenga conocimiento sobre lo que está gestionando. Por ello,  deberás  guardarlo  y  compartirlo  con  aquellas  personas  dentro  de  la organización que deban ejecutar Terraform. #flashcard
		  id:: 3137370d-5c3f-4161-a9cd-f9442040e083
		- (Page 19)
	- -
	- -
		- asignaremos  una  IP  elástica  a  la instancia  de  EC2.  Para  ello,  vamos  a  Modificar  el  example.tf  y  agregaremos  lo siguiente: } resource "aws_eip" "ip" { instance = "${aws_instance.example.id}"   Esto es similar a lo que hemos hecho en el ejemplo anterior (cuando agregamos un recurso de  instancia  EC2), excepto que  esta  vez estamos  construyendo un  tipo de recurso aws_eip. Lo que hace este tipo de recursos es asignar y asociar una IP elástica #flashcard
		  id:: 3501f50b-997b-4ad1-95a2-2bda5126906b
		- (Page 25)
	- -
	- -
		- En algunos casos hay dependencias entre recursos que no resultan visibles para Terraform. El argumento depends_on es aceptado por cualquier recurso y acepta una lista de recursos para crear dependencias explícitas. #flashcard
		  id:: 3007cd72-ae71-4a6f-97c4-16760f588f78
		- (Page 28)
	- -
	- -
		- Cuando  necesites  realizar  cambios  en  la  infraestructura,  en  lugar  de  actualizar  la infraestructura de forma manual en los servidores, puedes directamente realizar los cambios en  los  archivos de  configuración de  Terraform.  Esos  cambios  se validarán mediante  pruebas  automáticas  y  revisiones  de  códigos,  se  confirmará  el  código actualizado control de versiones, y luego se ejecutará el comando terraform apply para  que  Terraform  realice  las  llamadas  API  necesarias  para  implementar  los cambios. #flashcard
		  id:: b988f0d1-5064-4089-995e-a749d0fabb92
		- (Page 31)
	- -