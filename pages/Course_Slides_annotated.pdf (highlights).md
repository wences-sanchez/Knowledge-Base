title:: Course_Slides_annotated.pdf (highlights)
deck:: [[Other-Books::Course_Slides_annotated.pdf]]
author:: [[]]
full-title:: "Course_Slides_annotated.pdf"
category:: #books

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Esta es una nota emergente :) #flashcard
		  id:: d5d7aa02-832a-4972-9026-0b12d79ec916
			- “DevOps is a software engineering culture and practice that aims at unifying software development (Dev) and software operation (Ops)... DevOps aims at shorter development cycles, increased deployment frequency, more dependable releases, in close alignment with business objectives.”
		- (Page 3)
	- -
	- -
		- Which goals share dev and ops? #flashcard
		  id:: 761cfec6-7b63-40f2-98e0-d7d9123979f9
			- With DevOps, Dev and Ops work together and share the same goals.
		- (Page 13)
	- -
	- -
		- Dev and Ops share the same goals #flashcard
		  id:: 5fa80c6e-96f6-4dd6-81dc-4db85f981536
		- (Page 14)
	- -
	- -
		- What are the shared goals of dev and ops? #flashcard
		  id:: 79fe8ee6-1ac4-426c-aedc-e133857997d8
			- In a DevOps culture, devs care about stability as well as speed, and ops care about speed as well as stability.
		- (Page 15)
	- -
	- -
		- What is the relation between my IDE and the pipeline automation? #flashcard
		  id:: cf026035-179e-457d-b4dd-e40b7edf5eb8
			- Build automation is independent of an IDE • Even if you can build within the IDE, it should be able to work the same way outside of the IDE
		- (Page 28)
	- -
	- -
		- What is the relation between configuration and build automation? #flashcard
		  id:: 7333e106-b6e5-40bf-a4de-59b59533e0f5
			- As much as possible, build automation should be agnostic of the configuration of the machine that it is built on
		- (Page 28)
	- -
	- -
		- What is CI? #flashcard
		  id:: 56e578a9-c6b7-452b-b610-ff5f62b1f1fa
			- Continuous Integration (CI): the practice of frequently merging code changes done by developers
		- (Page 31)
	- -
	- -
		- id:: af80519e-3281-40c7-ba13-41167ffd6e17
		  > Wheter it may be deployed or not, it's an option that every company chooses #flashcard
			- Continuous Delivery (CD): the practice of continuously maintaining code in a deployable state
		- (Page 35)
	- -
	- -
		- Regardless of whether or not the decision is made to deploy, the code is always in a state that is able to be deployed. #flashcard
		  id:: 5883e9a7-5a55-4a2c-b615-a7a70eec7287
		- (Page 35)
	- -
	- -
		- What is Continous Deployment? #flashcard
		  id:: 4c1b0169-6dad-46ed-9693-1bda252799cd
			- Continuous Deployment: the practice of frequently deploying small code changes to production
		- (Page 36)
	- -
	- -
		- Stages of build automation. #flashcard
		  id:: 9d246ee2-d791-40e5-97f9-9b8042215607
			- Each version of the code goes through a series of stages such as automated build, automated testing, and manual acceptance testing. The result of this process is an artifact or package that is able to be deployed.
		- (Page 37)
	- -
	- -
		- An advantage of CD&D #flashcard
		  id:: 65f3c3bf-136b-4e1d-b5b2-185b03051db0
			- Reliable rollbacks – Robust automation means rollbacks are a reliable way to ensure stability for customers, and rollbacks don’t hurt developers because they can roll forward with a fix as soon as they have one.
		- (Page 38)
	- -
	- -
		- What is IaC? #flashcard
		  id:: 63998df7-53b9-435a-ab94-712b64230897
			- m
		- (Page 40)
	- -
	- -
		- Infrastructure as Code (IaC): manage and provision infrastructure through code and automation. #flashcard
		  id:: 6beb20b5-d56d-4d0d-ba5a-0ba85deaa173
		- (Page 40)
	- -
	- -
		- Benefits of IaC.
		  id:: 10a23fa1-2b7c-4de1-97a4-21a80c5ce144
		  
		  > With IaC, you can automate the tasks instead of manually go into every single machine. This is better because is less error-prone and a lot more straighforward. Ansible is a tool example #flashcard
			- Consistency in creation and management of resources – The same automation will run the same way every time. Reusability – Code can be used to make the same change consistently across multiple hosts and can be used again in the future. Scalability – Need a new instance? You can have one configured exactly the same way as the existing instances in minutes (or seconds). Self-documenting – With IaC, changes to infrastructure document themselves to a degree. The way a server is configured can be viewed in source control, rather than being a matter of who logged in to the server and did something. Simplify the complexity – Complex infrastructures can be stood up quickly once they are defined as code. A group of several interdependent servers can be provisioned on demand.
		- (Page 42)
	- -
	- -
		- Configuration Management is done by tools, not manually. 
		  id:: 501c933c-7787-4183-9b82-d3e07b9ecc1a
		  In the cloud, Configuration Management is crucial because there are so many things to configure..
		  You can make good use of version control.
		  Don't need to go machine by machine, also with the help of IaC #flashcard
			- Configuration Management: maintaining and changing the state of pieces of infrastructure in a consistent, maintainable, and stable way
		- (Page 44)
	- -
	- -
		- What is orchestration?
		  id:: d1501176-eda5-48ee-a084-448011b071b2
		  
		  > With the help of tools, you can orchestrate a server resources by adding to the service more resource nodes programatically (or even automatically if you want) so that the application could use less (or more) resources dinamically. #flashcard
			- Orchestration: automation that supports processes and workflows, such as provisioning resources
		- (Page 48)
	- -
	- -
		- What is monitoring?
		  id:: 8ac8e2f1-3dcc-462b-858c-17035873363b
		  
		  > Not only of post-mortem logs, but also with resources which are decreasing (before they become critical) #flashcard
			- Monitoring: The collection and presentation of data about the performance and stability of services and infrastructure
		- (Page 52)
	- -
	- -
		- What are microservices?
		  id:: 8ad94d5f-e786-468c-9bfa-1cae12e57e0c
		  
		  > We build one small module which is independent of every other and interacts by an API. "Every feature could be like a new module"
		  This module could be write even in other language. #flashcard
			- Microservices: A microservice architecture breaks an application up into a collection of small, loosely-coupled services
		- (Page 56)
	- -
	- -
		- Containers VS VMs #flashcard
		  id:: f985aa0f-1766-4d7d-9940-095e977c3484
			- Containers – Lightweight, isolated packages containing everything needed to run a piece of software • Require fewer resources than VMs – VMs contain an entire OS plus virtual versions of all the hardware • Containers have the bare minimum needed to run the software • Docker – Docker is currently the leading container technology
		- (Page 77)
	- -