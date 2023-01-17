# Effective DevOps With AWS

deck:: [[O'Reilly-Learning::Effective DevOps With AWS]]\
author:: [[Yogesh Raheja, Giuseppe Borgese, Nathaniel Felsen]]\
full-title:: "Effective DevOps With AWS"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781789539974/)

## Highlights
### Importing a custom library to Ansible for AWS CodeDeploy
- 

Lastly, we are going to edit the ansible.cfg file that is present in the root directory of the ansible repository to specify the location of the library folder as follows:
     # update ansible.cfg 
     [defaults]
     inventory = ./ec2.py 
     remote_user = ec2-user 
     become = True 
     become_method = sudo 
     become_user = root 
     nocows = 1
     library = library #flashcard 


    
-
### Key characteristics of a DevOps culture
- 

As we have noted, a DevOps culture relies on a certain number of principles. These principles are to source control (version control) everything, automate whatever is possible, and measure everything. #flashcard 


    
-
### Questions
- 

Questions
     What is DevOps?
     What is DevOps – IaC?
     List the key characteristics of a DevOps culture.
     What are the three major service models in the cloud?
     What is the AWS cloud? #flashcard 


    
-
