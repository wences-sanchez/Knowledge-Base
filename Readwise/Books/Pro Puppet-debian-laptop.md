# Pro Puppet

deck:: [[Other-Books::Pro Puppet]]\
author:: [[Spencer Krum, William Van Hevelingen, Ben Kero, James Turnbull y Jeffrey McCune]]\
full-title:: "Pro Puppet"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/51wVGUlFdzL._SL200_.jpg)
## Highlights
- id:: 6363992c-861e-431c-ae8b-9d37412c581d
  
  This book looks at how you can use Puppet to manage your configuration. #flashcard 
  
  
    ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
-
- id:: 6363992c-dfc6-4d79-a883-3ce0706bcbff
   ¿Qué es Puppet? #flashcard  #pink #rosa 
    Puppet is an open source framework and toolset for managing the configuration of computer systems.
  
    ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
-
- id:: 6363992c-8081-434b-9f63-2eb7e4bbecde
   ¿Qué tipo de arquitectura soporta Puppet? #flashcard  #blue #azul 
    Puppet is Ruby-based configuration management software, licensed as Apache 2.0, and it can run in either client-server or stand-alone mode.
  
    ([Location 690](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=690))
-
- id:: 6363992c-493d-4f57-842b-9d5fae6629d2
   ¿Puppet es open-source o privativo? #flashcard  #blue #azul 
    Puppet has two versions available: the open source version and the Enterprise version.
  
    ([Location 694](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=694))
-
- id:: 6363992c-df66-4ed5-9597-055f3f673132
   ¿Qué tipos de SO soporta Puppet? #flashcard  #blue #azul 
    Puppet can be used to manage configuration on Unix (including OS X), Linux, and Microsoft Windows platforms.
  
    ([Location 697](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=697))
-
- id:: 6363992c-9644-4503-a676-799225491b09
   ¿Cuáles son las capas de estructura de Puppet? #flashcard  #pink #rosa 
    three components: Deployment Layer Configuration Language and Resource Abstraction Layer Transactional Layer
  
    ([Location 701](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=701))
-
- id:: 6363992c-ddb9-4725-af98-27a0d3f9009b
  
  Deployment #flashcard  #blue #azul 
  
  
    ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
-
- id:: 6363992c-72c6-457c-ae8f-af01621b9edd
   ¿Qué es un Puppet Master?
   ¿Qué es un Puppet Agent?
   ¿Qué es un nodo? #flashcard  #pink #rosa 
    Puppet is usually deployed in a simple client-server model (Figure 1-2). The server is called a Puppet master, the Puppet client software is called an agent, and the host itself is defined as a node.
  
    ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
-
- id:: 6363992c-dda4-4d8d-aaed-c7011d66aadd
   ¿Qué es un Puppet Master? #flashcard  #pink #rosa 
    The Puppet master runs as a daemon on a host and contains the configuration required for the specific environment.
  
    ([Location 707](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=707))
-
- id:: 6363992c-74ee-4407-863b-1037cfc7db00
  
  The Puppet agents connect to the Puppet master through an encrypted and authenticated connection using standard SSL, and retrieve or “pull” any configuration to be applied. #flashcard  #pink #rosa 
  
  
    ([Location 708](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=708))
-
- id:: 6363992c-0d6e-4a3c-b321-fbb0de5ab722
  
  Each agent can run Puppet as a daemon, via a mechanism such as cron, or the connection can be manually triggered. #flashcard 
  
  
    ([Location 713](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=713))
-
- id:: 6363992c-8913-48b3-89a5-d57778b620d2
  
  The usual practice is to run Puppet as a daemon and have it periodically check with the master to confirm that its configuration is up-to-date or to retrieve any new configuration (Figure 1-3). #flashcard 
  
  
    ([Location 714](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=714))
-
- id:: 6363992c-e584-4d81-9073-d26d5f1159b0
  
  The Configuration Language and Resource Abstraction Layer #flashcard  #blue #azul 
  
  
    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
-
- id:: 6363992c-6b98-4698-b89f-9c0a1e1a16e7
   ¿Qué son los resources en Puppet? #flashcard  #pink #rosa 
    Puppet uses a declarative language, the Puppet language, to define your configuration items, which Puppet calls resources.
  
    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
-
- id:: 6363992c-6c7c-4659-942e-4eec0777c866
  
  The Configuration Language #flashcard 
  
  
    ([Location 730](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=730))
-
- id:: 6363992c-9cec-4982-9e3d-69c438bf846f
   Estructura de un resource en Puppet. #flashcard 
    Each resource is made up of a type (what sort of resource is being managed: packages, services, or cron jobs), a title (the name of the resource), and a series of attributes (values that specify the state of the resource—for example, whether a service is started or stopped).
  
    ([Location 741](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=741))
-
- id:: 6363992c-cb0c-48e6-a871-9989f44d7e3c
  
  The Resource Abstraction Layer #flashcard 
  
  
    ([Location 761](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=761))
-
- id:: 6363992c-df38-41d7-8e14-43d02464f01d
   ¿Qué es facter? #flashcard  #pink #rosa 
    Facter is a system inventory tool, also developed principally by Puppet Labs,
  
    ([Location 774](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=774))
-
- id:: 6363992c-6aa4-4138-b228-da1798058da5
  
  You can see the facts available on your clients by running the facter binary from the command line. #flashcard 
  
  
    ([Location 778](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=778))
-
- id:: 6363992c-b11a-4cde-9445-4ff07a512898
  
  The Transactional Layer #flashcard  #blue #azul 
  
  
    ([Location 787](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=787))
-
- id:: 6363992c-9073-47cf-a12a-e92d57057e9c
  
  Puppet’s transactional layer is its engine. #flashcard  #pink #rosa 
  
  
    ([Location 788](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=788))
-
- id:: 6363992c-d3b2-410b-b0bd-59bc57a8a109
   Pasos de la capa Transaccional de Puppet. #flashcard  #blue #azul 
    steps: Interpret and compile your configuration. Communicate the compiled configuration to the agent. Apply the configuration on the agent. Report the results of that application to the master.
  
    ([Location 789](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=789))
-
- id:: 6363992c-f120-43d3-9255-3e6fd5fb0758
  
  The first step Puppet takes is to analyze your configuration and calculate how to apply it to your agent. To do this, Puppet creates a graph showing all resources, with their relationships to each other and to each agent. This allows Puppet to work out the order, based on relationships you create, in which to apply each resource to your host. This model is one of Puppet’s most powerful features. #flashcard 
  
  
    ([Location 791](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=791))
-
- id:: 6363992c-e554-4607-9c82-c212c36e1384
  
  Puppet then takes the resources and compiles them into a catalog for each agent. The catalog is sent to the host and applied by the Puppet agent. The results of this application are then sent back to the master in the form of a report. #flashcard 
  
  
    ([Location 794](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=794))
-
- id:: 6363992c-cc70-42de-9cab-fb49b465dd00
  
  idempotency, #flashcard  #pink #rosa 
  
  
    ([Location 796](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=796))
-
- id:: 6363992c-03ee-4b9e-a516-7b9055f379c2
  
  you can’t roll back transactions as you can with some databases. You can, however, model transactions in a “noop,” or no-operation mode, that allows you to test the execution of your changes without applying them. #flashcard  #blue #azul 
  
  
    ([Location 799](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=799))
-
- id:: 6363992c-562e-4c6e-9758-e703b2d72ca2
   ¿En qué fichero está la configuración principal del Puppet Master? #flashcard  #pink #rosa 
    Puppet’s configuration will be located under the /etc/puppet directory. Puppet’s principal configuration file is called puppet.conf and is stored at /etc/puppet/puppet.conf
  
    ([Location 1027](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1027))
-
- id:: 6363992c-6ccc-4d23-a78d-689f2d1ddeac
  
  The puppet.conf configuration file is constructed much like an INI-style configuration file and divided into sections. Each section configures a particular element of Puppet. For example, the [agent] section configures the Puppet agent, and the [master] section configures the Puppet master binary. There is also a global configuration section called [main]. All components of Puppet set options specified in the [main] section. #flashcard  #blue #azul 
  
  
    ([Location 1036](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1036))
-
- id:: 6363992c-d0fa-40b0-8f1b-57c211eaedc6
  
  [main] server=puppet.example.com Replace puppet.example.com with the fully qualified domain name of your host. #flashcard  #orange #naranja 
  
  
    ([Location 1043](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1043))
-
- id:: 6363992c-a062-4d33-af5a-cd45a244cbef
  
  The site.pp file tells Puppet where and what configuration to load for our clients. We’re going to store this file in a directory called manifests under the /etc/puppet directory. #flashcard  #pink #rosa 
  
  
    ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
-
- id:: 6363992c-1162-4c46-9dbc-547f23fca018
   ¿Qué es el site.pp? #flashcard  #pink #rosa 
    The site.pp File
  
    ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
-
- id:: 6363992c-60c1-4524-ac2b-175b55c7dea0
   ¿Qué es un manifest en Puppet? #flashcard  #pink #rosa 
    Manifest is Puppet’s term for files containing configuration information. Manifest files have a suffix of .pp. The Puppet language is written into these files.
  
    ([Location 1055](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1055))
-
- id:: 6363992c-9fd0-4565-8e46-8909868d07ca
  
  Output from the daemon can be seen in /var/log/messages on Red Hat–based hosts #flashcard 
  
  
    ([Location 1079](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1079))
-
- id:: 6363992c-2fd2-4642-817b-59c554f63b94
  
  By default, the Puppet client runs as a daemon, and the puppet agent command forks off the Puppet daemon into the background and exits immediately. #flashcard 
  
  
    ([Location 1134](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1134))
-
- id:: 6363992c-62b5-43be-ba9b-3a133ac83559
  
  puppet# puppet cert list #flashcard  #orange #naranja 
  
  
    ([Location 1146](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1146))
-
- id:: 6363992c-f3bf-4a39-8c2d-8077a708dbcd
  
  puppet# puppet cert sign node1.pro-puppet.com #flashcard  #orange #naranja 
  
  
    ([Location 1153](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1153))
-
- id:: 6363992c-94d8-471b-9757-b7900ef76009
  
  puppet cert sign --all #flashcard  #orange #naranja 
  
  
    ([Location 1159](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1159))
-
- id:: 6363992c-0f5d-45b9-ba40-9a01f71a26d2
  
  concept of a “module,” which is a portable collection of manifests that contain resources, classes, definitions, files, and templates. #flashcard  #pink #rosa 
  
  
    ([Location 1191](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1191))
-
- id:: 6363992c-771b-42a0-b285-5f033089b52f
  
  Adding a Node Definition #flashcard 
  
  
    ([Location 1193](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1193))
-
- id:: 6363992c-9dba-425d-bb71-d24a9bf3b0f5
   ¿Cómo definimos un nodo en site.pp? #flashcard  #pink #rosa 
    For a node definition we specify the node name, enclosed in single quotes, and then specify the configuration that applies to it inside curly braces { }.
  
    ([Location 1199](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1199))
-
- id:: 6363992c-5443-4ae5-8440-2ae8b6e070cd
   Definición mejorada de un nodo en site.pp #flashcard  #pink #rosa 
    Here we specify an include directive in our node definition; it specifies a collection of configurations, called a class, that we want to apply to our host.
  
    ([Location 1219](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1219))
-
- id:: 6363992c-ada7-448d-9947-591785067120
  
  There are two ways to include a class: node /node1/ {   include ::sudo } node /node2/ {   class { '::sudo':      users => ['tom', 'jerry'],   } } #flashcard  #blue #azul 
  
  
    ([Location 1221](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1221))
-
- id:: 6363992c-d79f-4bcc-aec2-b400cf3e8307
   Clases parametrizadas #flashcard  #pink #rosa 
    The first syntax is bare and simple. The second syntax allows parameters to be passed into the class. This feature, generally called parameterized classes, allows classes to be written generally and then utilized specifically, increasing the reusability of Puppet code.
  
    ([Location 1224](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1224))
-
- id:: 6363992c-37fc-4294-bd34-71e035c76518
  
  The double-colon syntax explicitly instructs Puppet to use top scope to look up #flashcard  #blue #azul 
  
  
    ([Location 1229](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1229))
-
- id:: 6363992c-e4cf-4f30-b545-1eb24718048a
  
  A single module would contain everything required to configure a particular application. #flashcard  #blue #azul 
  
  
    ([Location 1236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1236))
-
- id:: 6363992c-02d0-4eb0-a661-826b725706c7
  
  Each module needs a specific directory structure and a file called init.pp. This structure allows Puppet to automatically load modules. #flashcard 
  
  
    ([Location 1239](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1239))
-
- id:: 6363992c-d6ee-4d55-8715-0b8f37e9e43a
  
  module path. #flashcard  #blue #azul 
  
  
    ([Location 1241](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1241))
-
- id:: 6363992c-dc17-4edb-b6fc-a09ef60aa54c
  
  [master] modulepath = /etc/puppet/modules:/var/lib/puppet/modules:/opt/modules #flashcard  #orange #naranja 
  
  
    ([Location 1244](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1244))
-
- id:: 6363992c-ee89-4c6b-9772-e53b88fbe768
  
  Module structure # mkdir –p /etc/puppet/modules/sudo/{files,templates,manifests} # touch /etc/puppet/modules/sudo/manifests/init.pp #flashcard  #orange #naranja 
  
  
    ([Location 1248](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1248))
-
- id:: 6363992c-c670-4fdf-84dd-677712e2ba8d
  
  The manifests directory will hold our init.pp file and any other configuration. #flashcard  #blue #azul 
  
  
    ([Location 1250](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1250))
-
- id:: 6363992c-6113-4e5a-9be6-836bd3e92472
  
  The init.pp file is the core of your module, and every module should have one. #flashcard  #blue #azul 
  
  
    ([Location 1251](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1251))
-
- id:: 6363992c-b29d-49a9-9457-c6cffb4ac243
  
  The files directory will hold any files we wish to serve as part of our module. #flashcard  #blue #azul 
  
  
    ([Location 1252](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1252))
-
- id:: 6363992c-bb20-48e6-9582-356ad4388d3f
  
  The init.pp file #flashcard 
  
  
    ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
-
- id:: 6363992c-4ec5-4be5-b822-862c060cf87e
  
  The templates directory will contain any templates that our module might use. #flashcard  #blue #azul 
  
  
    ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
-
- id:: 6363992c-fd7f-4000-a492-6839419c8786
  
  more details of Puppet’s conditional syntaxes #flashcard 
  
  
    ([Location 1270](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1270))
-
- id:: 6363992c-f8b0-4613-b755-44c2729e0484
  
  The == comparison operator is case-insensitive. To perform a case-sensitive comparison for strings, you must use the regular expression operator =∼ and you must fully root the regular expression; for example, $osfamily =∼ /^Debian$/. #flashcard 
  
  
    ([Location 1273](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1273))
-
- id:: 6363992c-674c-4b4e-831a-d131b0723a04
  
  Operating system family is just a name Puppet uses for binary-compatible groups of distributions; for example, Debian, Ubuntu, and Mint all share the osfamily Debian. #flashcard 
  
  
    ([Location 1277](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1277))
-
- id:: 6363992c-998c-4ec2-9823-24c02db6bdbb
  
  For example, if a file resource changes, you can tell Puppet to restart a service resource. #flashcard 
  
  
    ([Location 1294](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1294))
-
- id:: 6363992c-84f9-4d2e-b7b3-5c6d53608eb5
  
  puppet://$::server/modules/sudo/etc/sudoers #flashcard  #orange #naranja 
  
  
    ([Location 1305](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1305))
-
- id:: 6363992c-21e7-450f-9017-29376ddb47bf
  
  puppet:// part specifies that Puppet will use the Puppet file server protocol to retrieve the file. #flashcard  #blue #azul 
  
  
    ([Location 1306](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1306))
-
- id:: 6363992c-8688-4035-99c7-8322ba3678ff
  
  The $::server variable contains the hostname of our Puppet server. #flashcard  #blue #azul 
  
  
    ([Location 1309](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1309))
-
- id:: 6363992c-1beb-434b-b909-3e0c0febdd88
  
  puppet:///modules/sudo/etc/sudoers. #flashcard  #orange #naranja 
  
  
    ([Location 1312](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1312))
-
- id:: 6363992c-845a-4e59-a564-f1e65d038250
  
  In Puppet, the combined configuration to be applied to a host is called a catalog, and the process of applying it is called a run. You can find a glossary of Puppet terminology at http://docs.puppetlabs.com/references/glossary.html . #flashcard 
  
  
    ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1351))
-
- id:: 6363992c-e34a-4cde-98e0-41058ef82b35
  
  we see that the agent has cached the configuration for the host. By default, will Puppet use this cache if it fails to connect to the master during a future run. #flashcard  #blue #azul 
  
  
    ([Location 1355](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1355))
-
- id:: 6363992c-5956-4dcd-a34c-5be9fe200738
  
  puppet# puppet master --no-daemonize --verbose --debug #flashcard  #orange #naranja 
  
  
    ([Location 1364](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1364))
-
- id:: 6363992c-43e2-420f-8be4-80341a14ba73
  
  Resources #flashcard 
  
  
    ([Location 1386](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1386))
-
- id:: 6363992c-3468-42da-a541-18c3830633d8
  
  the Puppet client software is called the agent. #flashcard 
  
  
    ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
-
- id:: 6363992c-eb5d-4670-af5c-a35559854c0d
  
  Puppet calls the definition of the host itself a node. #flashcard 
  
  
    ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
-
- id:: 6363992c-46c8-4317-b454-3024d44ea134
  
  Puppet supports inheritance at the node level, but it is no longer considered best practice. #flashcard 
  
  
    ([Location 1511](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1511))
-
- id:: 6363992c-001c-4e42-91e6-d77e6baafc0a
  
  Node inheritance node basenode {     include  sudo     include  mailx } node   ' web.example.com '   inherits basenode {     include apache } #flashcard  #orange #naranja 
  
  
    ([Location 1516](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1516))
-
- id:: 6363992c-3618-4259-b3c5-e33659fb298a
  
  A better solution is to use parameterized classes and one glue class to define high-level behaviors at node level. #flashcard 
  
  
    ([Location 1526](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1526))
-
- id:: 6363992c-8963-45b9-aee3-c275bba803e8
  
  err: Cannot reassign variable location at /etc/puppet/manifests/node.pp:4 #flashcard  #orange #naranja 
  
  
    ([Location 1540](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1540))
-
- id:: 6363992c-0660-4127-9fd5-2bbdc125a487
  
  Why does this happen? Puppet is a declarative language. Allowing variable reassignment would require us to rely on order in the file to determine the value of the variable, and order does not matter in a declarative language. #flashcard 
  
  
    ([Location 1541](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1541))
-
- id:: 6363992c-d668-4d97-96ac-8e126704bcde
  
  you cannot redefine a variable inside the same scope it was defined in, like our node. #flashcard  #pink #rosa 
  
  
    ([Location 1543](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1543))
-
- id:: 6363992c-d98c-40f9-8b16-9de6f7a37705
  
  At any given time, four scopes are available to Puppet: top scope, node scope, parent scope, and local scope. #flashcard  #pink #rosa 
  
  
    ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
-
- id:: 6363992c-197a-47fb-ae0e-f690f5d40c0a
  
  Top scope is anything declared in site.pp or imported manifests. #flashcard  #pink #rosa 
  
  
    ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
-
- id:: 6363992c-a933-4591-b93c-785aa84cde86
  
  Local scope is the scope of a single class or defined type. #flashcard  #pink #rosa 
  
  
    ([Location 1550](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1550))
-
- id:: 6363992c-d600-42f3-a960-39c1c8f4fe82
  
  class ssh (   manage_package = false,   manage_service = false,   package_name   = $::ssh::params::sshd_package ) inherits ssh::params  {   if manage_package == true {     package { $package_name:       ensure => installed,     }   } #flashcard  #orange #naranja 
  
  
    ([Location 1585](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1585))
-
- id:: 6363992c-4600-472d-a17f-d9c80cc15053
  
  to enforce the style guide. It is called puppet-lint #flashcard 
  
  
    ([Location 1615](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1615))
-
- id:: 6363992c-12ea-484a-a02f-d550b43bad35
  
  node ' puppet.example.com ' {   include sudo } #flashcard  #orange #naranja 
  
  
    ([Location 1642](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1642))
-
- id:: 6363992c-86f4-4eee-80cc-6945df758099
  
  You can generate a blank puppet module using the syntax puppet module generate name-name, where the first name is the name of you or your organization, and the second is the name of the service you are managing, such as propuppet-amanda #flashcard 
  
  
    ([Location 1653](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1653))
-
- id:: 6363992c-f9f7-410b-a58e-b8020dd14163
  
  class ssh::install {   $package_name = $::osfamily  ?     'RedHat'  => "openssh-server",     'Debian'  => "openssh-server",     'Solaris' => "openssh",     },   package { 'ssh':     ensure => present,     name   => $package_name,   } } #flashcard  #orange #naranja 
  
  
    ([Location 1779](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1779))
-
- id:: 6363992c-d244-4820-ab5d-116e5f398f71
  
  Selector matching is case-insensitive. #flashcard 
  
  
    ([Location 1808](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1808))
-
- id:: 6363992c-cce2-4024-b11b-f5f156aa6812
  
  a best practice we recommend that you move all your conditional checks to a separate class. #flashcard 
  
  
    ([Location 1825](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1825))
-
- id:: 6363992c-b59c-4f54-a5d8-c8b3f4c6b2f4
  
  case $::osfamily {     Solaris: {       $ssh_package_name = 'cswopenssh'       $ssh_service_config = '/etc/opt/csw/ssh/sshd_config'     }     Debian: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     RedHat: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     default: {       fail("Module propuppet-ssh does not support osfamily: ${::osfamily}")     }   } #flashcard  #orange #naranja 
  
  
    ([Location 1890](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1890))
-
- id:: 6363992c-8c5d-4ec0-a122-e742e29099b7
  
  It is a best practice to establish relationships with an entire class, rather than with a resource contained within another class, because this allows the internal structure of the class to change without refactoring the resource declarations related to the class. #flashcard 
  
  
    ([Location 1908](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1908))
-
- id:: 6363992c-d2cd-4179-841b-cec17994b316
  
  the require metaparameter tells Puppet that all the resources in the specified class must be processed prior to the current resource. #flashcard  #blue #azul 
  
  
    ([Location 1910](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1910))
-
- id:: 6363992c-475f-45ac-9770-f8c481f6ffc5
  
  The notify metaparameter creates a notification relationship. If the current resource (the service’s configuration file) is changed, then Puppet should notify all the resources contained in the ssh::service class. In our current case, a “notification” will cause the service resources in the ssh::service class to restart, ensuring that if we change a configuration file, the service will be restarted and running with the correct, updated configuration. #flashcard  #blue #azul 
  
  
    ([Location 1912](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1912))
-
- id:: 6363992c-6c07-448b-9745-fa79faf2e5a7
  
  class ssh::service {   include ssh::params   service { $::ssh::params::ssh_service_name:     ensure      => running,     hasstatus   => true,     hasresstart => true,     enable      => true,     require     => Class['ssh::config'],   } } #flashcard  #orange #naranja 
  
  
    ([Location 1944](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1944))
-
- id:: 6363992c-236d-4c33-868d-bc77e3bae038
  
  File {     owner => 'postfix',     group => 'postfix',     mode  => 0644,   } #flashcard  #orange #naranja 
  
  
    ([Location 2011](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2011))
-
- id:: 6363992c-71ca-43b7-b4e8-4991030f8b52
  
  we specified the File resource type capitalized and without a title. This syntax is called a resource default, and it allows us to specify defaults for a particular resource type. #flashcard  #blue #azul 
  
  
    ([Location 2021](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2021))
-
- id:: 6363992c-e3e1-466b-b50b-c1d86c242a15
  
  class ssh { require ssh::params include ssh::install include ssh::config include ssh::service } #flashcard  #orange #naranja 
  
  
    ([Location 2047](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2047))
-
- id:: 6363992c-54fd-4c5d-80e7-9b69b5e45bcb
  
  check the syntax of your ERB templates #flashcard 
  
  
    ([Location 2074](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2074))
-
- id:: 6363992c-3bf6-493d-9b50-272f3c3c3d34
  
  Our first class is our mysql class, contained in the init.pp file, where we load all the required classes for this module: class mysql (   $group                   = 'mysql',   $service_enabled  = true,   $service_running  = true,   $user                     = 'mysql' ){   class { 'mysql::install':     user  => $user,     group => $group,   }   class { 'mysql::config':     user  => $user,     group => $group,   }   class { 'mysql::service':     ensure  => $service_running,     enabled => $service_enabled,   } } #flashcard  #orange #naranja 
  
  
    ([Location 2106](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2106))
-
- id:: 6363992c-e922-4726-a301-37bab0c45a6a
  
  class mysql::install (   $user,   $group ){ #flashcard  #orange #naranja 
  
  
    ([Location 2127](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2127))
-
- id:: 6363992c-c9d8-43d4-9652-e3fe47a478de
  
  Definitions are collections of resources like classes, but unlike classes they can be specified and are evaluated multiple times on a host. They also accept parameters. #flashcard  #pink #rosa 
  
  
    ([Location 2232](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2232))
-
- id:: 6363992c-541a-479f-ad1b-1a5c3e22e653
  
  Tip Remember that classes are singletons. They can be included multiple times on a node, but they will only be evaluated ONCE. A definition, because it takes parameters, can be declared multiple times, and each new declaration will be evaluated. #flashcard  #pink #rosa 
  
  
    ([Location 2233](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2233))
-
- id:: 6363992c-3f82-48bb-8e50-ad92e1a541ab
  
  The first definition define apache::vhost(   $docroot,   $port,   $priority,   $ssl=true,   $serveraliases = '',   $template='apache/vhost.conf.erb', ){   include apache   file {"/etc/apache2/sites-enabled/${priority}-${name}":     content => template($template),     owner   => 'root',     group   => 'root',     mode    => '0640',     require => Class['apache::install'],     notify  => Class['apache::service'],   } } #flashcard  #orange #naranja 
  
  
    ([Location 2236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2236))
-
- id:: 6363992c-3c32-4958-afea-9a7f78a28874
  
  The $name variable contains the name, also known as the title, of a declared defined resource. This is the value of the string before the colon when declaring the defined resource. The $title variable, which usually has the same value, is also available. #flashcard 
  
  
    ([Location 2258](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2258))
-
- id:: 6363992c-a4d5-4fce-8623-38f4626543af
  
  Putting the $name variable as part of the name of the exec resource will solve this problem. #flashcard 
  
  
    ([Location 2265](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2265))
-
- id:: 6363992c-4128-4ae8-9dc7-d0eac38cee2f
  
  autoloading. Puppet scans your module and loads any .pp file in the manifests directory that is named after the class it contains; for example, the install.pp file contains the apache::install class and so is autoloaded. The same thing happens with definitions: #flashcard  #pink #rosa 
  
  
    ([Location 2319](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2319))
-