# Pro Puppet

deck:: [[Other-Books::Pro Puppet]]\
author:: [[Spencer Krum, William Van Hevelingen, Ben Kero, James Turnbull y Jeffrey McCune]]\
full-title:: "Pro Puppet"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/51wVGUlFdzL._SL200_.jpg)
## Highlights
- This book looks at how you can use Puppet to manage your configuration. #flashcard 
  id:: 63cfbcda-9f4c-46cb-a68a-f24e0fb42f19
  
  
    ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
-
- ¿Qué es Puppet? #flashcard  #pink #rosa 
  id:: 63cfbcda-0694-4b21-aa86-9023a6c7d2db
    Puppet is an open source framework and toolset for managing the configuration of computer systems.
  
    ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
-
- ¿Qué tipo de arquitectura soporta Puppet? #flashcard  #blue #azul 
  id:: 63cfbcda-c18e-44d5-8ef2-f2229a9f537e
    Puppet is Ruby-based configuration management software, licensed as Apache 2.0, and it can run in either client-server or stand-alone mode.
  
    ([Location 690](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=690))
-
- ¿Puppet es open-source o privativo? #flashcard  #blue #azul 
  id:: 63cfbcda-2659-4a22-be43-aab86606ca54
    Puppet has two versions available: the open source version and the Enterprise version.
  
    ([Location 694](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=694))
-
- id:: 63c66a1a-dbcc-4bc5-bd41-2b9ec1339d09
   ¿Qué tipos de SO soporta Puppet? #flashcard  #blue #azul 
    Puppet can be used to manage configuration on Unix (including OS X), Linux, and Microsoft Windows platforms.
  
    ([Location 697](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=697))
-
- id:: 63c66a1a-69f1-49cc-a207-d596d9b4da5b
   ¿Cuáles son las capas de estructura de Puppet? #flashcard  #pink #rosa 
    three components: Deployment Layer Configuration Language and Resource Abstraction Layer Transactional Layer
  
    ([Location 701](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=701))
-
- Deployment #flashcard  #blue #azul 
  id:: 63cfbcda-8ed0-450a-8870-057283ca9e08
  
  
    ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
-
- ¿Qué es un Puppet Master?
  id:: 63cfbcda-4468-4ea3-97f2-6a9e254a71ec
   ¿Qué es un Puppet Agent?
   ¿Qué es un nodo? #flashcard  #pink #rosa 
    Puppet is usually deployed in a simple client-server model (Figure 1-2). The server is called a Puppet master, the Puppet client software is called an agent, and the host itself is defined as a node.
  
    ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
-
- ¿Qué es un Puppet Master? #flashcard  #pink #rosa 
  id:: 63cfbcda-e23f-4dee-a060-caf4144fceeb
    The Puppet master runs as a daemon on a host and contains the configuration required for the specific environment.
  
    ([Location 707](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=707))
-
- id:: 63c66a1a-e8ee-404d-9c0a-2a03f28b32ae
  
  The Puppet agents connect to the Puppet master through an encrypted and authenticated connection using standard SSL, and retrieve or “pull” any configuration to be applied. #flashcard  #pink #rosa 
  
  
    ([Location 708](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=708))
-
- id:: 63c66a1a-f7f1-445d-b66d-923562922605
  
  Each agent can run Puppet as a daemon, via a mechanism such as cron, or the connection can be manually triggered. #flashcard 
  
  
    ([Location 713](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=713))
-
- id:: 63c66a1a-cb70-417d-ad34-4ba971631acf
  
  The usual practice is to run Puppet as a daemon and have it periodically check with the master to confirm that its configuration is up-to-date or to retrieve any new configuration (Figure 1-3). #flashcard 
  
  
    ([Location 714](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=714))
-
- The Configuration Language and Resource Abstraction Layer #flashcard  #blue #azul 
  id:: 63cfbcda-6f7a-4a8d-963e-d22f474eca9d
  
  
    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
-
- id:: 63c66a1a-34a9-47e3-be6b-9632c0bd506f
   ¿Qué son los resources en Puppet? #flashcard  #pink #rosa 
    Puppet uses a declarative language, the Puppet language, to define your configuration items, which Puppet calls resources.
  
    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
-
- id:: 63c66a1a-2e42-4f8d-83ed-5d8cfb7d43e5
  
  The Configuration Language #flashcard 
  
  
    ([Location 730](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=730))
-
- Estructura de un resource en Puppet. #flashcard 
  id:: 63cfbcda-a0ee-4ce7-b24a-0aa7d8306e98
    Each resource is made up of a type (what sort of resource is being managed: packages, services, or cron jobs), a title (the name of the resource), and a series of attributes (values that specify the state of the resource—for example, whether a service is started or stopped).
  
    ([Location 741](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=741))
-
- id:: 63c66a1a-5d8f-4991-8b96-355ca1c820b8
  
  The Resource Abstraction Layer #flashcard 
  
  
    ([Location 761](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=761))
-
- id:: 63c66a1a-8a0a-4679-82c8-39217eb09444
   ¿Qué es facter? #flashcard  #pink #rosa 
    Facter is a system inventory tool, also developed principally by Puppet Labs,
  
    ([Location 774](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=774))
-
- id:: 63c66a1a-42ca-4691-adb0-8266361942eb
  
  You can see the facts available on your clients by running the facter binary from the command line. #flashcard 
  
  
    ([Location 778](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=778))
-
- id:: 63c66a1a-9164-4073-a1d1-992223708220
  
  The Transactional Layer #flashcard  #blue #azul 
  
  
    ([Location 787](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=787))
-
- id:: 63c66a1a-0f94-4e40-8a2f-06113456beeb
  
  Puppet’s transactional layer is its engine. #flashcard  #pink #rosa 
  
  
    ([Location 788](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=788))
-
- id:: 63c66a1a-c852-42c9-b931-8ec3688eabad
   Pasos de la capa Transaccional de Puppet. #flashcard  #blue #azul 
    steps: Interpret and compile your configuration. Communicate the compiled configuration to the agent. Apply the configuration on the agent. Report the results of that application to the master.
  
    ([Location 789](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=789))
-
- The first step Puppet takes is to analyze your configuration and calculate how to apply it to your agent. To do this, Puppet creates a graph showing all resources, with their relationships to each other and to each agent. This allows Puppet to work out the order, based on relationships you create, in which to apply each resource to your host. This model is one of Puppet’s most powerful features. #flashcard 
  id:: 63cfbcda-f104-4d53-8575-fb0d88480c61
  
  
    ([Location 791](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=791))
-
- Puppet then takes the resources and compiles them into a catalog for each agent. The catalog is sent to the host and applied by the Puppet agent. The results of this application are then sent back to the master in the form of a report. #flashcard 
  id:: 63cfbcda-614b-44e6-b289-51bd50c41a13
  
  
    ([Location 794](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=794))
-
- id:: 63c66a1a-ada8-4bf7-a5ef-88debacd2112
  
  idempotency, #flashcard  #pink #rosa 
  
  
    ([Location 796](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=796))
-
- you can’t roll back transactions as you can with some databases. You can, however, model transactions in a “noop,” or no-operation mode, that allows you to test the execution of your changes without applying them. #flashcard  #blue #azul 
  id:: 63cfbcda-2f97-4f71-b597-38da5bee9e97
  
  
    ([Location 799](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=799))
-
- ¿En qué fichero está la configuración principal del Puppet Master? #flashcard  #pink #rosa 
  id:: 63cfbcda-5a0d-4985-b768-55b74d3e92a4
    Puppet’s configuration will be located under the /etc/puppet directory. Puppet’s principal configuration file is called puppet.conf and is stored at /etc/puppet/puppet.conf
  
    ([Location 1027](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1027))
-
- id:: 63c66a1a-f8a9-4bef-855c-65b0d95028b5
  
  The puppet.conf configuration file is constructed much like an INI-style configuration file and divided into sections. Each section configures a particular element of Puppet. For example, the [agent] section configures the Puppet agent, and the [master] section configures the Puppet master binary. There is also a global configuration section called [main]. All components of Puppet set options specified in the [main] section. #flashcard  #blue #azul 
  
  
    ([Location 1036](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1036))
-
- id:: 63c66a1a-82d4-410c-acbe-fcc89083937f
  
  [main] server=puppet.example.com Replace puppet.example.com with the fully qualified domain name of your host. #flashcard  #orange #naranja 
  
  
    ([Location 1043](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1043))
-
- id:: 63c66a1a-db59-4616-8403-696ab8294d35
  
  The site.pp file tells Puppet where and what configuration to load for our clients. We’re going to store this file in a directory called manifests under the /etc/puppet directory. #flashcard  #pink #rosa 
  
  
    ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
-
- id:: 63c66a1a-7ac5-4d6b-86e1-31fa6f77b356
   ¿Qué es el site.pp? #flashcard  #pink #rosa 
    The site.pp File
  
    ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
-
- id:: 63c66a1a-d782-40a5-988b-3509dc70be5a
   ¿Qué es un manifest en Puppet? #flashcard  #pink #rosa 
    Manifest is Puppet’s term for files containing configuration information. Manifest files have a suffix of .pp. The Puppet language is written into these files.
  
    ([Location 1055](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1055))
-
- id:: 63c66a1a-1c51-49af-8d97-0892df166292
  
  Output from the daemon can be seen in /var/log/messages on Red Hat–based hosts #flashcard 
  
  
    ([Location 1079](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1079))
-
- id:: 63c66a1a-752e-4275-8117-eadd7683df66
  
  By default, the Puppet client runs as a daemon, and the puppet agent command forks off the Puppet daemon into the background and exits immediately. #flashcard 
  
  
    ([Location 1134](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1134))
-
- puppet# puppet cert list #flashcard  #orange #naranja 
  id:: 63cfbcda-d9e6-4238-8e57-5b00ba9273f5
  
  
    ([Location 1146](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1146))
-
- puppet# puppet cert sign node1.pro-puppet.com #flashcard  #orange #naranja 
  id:: 63cfbcda-5ca1-4a9f-aa0d-9b6fa2c15f02
  
  
    ([Location 1153](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1153))
-
- id:: 63c66a1a-5e2e-44d0-a318-77fc413550c8
  
  puppet cert sign --all #flashcard  #orange #naranja 
  
  
    ([Location 1159](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1159))
-
- id:: 63c66a1a-2fdb-4d81-90ee-3cc836cae578
  
  concept of a “module,” which is a portable collection of manifests that contain resources, classes, definitions, files, and templates. #flashcard  #pink #rosa 
  
  
    ([Location 1191](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1191))
-
- id:: 63c66a1a-6d3f-472b-8f1d-f85df29b1f2f
  
  Adding a Node Definition #flashcard 
  
  
    ([Location 1193](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1193))
-
- id:: 63c66a1a-8fd8-4372-9bf7-8de57b553d14
   ¿Cómo definimos un nodo en site.pp? #flashcard  #pink #rosa 
    For a node definition we specify the node name, enclosed in single quotes, and then specify the configuration that applies to it inside curly braces { }.
  
    ([Location 1199](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1199))
-
- Definición mejorada de un nodo en site.pp #flashcard  #pink #rosa 
  id:: 63cfbcda-f84d-4791-9fcf-8be6befbfe32
    Here we specify an include directive in our node definition; it specifies a collection of configurations, called a class, that we want to apply to our host.
  
    ([Location 1219](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1219))
-
- id:: 63c66a1a-4454-4adb-9beb-8e6bb237367d
  
  There are two ways to include a class: node /node1/ {   include ::sudo } node /node2/ {   class { '::sudo':      users => ['tom', 'jerry'],   } } #flashcard  #blue #azul 
  
  
    ([Location 1221](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1221))
-
- id:: 63c66a1a-b095-4a7b-a64f-b3fffca5907a
   Clases parametrizadas #flashcard  #pink #rosa 
    The first syntax is bare and simple. The second syntax allows parameters to be passed into the class. This feature, generally called parameterized classes, allows classes to be written generally and then utilized specifically, increasing the reusability of Puppet code.
  
    ([Location 1224](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1224))
-
- id:: 63c66a1a-8772-48f8-8eae-f1d13d30c8fc
  
  The double-colon syntax explicitly instructs Puppet to use top scope to look up #flashcard  #blue #azul 
  
  
    ([Location 1229](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1229))
-
- A single module would contain everything required to configure a particular application. #flashcard  #blue #azul 
  id:: 63cfbcda-c348-4cee-8e0e-d7316d3bb668
  
  
    ([Location 1236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1236))
-
- id:: 63c66a1a-c10b-434d-943f-8e013c29580a
  
  Each module needs a specific directory structure and a file called init.pp. This structure allows Puppet to automatically load modules. #flashcard 
  
  
    ([Location 1239](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1239))
-
- module path. #flashcard  #blue #azul 
  id:: 63cfbcda-0da8-42df-ab42-576293e7d974
  
  
    ([Location 1241](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1241))
-
- id:: 63c66a1a-442f-41a2-8019-d0bdbfa7d0a2
  
  [master] modulepath = /etc/puppet/modules:/var/lib/puppet/modules:/opt/modules #flashcard  #orange #naranja 
  
  
    ([Location 1244](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1244))
-
- Module structure # mkdir –p /etc/puppet/modules/sudo/{files,templates,manifests} # touch /etc/puppet/modules/sudo/manifests/init.pp #flashcard  #orange #naranja 
  id:: 63cfbcda-db03-4bf3-8ab7-bc2c29a1f735
  
  
    ([Location 1248](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1248))
-
- id:: 63c66a1a-9045-4a5e-b5f1-9dd60e2219d6
  
  The manifests directory will hold our init.pp file and any other configuration. #flashcard  #blue #azul 
  
  
    ([Location 1250](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1250))
-
- The init.pp file is the core of your module, and every module should have one. #flashcard  #blue #azul 
  id:: 63cfbcda-150f-46fc-b697-17427fb6142b
  
  
    ([Location 1251](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1251))
-
- id:: 63c66a1a-db90-4896-bfcf-e9118610a975
  
  The files directory will hold any files we wish to serve as part of our module. #flashcard  #blue #azul 
  
  
    ([Location 1252](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1252))
-
- The init.pp file #flashcard 
  id:: 63cfbcda-0016-4cfe-93c6-e251d60228a5
  
  
    ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
-
- id:: 63c66a1a-0c90-4e84-8994-617bd7c91ed0
  
  The templates directory will contain any templates that our module might use. #flashcard  #blue #azul 
  
  
    ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
-
- id:: 63c66a1a-198b-46ac-8fc1-6044f724a447
  
  more details of Puppet’s conditional syntaxes #flashcard 
  
  
    ([Location 1270](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1270))
-
- id:: 63c66a1a-ee0d-49d4-8597-963130a19805
  
  The == comparison operator is case-insensitive. To perform a case-sensitive comparison for strings, you must use the regular expression operator =∼ and you must fully root the regular expression; for example, $osfamily =∼ /^Debian$/. #flashcard 
  
  
    ([Location 1273](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1273))
-
- id:: 63c66a1a-d394-4fd1-9486-03243b59cc15
  
  Operating system family is just a name Puppet uses for binary-compatible groups of distributions; for example, Debian, Ubuntu, and Mint all share the osfamily Debian. #flashcard 
  
  
    ([Location 1277](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1277))
-
- For example, if a file resource changes, you can tell Puppet to restart a service resource. #flashcard 
  id:: 63cfbcda-b312-4731-90c0-894d0e5689be
  
  
    ([Location 1294](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1294))
-
- id:: 63c66a1a-175b-4fec-8783-a1c2027b1251
  
  puppet://$::server/modules/sudo/etc/sudoers #flashcard  #orange #naranja 
  
  
    ([Location 1305](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1305))
-
- id:: 63c66a1a-a957-4bf2-8d99-924d48672548
  
  puppet:// part specifies that Puppet will use the Puppet file server protocol to retrieve the file. #flashcard  #blue #azul 
  
  
    ([Location 1306](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1306))
-
- The $::server variable contains the hostname of our Puppet server. #flashcard  #blue #azul 
  id:: 63cfbcda-0878-46ed-a279-f3f1b780dba0
  
  
    ([Location 1309](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1309))
-
- id:: 63c66a1a-90a9-428c-b77b-2992d0ca8325
  
  puppet:///modules/sudo/etc/sudoers. #flashcard  #orange #naranja 
  
  
    ([Location 1312](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1312))
-
- id:: 63c66a1a-aa0c-4d4a-8294-f23a84331c0e
  
  In Puppet, the combined configuration to be applied to a host is called a catalog, and the process of applying it is called a run. You can find a glossary of Puppet terminology at http://docs.puppetlabs.com/references/glossary.html . #flashcard 
  
  
    ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1351))
-
- id:: 63c66a1a-f728-41db-bbfb-1005bd8b386c
  
  we see that the agent has cached the configuration for the host. By default, will Puppet use this cache if it fails to connect to the master during a future run. #flashcard  #blue #azul 
  
  
    ([Location 1355](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1355))
-
- puppet# puppet master --no-daemonize --verbose --debug #flashcard  #orange #naranja 
  id:: 63cfbcda-1c3f-42bd-a290-87670e9d8536
  
  
    ([Location 1364](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1364))
-
- id:: 63c66a1a-e52b-4915-93db-463a85715a85
  
  Resources #flashcard 
  
  
    ([Location 1386](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1386))
-
- id:: 63c66a1a-c2fc-47f6-a2ea-79f18163b709
  
  the Puppet client software is called the agent. #flashcard 
  
  
    ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
-
- id:: 63c66a1a-2843-4743-a9cb-5c545f38e719
  
  Puppet calls the definition of the host itself a node. #flashcard 
  
  
    ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
-
- id:: 63c66a1a-089b-4e69-8817-be35b3167d73
  
  Puppet supports inheritance at the node level, but it is no longer considered best practice. #flashcard 
  
  
    ([Location 1511](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1511))
-
- id:: 63c66a1a-ff4b-47d7-acfe-235969ab71c7
  
  Node inheritance node basenode {     include  sudo     include  mailx } node   ' web.example.com '   inherits basenode {     include apache } #flashcard  #orange #naranja 
  
  
    ([Location 1516](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1516))
-
- id:: 63c66a1a-f736-4999-bd5e-da27a597bfd9
  
  A better solution is to use parameterized classes and one glue class to define high-level behaviors at node level. #flashcard 
  
  
    ([Location 1526](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1526))
-
- err: Cannot reassign variable location at /etc/puppet/manifests/node.pp:4 #flashcard  #orange #naranja 
  id:: 63cfbcda-9895-4875-9bd3-14530f2ee70d
  
  
    ([Location 1540](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1540))
-
- Why does this happen? Puppet is a declarative language. Allowing variable reassignment would require us to rely on order in the file to determine the value of the variable, and order does not matter in a declarative language. #flashcard 
  id:: 63cfbcda-1c31-44e0-bf83-ce00978c326c
  
  
    ([Location 1541](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1541))
-
- id:: 63c66a1a-50bf-4abc-9a47-d25864c12e83
  
  you cannot redefine a variable inside the same scope it was defined in, like our node. #flashcard  #pink #rosa 
  
  
    ([Location 1543](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1543))
-
- At any given time, four scopes are available to Puppet: top scope, node scope, parent scope, and local scope. #flashcard  #pink #rosa 
  id:: 63cfbcda-f6c5-4f08-b8fc-056249a3e076
  
  
    ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
-
- Top scope is anything declared in site.pp or imported manifests. #flashcard  #pink #rosa 
  id:: 63cfbcda-da52-4215-9d43-b23e71e18d25
  
  
    ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
-
- id:: 63c66a1a-c7a4-4f67-95f4-a483fdf068f4
  
  Local scope is the scope of a single class or defined type. #flashcard  #pink #rosa 
  
  
    ([Location 1550](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1550))
-
- id:: 63c66a1a-597d-4c6b-bbe8-1d3ed7282d8c
  
  class ssh (   manage_package = false,   manage_service = false,   package_name   = $::ssh::params::sshd_package ) inherits ssh::params  {   if manage_package == true {     package { $package_name:       ensure => installed,     }   } #flashcard  #orange #naranja 
  
  
    ([Location 1585](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1585))
-
- id:: 63c66a1a-8e04-45fd-a514-e230053da80e
  
  to enforce the style guide. It is called puppet-lint #flashcard 
  
  
    ([Location 1615](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1615))
-
- node ' puppet.example.com ' {   include sudo } #flashcard  #orange #naranja 
  id:: 63cfbcda-661a-40f0-ae44-f0b135d58ec1
  
  
    ([Location 1642](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1642))
-
- id:: 63c66a1a-1f21-4972-b425-b291bdef4121
  
  You can generate a blank puppet module using the syntax puppet module generate name-name, where the first name is the name of you or your organization, and the second is the name of the service you are managing, such as propuppet-amanda #flashcard 
  
  
    ([Location 1653](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1653))
-
- id:: 63c66a1a-3fde-4fd7-828b-0aaa34b83388
  
  class ssh::install {   $package_name = $::osfamily  ?     'RedHat'  => "openssh-server",     'Debian'  => "openssh-server",     'Solaris' => "openssh",     },   package { 'ssh':     ensure => present,     name   => $package_name,   } } #flashcard  #orange #naranja 
  
  
    ([Location 1779](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1779))
-
- id:: 63c66a1a-06e7-464b-8281-d6ff147e950f
  
  Selector matching is case-insensitive. #flashcard 
  
  
    ([Location 1808](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1808))
-
- a best practice we recommend that you move all your conditional checks to a separate class. #flashcard 
  id:: 63cfbcda-d198-4bf4-994f-3ef42c1ea6ff
  
  
    ([Location 1825](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1825))
-
- case $::osfamily {     Solaris: {       $ssh_package_name = 'cswopenssh'       $ssh_service_config = '/etc/opt/csw/ssh/sshd_config'     }     Debian: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     RedHat: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     default: {       fail("Module propuppet-ssh does not support osfamily: ${::osfamily}")     }   } #flashcard  #orange #naranja 
  id:: 63cfbcda-0a92-40cb-a247-3769a22f0962
  
  
    ([Location 1890](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1890))
-
- It is a best practice to establish relationships with an entire class, rather than with a resource contained within another class, because this allows the internal structure of the class to change without refactoring the resource declarations related to the class. #flashcard 
  id:: 63cfbcda-561a-4949-9246-91470251e030
  
  
    ([Location 1908](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1908))
-
- the require metaparameter tells Puppet that all the resources in the specified class must be processed prior to the current resource. #flashcard  #blue #azul 
  id:: 63cfbcda-f8d3-407d-ab80-21511fc7506a
  
  
    ([Location 1910](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1910))
-
- id:: 63c66a1a-2fdd-44d6-bf09-0bab5ab5b8e9
  
  The notify metaparameter creates a notification relationship. If the current resource (the service’s configuration file) is changed, then Puppet should notify all the resources contained in the ssh::service class. In our current case, a “notification” will cause the service resources in the ssh::service class to restart, ensuring that if we change a configuration file, the service will be restarted and running with the correct, updated configuration. #flashcard  #blue #azul 
  
  
    ([Location 1912](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1912))
-
- class ssh::service {   include ssh::params   service { $::ssh::params::ssh_service_name:     ensure      => running,     hasstatus   => true,     hasresstart => true,     enable      => true,     require     => Class['ssh::config'],   } } #flashcard  #orange #naranja 
  id:: 63cfbcda-1cec-4780-b595-0e3ecf3f8930
  
  
    ([Location 1944](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1944))
-
- File {     owner => 'postfix',     group => 'postfix',     mode  => 0644,   } #flashcard  #orange #naranja 
  id:: 63cfbcda-a819-479e-aef1-9ba71a36a896
  
  
    ([Location 2011](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2011))
-
- we specified the File resource type capitalized and without a title. This syntax is called a resource default, and it allows us to specify defaults for a particular resource type. #flashcard  #blue #azul 
  id:: 63cfbcda-4114-4df1-9bcd-37538dc9cf19
  
  
    ([Location 2021](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2021))
-
- id:: 63c66a1a-a1c4-4830-a8f6-cc2cfbb8d98c
  
  class ssh { require ssh::params include ssh::install include ssh::config include ssh::service } #flashcard  #orange #naranja 
  
  
    ([Location 2047](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2047))
-
- id:: 63c66a1a-a3db-4c6e-8a46-da0ab8c49cd2
  
  check the syntax of your ERB templates #flashcard 
  
  
    ([Location 2074](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2074))
-
- id:: 63c66a1a-3111-4391-95d8-186b28033346
  
  Our first class is our mysql class, contained in the init.pp file, where we load all the required classes for this module: class mysql (   $group                   = 'mysql',   $service_enabled  = true,   $service_running  = true,   $user                     = 'mysql' ){   class { 'mysql::install':     user  => $user,     group => $group,   }   class { 'mysql::config':     user  => $user,     group => $group,   }   class { 'mysql::service':     ensure  => $service_running,     enabled => $service_enabled,   } } #flashcard  #orange #naranja 
  
  
    ([Location 2106](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2106))
-
- class mysql::install (   $user,   $group ){ #flashcard  #orange #naranja 
  id:: 63cfbcda-348e-4096-9bb7-6b09808e11f0
  
  
    ([Location 2127](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2127))
-
- Definitions are collections of resources like classes, but unlike classes they can be specified and are evaluated multiple times on a host. They also accept parameters. #flashcard  #pink #rosa 
  id:: 63cfbcda-f64f-4366-8fd2-85744d928077
  
  
    ([Location 2232](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2232))
-
- Tip Remember that classes are singletons. They can be included multiple times on a node, but they will only be evaluated ONCE. A definition, because it takes parameters, can be declared multiple times, and each new declaration will be evaluated. #flashcard  #pink #rosa 
  id:: 63cfbcda-654b-43e5-b36b-634ae066982b
  
  
    ([Location 2233](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2233))
-
- The first definition define apache::vhost(   $docroot,   $port,   $priority,   $ssl=true,   $serveraliases = '',   $template='apache/vhost.conf.erb', ){   include apache   file {"/etc/apache2/sites-enabled/${priority}-${name}":     content => template($template),     owner   => 'root',     group   => 'root',     mode    => '0640',     require => Class['apache::install'],     notify  => Class['apache::service'],   } } #flashcard  #orange #naranja 
  id:: 63cfbcda-2af9-4782-8aff-8c42d1c5c536
  
  
    ([Location 2236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2236))
-
- id:: 63c66a1a-2ffb-4b37-b4ad-69fd72154305
  
  The $name variable contains the name, also known as the title, of a declared defined resource. This is the value of the string before the colon when declaring the defined resource. The $title variable, which usually has the same value, is also available. #flashcard 
  
  
    ([Location 2258](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2258))
-
- id:: 63c66a1a-af05-47af-9b27-ede57c29142d
  
  Putting the $name variable as part of the name of the exec resource will solve this problem. #flashcard 
  
  
    ([Location 2265](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2265))
-
- autoloading. Puppet scans your module and loads any .pp file in the manifests directory that is named after the class it contains; for example, the install.pp file contains the apache::install class and so is autoloaded. The same thing happens with definitions: #flashcard  #pink #rosa 
  id:: 63cfbcda-21ef-4b26-83f9-4ad9d0e70b24
  
  
    ([Location 2319](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2319))
-