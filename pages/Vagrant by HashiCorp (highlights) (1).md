title:: Vagrant by HashiCorp (highlights) (1)
author:: [[vagrantup.com]]
full-title:: "Vagrant by HashiCorp"
category:: #articles
url:: https://www.vagrantup.com/docs/multi-machine

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- How do you include *two* machines in one Vagrantfile in **Vagrant**? #flashcard
		- Vagrant.configure("2") do |config|
		  config.vm.provision "shell", inline: "echo Hello"
		  
		  config.vm.define "web" do |web|
		    web.vm.box = "apache"
		  end
		  
		  config.vm.define "db" do |db|
		    db.vm.box = "mysql"
		  end
		  end
	- -