title:: Herramientas de Automatización de Despliegues Tema-3 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-3"
category:: #books

tags:: #[[Herramientas-de-Automatización-de-Despliegues]] #[[UNI]]

- #tags #[[Herramientas-de-Automatización-de-Despliegues]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/a882e1b4-ff60-4055-aa60-4ccd886b01ce.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- ¿Qué es un framework? +++ #car
	  id:: 63401516-bc51-446a-b865-16222c2b1f37
		- En el proceso de maduración del desarrollo de software han surgido los denominados marcos de trabajo, más conocidos por su nombre en inglés: frameworks. Su objetivo principal es el de simplificar y reducir el tiempo de desarrollo, permitiendo a los desarrolladores centrarse en aportar valor a la compañía e innovar.
		- (Page 4)
	- -
	- -
	- Nombra las tres partes de que se compone Chef: #car
	  id:: 63401516-3de0-43ed-9b27-af7b76a90f1b
		- El framework Chef está compuesto por tres componentes básicos que interactúan entre sí:
		- (Page 5)
	- -
	- -
	- ¿Qué hace el Servidor Chef? #car
		- El servidor Chef constituye el centro de los datos de configuración, que contiene los cookbooks,  que  son  los  módulos  de  configuración  de  recursos, las  políticas que se aplicarán a los diferentes nodos, y los metadatos, que describen cada uno de los nodos administrados por Chef.
		- (Page 5)
	- -
	- -
	- CONTINUE #car
		- desarrolladores  poder  centrarse  en  el  desarrollo  específico  que  cumpla  con  los requisitos  necesarios,  sin  tener  que  preocuparse  de  elementos  y  servicios  de  uso común  que  son  proporcionados  por  el  framework,  y  lograr  así  una  entrega  más rápida. Estos frameworks de software suelen ofrecernos además un conjunto común de convenciones, procedimientos y servicios que tienen como objetivo fomentar que el equipo desarrolle de forma homogénea, facilitando así el desarrollo sostenible del proyecto.
		- (Page 5)
	- -
	- -
	- ¿Cómo se comunican los nodos de Chef con el server? #car
	  id:: 63401516-7ef4-4d54-939a-4a0ddf3c258e
		- Los nodos usan la herramienta Chef Client para conectarse con el Chef Server y solicitar los detalles de configuración que deben aplicarse sobre la máquina donde se ejecutan. A este proceso de aplicar los cambios sobre los nodos se le denomina *Chef run*.
		- (Page 6)
	- -
	- -
	- Define Chef Server #car
	  id:: 63401516-4ddf-466c-89aa-b7af98d8b881
		-   Chef  Server:  servidor  centralizado  que  contiene  y  gestiona  la  configuración  de todos  los  nodos.  Puede  estar  ubicado  en  un  servidor  independiente  o  alojado como servicio en la nube en Chef.
		- (Page 7)
	- -
	- -
	- Define nodo en Chef #car
	  id:: 63401516-8750-4679-bee6-da0746a9fa51
		-   Nodo: incluye la información relativa a las recetas y roles que deben aplicarse en la máquina durante la ejecución de Chef Client. Los atributos y la lista de ejecución del nodo son sus principales características.
		- (Page 7)
	- -
	- -
	- Define Cookbook en Chef #car
		-   Cookbook:  contiene  todos  los  recursos  e  instrucciones  que  se  necesitan  para configurar  nodos,  y  pueden  ser  reutilizados  en  varias  listas  de  ejecución.  Los cookbooks se componen habitualmente de varias recetas.
		- (Page 7)
	- -
	- -
	- Define Receta (Recipe) en Chef #car
	  id:: 63401516-40c6-478b-8fb7-e13be9f1c635
		-   Recipes (recetas): consiste en un conjunto de recursos que configuran un nodo, y es una de las partes fundamentales de Chef.
		- (Page 7)
	- -
	- -
	- Define recurso en Chef #car
	  id:: 63401516-a646-4518-9921-4e7360c4f363
		-   Recursos:  son  una  abstracción  multiplataforma  de  partes  configurables  de  un nodo, como pueden ser usuarios, paquetes, archivos o directorios.
		- (Page 7)
	- -
	- -
	- Define Chef Client #car
		-   Chef Client (Cliente Chef): realiza el trabajo necesario en nombre del nodo, donde ejecuta las recetas correspondientes para configurar e instalar el software.
		- (Page 7)
	- -
	- -
	- Define 'Chef Solo' #car
	  id:: 63401516-d456-4b9f-805a-7390e64acd07
		-   Chef  Solo:  herramienta  de  línea  de  comandos  que  permite  ejecutar  cookbooks Chef independientemente, sin conectarse a un servidor Chef. Es una versión de código abierto del Chef Client.
		- (Page 8)
	- -
	- -
	- ¿Qué es Knife en Chef? #car
	  id:: 63401516-20c1-4295-be60-4271af0fd871
		-   Knife (cuchillo): herramienta de línea de comandos que utilizan los usuarios para cargar los ficheros de configuración en el servidor Chef.
		- (Page 8)
	- -
	- -
	- Ejemplo de Vagrantfile para Chef #car
	  id:: 63401516-0a6a-4820-9c41-1054492552b7
		- config.vm.provision :chef_solo do |chef| chef.cookbooks_path = "chef-repo/cookbooks" chef.add_recipe "chef_apache" chef.arguments = "--chef-license accept" end
		- (Page 12)
	- -
	- -
	- Ejemplo completo de Vagrantfile con Chef #car
	  id:: 63401516-4a2c-4e97-8ce9-14e8708e80a2
		- Vagrant.configure("2") do |config| config.vm.box = "ubuntu/bionic64" config.vm.network "private_network", ip: "192.168.33.40" config.vm.provider "virtualbox" do |vb| vb.memory = "1024" config.vm.provision :chef_solo do |chef| chef.cookbooks_path = "chef-repo/cookbooks" chef.add_recipe "chef_apache" chef.arguments = "--chef-license accept" end end end
		- (Page 12)
	- -
	- -
	- ¿Cómo podemos generar la estructura de nuestro cookbook? #car
		- Una  vez  creado  el  directorio  de  cookbooks,  para  generar  nuestro  cookbook utilizaremos  el  comando  chef  correspondiente,  que  creará  toda  la  estructura  de directorios y ficheros que se requiere. chef generate cookbook apache
		- (Page 13)
	- -
	- -
	- INCLUIR IMAGEN #car
	  id:: 63401516-9448-46ec-b2d4-e1ee1217eace
		- En esta estructura se pueden encontrar varios ficheros que se generan por defecto y que nos sirven de plantilla o versión inicial para incorporar funcionalidad a nuestro cookbook.  El  fichero  principal  donde  se  especifica  la  configuración  a  obtener  es  la receta por defecto, ubicado en: recipes/default.rb, al que vamos a incluir el primer apt_update 'Update the apt cache daily' do fragmento de código: end frequency 86400 action :periodic package 'apache2'
		- (Page 14)
	- -
	- -
	- Ejemplo de código en Chef #car
		- file '/etc/apache2/sites-enabled/000-default.conf' do action :delete template '/etc/apache2/sites-available/vagrant.conf' do source 'virtual-hosts.conf.erb' link '/etc/apache2/sites-enabled/vagrant.conf' do to '/etc/apache2/sites-available/vagrant.conf' cookbook_file “/vagrant/index.html" do source 'index.html' only_if do File.exist?('/etc/apache2/sites-enabled/vagrant.conf') end end end end end
		- (Page 15)
	- -
	- -
	- ¿Cómo se interpola una variable en Chef? #car
	  id:: 63401516-c0b7-4300-b795-8c9904341416
		- cookbook_file “#{node['apache']['document_root']}/index.html" do File.exist?('/etc/apache2/sites-enabled/vagrant.conf') source 'index.html' only_if do end end Tal como se muestra, la referencia al atributo se hace con el símbolo de la almohadilla (#) y, entre llaves ({}), el nombre del atributo dentro del objeto nodo.
		- (Page 17)
	- -
	- -
	- ¿Cómo se incluye una variable dentro de una plantilla en Chef? #car
	  id:: 63401516-7da3-4423-992c-f8ee7b444e1a
		- aparece un par de veces la referencia mediante la sintaxis de  expresiones  Ruby  al  atributo  node[:apache][:document_root]  que  habíamos definido en el fichero de atributos, que sigue el formato: <%= expresión %>
		- (Page 18)
	- -
	- -
	- service 'apache2' do supports :status => true action :nothing end En este recurso indicamos el nombre del servicio, en nuestro caso, 'apache2', y como argumentos estamos proporcionando supports para indicar que el estado del servicio se puede determinar mediante la opción status del sistema operativo, y action con el valor :nothing para especificar que no queremos hacer nada cuando Chef lea el recurso, ya que vamos a incluir notificaciones en los recursos que requieren que la configuración se recargue, y en ese momento es cuando el recurso ejecutará la acción que corresponda. #ñspace
		- (Page 19)
	- -
	- -
	- Ejemlo de Servicio en Chef #car
		- p
		- (Page 19)
	- -
	- -
	- Ejemplo de Chef que llama a otro resource #car
	  id:: 63401516-0888-4d90-a204-5b1e314a4a3a
		- template '/etc/apache2/sites-available/vagrant.conf' do source 'virtual-hosts.conf.erb' notifies :restart, resources(:service => "apache2") link '/etc/apache2/sites-enabled/vagrant.conf' do to '/etc/apache2/sites-available/vagrant.conf' notifies :restart, resources(:service => "apache2") end end Hemos incluido la notificación tanto en el fichero de configuración, como en el enlace que lo apunta, ya que así cualquier cambio en alguno de los dos recursos provocará la  recarga  de  la  configuración  de  Apache
		- (Page 19)
	- -