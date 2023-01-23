# Ansible

deck:: [[O'Reilly-Learning::Ansible]]\
author:: [[None]]\
full-title:: "Ansible"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781098109141/)
## Highlights
### 1. Introduction
- in the playbook would look something like this:
	- name: Install nginx
	  id:: 63c669e1-9d62-4fc2-adce-b38f598fb0ba
	       package:
	       name: nginx
	       Ansible will do the following:
	       Generate a Python script that installs the NGINX package
	       Copy the script to web1, web2, and web3
	       Execute the script on web1, web2, and web3
	       Wait for the script to complete execution on all hosts
	       Ansible will then move to the next task in the list and go through these same four steps.
	       It’s important to note the following:
	       Ansible runs each task in parallel across all hosts.
	       Ansible waits until all hosts have completed a task before moving to the next task.
	       Ansible runs the tasks in the order that you specify them. #flashcard
-
- id:: 63c669e1-1e91-4965-8875-b9f7c4ec58fe
  
  Push-based
     Chef and Puppet are configuration management systems that use agents. They are pull-based by default. Agents installed on the servers periodically check in with a central service and download configuration information from the service. Making configuration management changes to servers goes something like this:
     You: make a change to a configuration management script.
     You: push the change up to a configuration management central service.
     Agent on server: wakes up after periodic timer fires.
     Agent on server: connects to configuration management central service.
     Agent on server: downloads new configuration management scripts.
     Agent on server: executes configuration management scripts locally that change server state.
     In contrast, Ansible is push-based by default. Making a change looks like this:
     You: make a change to a playbook.
     You: run the new playbook.
     Ansible: connects to servers and executes modules that change the state of the servers.
     As soon as you run the ansible-playbook command, Ansible connects to the remote servers and does its thing; this lowers the risk of random servers potentially breaking whenever their scheduled tasks fail to change things successfully. The push-based approach has a significant advantage: you control when the changes happen to the servers. You do not need to wait around for a timer to expire. Each step in a playbook can target one or a group of servers. You get more work done instead of logging into the servers by hand. #flashcard
-
### 2. Playbooks: A Beginning
- id:: 63c669e1-7efd-4ed6-8e89-214575743220
  
  When the Provisioner Runs
     The first time you run vagrant up, Vagrant will execute the provisioner and record that the provisioner was run. If you halt the virtual machine and then start it up, Vagrant remembers that it has already run the provisioner and will not run it a second time.
     You can force Vagrant to run the provisioner against a running virtual machine as follows:
     $ vagrant provision
     You can also reboot a virtual machine and run the provisioner after reboot:
     $ vagrant reload --provision
     Similarly, you can start up a halted virtual machine and have Vagrant run the provisioner:
     $ vagrant up --provision
     Or you can start up the virtual machine and not run the provisioner:
     $ vagrant up --no-provision
     We use these commands quite often to run playbooks from the command line, with a tag or a limit. #flashcard
-
### 3. Inventory: Describing Your Servers
- id:: 63c669e1-0524-41dc-90d6-0d5e6e49b4b2
   [Figure 3.2](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781098109141/files/assets/aur3_0302.png) #flashcard 
    To sum up, a playbook contains one or more plays. A play associates an unordered set of hosts with an ordered list of tasks. Each task is associated with exactly one module. Figure 3-2 depicts the relationships between playbooks, plays, hosts, tasks, and modules.
-
### 4. Variables and Facts
- id:: 63c669e1-7345-4256-aabc-e519e23ea5f8
  
  If the inventory file is marked executable, Ansible will assume it is a dynamic inventory script and will execute the file instead of reading it. #flashcard
-
- id:: 63c669e1-0396-40b0-bd8a-316c42ced8c4
  
  Finally, you’ll hear people talk about provisioning new servers. In the context of public clouds such as Amazon EC2, provisioning refers to spinning up new virtual machine instances or cloud-native software as a service (SaaS). Ansible has got you covered here, with modules for talking to clouds #flashcard
-
- id:: 63c669e1-2424-4120-b6c4-1b1048379cba
  
  No daemons
     There is no Ansible agent listening on a port. Therefore, when you use Ansible, there is no extra attack surface. (There is still an attack surface with software supply chain elements like Python libraries and other imported content.) #flashcard
-
- id:: 63c669e1-20aa-4492-998c-03766e795df5
   How can you ssh into a machine which is a Vagrant VM? #flashcard 
    $ ssh vagrant@127.0.0.1 -p 2222 \
     -i .vagrant/machines/default/virtualbox/private_key
-
- id:: 63c669e1-29eb-4b4f-bfc3-74e608493c47
  
  You had to type a lot to use Ansible to ping your test server. Fortunately, Ansible has ways to organize these sorts of variables, so you don’t have to put them all in one place. Right now, we’ll add one such mechanism, the ansible.cfg file, to set some defaults so we don’t need to type as much on the command line. #flashcard
-
- id:: 63c669e1-1bff-446b-bb2f-6a7ca2ae4303
  
  If we run a web server on port 80 of our Vagrant machine, we can access it at http://192.168.33.10.
     This configuration uses a Vagrant private network. The machine will be accessible only from the machine that runs Vagrant. You won’t be able to connect to this IP address from another physical machine, even if it’s on the same network as the machine running Vagrant. However, different Vagrant machines can connect to each other. #flashcard
-
- id:: 63c669e1-f87d-42be-b374-166c3051f1a3
   A loop example in Ansible #flashcard 
    Loop
     When you want to run a task with each item from a list, you can use loop. A loop executes the task multiple times, each time replacing item with different values from the specified list:
	- name: Copy TLS files
	       copy:
	       src: "{{ item }}"
	       dest: "{{ tls_dir }}"
	       mode: '0600'
	       loop:
	- "{{ key_file }}"
	- "{{ cert_file }}"
	       notify: Restart nginx
-
### 5. Introducing Mezzanine: Our Test Application
- id:: 63c669e1-aec4-4de2-a479-50839afdf610
  
  Sometimes, a task that’s running on one host needs the value of a variable defined on another host. Say you need to create a configuration file on web servers that contains the IP address of the eth1 interface of the database server, and you don’t know in advance what this IP address is. This IP address is available as the ansible_eth1.ipv4.address fact for the database server.
     The solution is to use the hostvars variable. This is a dictionary that contains all of the variables defined on all of the hosts, keyed by the hostname as known to Ansible. If Ansible has not yet gathered facts on a host, you will not be able to access its facts by using the hostvars variable, unless fact caching is enabled.1
     Continuing our example, if our database server is db.example.com, then we could put the following in a configuration template:
     {{ hostvars['db.example.com'].ansible_eth1.ipv4.address }}
     This evaluates to the ansible_eth1.ipv4.address fact associated with the host named db.example.com.
     HOSTVARS VERSUS HOST_VARS
     Please be warned that hostvars is computed when you run Ansible, while host_vars is a directory that you can use to define variables for a particular system. #flashcard
-
### 10. Callback Plugins
- id:: 63c669e1-09ed-4434-aa51-b6b1a1a2597c
  
  Ansible supports a collection of lookups for retrieving data from diverse sources. To list the lookups in your installed Ansible, try:
     $ ansible-doc -t lookup -l #flashcard
-
### 14. Quality Assurance with Molecule
- id:: 63c669e1-b96e-445a-a2c6-5223f0e653d0
  
  molecule init extends ansible-galaxy role init by creating a directory tree for a role with additional files, for testing with Molecule. The following command should get you started running Molecule:
     $ molecule init role my_new_role --driver-name docker #flashcard
-