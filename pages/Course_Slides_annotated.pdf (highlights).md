title:: Course_Slides_annotated.pdf (highlights)
author:: [[]]
full-title:: "Course_Slides_annotated.pdf"
category:: #books

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- Esta es una nota emergente :) #car
		- “DevOps is a software engineering culture and practice that aims at unifying software development (Dev) and software operation (Ops)... DevOps aims at shorter development cycles, increased deployment frequency, more dependable releases, in close alignment with business objectives.”
		- (Page 3)
	- -
	- -
	- Which goals share dev and ops? #car
		- With DevOps, Dev and Ops work together and share the same goals.
		- (Page 13)
	- -
	- -
	- Dev and Ops share the same goals #ñspace
		- (Page 14)
	- -
	- -
	- What are the shared goals of dev and ops? #car
	  id:: 63401501-87ac-4772-b27a-602d2e518825
		- In a DevOps culture, devs care about stability as well as speed, and ops care about speed as well as stability.
		- (Page 15)
	- -
	- -
	- What is the relation between my IDE and the pipeline automation? #car
		- Build automation is independent of an IDE • Even if you can build within the IDE, it should be able to work the same way outside of the IDE
		- (Page 28)
	- -
	- -
	- What is the relation between configuration and build automation? #car
	  id:: 63401501-6d6c-49bb-845c-a5d4c546c8a1
		- As much as possible, build automation should be agnostic of the configuration of the machine that it is built on
		- (Page 28)
	- -
	- -
	- What is CI? #car
	  id:: 63401501-e98b-4aba-b99b-02f890276dd0
		- Continuous Integration (CI): the practice of frequently merging code changes done by developers
		- (Page 31)
	- -
	- -
	- id:: 63401501-af6a-4cbe-9bfe-6d229094aa46
	  > Wheter it may be deployed or not, it's an option that every company chooses #car
		- Continuous Delivery (CD): the practice of continuously maintaining code in a deployable state
		- (Page 35)
	- -
	- -
	- Regardless of whether or not the decision is made to deploy, the code is always in a state that is able to be deployed. #ñspace
		- (Page 35)
	- -
	- -
	- What is Continous Deployment? #car
		- Continuous Deployment: the practice of frequently deploying small code changes to production
		- (Page 36)
	- -
	- -
	- Stages of build automation. #car
	  id:: 63401501-270a-446a-b59a-a7f9f42956f3
		- Each version of the code goes through a series of stages such as automated build, automated testing, and manual acceptance testing. The result of this process is an artifact or package that is able to be deployed.
		- (Page 37)
	- -
	- -
	- An advantage of CD&D #car
	  id:: 63401501-d48b-4c15-b832-5b2bab78fac5
		- Reliable rollbacks – Robust automation means rollbacks are a reliable way to ensure stability for customers, and rollbacks don’t hurt developers because they can roll forward with a fix as soon as they have one.
		- (Page 38)
	- -
	- -
	- What is IaC? #car
	  id:: 63401501-d09d-4206-834e-6d8476f6d85f
		- m
		- (Page 40)
	- -
	- -
	- Infrastructure as Code (IaC): manage and provision infrastructure through code and automation. #ñspace
		- (Page 40)
	- -
	- -
	- Benefits of IaC.
	  id:: 63401501-54a4-4926-a6d4-51a072df9c1a
	  
	  > With IaC, you can automate the tasks instead of manually go into every single machine. This is better because is less error-prone and a lot more straighforward. Ansible is a tool example #car
		- Consistency in creation and management of resources – The same automation will run the same way every time. Reusability – Code can be used to make the same change consistently across multiple hosts and can be used again in the future. Scalability – Need a new instance? You can have one configured exactly the same way as the existing instances in minutes (or seconds). Self-documenting – With IaC, changes to infrastructure document themselves to a degree. The way a server is configured can be viewed in source control, rather than being a matter of who logged in to the server and did something. Simplify the complexity – Complex infrastructures can be stood up quickly once they are defined as code. A group of several interdependent servers can be provisioned on demand.
		- (Page 42)
	- -
	- -
	- Configuration Management is done by tools, not manually. 
	  id:: 63401501-ad6b-413f-8807-159efd42c69e
	  In the cloud, Configuration Management is crucial because there are so many things to configure..
	  You can make good use of version control.
	  Don't need to go machine by machine, also with the help of IaC #car
		- Configuration Management: maintaining and changing the state of pieces of infrastructure in a consistent, maintainable, and stable way
		- (Page 44)
	- -
	- -
	- What is orchestration?
	  id:: 63401501-c675-4ba1-b4fb-cfd1ffb74ac8
	  
	  > With the help of tools, you can orchestrate a server resources by adding to the service more resource nodes programatically (or even automatically if you want) so that the application could use less (or more) resources dinamically. #car
		- Orchestration: automation that supports processes and workflows, such as provisioning resources
		- (Page 48)
	- -
	- -
	- What is monitoring?
	  id:: 63401501-30ca-4a66-b0fe-30327950f2f0
	  
	  > Not only of post-mortem logs, but also with resources which are decreasing (before they become critical) #car
		- Monitoring: The collection and presentation of data about the performance and stability of services and infrastructure
		- (Page 52)
	- -
	- -
	- What are microservices?
	  id:: 63401501-deb4-4ef1-8172-1121ee09beea
	  
	  > We build one small module which is independent of every other and interacts by an API. "Every feature could be like a new module"
	  This module could be write even in other language. #car
		- Microservices: A microservice architecture breaks an application up into a collection of small, loosely-coupled services
		- (Page 56)
	- -
	- -
	- Containers VS VMs #car
		- Containers – Lightweight, isolated packages containing everything needed to run a piece of software • Require fewer resources than VMs – VMs contain an entire OS plus virtual versions of all the hardware • Containers have the bare minimum needed to run the software • Docker – Docker is currently the leading container technology
		- (Page 77)
	- -