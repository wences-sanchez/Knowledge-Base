# Practical Ansible 2

deck:: [[O'Reilly-Learning::Practical Ansible 2]]\
author:: [[None]]\
full-title:: "Practical Ansible 2"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/practical-ansible-2/9781789807462/ibis_generated_cover_thumbnail.jpg)

## Highlights
### Understanding how Ansible connects to hosts
- 
 [CODE] Do ping to a group of an inventory file with Ansible: #flashcard 
    $ ansible webservers -m ping

    
-
### Verifying the Ansible installation
- 
 [CODE] Display facts but with a filter: #flashcard 
    $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*"

    
-
- 
 [CODE] Display facts about your inventory: #flashcard 
    $ ansible frontends -i hosts -m setup | less

    
-
- 
 [CODE] Do a ping to the target hosts: #flashcard 
    $ ansible frontends -i hosts -m ping

    
-
