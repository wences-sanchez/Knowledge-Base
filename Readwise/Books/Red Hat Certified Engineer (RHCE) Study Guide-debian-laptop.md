# Red Hat Certified Engineer (RHCE) Study Guide

deck:: [[O'Reilly-Learning::Red Hat Certified Engineer (RHCE) Study Guide]]\
author:: [[None]]\
full-title:: "Red Hat Certified Engineer (RHCE) Study Guide"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781484268612/)
## Highlights
### 1. Understanding Ansible and the Red Hat RHCE
- id:: 6363992e-f94f-4444-bb43-bf4331bedc99
  
  NoteThe word “ansible” was first used by the author Ursula K. Le Guin in her 1966 novel Rocannon’s World. As a contraction of the word “answerable,” it references fictional devices that can send messages over interstellar distances to managed systems. Ansible from Red Hat may not work over interstellar distances, but it certainly does manage devices usually located on planet Earth. #flashcard  #curiosities
-
### 2. Working with the Ansible Configuration
- id:: 6363992e-6073-46cd-bb24-d24bafbb1781
   Where can I find Ansible configuration info? #flashcard 
    NoteThe effective configuration for Ansible can be determined from the command ansible --version. Run this command from the directory in which you would execute the other Ansible commands for your project.
-
- id:: 6363992e-9737-4cdc-9851-a62445f1e02a
   About the order of Ansible configuration files and its precedence. #flashcard 
    The effective Ansible configuration is applied on the first found – first applied basis. It is important to note that only one configuration can be active and applied and that these configurations are NOT cumulative. The search order is shown in the following bulleted list, with the search from the top of the list to the bottom. The least effective configuration is the /etc/ansible/ansible.cfg at the bottom of the list.
     ANSIBLE_CONFIG: If the environment variable, ANSIBLE_CONFIG, is set, then this configuration is used. Default options are used for any configuration option not set. This default behavior is common with all configurations.
     ansible.cfg: If there is an ansible.cfg file in the current working directory (CWD), AND the ANSIBLE_CONFIG environment variable has not been set, then it is this file that is used.
     ~/.ansible.cfg: If no previously listed configuration is detected, Ansible will check the current user’s home directory for a hidden file called .ansible.cfg. If the file exists, then it becomes the third choice within the hierarchy. This is a great option for a user to create, acting as a default for all user projects except those needing a little tweaking. Those needing tweaks can have a configuration file added to the project directory; alternatively, as you will learn, variables can be set to overwrite certain options as can settings within Ansible Playbooks. So, there are lots of options to tweak the configuration as needed.
     /etc/ansible/ansible.cfg: The default file where no other configuration is in place or detected. The file itself only contains comments, meaning that there are no effective settings from the file. Don’t despair though; this will result in the default settings being applied for all settings. The file itself is not wasted, acting as great documentation for the configuration files that you may want to implement.
-
- id:: 6363992e-5731-41cf-9093-6e2b11077d42
  
  ImportantIt is very important for Ansible security that a configuration file is never loaded from a world-writable directory. If a directory is world writable, (where others have the write permission), it is possible that a rogue ansible.cfg file is added to your working directory by another user either deliberately or by mistake #flashcard
-
- id:: 6363992e-0b50-475b-b775-09447fca8480
   How do you see the Ansible full config? #flashcard 
    We will also be able to print the effective settings, that is, the default settings. For this, we have access to the command ansible-config, which has a stunning three subcommands:
     ansible-config view: Print the contents of the current effective Ansible configuration.
     ansible-config dump: Print the effective settings, which are made up from explicit settings from the effective files and the default settings where an option is unset.
     ansible-config list: This fully details the settings that can be made, either through variables or via directives in the configuration file or Playbook.
-
- id:: 6363992e-3a13-4b89-ade8-b6228ba1b4ef
   When testing if the Ansible configuration parameters are input correctly. #flashcard 
    We do have to take care with this command, as there is absolutely no checking of the section headers we have used or of the key or values supplied. The file will print as long as it matches the INI file format. Checking the effective settings with the dump subcommand is so much more useful, especially when we filter with the --only-changed option. Come on; I will show you.
     $ ansible-config dump --only-changed
     DEFAULT_BECOME(/home/tux/.ansible.cfg) = True
     DEFAULT_BECOME_METHOD(/home/tux/.ansible.cfg) = sudo
     DEFAULT_HOST_LIST(/home/tux/.ansible.cfg) = ['/home/tux/inventory']
     DEFAULT_REMOTE_USER(/home/tux/.ansible.cfg) = ansible
     Listing 2-16Viewing Settings Changed from the Default
     The output now also confirms that the settings are valid and usable by Ansible. If the key or header is not recognized, then it does not change anything and the section header or setting is not effective. If we find that we do not see the option or options that we are looking for within the output, it is likely that our fat fingers have got somewhat in the way of perfection.
-