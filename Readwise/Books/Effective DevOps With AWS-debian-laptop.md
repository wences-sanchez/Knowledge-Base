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
- Lastly, we are going to edit the ansible.cfg file that is present in the root directory of the ansible repository to specify the location of the library folder as follows:
# update ansible.cfg 
id:: 63639918-6216-44fd-a861-17fa75e94a2e
   [defaults]
   inventory = ./ec2.py 
   remote_user = ec2-user 
   become = True 
   become_method = sudo 
   become_user = root 
   nocows = 1
   library = library #flashcard
-