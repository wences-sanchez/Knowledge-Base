# Vagrant by HashiCorp

deck:: [[Across-the-Net]]\
author:: [[vagrantup.com]]\
full-title:: "Vagrant by HashiCorp"\
category:: #articles\
url:: https://www.vagrantup.com/docs/multi-machine\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)

## Highlights
- 
 How do you include *two* machines in one Vagrantfile in **Vagrant**? #flashcard 
    Vagrant.configure("2") do |config|
     config.vm.provision "shell", inline: "echo Hello"
     config.vm.define "web" do |web|
     web.vm.box = "apache"
     end
     config.vm.define "db" do |db|
     db.vm.box = "mysql"
     end
     end

    
-
