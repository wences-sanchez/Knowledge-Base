# Pro Puppet

deck:: [[Other-Books::Pro Puppet]]\
author:: [[Spencer Krum, William Van Hevelingen, Ben Kero, James Turnbull y Jeffrey McCune]]\
full-title:: "Pro Puppet"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/51wVGUlFdzL._SL200_.jpg)

## Highlights
- 

This book looks at how you can use Puppet to manage your configuration. #flashcard 


    ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
-
- 
 ¿Qué es Puppet? #flashcard  #pink #rosa 
    Puppet is an open source framework and toolset for managing the configuration of computer systems.

    ([Location 670](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=670))
-
- 
 ¿Qué tipo de arquitectura soporta Puppet? #flashcard  #blue #azul 
    Puppet is Ruby-based configuration management software, licensed as Apache 2.0, and it can run in either client-server or stand-alone mode.

    ([Location 690](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=690))
-
- 
 ¿Puppet es open-source o privativo? #flashcard  #blue #azul 
    Puppet has two versions available: the open source version and the Enterprise version.

    ([Location 694](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=694))
-
- 
 ¿Qué tipos de SO soporta Puppet? #flashcard  #blue #azul 
    Puppet can be used to manage configuration on Unix (including OS X), Linux, and Microsoft Windows platforms.

    ([Location 697](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=697))
-
- 
 ¿Cuáles son las capas de estructura de Puppet? #flashcard  #pink #rosa 
    three components: Deployment Layer Configuration Language and Resource Abstraction Layer Transactional Layer

    ([Location 701](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=701))
-
- 

Deployment #flashcard  #blue #azul 


    ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
-
- 
 ¿Qué es un Puppet Master?
   ¿Qué es un Puppet Agent?
   ¿Qué es un nodo? #flashcard  #pink #rosa 
    Puppet is usually deployed in a simple client-server model (Figure 1-2). The server is called a Puppet master, the Puppet client software is called an agent, and the host itself is defined as a node.

    ([Location 704](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=704))
-
- 
 ¿Qué es un Puppet Master? #flashcard  #pink #rosa 
    The Puppet master runs as a daemon on a host and contains the configuration required for the specific environment.

    ([Location 707](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=707))
-
- 

The Puppet agents connect to the Puppet master through an encrypted and authenticated connection using standard SSL, and retrieve or “pull” any configuration to be applied. #flashcard  #pink #rosa 


    ([Location 708](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=708))
-
- 

Each agent can run Puppet as a daemon, via a mechanism such as cron, or the connection can be manually triggered. #flashcard 


    ([Location 713](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=713))
-
- 

The usual practice is to run Puppet as a daemon and have it periodically check with the master to confirm that its configuration is up-to-date or to retrieve any new configuration (Figure 1-3). #flashcard 


    ([Location 714](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=714))
-
- 

The Configuration Language and Resource Abstraction Layer #flashcard  #blue #azul 


    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
-
- 
 ¿Qué son los resources en Puppet? #flashcard  #pink #rosa 
    Puppet uses a declarative language, the Puppet language, to define your configuration items, which Puppet calls resources.

    ([Location 723](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=723))
-
- 

The Configuration Language #flashcard 


    ([Location 730](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=730))
-
- 
 Estructura de un resource en Puppet. #flashcard 
    Each resource is made up of a type (what sort of resource is being managed: packages, services, or cron jobs), a title (the name of the resource), and a series of attributes (values that specify the state of the resource—for example, whether a service is started or stopped).

    ([Location 741](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=741))
-
- 

The Resource Abstraction Layer #flashcard 


    ([Location 761](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=761))
-
- 
 ¿Qué es facter? #flashcard  #pink #rosa 
    Facter is a system inventory tool, also developed principally by Puppet Labs,

    ([Location 774](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=774))
-
- 

You can see the facts available on your clients by running the facter binary from the command line. #flashcard 


    ([Location 778](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=778))
-
- 

The Transactional Layer #flashcard  #blue #azul 


    ([Location 787](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=787))
-
- 

Puppet’s transactional layer is its engine. #flashcard  #pink #rosa 


    ([Location 788](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=788))
-
- 
 Pasos de la capa Transaccional de Puppet. #flashcard  #blue #azul 
    steps: Interpret and compile your configuration. Communicate the compiled configuration to the agent. Apply the configuration on the agent. Report the results of that application to the master.

    ([Location 789](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=789))
-
- 

The first step Puppet takes is to analyze your configuration and calculate how to apply it to your agent. To do this, Puppet creates a graph showing all resources, with their relationships to each other and to each agent. This allows Puppet to work out the order, based on relationships you create, in which to apply each resource to your host. This model is one of Puppet’s most powerful features. #flashcard 


    ([Location 791](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=791))
-
- 

Puppet then takes the resources and compiles them into a catalog for each agent. The catalog is sent to the host and applied by the Puppet agent. The results of this application are then sent back to the master in the form of a report. #flashcard 


    ([Location 794](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=794))
-
- 

idempotency, #flashcard  #pink #rosa 


    ([Location 796](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=796))
-
- 

you can’t roll back transactions as you can with some databases. You can, however, model transactions in a “noop,” or no-operation mode, that allows you to test the execution of your changes without applying them. #flashcard  #blue #azul 


    ([Location 799](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=799))
-
- 
 ¿En qué fichero está la configuración principal del Puppet Master? #flashcard  #pink #rosa 
    Puppet’s configuration will be located under the /etc/puppet directory. Puppet’s principal configuration file is called puppet.conf and is stored at /etc/puppet/puppet.conf

    ([Location 1027](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1027))
-
- 

The puppet.conf configuration file is constructed much like an INI-style configuration file and divided into sections. Each section configures a particular element of Puppet. For example, the [agent] section configures the Puppet agent, and the [master] section configures the Puppet master binary. There is also a global configuration section called [main]. All components of Puppet set options specified in the [main] section. #flashcard  #blue #azul 


    ([Location 1036](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1036))
-
- 

[main] server=puppet.example.com Replace puppet.example.com with the fully qualified domain name of your host. #flashcard  #orange #naranja 


    ([Location 1043](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1043))
-
- 

The site.pp file tells Puppet where and what configuration to load for our clients. We’re going to store this file in a directory called manifests under the /etc/puppet directory. #flashcard  #pink #rosa 


    ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
-
- 
 ¿Qué es el site.pp? #flashcard  #pink #rosa 
    The site.pp File

    ([Location 1052](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1052))
-
- 
 ¿Qué es un manifest en Puppet? #flashcard  #pink #rosa 
    Manifest is Puppet’s term for files containing configuration information. Manifest files have a suffix of .pp. The Puppet language is written into these files.

    ([Location 1055](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1055))
-
- 

Output from the daemon can be seen in /var/log/messages on Red Hat–based hosts #flashcard 


    ([Location 1079](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1079))
-
- 

By default, the Puppet client runs as a daemon, and the puppet agent command forks off the Puppet daemon into the background and exits immediately. #flashcard 


    ([Location 1134](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1134))
-
- 

puppet# puppet cert list #flashcard  #orange #naranja 


    ([Location 1146](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1146))
-
- 

puppet# puppet cert sign node1.pro-puppet.com #flashcard  #orange #naranja 


    ([Location 1153](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1153))
-
- 

puppet cert sign --all #flashcard  #orange #naranja 


    ([Location 1159](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1159))
-
- 

concept of a “module,” which is a portable collection of manifests that contain resources, classes, definitions, files, and templates. #flashcard  #pink #rosa 


    ([Location 1191](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1191))
-
- 

Adding a Node Definition #flashcard 


    ([Location 1193](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1193))
-
- 
 ¿Cómo definimos un nodo en site.pp? #flashcard  #pink #rosa 
    For a node definition we specify the node name, enclosed in single quotes, and then specify the configuration that applies to it inside curly braces { }.

    ([Location 1199](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1199))
-
- 
 Definición mejorada de un nodo en site.pp #flashcard  #pink #rosa 
    Here we specify an include directive in our node definition; it specifies a collection of configurations, called a class, that we want to apply to our host.

    ([Location 1219](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1219))
-
- 

There are two ways to include a class: node /node1/ {   include ::sudo } node /node2/ {   class { '::sudo':      users => ['tom', 'jerry'],   } } #flashcard  #blue #azul 


    ([Location 1221](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1221))
-
- 
 Clases parametrizadas #flashcard  #pink #rosa 
    The first syntax is bare and simple. The second syntax allows parameters to be passed into the class. This feature, generally called parameterized classes, allows classes to be written generally and then utilized specifically, increasing the reusability of Puppet code.

    ([Location 1224](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1224))
-
- 

The double-colon syntax explicitly instructs Puppet to use top scope to look up #flashcard  #blue #azul 


    ([Location 1229](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1229))
-
- 

A single module would contain everything required to configure a particular application. #flashcard  #blue #azul 


    ([Location 1236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1236))
-
- 

Each module needs a specific directory structure and a file called init.pp. This structure allows Puppet to automatically load modules. #flashcard 


    ([Location 1239](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1239))
-
- 

module path. #flashcard  #blue #azul 


    ([Location 1241](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1241))
-
- 

[master] modulepath = /etc/puppet/modules:/var/lib/puppet/modules:/opt/modules #flashcard  #orange #naranja 


    ([Location 1244](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1244))
-
- 

Module structure # mkdir –p /etc/puppet/modules/sudo/{files,templates,manifests} # touch /etc/puppet/modules/sudo/manifests/init.pp #flashcard  #orange #naranja 


    ([Location 1248](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1248))
-
- 

The manifests directory will hold our init.pp file and any other configuration. #flashcard  #blue #azul 


    ([Location 1250](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1250))
-
- 

The init.pp file is the core of your module, and every module should have one. #flashcard  #blue #azul 


    ([Location 1251](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1251))
-
- 

The files directory will hold any files we wish to serve as part of our module. #flashcard  #blue #azul 


    ([Location 1252](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1252))
-
- 

The init.pp file #flashcard 


    ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
-
- 

The templates directory will contain any templates that our module might use. #flashcard  #blue #azul 


    ([Location 1253](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1253))
-
- 

more details of Puppet’s conditional syntaxes #flashcard 


    ([Location 1270](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1270))
-
- 

The == comparison operator is case-insensitive. To perform a case-sensitive comparison for strings, you must use the regular expression operator =∼ and you must fully root the regular expression; for example, $osfamily =∼ /^Debian$/. #flashcard 


    ([Location 1273](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1273))
-
- 

Operating system family is just a name Puppet uses for binary-compatible groups of distributions; for example, Debian, Ubuntu, and Mint all share the osfamily Debian. #flashcard 


    ([Location 1277](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1277))
-
- 

For example, if a file resource changes, you can tell Puppet to restart a service resource. #flashcard 


    ([Location 1294](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1294))
-
- 

puppet://$::server/modules/sudo/etc/sudoers #flashcard  #orange #naranja 


    ([Location 1305](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1305))
-
- 

puppet:// part specifies that Puppet will use the Puppet file server protocol to retrieve the file. #flashcard  #blue #azul 


    ([Location 1306](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1306))
-
- 

The $::server variable contains the hostname of our Puppet server. #flashcard  #blue #azul 


    ([Location 1309](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1309))
-
- 

puppet:///modules/sudo/etc/sudoers. #flashcard  #orange #naranja 


    ([Location 1312](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1312))
-
- 

In Puppet, the combined configuration to be applied to a host is called a catalog, and the process of applying it is called a run. You can find a glossary of Puppet terminology at http://docs.puppetlabs.com/references/glossary.html . #flashcard 


    ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1351))
-
- 

we see that the agent has cached the configuration for the host. By default, will Puppet use this cache if it fails to connect to the master during a future run. #flashcard  #blue #azul 


    ([Location 1355](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1355))
-
- 

puppet# puppet master --no-daemonize --verbose --debug #flashcard  #orange #naranja 


    ([Location 1364](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1364))
-
- 

Resources #flashcard 


    ([Location 1386](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1386))
-
- 

the Puppet client software is called the agent. #flashcard 


    ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
-
- 

Puppet calls the definition of the host itself a node. #flashcard 


    ([Location 1439](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1439))
-
- 

Puppet supports inheritance at the node level, but it is no longer considered best practice. #flashcard 


    ([Location 1511](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1511))
-
- 

Node inheritance node basenode {     include  sudo     include  mailx } node   ' web.example.com '   inherits basenode {     include apache } #flashcard  #orange #naranja 


    ([Location 1516](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1516))
-
- 

A better solution is to use parameterized classes and one glue class to define high-level behaviors at node level. #flashcard 


    ([Location 1526](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1526))
-
- 

err: Cannot reassign variable location at /etc/puppet/manifests/node.pp:4 #flashcard  #orange #naranja 


    ([Location 1540](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1540))
-
- 

Why does this happen? Puppet is a declarative language. Allowing variable reassignment would require us to rely on order in the file to determine the value of the variable, and order does not matter in a declarative language. #flashcard 


    ([Location 1541](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1541))
-
- 

you cannot redefine a variable inside the same scope it was defined in, like our node. #flashcard  #pink #rosa 


    ([Location 1543](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1543))
-
- 

At any given time, four scopes are available to Puppet: top scope, node scope, parent scope, and local scope. #flashcard  #pink #rosa 


    ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
-
- 

Top scope is anything declared in site.pp or imported manifests. #flashcard  #pink #rosa 


    ([Location 1545](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1545))
-
- 

Local scope is the scope of a single class or defined type. #flashcard  #pink #rosa 


    ([Location 1550](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1550))
-
- 

class ssh (   manage_package = false,   manage_service = false,   package_name   = $::ssh::params::sshd_package ) inherits ssh::params  {   if manage_package == true {     package { $package_name:       ensure => installed,     }   } #flashcard  #orange #naranja 


    ([Location 1585](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1585))
-
- 

to enforce the style guide. It is called puppet-lint #flashcard 


    ([Location 1615](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1615))
-
- 

node ' puppet.example.com ' {   include sudo } #flashcard  #orange #naranja 


    ([Location 1642](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1642))
-
- 

You can generate a blank puppet module using the syntax puppet module generate name-name, where the first name is the name of you or your organization, and the second is the name of the service you are managing, such as propuppet-amanda #flashcard 


    ([Location 1653](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1653))
-
- 

class ssh::install {   $package_name = $::osfamily  ?     'RedHat'  => "openssh-server",     'Debian'  => "openssh-server",     'Solaris' => "openssh",     },   package { 'ssh':     ensure => present,     name   => $package_name,   } } #flashcard  #orange #naranja 


    ([Location 1779](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1779))
-
- 

Selector matching is case-insensitive. #flashcard 


    ([Location 1808](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1808))
-
- 

a best practice we recommend that you move all your conditional checks to a separate class. #flashcard 


    ([Location 1825](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1825))
-
- 

case $::osfamily {     Solaris: {       $ssh_package_name = 'cswopenssh'       $ssh_service_config = '/etc/opt/csw/ssh/sshd_config'     }     Debian: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     RedHat: {       $ssh_package_name = 'openssh-server'       $ssh_service_config = '/etc/ssh/sshd_config'     }     default: {       fail("Module propuppet-ssh does not support osfamily: ${::osfamily}")     }   } #flashcard  #orange #naranja 


    ([Location 1890](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1890))
-
- 

It is a best practice to establish relationships with an entire class, rather than with a resource contained within another class, because this allows the internal structure of the class to change without refactoring the resource declarations related to the class. #flashcard 


    ([Location 1908](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1908))
-
- 

the require metaparameter tells Puppet that all the resources in the specified class must be processed prior to the current resource. #flashcard  #blue #azul 


    ([Location 1910](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1910))
-
- 

The notify metaparameter creates a notification relationship. If the current resource (the service’s configuration file) is changed, then Puppet should notify all the resources contained in the ssh::service class. In our current case, a “notification” will cause the service resources in the ssh::service class to restart, ensuring that if we change a configuration file, the service will be restarted and running with the correct, updated configuration. #flashcard  #blue #azul 


    ([Location 1912](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1912))
-
- 

class ssh::service {   include ssh::params   service { $::ssh::params::ssh_service_name:     ensure      => running,     hasstatus   => true,     hasresstart => true,     enable      => true,     require     => Class['ssh::config'],   } } #flashcard  #orange #naranja 


    ([Location 1944](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=1944))
-
- 

File {     owner => 'postfix',     group => 'postfix',     mode  => 0644,   } #flashcard  #orange #naranja 


    ([Location 2011](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2011))
-
- 

we specified the File resource type capitalized and without a title. This syntax is called a resource default, and it allows us to specify defaults for a particular resource type. #flashcard  #blue #azul 


    ([Location 2021](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2021))
-
- 

class ssh { require ssh::params include ssh::install include ssh::config include ssh::service } #flashcard  #orange #naranja 


    ([Location 2047](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2047))
-
- 

check the syntax of your ERB templates #flashcard 


    ([Location 2074](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2074))
-
- 

Our first class is our mysql class, contained in the init.pp file, where we load all the required classes for this module: class mysql (   $group                   = 'mysql',   $service_enabled  = true,   $service_running  = true,   $user                     = 'mysql' ){   class { 'mysql::install':     user  => $user,     group => $group,   }   class { 'mysql::config':     user  => $user,     group => $group,   }   class { 'mysql::service':     ensure  => $service_running,     enabled => $service_enabled,   } } #flashcard  #orange #naranja 


    ([Location 2106](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2106))
-
- 

class mysql::install (   $user,   $group ){ #flashcard  #orange #naranja 


    ([Location 2127](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2127))
-
- 

Definitions are collections of resources like classes, but unlike classes they can be specified and are evaluated multiple times on a host. They also accept parameters. #flashcard  #pink #rosa 


    ([Location 2232](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2232))
-
- 

Tip Remember that classes are singletons. They can be included multiple times on a node, but they will only be evaluated ONCE. A definition, because it takes parameters, can be declared multiple times, and each new declaration will be evaluated. #flashcard  #pink #rosa 


    ([Location 2233](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2233))
-
- 

The first definition define apache::vhost(   $docroot,   $port,   $priority,   $ssl=true,   $serveraliases = '',   $template='apache/vhost.conf.erb', ){   include apache   file {"/etc/apache2/sites-enabled/${priority}-${name}":     content => template($template),     owner   => 'root',     group   => 'root',     mode    => '0640',     require => Class['apache::install'],     notify  => Class['apache::service'],   } } #flashcard  #orange #naranja 


    ([Location 2236](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2236))
-
- 

The $name variable contains the name, also known as the title, of a declared defined resource. This is the value of the string before the colon when declaring the defined resource. The $title variable, which usually has the same value, is also available. #flashcard 


    ([Location 2258](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2258))
-
- 

Putting the $name variable as part of the name of the exec resource will solve this problem. #flashcard 


    ([Location 2265](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2265))
-
- 

autoloading. Puppet scans your module and loads any .pp file in the manifests directory that is named after the class it contains; for example, the install.pp file contains the apache::install class and so is autoloaded. The same thing happens with definitions: #flashcard  #pink #rosa 


    ([Location 2319](https://readwise.io/to_kindle?action=open&asin=B00I1X40FE&location=2319))
-