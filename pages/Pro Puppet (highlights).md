title:: Pro Puppet (highlights)
deck:: [[Other-Books::Pro Puppet]]
author:: [[Spencer Krum, William Van Hevelingen, Ben Kero, James Turnbull y Jeffrey McCune]]
full-title:: "Pro Puppet"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/51wVGUlFdzL._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- This book looks at how you can use Puppet to manage your configuration. #flashcard
		  id:: baa91108-c59d-4e81-8d83-920bba186349
		- ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
	- -
	- -
		- ¿Qué es Puppet? #flashcard
		  id:: baec5112-28e4-4b11-b64a-d4f81bf319d3
			- Puppet is an open source framework and toolset for managing the configuration of computer systems.
		- tags:: [[pink]] [[rosa]]
		- ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
	- -
	- -
		- ¿Qué tipo de arquitectura soporta Puppet? #flashcard
		  id:: 11473c63-3109-4675-ab85-22c2f71397d6
			- Puppet is Ruby-based configuration management software, licensed as Apache 2.0, and it can run in either client-server or stand-alone mode.
		- tags:: [[blue]] [[azul]]
		- ([Location 690](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=690))
	- -
	- -
		- ¿Puppet es open-source o privativo? #flashcard
		  id:: c30198c2-7b7f-4d48-bd51-3b2c7000edad
			- Puppet has two versions available: the open source version and the Enterprise version.
		- tags:: [[blue]] [[azul]]
		- ([Location 694](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=694))
	- -
	- -
		- ¿Qué tipos de SO soporta Puppet? #flashcard
		  id:: 0ce8f125-daf7-4888-8aaf-ff1f79390f64
			- Puppet can be used to manage configuration on Unix (including OS X), Linux, and Microsoft Windows platforms.
		- tags:: [[blue]] [[azul]]
		- ([Location 697](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=697))
	- -
	- -
		- ¿Cuáles son las capas de estructura de Puppet? #flashcard
		  id:: 2e8a7125-50a5-4e1a-949d-58ebc63fdfcb
			- three components: Deployment Layer Configuration Language and Resource Abstraction Layer Transactional Layer
		- tags:: [[pink]] [[rosa]]
		- ([Location 701](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=701))
	- -
	- -
		- Deployment #flashcard
		  id:: 3778ed1e-65d9-486f-9ac1-e478e396818f
		- tags:: [[blue]] [[azul]]
		- ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
	- -
	- -
		- ¿Qué es un Puppet Master?
		  id:: 413dc466-7b0b-466b-bc7e-d378e2af3ed3
		  ¿Qué es un Puppet Agent?
		  ¿Qué es un nodo? #flashcard
			- Puppet is usually deployed in a simple client-server model (Figure 1-2). The server is called a Puppet master, the Puppet client software is called an agent, and the host itself is defined as a node.
		- tags:: [[pink]] [[rosa]]
		- ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
	- -
	- -
		- ¿Qué es un Puppet Master? #flashcard
		  id:: 7ad1633a-ddec-4584-a640-23d17e90c684
			- The Puppet master runs as a daemon on a host and contains the configuration required for the specific environment.
		- tags:: [[pink]] [[rosa]]
		- ([Location 707](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=707))
	- -
	- -
		- The Puppet agents connect to the Puppet master through an encrypted and authenticated connection using standard SSL, and retrieve or “pull” any configuration to be applied. #flashcard
		  id:: 92fe1ddf-b807-49d2-ab8a-99126e2e461c
		- tags:: [[pink]] [[rosa]]
		- ([Location 708](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=708))
	- -
	- -
		- Each agent can run Puppet as a daemon, via a mechanism such as cron, or the connection can be manually triggered. #flashcard
		  id:: 40abcc62-09af-4e23-8e7b-fbad562d755a
		- ([Location 713](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=713))
	- -
	- -
		- The usual practice is to run Puppet as a daemon and have it periodically check with the master to confirm that its configuration is up-to-date or to retrieve any new configuration (Figure 1-3). #flashcard
		  id:: 065e0523-c1c9-4d80-b9fb-69ccc46f5508
		- ([Location 714](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=714))
	- -
	- -
		- The Configuration Language and Resource Abstraction Layer #flashcard
		  id:: f8274e44-73fd-4d9a-8852-df95b2594bae
		- tags:: [[blue]] [[azul]]
		- ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
	- -
	- -
		- ¿Qué son los resources en Puppet? #flashcard
		  id:: 42232b03-35d7-485b-b727-21291cc2ec71
			- Puppet uses a declarative language, the Puppet language, to define your configuration items, which Puppet calls resources.
		- tags:: [[pink]] [[rosa]]
		- ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
	- -
	- -
		- The Configuration Language #flashcard
		  id:: 9a00fae7-e6eb-46db-8018-f307a5de3f2f
		- ([Location 730](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=730))
	- -
	- -
		- Estructura de un resource en Puppet. #flashcard
		  id:: 89c278cd-83f6-4e34-9f23-d57eae3457c8
			- Each resource is made up of a type (what sort of resource is being managed: packages, services, or cron jobs), a title (the name of the resource), and a series of attributes (values that specify the state of the resource—for example, whether a service is started or stopped).
		- ([Location 741](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=741))
	- -
	- -
		- The Resource Abstraction Layer #flashcard
		  id:: d2433490-e0b2-4963-b060-dc498e879b4a
		- ([Location 761](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=761))
	- -
	- -
		- ¿Qué es facter? #flashcard
		  id:: e742db7e-6d74-49e6-b92d-233b1639bb3f
			- Facter is a system inventory tool, also developed principally by Puppet Labs,
		- tags:: [[pink]] [[rosa]]
		- ([Location 774](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=774))
	- -
	- -
		- You can see the facts available on your clients by running the facter binary from the command line. #flashcard
		  id:: 48e76ea2-99c9-4001-a2c6-19acc9039374
		- ([Location 778](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=778))
	- -
	- -
		- The Transactional Layer #flashcard
		  id:: ab9c5214-2016-4fd4-8f9e-fd6c448ccadc
		- tags:: [[blue]] [[azul]]
		- ([Location 787](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=787))
	- -
	- -
		- Puppet’s transactional layer is its engine. #flashcard
		  id:: f8f09bde-27eb-463b-9918-a55c68f77791
		- tags:: [[pink]] [[rosa]]
		- ([Location 788](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=788))
	- -
	- -
		- Pasos de la capa Transaccional de Puppet. #flashcard
		  id:: 166d887f-503b-49dc-848a-34c7b071b926
			- steps: Interpret and compile your configuration. Communicate the compiled configuration to the agent. Apply the configuration on the agent. Report the results of that application to the master.
		- tags:: [[blue]] [[azul]]
		- ([Location 789](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=789))
	- -
	- -
		- The first step Puppet takes is to analyze your configuration and calculate how to apply it to your agent. To do this, Puppet creates a graph showing all resources, with their relationships to each other and to each agent. This allows Puppet to work out the order, based on relationships you create, in which to apply each resource to your host. This model is one of Puppet’s most powerful features. #flashcard
		  id:: fe78359b-edce-4aed-8a9f-bd41e5668b0a
		- ([Location 791](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=791))
	- -
	- -
		- Puppet then takes the resources and compiles them into a catalog for each agent. The catalog is sent to the host and applied by the Puppet agent. The results of this application are then sent back to the master in the form of a report. #flashcard
		  id:: eb07e21b-df70-4944-95a9-5d97516f950b
		- ([Location 794](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=794))
	- -
	- -
		- idempotency, #flashcard
		  id:: 0206d3fb-63d8-454a-99e3-238b24193ba2
		- tags:: [[pink]] [[rosa]]
		- ([Location 796](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=796))
	- -
	- -
		- you can’t roll back transactions as you can with some databases. You can, however, model transactions in a “noop,” or no-operation mode, that allows you to test the execution of your changes without applying them. #flashcard
		  id:: 4e10d26e-6da7-4713-a4fb-9a246ff7510e
		- tags:: [[blue]] [[azul]]
		- ([Location 799](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=799))
	- -
	- -
		- ¿En qué fichero está la configuración principal del Puppet Master? #flashcard
		  id:: b67e890d-e96f-4cca-ac21-d6f93f1d30e9
			- Puppet’s configuration will be located under the /etc/puppet directory. Puppet’s principal configuration file is called puppet.conf and is stored at /etc/puppet/puppet.conf
		- tags:: [[pink]] [[rosa]]
		- ([Location 1027](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1027))
	- -
	- -
		- The puppet.conf configuration file is constructed much like an INI-style configuration file and divided into sections. Each section configures a particular element of Puppet. For example, the [agent] section configures the Puppet agent, and the [master] section configures the Puppet master binary. There is also a global configuration section called [main]. All components of Puppet set options specified in the [main] section. #flashcard
		  id:: 40a3396c-45ac-45c5-964e-41d2ba37ac8f
		- tags:: [[blue]] [[azul]]
		- ([Location 1036](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1036))
	- -
	- -
		- [main] server=puppet.example.com Replace puppet.example.com with the fully qualified domain name of your host. #flashcard
		  id:: 24998f5e-17e1-48a8-a8be-aa1fc1b2323e
		- tags:: [[orange]] [[naranja]]
		- ([Location 1043](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1043))
	- -
	- -
		- The site.pp file tells Puppet where and what configuration to load for our clients. We’re going to store this file in a directory called manifests under the /etc/puppet directory. #flashcard
		  id:: b2fc6514-d501-41dd-aded-7f1ffe9aa126
		- tags:: [[pink]] [[rosa]]
		- ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
	- -
	- -
		- ¿Qué es el site.pp? #flashcard
		  id:: 7bdc8108-8fd2-4b5d-90eb-3a4667c27369
			- The site.pp File
		- tags:: [[pink]] [[rosa]]
		- ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
	- -
	- -
		- ¿Qué es un manifest en Puppet? #flashcard
		  id:: a3e04fbe-053d-4be0-8639-0997c2e0ff2a
			- Manifest is Puppet’s term for files containing configuration information. Manifest files have a suffix of .pp. The Puppet language is written into these files.
		- tags:: [[pink]] [[rosa]]
		- ([Location 1055](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1055))
	- -
	- -
		- Output from the daemon can be seen in /var/log/messages on Red Hat–based hosts #flashcard
		  id:: c2f953f6-b68c-4e51-913a-59d681732bca
		- ([Location 1079](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1079))
	- -
	- -
		- By default, the Puppet client runs as a daemon, and the puppet agent command forks off the Puppet daemon into the background and exits immediately. #flashcard
		  id:: 0defb040-3c61-4caf-ad34-262afa937f5f
		- ([Location 1134](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1134))
	- -
	- -
		- puppet# puppet cert list #flashcard
		  id:: 80478ea5-699f-4de4-9b60-fe987ca1bad0
		- tags:: [[orange]] [[naranja]]
		- ([Location 1146](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1146))
	- -
	- -
		- puppet# puppet cert sign node1.pro-puppet.com #flashcard
		  id:: fc62c7bd-65f9-414a-a68d-12cf60fbee5f
		- tags:: [[orange]] [[naranja]]
		- ([Location 1153](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1153))
	- -
	- -
		- puppet cert sign --all #flashcard
		  id:: c6cecdc9-f103-47ff-a306-2b3ad5f766d2
		- tags:: [[orange]] [[naranja]]
		- ([Location 1159](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1159))
	- -
	- -
		- concept of a “module,” which is a portable collection of manifests that contain resources, classes, definitions, files, and templates. #flashcard
		  id:: fe1c3fe3-18a1-48a8-a168-53d7b640d8e2
		- tags:: [[pink]] [[rosa]]
		- ([Location 1191](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1191))
	- -
	- -
		- Adding a Node Definition #flashcard
		  id:: 83c838d1-0a62-4f1d-b4fa-5f0e123ae151
		- ([Location 1193](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1193))
	- -
	- -
		- ¿Cómo definimos un nodo en site.pp? #flashcard
		  id:: 36e60f56-69af-4e31-99e1-a9da33b49f45
			- For a node definition we specify the node name, enclosed in single quotes, and then specify the configuration that applies to it inside curly braces { }.
		- tags:: [[pink]] [[rosa]]
		- ([Location 1199](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1199))
	- -
	- -
		- Definición mejorada de un nodo en site.pp #flashcard
		  id:: eb6ffc12-3b9d-4fd9-b9f9-21e56a632f99
			- Here we specify an include directive in our node definition; it specifies a collection of configurations, called a class, that we want to apply to our host.
		- tags:: [[pink]] [[rosa]]
		- ([Location 1219](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1219))
	- -
	- -
		- There are two ways to include a class: node /node1/ {   include ::sudo } node /node2/ {   class { '::sudo':      users => ['tom', 'jerry'],   } } #flashcard
		  id:: c97325f3-ef60-41eb-bc02-0a358c2127b0
		- tags:: [[blue]] [[azul]]
		- ([Location 1221](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1221))
	- -
	- -
		- Clases parametrizadas #flashcard
		  id:: e8218188-bd01-48c3-9aa9-2b7e0d4dcb2c
			- The first syntax is bare and simple. The second syntax allows parameters to be passed into the class. This feature, generally called parameterized classes, allows classes to be written generally and then utilized specifically, increasing the reusability of Puppet code.
		- tags:: [[pink]] [[rosa]]
		- ([Location 1224](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1224))
	- -
	- -
		- The double-colon syntax explicitly instructs Puppet to use top scope to look up #flashcard
		  id:: bd79d53d-336b-44e1-b945-b85393896536
		- tags:: [[blue]] [[azul]]
		- ([Location 1229](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1229))
	- -
	- -
		- A single module would contain everything required to configure a particular application. #flashcard
		  id:: 450e0647-e404-419d-9edf-059e475c98f2
		- tags:: [[blue]] [[azul]]
		- ([Location 1236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1236))
	- -
	- -
		- Each module needs a specific directory structure and a file called init.pp. This structure allows Puppet to automatically load modules. #flashcard
		  id:: 112d0b28-db2e-47ee-8cb0-25ab5c7dddf8
		- ([Location 1239](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1239))
	- -
	- -
		- module path. #flashcard
		  id:: 26957c01-14fd-492f-8226-b8977d4ccce3
		- tags:: [[blue]] [[azul]]
		- ([Location 1241](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1241))
	- -
	- -
		- [master] modulepath = /etc/puppet/modules:/var/lib/puppet/modules:/opt/modules #flashcard
		  id:: fec8d7dc-4e38-4d66-842e-2ed999521d69
		- tags:: [[orange]] [[naranja]]
		- ([Location 1244](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1244))
	- -
	- -
		- Module structure # mkdir –p /etc/puppet/modules/sudo/{files,templates,manifests} # touch /etc/puppet/modules/sudo/manifests/init.pp #flashcard
		  id:: 40fcb8bd-5c9c-4311-bdb8-44aef110b2e8
		- tags:: [[orange]] [[naranja]]
		- ([Location 1248](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1248))
	- -
	- -
		- The manifests directory will hold our init.pp file and any other configuration. #flashcard
		  id:: 6838daff-70b8-40e6-aa03-d8126b865815
		- tags:: [[blue]] [[azul]]
		- ([Location 1250](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1250))
	- -
	- -
		- The init.pp file is the core of your module, and every module should have one. #flashcard
		  id:: 1ccbadf7-fe10-44bf-80ab-c9e644d4bdae
		- tags:: [[blue]] [[azul]]
		- ([Location 1251](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1251))
	- -
	- -
		- The files directory will hold any files we wish to serve as part of our module. #flashcard
		  id:: 640a264b-cf0b-441c-8b58-d4f954f7cadf
		- tags:: [[blue]] [[azul]]
		- ([Location 1252](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1252))
	- -
	- -
		- The init.pp file #flashcard
		  id:: 7ed3a1b4-a736-4f1d-ba44-4d92b20ecc96
		- ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
	- -
	- -
		- The templates directory will contain any templates that our module might use. #flashcard
		  id:: e23a21e8-3f4f-4610-9747-a48561b2b6f5
		- tags:: [[blue]] [[azul]]
		- ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
	- -
	- -
		- more details of Puppet’s conditional syntaxes #flashcard
		  id:: 1179a7e2-021d-4a84-af7c-d686dbbe93e7
		- ([Location 1270](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1270))
	- -
	- -
		- The == comparison operator is case-insensitive. To perform a case-sensitive comparison for strings, you must use the regular expression operator =∼ and you must fully root the regular expression; for example, $osfamily =∼ /^Debian$/. #flashcard
		  id:: 6d0654bb-c9aa-456a-9a5a-413301069d2e
		- ([Location 1273](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1273))
	- -
	- -
		- Operating system family is just a name Puppet uses for binary-compatible groups of distributions; for example, Debian, Ubuntu, and Mint all share the osfamily Debian. #flashcard
		  id:: 85ae528e-9b91-4e5c-83b8-ab00bb9ba2f3
		- ([Location 1277](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1277))
	- -
	- -
		- For example, if a file resource changes, you can tell Puppet to restart a service resource. #flashcard
		  id:: 2c84c1c0-d5d6-4d71-ae0c-49e21d6f4799
		- ([Location 1294](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1294))
	- -
	- -
		- puppet://$::server/modules/sudo/etc/sudoers #flashcard
		  id:: eea802f1-52f9-48a6-954b-41b9cdbd0f96
		- tags:: [[orange]] [[naranja]]
		- ([Location 1305](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1305))
	- -
	- -
		- puppet:// part specifies that Puppet will use the Puppet file server protocol to retrieve the file. #flashcard
		  id:: bfadd294-5bd4-4064-92d8-6fac3e1baf50
		- tags:: [[blue]] [[azul]]
		- ([Location 1306](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1306))
	- -
	- -
		- The $::server variable contains the hostname of our Puppet server. #flashcard
		  id:: af72b9b6-b20b-4880-b490-d8e3e34a3fa6
		- tags:: [[blue]] [[azul]]
		- ([Location 1309](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1309))
	- -
	- -
		- puppet:///modules/sudo/etc/sudoers. #flashcard
		  id:: e665ee19-ecdd-41d9-a306-bdf87bd3af11
		- tags:: [[orange]] [[naranja]]
		- ([Location 1312](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1312))
	- -
	- -
		- In Puppet, the combined configuration to be applied to a host is called a catalog, and the process of applying it is called a run. You can find a glossary of Puppet terminology at http://docs.puppetlabs.com/references/glossary.html . #flashcard
		  id:: 90373dac-364a-4a6c-9fa3-42d2072d07d0
		- ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1351))
	- -
	- -
		- we see that the agent has cached the configuration for the host. By default, will Puppet use this cache if it fails to connect to the master during a future run. #flashcard
		  id:: 2f6866fc-fdf9-4801-bc82-e25a40dbf872
		- tags:: [[blue]] [[azul]]
		- ([Location 1355](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1355))
	- -
	- -
		- puppet# puppet master --no-daemonize --verbose --debug #flashcard
		  id:: e9b325b8-22cc-4c9b-8e50-c29dd2e2f3ef
		- tags:: [[orange]] [[naranja]]
		- ([Location 1364](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1364))
	- -
	- -
		- Resources #flashcard
		  id:: b0656751-bbd4-4f7a-b20c-ff259febab7d
		- ([Location 1386](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1386))
	- -
	- -
		- the Puppet client software is called the agent. #flashcard
		  id:: b00bea64-1dc7-49df-91bd-4fa7fa25b204
		- ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
	- -
	- -
		- Puppet calls the definition of the host itself a node. #flashcard
		  id:: a9775365-e831-40a5-925a-c740c83fadde
		- ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
	- -
	- -
		- Puppet supports inheritance at the node level, but it is no longer considered best practice. #flashcard
		  id:: 709fba4e-e744-463c-95cc-5b495897b534
		- ([Location 1511](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1511))
	- -
	- -
		- Node inheritance node basenode {     include  sudo     include  mailx } node   ' web.example.com '   inherits basenode {     include apache } #flashcard
		  id:: ccae5479-99e2-4d86-a029-0dbdcf102fc4
		- tags:: [[orange]] [[naranja]]
		- ([Location 1516](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1516))
	- -
	- -
		- A better solution is to use parameterized classes and one glue class to define high-level behaviors at node level. #flashcard
		  id:: 72456244-8134-46cf-84fa-a89f5c306282
		- ([Location 1526](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1526))
	- -
	- -
		- err: Cannot reassign variable location at /etc/puppet/manifests/node.pp:4 #flashcard
		  id:: 59292d59-1695-4cb5-aa74-5852ba927606
		- tags:: [[orange]] [[naranja]]
		- ([Location 1540](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1540))
	- -
	- -
		- Why does this happen? Puppet is a declarative language. Allowing variable reassignment would require us to rely on order in the file to determine the value of the variable, and order does not matter in a declarative language. #flashcard
		  id:: ec741cf0-8fcb-4dee-8d51-fffd64ea30a0
		- ([Location 1541](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1541))
	- -
	- -
		- you cannot redefine a variable inside the same scope it was defined in, like our node. #flashcard
		  id:: f45790eb-2b90-4eb4-891d-f5808f015ad1
		- tags:: [[pink]] [[rosa]]
		- ([Location 1543](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1543))
	- -
	- -
		- At any given time, four scopes are available to Puppet: top scope, node scope, parent scope, and local scope. #flashcard
		  id:: 540a4f60-1f1d-48f0-8024-07b05801a58b
		- tags:: [[pink]] [[rosa]]
		- ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
	- -
	- -
		- Top scope is anything declared in site.pp or imported manifests. #flashcard
		  id:: c43c11ff-21a4-4064-9915-c37978821d47
		- tags:: [[pink]] [[rosa]]
		- ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
	- -
	- -
		- Local scope is the scope of a single class or defined type. #flashcard
		  id:: d6335272-1da9-4304-bc44-781417610a67
		- tags:: [[pink]] [[rosa]]
		- ([Location 1550](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1550))
	- -
	- -
		- class ssh (   manage_package = false,   manage_service = false,   package_name   = $::ssh::params::sshd_package ) inherits ssh::params  {   if manage_package == true {     package { $package_name:       ensure => installed,     }   } #flashcard
		  id:: ac2abbed-2926-4071-bc62-30fb9ac4b9dc
		- tags:: [[orange]] [[naranja]]
		- ([Location 1585](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1585))
	- -
	- -
		- to enforce the style guide. It is called puppet-lint #flashcard
		  id:: 4ff49657-9e65-4bbd-a55a-b6163998a600
		- ([Location 1615](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1615))
	- -
	- -
		- node ' puppet.example.com ' {   include sudo } #flashcard
		  id:: 620c8d8b-2de7-4a61-92c7-9431f7d48f17
		- tags:: [[orange]] [[naranja]]
		- ([Location 1642](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1642))
	- -
	- -
		- You can generate a blank puppet module using the syntax puppet module generate name-name, where the first name is the name of you or your organization, and the second is the name of the service you are managing, such as propuppet-amanda #flashcard
		  id:: cd3ef5a2-8eda-4fc0-a7d5-f408093f17c2
		- ([Location 1653](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1653))
	- -
	- -
		- class ssh::install {   $package_name = $::osfamily  ?     'RedHat'  => "openssh-server",     'Debian'  => "openssh-server",     'Solaris' => "openssh",     },   package { 'ssh':     ensure => present,     name   => $package_name,   } } #flashcard
		  id:: 6140fcb1-d17d-4de0-8d98-9b67f687ca4e
		- tags:: [[orange]] [[naranja]]
		- ([Location 1779](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1779))
	- -
	- -
		- Selector matching is case-insensitive. #flashcard
		  id:: 0b62e57a-a4c1-4398-bc6d-47f3208ccd63
		- ([Location 1808](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1808))
	- -
	- -
		- a best practice we recommend that you move all your conditional checks to a separate class. #flashcard
		  id:: 17741aa7-d2c6-4291-b488-756472c2fb53
		- ([Location 1825](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1825))
	- -
	- -
		- case $::osfamily {     Solaris: {       $ssh_package_name = 'cswopenssh'       $ssh_service_config = '/etc/opt/csw/ssh/sshd_config'     }     Debian: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     RedHat: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     default: {       fail("Module propuppet-ssh does not support osfamily: ${::osfamily}")     }   } #flashcard
		  id:: cc8010fb-021d-4f68-82fd-15a806e464f7
		- tags:: [[orange]] [[naranja]]
		- ([Location 1890](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1890))
	- -
	- -
		- It is a best practice to establish relationships with an entire class, rather than with a resource contained within another class, because this allows the internal structure of the class to change without refactoring the resource declarations related to the class. #flashcard
		  id:: 8d4b8d3b-2e30-44f7-bda7-ea2caccd6310
		- ([Location 1908](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1908))
	- -
	- -
		- the require metaparameter tells Puppet that all the resources in the specified class must be processed prior to the current resource. #flashcard
		  id:: 1539d26f-8de7-486c-b3b1-bd39c50cc268
		- tags:: [[blue]] [[azul]]
		- ([Location 1910](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1910))
	- -
	- -
		- The notify metaparameter creates a notification relationship. If the current resource (the service’s configuration file) is changed, then Puppet should notify all the resources contained in the ssh::service class. In our current case, a “notification” will cause the service resources in the ssh::service class to restart, ensuring that if we change a configuration file, the service will be restarted and running with the correct, updated configuration. #flashcard
		  id:: 021da050-2121-4ecf-9ca6-93a3cddb9ea6
		- tags:: [[blue]] [[azul]]
		- ([Location 1912](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1912))
	- -
	- -
		- class ssh::service {   include ssh::params   service { $::ssh::params::ssh_service_name:     ensure      => running,     hasstatus   => true,     hasresstart => true,     enable      => true,     require     => Class['ssh::config'],   } } #flashcard
		  id:: df5d5826-32e6-4527-a01a-9a650840ab03
		- tags:: [[orange]] [[naranja]]
		- ([Location 1944](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1944))
	- -
	- -
		- File {     owner => 'postfix',     group => 'postfix',     mode  => 0644,   } #flashcard
		  id:: 2a04b7ed-140e-4098-955a-5d95d32b754d
		- tags:: [[orange]] [[naranja]]
		- ([Location 2011](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2011))
	- -
	- -
		- we specified the File resource type capitalized and without a title. This syntax is called a resource default, and it allows us to specify defaults for a particular resource type. #flashcard
		  id:: d0b35093-2fe6-4401-aec0-b954a5287423
		- tags:: [[blue]] [[azul]]
		- ([Location 2021](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2021))
	- -
	- -
		- class ssh { require ssh::params include ssh::install include ssh::config include ssh::service } #flashcard
		  id:: 297080a3-3b98-479e-b462-63cc06feaf41
		- tags:: [[orange]] [[naranja]]
		- ([Location 2047](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2047))
	- -
	- -
		- check the syntax of your ERB templates #flashcard
		  id:: 98e81332-e517-4abd-aabd-d700ea78ca7a
		- ([Location 2074](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2074))
	- -
	- -
		- Our first class is our mysql class, contained in the init.pp file, where we load all the required classes for this module: class mysql (   $group                   = 'mysql',   $service_enabled  = true,   $service_running  = true,   $user                     = 'mysql' ){   class { 'mysql::install':     user  => $user,     group => $group,   }   class { 'mysql::config':     user  => $user,     group => $group,   }   class { 'mysql::service':     ensure  => $service_running,     enabled => $service_enabled,   } } #flashcard
		  id:: 88a04156-fad7-40bd-93e4-77f2865be487
		- tags:: [[orange]] [[naranja]]
		- ([Location 2106](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2106))
	- -
	- -
		- class mysql::install (   $user,   $group ){ #flashcard
		  id:: 518fcfe4-67c9-446a-980f-9f4fdffa9a31
		- tags:: [[orange]] [[naranja]]
		- ([Location 2127](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2127))
	- -
	- -
		- Definitions are collections of resources like classes, but unlike classes they can be specified and are evaluated multiple times on a host. They also accept parameters. #flashcard
		  id:: 717ba6d0-670c-4b82-9dc7-e6ba9215a066
		- tags:: [[pink]] [[rosa]]
		- ([Location 2232](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2232))
	- -
	- -
		- Tip Remember that classes are singletons. They can be included multiple times on a node, but they will only be evaluated ONCE. A definition, because it takes parameters, can be declared multiple times, and each new declaration will be evaluated. #flashcard
		  id:: 80b4a5df-6c4b-4ee1-87af-8ee84e61d1e5
		- tags:: [[pink]] [[rosa]]
		- ([Location 2233](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2233))
	- -
	- -
		- The first definition define apache::vhost(   $docroot,   $port,   $priority,   $ssl=true,   $serveraliases = '',   $template='apache/vhost.conf.erb', ){   include apache   file {"/etc/apache2/sites-enabled/${priority}-${name}":     content => template($template),     owner   => 'root',     group   => 'root',     mode    => '0640',     require => Class['apache::install'],     notify  => Class['apache::service'],   } } #flashcard
		  id:: 76fbaef6-6431-4946-a600-f30ab343085f
		- tags:: [[orange]] [[naranja]]
		- ([Location 2236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2236))
	- -
	- -
		- The $name variable contains the name, also known as the title, of a declared defined resource. This is the value of the string before the colon when declaring the defined resource. The $title variable, which usually has the same value, is also available. #flashcard
		  id:: a55c5ae5-7fa0-4b49-81b5-a9426f0c4ad3
		- ([Location 2258](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2258))
	- -
	- -
		- Putting the $name variable as part of the name of the exec resource will solve this problem. #flashcard
		  id:: 43883389-7879-4461-abc6-2b9a7328c2b0
		- ([Location 2265](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2265))
	- -
	- -
		- autoloading. Puppet scans your module and loads any .pp file in the manifests directory that is named after the class it contains; for example, the install.pp file contains the apache::install class and so is autoloaded. The same thing happens with definitions: #flashcard
		  id:: c296ed6a-dbaf-49f9-a24f-8829d5be39f6
		- tags:: [[pink]] [[rosa]]
		- ([Location 2319](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2319))
	- -