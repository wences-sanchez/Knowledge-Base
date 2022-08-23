tags:: O'Reilly-Learning, Docker, Videos

- ## Week 1: Introduction
	- ### Introduction to Local Development VS VirtualBox VS Docker -- WHY use docker?
		- The configuration of the DEV always tends to be different form PROD.
		- #### The local development environment
			- The problem is that the local PC of a dev can't provide the same things than a Server.
			- We can't rely on our local PCs
			- Its performance is worse
		- #### Virtual Machines
			- There is really no much support for them
			- An alternative is **Vagrant**
				- But its scripts to provision are very large
				- Also, speed is a negative factor on local environment
			- **Configuration drift** => differences between environments
		- #### Containers
			- A container is not so much different from a Virtual Machine
			- The main difference is that the processes run on the OS
			-