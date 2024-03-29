title:: Herramientas de Automatización de Despliegues Tema-3 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-3"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/a882e1b4-ff60-4055-aa60-4ccd886b01ce.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Qué es un framework? +++ #flashcard
		  id:: e8063b0c-1ed1-4b35-887a-fac237a2403a
			- En el proceso de maduración del desarrollo de software han surgido los denominados marcos de trabajo, más conocidos por su nombre en inglés: frameworks. Su objetivo principal es el de simplificar y reducir el tiempo de desarrollo, permitiendo a los desarrolladores centrarse en aportar valor a la compañía e innovar.
		- (Page 4)
	- -
	- -
		- Nombra las tres partes de que se compone Chef: #flashcard
		  id:: 57df5a0d-7763-4f9e-986b-41a92079f5b2
			- El framework Chef está compuesto por tres componentes básicos que interactúan entre sí:
		- (Page 5)
	- -
	- -
		- ¿Qué hace el Servidor Chef? #flashcard
		  id:: 608296be-90dd-43a1-b005-4050d20b2cd8
			- El servidor Chef constituye el centro de los datos de configuración, que contiene los cookbooks,  que  son  los  módulos  de  configuración  de  recursos, las  políticas que se aplicarán a los diferentes nodos, y los metadatos, que describen cada uno de los nodos administrados por Chef.
		- (Page 5)
	- -
	- -
		- CONTINUE #flashcard
		  id:: 9fb458f0-4808-4ed9-935e-75b1bdb06f24
			- desarrolladores  poder  centrarse  en  el  desarrollo  específico  que  cumpla  con  los requisitos  necesarios,  sin  tener  que  preocuparse  de  elementos  y  servicios  de  uso común  que  son  proporcionados  por  el  framework,  y  lograr  así  una  entrega  más rápida. Estos frameworks de software suelen ofrecernos además un conjunto común de convenciones, procedimientos y servicios que tienen como objetivo fomentar que el equipo desarrolle de forma homogénea, facilitando así el desarrollo sostenible del proyecto.
		- (Page 5)
	- -
	- -
		- ¿Cómo se comunican los nodos de Chef con el server? #flashcard
		  id:: 37b27d97-f10d-4eb4-95e6-e2104b047977
			- Los nodos usan la herramienta Chef Client para conectarse con el Chef Server y solicitar los detalles de configuración que deben aplicarse sobre la máquina donde se ejecutan. A este proceso de aplicar los cambios sobre los nodos se le denomina *Chef run*.
		- (Page 6)
	- -
	- -
		- Define Chef Server #flashcard
		  id:: 9354c8c6-108b-4283-9833-845dd671cf15
			-   Chef  Server:  servidor  centralizado  que  contiene  y  gestiona  la  configuración  de todos  los  nodos.  Puede  estar  ubicado  en  un  servidor  independiente  o  alojado como servicio en la nube en Chef.
		- (Page 7)
	- -
	- -
		- Define nodo en Chef #flashcard
		  id:: c0de983f-fa54-460f-b8cf-4c9ae7364690
			-   Nodo: incluye la información relativa a las recetas y roles que deben aplicarse en la máquina durante la ejecución de Chef Client. Los atributos y la lista de ejecución del nodo son sus principales características.
		- (Page 7)
	- -
	- -
		- Define Cookbook en Chef #flashcard
		  id:: 8bb296cb-3066-4be9-9d7b-df3e57df7933
			-   Cookbook:  contiene  todos  los  recursos  e  instrucciones  que  se  necesitan  para configurar  nodos,  y  pueden  ser  reutilizados  en  varias  listas  de  ejecución.  Los cookbooks se componen habitualmente de varias recetas.
		- (Page 7)
	- -
	- -
		- Define Receta (Recipe) en Chef #flashcard
		  id:: f332ffb1-e8d0-4a7f-a699-951e116066eb
			-   Recipes (recetas): consiste en un conjunto de recursos que configuran un nodo, y es una de las partes fundamentales de Chef.
		- (Page 7)
	- -
	- -
		- Define recurso en Chef #flashcard
		  id:: baab500c-82c8-4713-939f-1f616bf424fe
			-   Recursos:  son  una  abstracción  multiplataforma  de  partes  configurables  de  un nodo, como pueden ser usuarios, paquetes, archivos o directorios.
		- (Page 7)
	- -
	- -
		- Define Chef Client #flashcard
		  id:: 78082f66-3549-43ba-b69a-17af2b12d83c
			-   Chef Client (Cliente Chef): realiza el trabajo necesario en nombre del nodo, donde ejecuta las recetas correspondientes para configurar e instalar el software.
		- (Page 7)
	- -
	- -
		- Define 'Chef Solo' #flashcard
		  id:: 56ec315e-fe84-456f-91cb-0d6dcde3e17e
			-   Chef  Solo:  herramienta  de  línea  de  comandos  que  permite  ejecutar  cookbooks Chef independientemente, sin conectarse a un servidor Chef. Es una versión de código abierto del Chef Client.
		- (Page 8)
	- -
	- -
		- ¿Qué es Knife en Chef? #flashcard
		  id:: 6ece14a2-e55e-4b59-960b-be0d8104e195
			-   Knife (cuchillo): herramienta de línea de comandos que utilizan los usuarios para cargar los ficheros de configuración en el servidor Chef.
		- (Page 8)
	- -
	- -
		- Ejemplo de Vagrantfile para Chef #flashcard
		  id:: 35787a03-304a-4f13-907f-ebe029a11ee5
			- config.vm.provision :chef_solo do |chef| chef.cookbooks_path = "chef-repo/cookbooks" chef.add_recipe "chef_apache" chef.arguments = "--chef-license accept" end
		- (Page 12)
	- -
	- -
		- Ejemplo completo de Vagrantfile con Chef #flashcard
		  id:: ee9ded7d-27c2-41ac-a09e-ae5eb8fe91b1
			- Vagrant.configure("2") do |config| config.vm.box = "ubuntu/bionic64" config.vm.network "private_network", ip: "192.168.33.40" config.vm.provider "virtualbox" do |vb| vb.memory = "1024" config.vm.provision :chef_solo do |chef| chef.cookbooks_path = "chef-repo/cookbooks" chef.add_recipe "chef_apache" chef.arguments = "--chef-license accept" end end end
		- (Page 12)
	- -
	- -
		- ¿Cómo podemos generar la estructura de nuestro cookbook? #flashcard
		  id:: 5fd202e9-e0fd-49a8-a8b6-84984e937e59
			- Una  vez  creado  el  directorio  de  cookbooks,  para  generar  nuestro  cookbook utilizaremos  el  comando  chef  correspondiente,  que  creará  toda  la  estructura  de directorios y ficheros que se requiere. chef generate cookbook apache
		- (Page 13)
	- -
	- -
		- INCLUIR IMAGEN #flashcard
		  id:: ff37cbd6-da73-4800-826c-4cf40a9649da
			- En esta estructura se pueden encontrar varios ficheros que se generan por defecto y que nos sirven de plantilla o versión inicial para incorporar funcionalidad a nuestro cookbook.  El  fichero  principal  donde  se  especifica  la  configuración  a  obtener  es  la receta por defecto, ubicado en: recipes/default.rb, al que vamos a incluir el primer apt_update 'Update the apt cache daily' do fragmento de código: end frequency 86400 action :periodic package 'apache2'
		- (Page 14)
	- -
	- -
		- Ejemplo de código en Chef #flashcard
		  id:: a1cfbf15-815e-4970-ae53-324f2ae613b8
			- file '/etc/apache2/sites-enabled/000-default.conf' do action :delete template '/etc/apache2/sites-available/vagrant.conf' do source 'virtual-hosts.conf.erb' link '/etc/apache2/sites-enabled/vagrant.conf' do to '/etc/apache2/sites-available/vagrant.conf' cookbook_file “/vagrant/index.html" do source 'index.html' only_if do File.exist?('/etc/apache2/sites-enabled/vagrant.conf') end end end end end
		- (Page 15)
	- -
	- -
		- ¿Cómo se interpola una variable en Chef? #flashcard
		  id:: 9edec72e-3a78-4d13-8d1b-3c4171b004ab
			- cookbook_file “#{node['apache']['document_root']}/index.html" do File.exist?('/etc/apache2/sites-enabled/vagrant.conf') source 'index.html' only_if do end end Tal como se muestra, la referencia al atributo se hace con el símbolo de la almohadilla (#) y, entre llaves ({}), el nombre del atributo dentro del objeto nodo.
		- (Page 17)
	- -
	- -
		- ¿Cómo se incluye una variable dentro de una plantilla en Chef? #flashcard
		  id:: 2a95c947-8e2b-4d76-9d17-c720a8c56ffd
			- aparece un par de veces la referencia mediante la sintaxis de  expresiones  Ruby  al  atributo  node[:apache][:document_root]  que  habíamos definido en el fichero de atributos, que sigue el formato: <%= expresión %>
		- (Page 18)
	- -
	- -
		- service 'apache2' do supports :status => true action :nothing end En este recurso indicamos el nombre del servicio, en nuestro caso, 'apache2', y como argumentos estamos proporcionando supports para indicar que el estado del servicio se puede determinar mediante la opción status del sistema operativo, y action con el valor :nothing para especificar que no queremos hacer nada cuando Chef lea el recurso, ya que vamos a incluir notificaciones en los recursos que requieren que la configuración se recargue, y en ese momento es cuando el recurso ejecutará la acción que corresponda. #flashcard
		  id:: 805abebf-2065-4ba6-b00b-aeb7fa2b5f9c
		- (Page 19)
	- -
	- -
		- Ejemlo de Servicio en Chef #flashcard
		  id:: 9f1a79fb-e397-41a1-a1f8-fdefeaaa8876
			- p
		- (Page 19)
	- -
	- -
		- Ejemplo de Chef que llama a otro resource #flashcard
		  id:: 1a297d1d-9d8c-4c78-bef2-b5aaca7c33fb
			- template '/etc/apache2/sites-available/vagrant.conf' do source 'virtual-hosts.conf.erb' notifies :restart, resources(:service => "apache2") link '/etc/apache2/sites-enabled/vagrant.conf' do to '/etc/apache2/sites-available/vagrant.conf' notifies :restart, resources(:service => "apache2") end end Hemos incluido la notificación tanto en el fichero de configuración, como en el enlace que lo apunta, ya que así cualquier cambio en alguno de los dos recursos provocará la  recarga  de  la  configuración  de  Apache
		- (Page 19)
	- -