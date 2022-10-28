title:: Vagrant by HashiCorp (highlights)
author:: [[vagrantup.com]]
full-title:: "Vagrant by HashiCorp"
category:: #articles
url:: https://www.vagrantup.com/docs/multi-machine

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- Vagrant.configure("2") do |config|
	  config.vm.provision "shell", inline: "echo Hello"
	  
	  config.vm.define "web" do |web|
	    web.vm.box = "apache"
	  end
	  
	  config.vm.define "db" do |db|
	    db.vm.box = "mysql"
	  end
	  end
		- **Note**: How do you include *two* machines in one Vagrantfile in **Vagrant**?