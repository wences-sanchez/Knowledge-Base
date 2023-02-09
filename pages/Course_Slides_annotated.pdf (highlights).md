title:: Course_Slides_annotated.pdf (highlights)
author:: [[]]
full-title:: "Course_Slides_annotated.pdf"
category:: #books

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- Esta es una nota emergente :) #card
		- “DevOps is a software engineering culture and practice that aims at unifying software development (Dev) and software operation (Ops)... DevOps aims at shorter development cycles, increased deployment frequency, more dependable releases, in close alignment with business objectives.”
		- (Page 3)
	- -
	- -
	- Which goals share dev and ops? #card
		- With DevOps, Dev and Ops work together and share the same goals.
		- (Page 13)
	- -
	- -
	- Dev and Ops share the same goals #ñspace
		- (Page 14)
	- -
	- -
	- What are the shared goals of dev and ops? #card
		- In a DevOps culture, devs care about stability as well as speed, and ops care about speed as well as stability.
		- (Page 15)
	- -
	- -
	- What is the relation between my IDE and the pipeline automation? #card
		- Build automation is independent of an IDE • Even if you can build within the IDE, it should be able to work the same way outside of the IDE
		- (Page 28)
	- -
	- -
	- What is the relation between configuration and build automation? #card
		- As much as possible, build automation should be agnostic of the configuration of the machine that it is built on
		- (Page 28)
	- -
	- -
	- What is CI? #card
		- Continuous Integration (CI): the practice of frequently merging code changes done by developers
		- (Page 31)
	- -
	- -
	- > Wheter it may be deployed or not, it's an option that every company chooses #card
		- Continuous Delivery (CD): the practice of continuously maintaining code in a deployable state
		- (Page 35)
	- -
	- -
	- Regardless of whether or not the decision is made to deploy, the code is always in a state that is able to be deployed. #ñspace
		- (Page 35)
	- -
	- -
	- What is Continous Deployment? #card
		- Continuous Deployment: the practice of frequently deploying small code changes to production
		- (Page 36)
	- -
	- -
	- Stages of build automation. #card
		- Each version of the code goes through a series of stages such as automated build, automated testing, and manual acceptance testing. The result of this process is an artifact or package that is able to be deployed.
		- (Page 37)
	- -
	- -
	- An advantage of CD&D #card
		- Reliable rollbacks – Robust automation means rollbacks are a reliable way to ensure stability for customers, and rollbacks don’t hurt developers because they can roll forward with a fix as soon as they have one.
		- (Page 38)
	- -
	- -
	- What is IaC? #card
		- m
		- (Page 40)
	- -
	- -
	- Infrastructure as Code (IaC): manage and provision infrastructure through code and automation. #ñspace
		- (Page 40)
	- -
	- -
	- Benefits of IaC.
	  
	  > With IaC, you can automate the tasks instead of manually go into every single machine. This is better because is less error-prone and a lot more straighforward. Ansible is a tool example #card
		- Consistency in creation and management of resources – The same automation will run the same way every time. Reusability – Code can be used to make the same change consistently across multiple hosts and can be used again in the future. Scalability – Need a new instance? You can have one configured exactly the same way as the existing instances in minutes (or seconds). Self-documenting – With IaC, changes to infrastructure document themselves to a degree. The way a server is configured can be viewed in source control, rather than being a matter of who logged in to the server and did something. Simplify the complexity – Complex infrastructures can be stood up quickly once they are defined as code. A group of several interdependent servers can be provisioned on demand.
		- (Page 42)
	- -
	- -
	- Configuration Management is done by tools, not manually. 
	  In the cloud, Configuration Management is crucial because there are so many things to configure..
	  You can make good use of version control.
	  Don't need to go machine by machine, also with the help of IaC #card
		- Configuration Management: maintaining and changing the state of pieces of infrastructure in a consistent, maintainable, and stable way
		- (Page 44)
	- -
	- -
	- What is orchestration?
	  
	  > With the help of tools, you can orchestrate a server resources by adding to the service more resource nodes programatically (or even automatically if you want) so that the application could use less (or more) resources dinamically. #card
		- Orchestration: automation that supports processes and workflows, such as provisioning resources
		- (Page 48)
	- -
	- -
	- What is monitoring?
	  
	  > Not only of post-mortem logs, but also with resources which are decreasing (before they become critical) #card
		- Monitoring: The collection and presentation of data about the performance and stability of services and infrastructure
		- (Page 52)
	- -
	- -
	- What are microservices?
	  
	  > We build one small module which is independent of every other and interacts by an API. "Every feature could be like a new module"
	  This module could be write even in other language. #card
		- Microservices: A microservice architecture breaks an application up into a collection of small, loosely-coupled services
		- (Page 56)
	- -
	- -
	- Containers VS VMs #card
		- Containers – Lightweight, isolated packages containing everything needed to run a piece of software • Require fewer resources than VMs – VMs contain an entire OS plus virtual versions of all the hardware • Containers have the bare minimum needed to run the software • Docker – Docker is currently the leading container technology
		- (Page 77)
	- -