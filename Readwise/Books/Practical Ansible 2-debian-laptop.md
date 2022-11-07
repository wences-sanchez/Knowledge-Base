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
- id:: 6363992b-e814-4829-a099-16c1ff0a3f32
   [CODE] Do ping to a group of an inventory file with Ansible: #flashcard 
    $ ansible webservers -m ping
-
### Verifying the Ansible installation
- id:: 6363992b-618c-4f16-ad73-21174f9e7264
   [CODE] Display facts but with a filter: #flashcard 
    $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*"
-
- id:: 6363992b-71b5-4cc2-b2fb-9a6e7cc22694
   [CODE] Display facts about your inventory: #flashcard 
    $ ansible frontends -i hosts -m setup | less
-
- id:: 6363992b-c92b-49d2-a535-ab1552dda0a9
   [CODE] Do a ping to the target hosts: #flashcard 
    $ ansible frontends -i hosts -m ping
-