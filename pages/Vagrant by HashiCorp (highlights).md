title:: Vagrant by HashiCorp (highlights)
deck:: [[Across-the-Net]]
author:: [[vagrantup.com]]
full-title:: "Vagrant by HashiCorp"
category:: #articles
url:: https://www.vagrantup.com/docs/multi-machine

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How do you include *two* machines in one Vagrantfile in **Vagrant**? #flashcard
		  id:: 4890af63-2766-4e43-8a52-c56e9dbe5262
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