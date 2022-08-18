title:: Ansible: From Basics to Guru

- #tags #O'Reilly #Ansible
- ## Module 1: Getting Started
-
	- ### Lesson 1: Preparing your Managed Infrastructure
		- What is Ansible (generally)? #carta
			- Ansible is a configuration management tool
			- It is used  to manage configuration on a pre-deployed infrastructure
			- It's a DevOps tool
		- What is the control node? #carta
			- Where the Ansible software is installed
		- The control node needs Ansible installed
		- The manages nodes need SSH, a user account, privilege escalation (be careful with SSH keys).
		- DNS or /etc/hosts are generic solutions that provide hostname to IP address resolving
		- Ansible also needs an inventory:
			- To identify managed hosts
			- To define host groups to be used by Ansible
		- #### Understanding Ad-hoc Commands
			- With _command_ we can run any shell command in Ansible
		- #### 1.7 Configuring Linux Managed Hosts with Ad-hoc Commands
		- #### 1.9 Understanding ansible.cfg
			- You can put the settings in ansible.cfg instead of the playbooks or CLI
			- Se puede poner los datos que no queramos tener que escribir cada vez en el fichero **ansible.cfg**
	- ---
	- ### Lesson 2: Using Ad-hoc Commands
	- An ansible module is a Python script
	- In Ad-hoc commands, -m is for address a specific module and -a for module arguments
	-
	- ¿Cómo puedo consultar los módulos de Ansible desde la terminal?
		- **ansible-doc [-t module] -l** muestra todos los módulos
		- **ansible-doc ...** muestra un módulo específico que introduzcamos
	- ### Módulos más importantes de Ansible
		- **command**: For running arbitrary commands on the managed nodes
		- **shell**: Same as *command* but allows pipes and redirects
		- **package**: For managing packages
		- **user**: For user management
		-
		- But be aware of idempotency!!!
		- If a task founds that its change is already done, it doesn't fail. It just notifies *change: false*
	- ---
	- ### Lesson 3: Using Ansible Playbook
		- A playbook is a collection of plays
		- Ansible goes task by task, waiting every host to finishes it before moving on to the next.
		  
		  
		  
		  * `-vv` fails
		  * `-vvvv` complete debugging
		  
		  * If the desired state is the same, we'll see *OK*, otherwise we'll see *Changed*
		  
		  * Fact Gathering is only useful if we are using variables. We can disable it with `gather_facts: false` if don't
		  
		  ---
		  
		  #spaced
		  > Let's run it Ansible playbook on run and test httpd.yaml. As you can see, we are skipping the fact gathering that makes it really much faster. And then it's trying to install the package again. 
		  
		  > That's something that's not needed anymore because we have already done that in the play that we were just running. 
		  
		  > **But the thing is that behind package management there is yum/dnf on recent RedHat that needs to update package cash and stuff like that. And that always takes a minute or so.** So there we go start and enable service that also shoot not take too much time.
		  
		  ---
		  
		  #spaced
		  * If a task fails to run a specific host, the following ones are not executed unless we specify `ignore_errors: true`
		  
		  * There is no easy way to undo a playbook
		  
		  ---
## Lesson 4: Using Ansible Tower

* Ansible Tower has more features that are not in the CLI version:
1. Role-Based access control
2. Caching of passwords
3. Workflow designer

* Ansible automation platform is a very useful site =)

---
# Module 2: Developing Flexible Playbooks

#spaced
## Lesson 5: Working with Variables

* You should separate information from the code

* Las comillas para interpolar solo hacen falta si la variable está al principio de la línea

* Las variables se definen con:
```
vars:
user: lisa
tasks:
- ...
```

* Hay que tener en cuenta que las variables se convierten en valores al rodearlas con llaves. En cualquier sitio.

* Si usamos variables, el **gather_facts** es **necesario**

* There are different ways to define variables: #flashcard
1. In the play header using **vars:**
2. In the play header using an include with **vars_files:**
3. Using the **set_fact** module in a play
4. On the command line, using the **-e key=value** option
5. As inventory variables
6. As host or **host_group** variables
7. Using **vars_pronpt:** to request values from the user while running the playbook

2. We put the variables like this:
 `key: var`

3. **set_fact** is a module that can be used anywhere in the playbook (nice!). It's dynamic.
 We write it like this:
```
- name: ...
tasks:
- set_fact:
    my_var: my_value
- debug:
    msg: The value is {{ my_var }}
```

7. **vars_prompt** to sensitive info
 * When we specify `private: no`, the user can see the answer

```
- name: ...
vars_prompt:
- name: package
  prompt: Wich package do you want?
  private: no
```

* It is possible to put variables inside a file that matches a host or group and then just simply target to it in the `hosts:` section.

* **ansible_facts** es una variable!! Como un diccionario con:
`ansible_facts['key']['another_key']`	// Newest
`ansible_facts.key.another_key`		// Older but still

But is always recommended to use the ansible_facts key.

---
#spaced
### 5.6 Speeding up Fact Collection

> The issue is in some conditions, **fact collection** may be very **slow**. 
> And if that is happening because you are just working against lots of host, you can use a fact cache but setting up a fact cache is a bit of additional work and it has disadvantages.
> Because if you use facts from a cache, you don't have the up-to-date values. 
> If you are experiencing slow facts gathering, you should also ensure that **host name resolution** is set up on **all hosts**. 
> An easy way to do so is to make sure that on all of the managed hosts, there is an /etc/hosts file that allows for name resolution between all of the managed hosts.

* `$ ansible all -m copy -a "src=/etc/hosts dest=/etc/hosts`

---

* Cuando escribimos en YAML líneas con guiones, las líneas siguientes que están al mismo nivel están dentro del mismo item o elemento de esa lista. #spaced #daily-notes #Ansible

---
### 5.8 Using magic variables

* **hostvars** can be used to address facts or inventory variables from other hosts:
`{{ hostvars['machine2']['ansible_facts']...  }}`

#spaced
### 5.10 Ansible Vault

* With **ansible-vault create**, we create a file with variables. And that file is encrypted by a password.

* We have to add **--ask-vault-pass** to a CLI called playbook in order to run it.

* We can use **--vault-password-file=my_pass_file** if we don't want to type our password

---

#spaced
## Lesson 6: Using Conditionals

* Si una task falla, el handler **NO** se ejecutará
* Se puede cambianr con **force_handlers: yes**
* Si una task no cambia nada, el handler **NO** se ejecutará

* *ansible_distribution* shows the OS distro
### 6.5 Using Blocks

* **block:** is useful to group some tasks with a *when:*, for example

* **block:** ... **rescue:** ... **always:** ... // is used to make try-catchs
* But remember not to use idempotency!!
### 6.6 Using loop

* The **loop** syntax is preferred over **with_X**

* If you don't specify the list in the main section of the task (you use *loop*), the task will rerun N times
### 6.7 Managing Failure with the fail Module

* Use **fail** to express a negative output with a message. **failed_when** to know if it occured

* You have to use `ignore_errors: yes`

* With **fail** module, you can print an error message, indicating with **when: `<expr> ` the case.
* Using `<variable>.err` is a good idea to approach it.
### 6.8 Using the assert Module

* With the assert Module you can set *fail* and *ok* messages

* To see all the facts of a machine:
**$ ansible `<host>` -m setup
---

#spaced
## Lesson 7: Managing Files

* **Synchronize** is more efficient than **copy**
* But requires *rsync* in both hosts

* We use *lineinfile* to add a line to a file. Also *blockinfile* is similar

* With **find** we can search inside a file as we do in Unix

* When we are in a conditional, we don't put "'
- The **fetch** module lets us to copy files from remote to local
  
  ---
- How can you copy content from a remote machine to a local host in Ansible? #flashcard
	- With the **fetch** module
- What is the exact syntax of register a variable in Ansible? #flashcard
	- With: `register: <var>` inside the parent module
- Remember to remove the `{ }` when dealing with conditionals in Ansible!!!!
- And include the `' '`#spaced 
  
  
  
  ---
## Lesson 8: Using Roles and Collections
### Collections
- Collections are new in Ansible
### Roles
- The pre_task are executed before the roles
- `$ ansible-galaxy role install <role_name>`
-
- Its website is galaxy.ansible.com
- `$ ansible-galaxy role list` lists all the roles installed
- **default** can be overwritten by **vars** in the roles directory
- The tasks/main.yml contains the principal part
- Inside taks/, we can organize our code in different files .yml
- templates/ dir contains the templates
- In a playbook, it's a collection of tasks,
	- `include_vars: # ...`
	- `include tasks: # ...`
- ![[Pasted image 20220729132914.png]]
- Collections are NOT a default part of Ansible2.9
- You can use a requirements.ym file to install multiple
- **default** values are for values that are going to crash the role if not
- We have to include the rol inside a playbook in order to run it
  
  ---
# Module 3: Advanced Ansible Management
## Lesson 9: Ansible Best Practices and Optimization
- What is the difference between include and import in Ansible? #flashcard
	- *Include* is dynamic, *Import* is added statically (before the actual play is started).