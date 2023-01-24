# Course_Slides_annotated.pdf

deck:: [[Other-Books::Course_Slides_annotated.pdf]]\
author:: [[None]]\
full-title:: "Course_Slides_annotated.pdf"\
category:: #books\
\

![](https://readwise-assets.s3.amazonaws.com/static/images/default-book-icon-3.40504e56b01b.png)
## Highlights
- id:: 63c669f2-f6f5-48ee-9972-8b29876e754c
   Esta es una nota emergente :) #flashcard 
    “DevOps is a software engineering culture and practice that aims at unifying software development (Dev) and software operation (Ops)... DevOps aims at shorter development cycles, increased deployment frequency, more dependable releases, in close alignment with business objectives.”
  
     (Page 3)
-
- Which goals share dev and ops? #flashcard 
  id:: 63cfbcc1-707d-4201-b421-e2aab456d79b
    With DevOps, Dev and Ops work together and share the same goals.
  
     (Page 13)
-
- id:: 63c669f2-1bc1-4a5f-9bea-1460ee164128
  
  Dev and Ops share the same goals #flashcard 
  
  
     (Page 14)
-
- id:: 63c669f2-cc18-4fe5-9025-32e3ee51122c
   What are the shared goals of dev and ops? #flashcard 
    In a DevOps culture, devs care about stability as well as speed, and ops care about speed as well as stability.
  
     (Page 15)
-
- id:: 63c669f2-3bd2-4296-806d-722a6751bd8a
   What is the relation between my IDE and the pipeline automation? #flashcard 
    Build automation is independent of an IDE • Even if you can build within the IDE, it should be able to work the same way outside of the IDE
  
     (Page 28)
-
- id:: 63c669f2-33d4-4f2e-a23d-00af8f984cad
   What is the relation between configuration and build automation? #flashcard 
    As much as possible, build automation should be agnostic of the configuration of the machine that it is built on
  
     (Page 28)
-
- id:: 63c669f2-1ee1-46b6-9103-b214124bf3b8
   What is CI? #flashcard 
    Continuous Integration (CI): the practice of frequently merging code changes done by developers
  
     (Page 31)
-
- id:: 63c669f2-e7d1-44e3-ad37-6c00ac480a89
   > Wheter it may be deployed or not, it's an option that every company chooses #flashcard 
    Continuous Delivery (CD): the practice of continuously maintaining code in a deployable state
  
     (Page 35)
-
- id:: 63c669f2-92ff-4a5b-a117-e8aefda47468
  
  Regardless of whether or not the decision is made to deploy, the code is always in a state that is able to be deployed. #flashcard 
  
  
     (Page 35)
-
- What is Continous Deployment? #flashcard 
  id:: 63cfbcc1-8707-4362-936d-88b704123181
    Continuous Deployment: the practice of frequently deploying small code changes to production
  
     (Page 36)
-
- Stages of build automation. #flashcard 
  id:: 63cfbcc1-745e-4acf-822b-5cc14aa212e4
    Each version of the code goes through a series of stages such as automated build, automated testing, and manual acceptance testing. The result of this process is an artifact or package that is able to be deployed.
  
     (Page 37)
-
- id:: 63c669f2-d3ac-498d-ad7f-c7dbaa219d6c
   An advantage of CD&D #flashcard 
    Reliable rollbacks – Robust automation means rollbacks are a reliable way to ensure stability for customers, and rollbacks don’t hurt developers because they can roll forward with a fix as soon as they have one.
  
     (Page 38)
-
- id:: 63c669f2-e28c-41e6-8a1a-c8dc63a95c52
   What is IaC? #flashcard 
    m
  
     (Page 40)
-
- Infrastructure as Code (IaC): manage and provision infrastructure through code and automation. #flashcard 
  id:: 63cfbcc1-20db-498a-9771-99dda25a8240
  
  
     (Page 40)
-
- id:: 63c669f2-252f-4e47-8af0-78215b6eea5b
   Benefits of IaC.
   > With IaC, you can automate the tasks instead of manually go into every single machine. This is better because is less error-prone and a lot more straighforward. Ansible is a tool example #flashcard 
    Consistency in creation and management of resources – The same automation will run the same way every time. Reusability – Code can be used to make the same change consistently across multiple hosts and can be used again in the future. Scalability – Need a new instance? You can have one configured exactly the same way as the existing instances in minutes (or seconds). Self-documenting – With IaC, changes to infrastructure document themselves to a degree. The way a server is configured can be viewed in source control, rather than being a matter of who logged in to the server and did something. Simplify the complexity – Complex infrastructures can be stood up quickly once they are defined as code. A group of several interdependent servers can be provisioned on demand.
  
     (Page 42)
-
- id:: 63c669f2-14c9-452e-ae41-5f8c3ccf228f
   Configuration Management is done by tools, not manually. 
   In the cloud, Configuration Management is crucial because there are so many things to configure..
   You can make good use of version control.
   Don't need to go machine by machine, also with the help of IaC #flashcard 
    Configuration Management: maintaining and changing the state of pieces of infrastructure in a consistent, maintainable, and stable way
  
     (Page 44)
-
- What is orchestration?
  id:: 63cfbcc1-8700-417a-9169-2c12775c3d70
   > With the help of tools, you can orchestrate a server resources by adding to the service more resource nodes programatically (or even automatically if you want) so that the application could use less (or more) resources dinamically. #flashcard 
    Orchestration: automation that supports processes and workflows, such as provisioning resources
  
     (Page 48)
-
- id:: 63c669f2-398c-42ec-90f5-f821509c0a2e
   What is monitoring?
   > Not only of post-mortem logs, but also with resources which are decreasing (before they become critical) #flashcard 
    Monitoring: The collection and presentation of data about the performance and stability of services and infrastructure
  
     (Page 52)
-
- id:: 63c669f2-5e4f-4f4e-a3fa-ee120461cca2
   What are microservices?
   > We build one small module which is independent of every other and interacts by an API. "Every feature could be like a new module"
   This module could be write even in other language. #flashcard 
    Microservices: A microservice architecture breaks an application up into a collection of small, loosely-coupled services
  
     (Page 56)
-
- id:: 63c669f2-015a-4de0-a052-2c14c6a8dc3d
   Containers VS VMs #flashcard 
    Containers – Lightweight, isolated packages containing everything needed to run a piece of software • Require fewer resources than VMs – VMs contain an entire OS plus virtual versions of all the hardware • Containers have the bare minimum needed to run the software • Docker – Docker is currently the leading container technology
  
     (Page 77)
-