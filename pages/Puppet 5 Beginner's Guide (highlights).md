title:: Puppet 5 Beginner's Guide (highlights)
deck:: [[O'Reilly-Learning::Puppet 5 Beginner's Guide]]
author:: [[John Arundel]]
full-title:: "Puppet 5 Beginner's Guide"
category:: #books

tags:: O'Reilly-Learning Puppet

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 1. Getting started with Puppet
	- 2. Creating your first manifests
	- 4. Understanding Puppet resources
	- 8. Classes, roles, and profiles
	- 9. Managing files with templates
	- Using templates in your manifests
		- -
		- Why not just use containers?Containers! Is there any word more thrilling to the human soul? Many people feel as though containers are going to make configuration management problems just go away. This feeling rarely lasts beyond the first few hours of trying to containerize an app. Yes, containers make it easy to deploy and manage software, but where do containers come from? It turns out someone has to build and maintain them, and that means managing Dockerfiles, volumes, networks, clusters, image repositories, dependencies, and so on. In other words, configuration. There is an axiom of computer science which I just invented, called The Law of Conservation of Pain. If you save yourself pain in one place, it pops up again in another. Whatever cool new technology comes along, it won't solve all our problems; at best, it will replace them with refreshingly different problems.Yes, containers are great, but the truth is, container-based systems require even more configuration management. You need to configure the nodes that run the containers, build and update the container images based on a central policy, create and maintain the container network and clusters, and so on. #flashcard
		- -
		- -
		- If you want to see what change Puppet would actually make to the file, you can use the --show_diff option: #flashcard
		- -
		- -
		- Creating or managing permissions on a directory is a common task, and Puppet uses the file resource to do this too. If the value of the ensure attribute is directory, the file will be a directory (file_directory.pp):
		  
		  file { '/etc/config_dir':
		  ensure => directory,
		  }
		  As with regular files, you can use the owner, group, and mode attributes to control access to directories. #flashcard
		- -
		- -
		- # Manage NTP
		  class pbg_ntp_params (
		  String $version = 'installed',
		  ) {
		  ensure_packages(['ntp'],
		    {
		      'ensure' => $version,
		    }
		  )
		  } #flashcard
			- Example of class definition in Puppet
		- -
		- -
		- The following example shows what these markers look like (aws_credentials.epp):
		  
		  aws_access_key_id = <%= $aws_access_key %>
		  Everything outside the <%= and %> delimiters is literal text and will be rendered as-is by Puppet. #flashcard
			- Example of syntax of templates in Puppet
		- -
		- -
		- To reference a template file from within a module (for example, in our NTP module from Chapter 7, Mastering modules), put the file in the modules/pbg_ntp/templates/ directory, and prefix the filename with pbg_ntp/, as in the following example:
		  
		  file { '/etc/ntp.conf':
		  content => epp('pbg_ntp/ntp.conf.epp'),
		  } #flashcard
		- -
	- What is Puppet?
		- -
		- Because you can't necessarily tell in advance what applying a Puppet manifest will change on the system, it's a good idea to do a dry run first. Adding the --noop flag to puppet apply will show you what Puppet would have done, without actually changing anything #flashcard
		- -
	- Exec resources
	- Defined resource types
		- -
		- Puppet programs are called manifests #flashcard
		- -
	- Services
		- -
		- While the other resource types we've seen so far (file, package, service, user, ssh_authorized_key, and cron) have modeled some concrete piece of state on the node, such as a file, the exec resource is a little different. An exec allows you to run any arbitrary command on the node. This might create or modify state, or it might not; anything you can run from the command line, you can run via an exec resource. #flashcard
		- -
		- -
		- You can see that instead of the class keyword, we use the define keyword. This tells Puppet that we are creating a defined resource type instead of a class. The type is called user_with_key, and once it's defined, we can declare as many instances of it as we want, just like any other Puppet resource: #flashcard
			- Differences between class and defined resource in Puppet
		- -
		- -
		- called declarative style #flashcard
		- -
		- -
		- If you're struggling to remember all the different attributes of all the different resources, Puppet has a built-in help feature that will remind you. Run the following command, for example:
		  
		  puppet describe service
		  This will give a description of the service resource, along with a complete list of attributes and allowed values. This works for all built-in resource types as well as many provided by third-party modules. To see a list of all the available resource types, run the following command:
		  
		  puppet describe --list #flashcard
		- -
		- -
		- Suppose you only want an exec resource to be applied under certain conditions. For example, a command which processes incoming data files only needs to run if there are data files waiting to be processed. In this case, it's no good adding a creates attribute; we want the existence of a certain file to trigger the exec, not prevent it.
		  
		  The onlyif attribute is a good way to solve this problem. It specifies a command for Puppet to run, and the exit status from this command determines whether or not the exec will be applied. On Unix-like systems, commands generally return an exit status of zero to indicate success and a non-zero value for failure. The following example shows how to use onlyif in this way (exec_onlyif.pp):
		  
		  exec { 'process-incoming-cat-pictures':
		  command => '/usr/local/bin/cat-picture-generator --import /tmp/incoming/*',
		  onlyif  => '/bin/ls /tmp/incoming/*',
		  }
		  The exact command isn't important here, but let's assume it's something that we would only want to run if there are any files in the /tmp/incoming/ directory.
		  
		  The onlyif attribute specifies the check command which Puppet should run first, to determine whether or not the exec resource needs to be applied. If there is nothing in the /tmp/incoming/ directory, then ls /tmp/incoming/* will return a non-zero exit status. Puppet interprets this as failure, so does not apply the exec resource. #flashcard
		- -
		- -
		- Tip
		  Remember this rule of thumb when deciding whether to create a class or a defined resource type: if it's reasonable to have more than one instance on a given node, it should be a defined resource type, but if there will only ever be one instance, it should be a class. #flashcard
		- -
		- -
		- It's worth noting that there are two different ways to use Puppet. The first way, known as agent/master architecture, uses a special node dedicated to running Puppet, which all other nodes contact to get their configuration. #flashcard
		- -
		- -
		- You might have noticed a new attribute, called notify, in the file resource in the previous example:
		  
		  file { '/etc/mysql/mysql.cnf':
		  source => '/examples/files/mysql.cnf',
		  notify => Service['mysql'],
		  }
		  What does this do? Imagine you've made a change to the mysql.cnf file and applied this change with Puppet. The updated file will be written to a disk, but because the mysql service is already running, it has no way of knowing that its config file has changed. Therefore, your changes will not actually take effect until the service is restarted. However, Puppet can do this for you if you specify the notify attribute on the file resource. The value of notify is the resource to notify about the change, and what that involves depends on the type of resource that's being notified. When it's a service, the default action is to restart the service. #flashcard
		- -
	- 5. Variables, expressions, and facts
	- Summary
		- -
		- The other way, known as stand-alone Puppet or masterless, does not need a special Puppet master node. Puppet runs on each individual node and does not need to contact a central location to get its configuration. Instead, you use Git, or any other way of copying files to the node, such as SFTP or rsync, to update the Puppet manifests on each node. #flashcard
		- -
	- Distributing Puppet manifests
		- -
		- The dollar sign ($) tells Puppet that what follows is a variable name. Variable names must begin with a lowercase letter or an underscore, though the rest of the name can also contain uppercase letters or numbers.
		  
		  A variable can contain different types of data; one such type is a String (like php7.0-cli), but Puppet variables can also contain Number or Boolean values (true or false). Here are a few examples (variable_simple.pp):
		  
		  $my_name = 'Zaphod Beeblebrox'
		  $answer = 42
		  $scheduled_for_demolition = true #flashcard
		- -
		- -
		- We can summarize the rules by saying that nodes should only include roles, and roles should only include profiles. #flashcard
		- -
		- -
		- Another way to use Puppet is to do without the master server altogether, and use Git to distribute manifests to client nodes, which then runs puppet apply to update their configuration. This stand-alone Puppet architecture doesn't require a dedicated Puppet master server, and there's no single point of failure. #flashcard
		- -
		- -
		- To interpolate (that is, to insert the value of) a variable in a string, prefix its name with a $ character and surround it with curly braces ({}). This tells Puppet to replace the variable's name with its value in the string. #flashcard
		- -
		- -
		- A resource declaration follows this pattern:RESOURCE_TYPE { TITLE:
		  ATTRIBUTE => VALUE,
		  ...
		  } #flashcard
		- -
	- Fetching and applying changes automatically
		- -
		- A hash, also known as a dictionary in some programming languages, is like an array, but instead of just being a sequence of values, each value has a name (variable_hash.pp):
		  
		  $heights = {
		  'john'    => 193,
		  'rabiah'  => 120,
		  'abigail' => 181,
		  'melina'  => 164,
		  'sumiko'  => 172,
		  }
		  
		  notice("John's height is ${heights['john']}cm.") #flashcard
		- -
	- Managing packages
		- -
		- In a stand-alone Puppet architecture, each node needs to automatically fetch any changes from the Git repo at regular intervals, and apply them with Puppet. #flashcard
		- -
	- Introducing expressions
		- -
		- package { 'cowsay':
		  ensure => installed,
		  } #flashcard
		- -
		- -
		- The if statement allows you to take a yes/no decision based on the value of a Boolean expression. But if you need to make a choice among more than two options, you can use a case statement instead (case.pp):
		  
		  $webserver = 'nginx'
		  case $webserver {
		  'nginx': {
		    notice("Looks like you're using Nginx! Good choice!")
		  }
		  'apache': {
		    notice("Ah, you're an Apache fan, eh?")
		  }
		  'IIS': {
		    notice('Well, somebody has to.')
		  }
		  default: {
		    notice("I'm not sure which webserver you're using!")
		  }
		  } #flashcard
		- -
		- -
		- sudo puppet apply /examples/package.pp #flashcard
		- -
	- Finding out facts
		- -
		- If you want to see what version of a package Puppet thinks you have installed, you can use the puppet resource tool:puppet resource package openssl
		  package { 'openssl':
		  ensure => '1.0.2g-1ubuntu4.8',
		  } #flashcard
		- -
		- -
		- You can access Facter facts in your manifest using the facts hash. This is a Puppet variable called $facts which is available everywhere in the manifest, and to get a particular fact, you supply the name of the fact you want as the key (facts_hash.pp):
		  
		  notice($facts['kernel'])
		  On the Vagrant box, or any Linux system, this will return the value Linux.
		  
		  In older versions of Puppet, each fact was a distinct global variable, like this:
		  
		  notice($::kernel)
		  You will still see this style of fact reference in some Puppet code, though it is now deprecated and will eventually stop working, so you should always use the $facts hash instead. #flashcard
		- -
		- -
		- puppet resource -e package openssl #flashcard
		- -
	- Iterating over arrays
		- -
		- Let's look at a schematic version of an each loop:
		  
		  ARRAY.each | ELEMENT | {
		  BLOCK
		  } #flashcard
		- -
	- 6. Managing data with Hiera
		- -
		- In your manifest, you query the database using the lookup() function, as in the following example (lookup.pp):
		  
		  file { lookup('backup_path', String):
		  ensure => directory,
		  }
		  The arguments to lookup are the name of the Hiera key you want to retrieve (for example backup_path), and the expected data type (for example String). #flashcard
		- -
	- Types of Hiera data
		- -
		- example:
		  
		  cobbler_config:
		  manage_dhcp: true
		  pxe_just_once: true
		  Each key-value pair in the hash is listed, indented on its own line. The cobbler_config hash has two keys, manage_dhcp and pxe_just_once. The value associated with each of those keys is true.
		  
		  When you call lookup('cobbler_config', Hash) in a manifest, the data will be returned as a Puppet hash, and you can reference individual values in it using the normal Puppet hash syntax #flashcard
			- Also with dot notation usage
		- -
	- The hierarchy
		- -
		- usually in common.yaml), but override them in specific circumstances. For example, you can set a data source in the hierarchy based on the value of a Puppet fact, such as the hostname:
		- -
	- Creating resources with Hiera data
		- -
		- lookup('users', Array[String]).each | String $username | {
		  user { $username:
		    ensure => present,
		  }
		  }
		  Combining Hiera data with resource iteration is a powerful idea. This short manifest could manage all the users in your infrastructure, without you ever having to edit the Puppet code to make changes. To add new users, you need only edit the Hiera data. #flashcard
		- -
		- -
		- When we call each on this hash, we specify two parameters to the loop instead of one:
		  
		  | String $username, Hash $attrs |
		  As we saw in Chapter 5, Variables, expressions, and facts, when iterating over a hash, these two parameters receive the hash key and its value, respectively.
		  
		  Inside the loop, we create a user resource for each element of the hash:
		  
		  user { $username:
		  * => $attrs,
		  }
		  You may recall from the previous chapter that the * operator (the attribute splat operator) tells Puppet to treat $attrs as a hash of attribute-value pairs. #flashcard
		- -
	- 7. Mastering modules
		- -
		- r10k is the de facto standard module manager for Puppet deployments, and we'll be using it to manage modules throughout the rest of this book #flashcard
			- What is r10k in Puppet?
		- -
		- -
		- you can use the generate-puppetfile tool to find out what dependencies you need so that you can add them to your Puppetfile. #flashcard
		- -
	- Using modules in your manifests
		- -
		- Next comes a resource declaration:
		  
		  mysql::db { 'cat_pictures':
		  user     => 'greebo',
		  password => 'tabby',
		  host     => 'localhost',
		  grant    => ['SELECT', 'UPDATE'],
		  }
		  As you can see, this looks just like the built-in resources we've used before, such as the file and package resources. In effect, the mysql module has added a new resource type to Puppet: mysql::db. This resource models a specific MySQL database: cat_pictures in our example. #flashcard
		- -
	- Exploring the standard library
		- -
		- When you declare the same package resource in more than one place, Puppet will give an error message and refuse to run. If the package is declared by ensure_packages(), however, Puppet will run successfully. #flashcard
		- -
		- -
		- If you need to pass additional attributes to the package resource, you can supply them in a hash as the second argument to ensure_packages(), like this (package_ensure_params.pp):
		  
		  ensure_packages(['cowsay'],
		  {
		    'ensure' => 'latest',
		  }
		  ) #flashcard
		- -
		- -
		- The dirname() function is very useful if you have a string path to a file or directory and you want to reference its parent directory, for example to declare it as a Puppet resource (dirname.pp):
		  
		  $file = '/var/www/vhosts/mysite'
		  notice(dirname($file))
		- -
		- -
		- With the pry gem installed in Puppet's context, you can call pry() at any point in your code. When you apply the manifest, Puppet will start an interactive Pry shell at the point where the pry() function is called. You can then run the catalog command to inspect Puppet's catalog #flashcard
		- -
	- Writing your own modules
		- -
		- puppet:///modules/pbg_ntp/ntp.conf
		  We haven't seen this kind of file source before, and it's generally only used within module code. The puppet:// prefix indicates that the file comes from within the Puppet repo, and the path /modules/pbg_ntp/ tells Puppet to look within the pbg_ntp module for it. #flashcard
		- -
		- -
		- We can use r10k to install our new module, just as we did with the Puppet Forge modules, with one small difference. Since our module isn't on the Puppet Forge (yet), just specifying the name of the module in our Puppetfile isn't enough; we need to supply the Git URL so that r10k can clone the module from GitHub.
		  
		  Add the following mod statement to your Puppetfile (using your GitHub URL instead of mine):
		  mod 'pbg_ntp',
		  :git => 'https://github.com/bitfield/pbg_ntp.git',
		  :tag => '0.1.1' #flashcard
		- -
		- -
		- The following example shows a class definition, which makes the class available to Puppet, but does not (yet) apply any of its contained resources:
		  
		  class CLASS_NAME {
		  ...
		  }
		  The following example shows a declaration of the CLASS_NAME class. A declaration tells Puppet to apply all the resources in that class (and the class must have already been defined):
		  
		  include CLASS_NAME #flashcard
		- -