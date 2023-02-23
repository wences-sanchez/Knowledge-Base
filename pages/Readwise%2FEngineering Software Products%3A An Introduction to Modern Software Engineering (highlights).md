title:: Readwise/Engineering Software Products: An Introduction to Modern Software Engineering (highlights)



deck:: [[Other-Books::Engineering Software Products: An Introduction to Modern Software Engineering]]\
author:: [[Ian Sommerville]]\
full-title:: "Engineering Software Products: An Introduction to Modern Software Engineering"\
category:: #books\
\

- Highlights first synced by [[Readwise]] [[Tuesday, 21-02-2023]]
	- -
		- As more and more companies automated their business, however, it became clear that most businesses didn’t really need custom software. They could use generic software products that were designed for common business problems. The software product industry developed to meet this need. Project-based software engineering techniques were adapted to software product development. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gssn97ry3segmxx2vde75w40))
	- -
	- -
		- Project-based techniques are not suited to product development because of fundamental differences between project-based and product-based software engineering. These differences are illustrated in [Figures 1.1](#P7001016428000000000000000000161) and [1.2](#P7001016428000000000000000000170).
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/35544017/idf0003-01_png-f0003-01.png)
		  
		  Figure 1.1
		  
		  Project-based software engineering
		  
		  [Figure 1.1 Full Alternative Text](#la_f0003-01)
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/35544017/idf0003-02_png-f0003-02.png)
		  
		  Figure 1.2
		  
		  Product-based software engineering #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gssnc09nkh1qgt6gb54gv25d))
	- -
	- -
		- What is the main difference between software projects and software products? #flashcard
			- Software projects involve an external client or customer who decides on the functionality of the system and enters into a legal contract with the software development company. The customer’s problem and current processes are used as a basis for creating the software requirements, which specify the software to be implemented. As the business changes, the supporting software has to change. The company using the software decides on and pays for the changes. Software often has a long lifetime, and the costs of changing large systems after delivery usually exceed the initial software development costs.
			  
			  Software products are specified and developed in a different way. There is no external customer who creates requirements that define what the software must do. The software developer decides on the features of the product, when new releases are to be made available, the platforms on which the software will be implemented, and so on. The needs of potential customers for the software are obviously considered, but customers can’t insist that the software includes particular features or attributes. The development company chooses when changes will be made to the software and when they will be released to users.
		- ([View Highlight](https://read.readwise.io/read/01gssnjn0m3t8hak7g0j23g6h9))
	- -
	- -
		- the key characteristic of product development is that there is no external customer who generates software requirements and pays for the software. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gssnz6dfa3vnmtaahppe9hsd))
	- -
	- -
		- This is also true for some other types of software development:
		  
		  1.  Student projects As part of a computing or engineering course, students may be set assignments in which they work in groups to develop software. The group is responsible for deciding on the features of the system and how to work together to implement these features.
		    
		  2.  Research software Software is developed by a research team to support their work. For example, climate research depends on large-scale climate models that are designed by researchers and implemented in software. On a smaller scale, an engineering group may build software to model the characteristics of the material they are using.
		    
		  3.  Internal tool development A software development team may decide that it needs some specific tools to support their work. They specify and implement these tools as “internal” products.
		    
		  
		  You can use the product development techniques that I explain here for any type of software development that is not driven by external customer requirements. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gssp0x45v8e1f2fh8n5a2bbe))
	- -
	- -
		- In favour of software engineering #flashcard
			- There is a common view that software product engineering is simply advanced programming and that traditional software engineering is irrelevant. All you need to know is how to use a programming language plus the frameworks and libraries for that language. This is a misconception and I have written this book to explain the activities, apart from programming, that I believe are essential for developing high-quality software products.
		- ([View Highlight](https://read.readwise.io/read/01gsspetqj04mwwthjtgskp4sj))
	- -
	- -
		- Q: What are the three fundamental questions that need to be answered when developing a product vision?
		  A: 1. What is the product? 2. Who are the target users and customers? 3. Why should customers buy the product? #flashcard
			- Your starting point for product development should be an informal “product vision.” A product vision is a simple and succinct statement that defines the essence of the product that is being developed. It explains how the product differs from other competing products. This product vision is used as a basis for developing a more detailed description of the features and attributes of the product. As new features are proposed, you should check them against the vision to make sure they contribute to it.
			  
			  The product vision should answer three fundamental questions:
			  
			  1.  *What* is the product that you propose to develop? What makes this product different from competing products?
			    
			  2.  *Who* are the target users and customers for the product?
			    
			  3.  *Why* should customers buy this product?
		- ([View Highlight](https://read.readwise.io/read/01gsspj2pchckkskqkezm1yxve))
	- -
	- -
		- The template from Geoffrey Moore's book "Crossing the Chasm" is a structured approach for writing a product vision based on keywords. This approach is described by Joel Spolsky in his blog "Joel on Software", where he provides an example of a product described using this template. The template includes key words such as target customer, statement of the need or opportunity, product category, key benefit, primary competitive alternative and statement of primary differentiation. #flashcard
			- If you search the web for “product vision,” you will find several variants of these questions and templates for expressing the product vision. Any of these templates can be used. The template that I like comes from the book *Crossing the Chasm* by Geoffrey Moore.[1](#P70010164280000000000000000002BE) Moore suggests using a structured approach to writing the product vision based on keywords:
			  
			  [1](#r__P70010164280000000000000000002BE)Geoffrey Moore, *Crossing the Chasm: Marketing and selling technology products to mainstream customers* (Capstone Trade Press, 1998).
			  
			  •   FOR (target customer)
			    
			  •   WHO (statement of the need or opportunity)
			    
			  •   The (PRODUCT NAME) is a (product category)
			    
			  •   THAT (key benefit, compelling reason to buy)
			    
			  •   UNLIKE (primary competitive alternative)
			    
			  •   OUR PRODUCT (statement of primary differentiation)
			    
			  
			  On his blog *Joel on Software*, Joel Spolsky gives an example of a product described using this vision template
		- ([View Highlight](https://read.readwise.io/read/01gsspzmdmtnm43wpf9pgz8njm))
	- -
	- -
		- Q: What is a software product?
		  A: A software product is a software system that includes general functionality that is likely to be useful to a wide range of customers. #flashcard
			- Software products are software systems that include general functionality that is likely to be useful to a wide range of customers.
		- ([View Highlight](https://read.readwise.io/read/01gssrwgba2raa7eb49mmg5bx7))
	- -
	- -
		- :
		  
		  What are the disadvantages of using plan-driven development for small and medium-sized software products? #flashcard
			- If plan-driven development is used for small and medium-sized software products, however, the overhead involved is so large that it dominates the software development process. Too much time is spent writing documents that may never be read rather than writing code. The system is specified in detail before implementation begins. Specification errors, omissions, and misunderstandings are often discovered only after a significant chunk of the system has been implemented.
		- ([View Highlight](https://read.readwise.io/read/01gssscvey93hnxe3zs25s7yq6))
	- -
	- -
		- The Agile Manifesto #flashcard
			- We are uncovering better ways of developing software by doing it and helping others to do it. Through this work, we have come to value:
			  
			  •   - individuals and interactions over processes and tools;
			    
			  •   - working software over comprehensive documentation;
			    
			  •   - customer collaboration over contract negotiation;
			    
			  •   - responding to change over following a plan.
			    
			  
			  While there is value on the items on the right, we value the items on the left more.
		- ([View Highlight](https://read.readwise.io/read/01gssstvmdgbxamm6wxnd1tm3v))
	- -
	- -
		- According to the Agile mindset, the details of all the features come later. You'll define those in future increments. #flashcard
			- With incremental development, you delay decisions until you really need to make them. You start by prioritizing the features so that the most important features are implemented first. You don’t worry about the details of all the features—you define only the details of the feature that you plan to include in an increment. That feature is then implemented and delivered. Users or surrogate users can try it out and provide feedback to the development team. You then go on to define and implement the next feature of the system.
		- ([View Highlight](https://read.readwise.io/read/01gsst01s053et6ex29h1cy5xv))
	- -
	- -
		- In Agile development there isn't any functional requirements list... #flashcard
			- There is no “grand plan” for the system. Instead, what needs to be implemented (the requirements) in each increment are established in discussions with a customer representative. The requirements are written as user stories. The stories to be included in a release are determined by the time available and their relative priority.
		- ([View Highlight](https://read.readwise.io/read/01gsstg8fa4a1bs7c78stx9q94))
	- -
	- -
		- How will you build an automated pipeline step by step alongside you code #flashcard
			- Instead of writing code and then tests for that code, developers write the tests first. This helps clarify what the code should actually do and that there is always a “tested” version of the code available. An automated unit test framework is used to run the tests after every change. New code should not “break” code that has already been implemented.
		- ([View Highlight](https://read.readwise.io/read/01gsstna76h505ga2keyr8hy72))
	- -
- New highlights added [[Thursday, 23-02-2023]] at 6:26 PM
	- -
		- About planning in advance, like you are used to do (in Agile) #flashcard
			- managers need to know what is going on and whether or not a software development project is likely to deliver the software on time and within its budget. Traditionally, this involves drawing up a project plan that shows a set of milestones (what will be achieved), deliverables (what will be delivered by the team), and deadlines (when a milestone will be reached). The “grand plan” for the project shows everything from start to finish. Progress is assessed by comparing that plan with what has been achieved.
			  
			  The problem with up-front project planning is that it involves making detailed decisions about the software long before implementation begins. Inevitably things change. New requirements emerge, team members come and go, business priorities evolve, and so on. Almost from the day they are formulated, project plans have to change. Sometimes this means that “finished” work has to be redone. This is inefficient and often delays the final delivery of the software.
			  
			  On this basis, the developers of agile methods argued that plan-based management is wasteful and unnecessary. It is better to plan incrementally so that the plan can change in response to changing circumstances. At the start of each development cycle, decisions are made on what features should be prioritized, how these should be developed and what each team member should do. Planning should be informal with minimal documentation and with no designated project manager.
		- ([View Highlight](https://read.readwise.io/read/01gswhs23890y20hwtb42gpyb7))
	- -
	- -
		- The other Scrum term that may need explanation is “potentially shippable product increment.” This means that the outcome of each sprint should be product-quality code. It should be completely tested, documented, and, if necessary, reviewed. Tests should be delivered with the code. There should always be a high-quality system available that can be demonstrated to management or potential customers. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gswj5q2dcdnz0acxz4qwykwm))
	- -
	- -
		- The team works on the things they have planned to do during the sprint, like tasks or projects. They have a certain amount of time to do the tasks. If they don't finish everything, they put the unfinished tasks back on the list for later. They don't get extra time to finish them. #flashcard
			- During implementation, the team implements as many of the sprint backlog items as they can in the fixed time period allowed for the sprint. Incomplete items are returned to the product backlog. Sprints are never extended to finish an incomplete item.
		- ([View Highlight](https://read.readwise.io/read/01gswjax0wgsaw6r7w8pefbywq))
	- -
	- -
		- When estimating the effort needed to complete a project, two metrics are usually used. The first is called "effort required" which is the amount of effort, usually in person-hours or person-days, it would take one person to finish the project. 
		  
		  The second metric is called "story points" which is an estimate of the effort involved in implementing a project taking into account the size, complexity and any unknown characteristics of the work. 
		  
		  Story points are usually compared to a baseline task, with other tasks being estimated by comparison to it. Story points are more abstract than effort required because everyone's individual abilities do not matter. #flashcard
			- PBI estimates provide an indication of the effort required to complete each item. Two metrics are commonly used:
			  
			  1.  Effort required The amount of effort may be expressed in person-hours or person-days—that is, the number of hours or days it would take one person to implement that PBI. This is not the same as calendar time. Several people may work on an item, which may shorten the calendar time required. Alternatively, a developer may have other responsibilities that prevent full-time work on a project. Then the calendar time required is longer than the effort estimate.
			    
			  2.  Story points Story points are an arbitrary estimate of the effort involved in implementing a PBI, taking into account the size of the task, its complexity, the technology that may be required, and the “unknown” characteristics of the work. Story points were derived originally by comparing user stories, but they can be used for estimating any kind of PBI. Story points are estimated relatively. The team agrees on the story points for a baseline task. Other tasks are then estimated by comparison with this baseline—for example, more or less complex, larger or smaller, and so on. The advantage of story points is that they are more abstract than effort required because all story points should be the same, irrespective of individual abilities.
			    
			  
			  Effort estimation is hard, especially at the beginning of a project when a team has little or no previous experience with this type of work or when technologies new to the team are used. Estimates are based on the subjective judgment of the team members, and initial estimates are inevitably wrong. Estimates usually improve, however, as the team gains experience with the product and its development process.
			  
			  The Scrum method recommends a team-based estimation approach called “Planning Poker,” which I don’t go into here. The rationale is that teams should be able to make better estimates than individuals. However, there is no convincing empirical evidence showing that collective estimation is better than estimates made by experienced, individual developers.
			  
			  After a number of sprints have been completed, it becomes possible for a team to estimate its “velocity.” Simplistically, a team’s velocity is the sum of the size estimates of the items that have been completed during a fixed-time sprint. For example, assume that PBIs are estimated in story points and, in consecutive sprints, the team implements 17, 14, 16, and 19 story points. The team’s velocity is therefore between 16 and 17 story points per sprint.
		- tags:: [[ghost]]
		- ([View Highlight](https://read.readwise.io/read/01gswmb3vm7b204t8dnytebsk3))
	- -
	- -
		- When planning a sprint, the team do three things:
		  
		  •   agree on a sprint goal;
		    
		  •   decide on the list of items from the product backlog that should be implemented;
		    
		  •   create a sprint backlog, a more detailed version of the product backlog that records the work to be done during the sprint. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gswmqw0bdd86y2p1rw4r0qpp))
	- -
	- -
		- Sometimes, a PBI can be transferred directly to the sprint backlog. However, the team normally breaks down each PBI into smaller tasks that are added to the sprint backlog. All team members then discuss how these tasks will be allocated. Each task should have a relatively short duration—one or two days at most—so that the team can assess its progress #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gswndhcwxtnhd173jja5erjs))
	- -
	- -
		- The developers of Scrum assumed that team members are co-located. They work in the same office and can communicate informally. If one team member needs to know something about what another has done, they simply talk to each other to find out. There is no need for people to document their work for others to read #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gswp2w1k8wn0v4kvsvty9rz3))
	- -
	- -
		- You’ll have to have this!!! 
		  Because whatever people tell you, it will be recorded either in a video or in an instant message application!!😇😇😇 #flashcard
			- If co-located working with daily meetings is impractical, then the team must work out other ways to communicate. Messaging systems, such as Slack, can be effective for informal communications. The benefit of messaging is that all messages are recorded so that people can catch up on conversations that they missed. Messaging does not have the immediacy of face-to-face communication, but it is better than email or shared documents for coordination.
		- tags:: [[mind]]
		- ([View Highlight](https://read.readwise.io/read/01gswp549arm0cr1rhjjn7gffh))
	- -
	- -
		- •   The best way to develop software products is to use agile software engineering methods that are geared to rapid product development and delivery.
		    
		  •   Agile methods are based on iterative development and the minimization of overheads during the development process.
		    
		  •   Extreme Programming (XP) is an influential agile method that introduced agile development practices such as user stories, test-first development, and continuous integration. These are now mainstream software development activities.
		    
		  •   Scrum is an agile method that focuses on agile planning and management. Unlike XP, it does not define the engineering practices to be used. The development team may use any technical practices they consider appropriate for the product being developed.
		    
		  •   In Scrum, work to be done is maintained in a product backlog, a list of work items to be completed. Each increment of the software implements some of the work items from the product backlog.
		    
		  •   Sprints are fixed-time activities (usually two to four weeks) in which a product increment is developed. Increments should be potentially shippable; that is, they should not need further work before they are delivered.
		    
		  •   A self-organizing team is a development team that organizes the work to be done by discussion and agreement among team members.
		    
		  •   Scrum practices, such as the product backlog, sprints, and self-organizing teams, can be used in any agile development process, even if other aspects of Scrum are not used. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gswpqqp6f8pebmmb6ych3kmz))
	- -
	- 3 Features, Scenarios, and Stories
		- -
			- Software products are not made to meet what a person wants. So, the techniques used to find out what the person wants and document it cannot be used for product engineering. You don't need to have a very detailed list of what the person wants for the software development agreement. Product development changes quickly, so there is no need to talk for a long time when what is wanted changes. #flashcard
				- As I explained in [Chapter 1](https://readwise.io/reader/document_raw_content/35544017#P700101642800000000000000000014B), software products are not developed to meet the requirements of a specific client. Consequently, techniques that have been developed for eliciting, documenting, and managing software requirements aren’t used for product engineering. You don’t need to have a complete and detailed requirements document as part of a software development contract. There is no need for prolonged consultations when requirements change. Product development is incremental and agile
			- tags:: [[ghost]]
			- ([View Highlight](https://read.readwise.io/read/01gswq2hhzwf9p6r56g5cscyry))
		- -
		- -
			- This lesson assumes that there is a client. So I’m not so sure if just me is appropriate for eliciting tasks:
			  
			  Why don’t you go for a global project? #flashcard
				- In this chapter, I assume that informal user consultations are possible. I explain ways of representing users (personas) and communicating with them and other product stakeholders. I focus on how short, natural language descriptions (scenarios and stories) can be used to visualize and document how users might interact with a software product.
			- ([View Highlight](https://read.readwise.io/read/01gswq9n9sfvbch2bbkyg8q9xx))
		- -
		- -
			- What Persona means (in feature development) #flashcard
				- From these data, you can abstract the essential information about the different types of product users and then use this as a basis for creating personas. These personas should then be cross-checked against the user data to make sure that they reflect typical product users.
			- ([View Highlight](https://read.readwise.io/read/01gswrv3qes0hqbhkh0x5qz64w))
		- -
		- -
			- ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/35544017/idf0061-01_png-f0061-01.png)
			  
			  Figure 3.5
			  
			  Elements of a scenario description #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gsws4q9vkh7gh537qk3wapaq))
		- -
		- -
			- Key Points
			  
			  •   A software product feature is a fragment of functionality that implements something a user may need or want when using the product.
			    
			  •   The first stage of product development is to identify the list of product features in which you name each feature and give a brief description of its functionality.
			    
			  •   Personas are “imagined users”— character portraits of types of users you think might use your product.
			    
			  •   A persona description should paint a picture of a typical product user. It should describe the user’s educational background, technology experience, and why they might want to use your product.
			    
			  •   A scenario is a narrative that describes a situation where a user is accessing product features to do something that they want to do.
			    
			  •   Scenarios should always be written from the user’s perspective and should be based on identified personas or real users.
			    
			  •   User stories are finer-grain narratives that set out, in a structured way, something that a user wants from a software system.
			    
			  •   User stories may be used to extend and add detail to a scenario or as part of the description of system features.
			    
			  •   The key influences in feature identification and design are user research, domain knowledge, product knowledge, and technology knowledge.
			    
			  •   You can identify features from scenarios and stories by highlighting user actions in these narratives and thinking about the features that you need to support these actions. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gswz5ydweb9e3s190efbs9a0))
		- -
		- -
			- “An Introduction to Feature-Driven Development” This article is an introduction to this agile method that focuses on features, a key element of software products. (S. Palmer, 2009)
			  
			  **[https://dzone.com/articles/introduction-feature-driven](https://dzone.com/articles/introduction-feature-driven)** #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gswzdshqrghsa8c5rjp47f5b))
		- -
		- -
			- “10 Tips for Writing Good User Stories” Sound advice on story writing is presented by an author who takes a pragmatic view of the value of user stories. (R. Pichler, 2016)
			  
			  **[http://www.romanpichler.com/blog/10-tips-writing-good-user-stories/](http://www.romanpichler.com/blog/10-tips-writing-good-user-stories/)** #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gswzebagtkexhyqq5z4t4vjt))
		- -
		- 4 Software Architecture
			- -
				- Q: What is architecture?
				  A: Architecture is the fundamental organization of a software system, consisting of components, relationships, and principles which guide its design and evolution. #flashcard
					- Architecture is the fundamental organization of a software system embodied in its components, their relationships to each other and to the environment, and the principles guiding its design and evolution.
				- tags:: [[ghost]]
				- ([View Highlight](https://read.readwise.io/read/01gswzy6wepp4npmh0me96nf16))
			- -
			- -
				- Cloud computing is very common now, so you have to decide if you want to make your system work on one computer or on the cloud. You can rent a computer from Amazon or another company, but this doesn't use all of the benefits of the cloud. To use the cloud, you need to design your system to work with services and use the specific programs from the cloud provider. This will help your system stay strong and be able to grow as needed. #flashcard
					- Cloud computing is now ubiquitous so a key decision you have to make is whether to design your system to run on individual servers or on the cloud. Of course, it is possible to rent a server from Amazon or some other provider, but this does not really take full advantage of the cloud. To develop for the cloud, you need to design your architecture as a service-oriented system and use the platform APIs provided by the cloud vendor to implement your software. These allow for automatic scalability and system resilience.
				- tags:: [[ghost]] [[mind]] [[favourite]]
				- ([View Highlight](https://read.readwise.io/read/01gsx42s8f5waefd7yn7a0xteh))
			- -
			- -
				- “Five Reasons Developers Don’t Use UML and Six Reasons to Use It” This article sets out arguments for using the UML when designing software architectures. (B. Pollack, 2010)
				  
				  **[https://saturnnetwork.wordpress.com/2010/10/22/five-reasons-developers-dont-use-uml-and-six-reasons-to-use-it/](https://saturnnetwork.wordpress.com/2010/10/22/five-reasons-developers-dont-use-uml-and-six-reasons-to-use-it/)** #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gsx54zrww0sba6p3ayaw9xd5))
			- -
			- -
				- “To SQL or NoSQL? That’s the Database Question” This is a good, short introduction to the pros and cons of relational and NoSQL databases. (L. Vaas, 2016)
				  
				  **[https://arstechnica.com/information-technology/2016/03/to-sql-or-nosql-thats-the-database-question/](https://arstechnica.com/information-technology/2016/03/to-sql-or-nosql-thats-the-database-question/)** #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gsx55pcj6eb4wjsvj9dc2p95))
			- -
		- 5 Cloud-Based Software
			- -
				- The cloud is a special way of using computers. It is made up of lots of remote servers that companies own and rent out to other people. Instead of having real, physical computers, these servers are in the form of software, which means they exist only on the internet. You can rent as many servers as you need, run your own software on them and give access to other people who can use them from their own computers, tablets, and TVs. The cloud is very powerful and can run multiple servers at the same time without any problem. #flashcard
					- The convergence of powerful, multicore computer hardware and high-speed networking has led to the development of “the cloud.” Put simply, the cloud is a very large number of remote servers that are offered for rent by companies that own these servers. You can rent as many servers as you need, run your software on these servers, and make them available to your customers. Your customers can access these servers from their own computers or other networked devices such as a tablet or a TV. You may rent a server and install your own software, or you may pay for access to software products that are available on the cloud.
					  
					  The remote servers are “virtual servers,” which means they are implemented in software rather than hardware. Many virtual servers can run simultaneously on each cloud hardware node, using virtualization support that is built in to the hardware. Running multiple servers has very little effect on server performance. The hardware is so powerful that it can easily run several virtual servers at the same time.
				- tags:: [[ghost]]
				- ([View Highlight](https://read.readwise.io/read/01gsx5bzm154a3brf0rtrz484c))
			- -
			- -
				- servers.
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/35544017/idf0117-01_png-f0117-01.png)
				  
				  Figure 5.1
				  
				  Scalability, elasticity, and resilience #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gsx5heakc3h0nypp4gzvv28a))
			- -
			- -
				- The problem with implementing virtual servers on top of VMs is that creating a VM involves loading and starting up a large and complex operating system (OS). The time needed to install the OS and set up the other software on the VM is typically between 2 and 5 minutes on public cloud providers such as AWS. This means that you cannot instantly react to changing demands by starting up and shutting down VMs.
				  
				  In many cases, you don’t really need the generality of a virtual machine. If you are running a cloud-based system with many instances of applications or services, these all use the same operating system. To cater to this situation, a simpler, lightweight, virtualization technology called “containers” may be used.
				  
				  Using containers dramatically speeds up the process of deploying virtual servers on the cloud. Containers are usually megabytes in size, whereas VMs are gigabytes. Containers can be started up and shut down in a few seconds rather than the few minutes required for a VM. Many companies that provide cloud-based software have now switched from VMs to containers because containers are faster to load and less demanding of machine resources. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gsx5yv937tb8qawhhjsfcvsv))
			- -
			- -
				- Key Points
				  
				  •   The cloud is made up of a large number of virtual servers that you can rent for your own use. You and your customers access these servers remotely over the Internet and pay for the amount of server time used.
				    
				  •   Virtualization is a technology that allows multiple server instances to be run on the same physical computer. This means you can create isolated instances of your software for deployment on the cloud.
				    
				  •   Virtual machines are physical server replicas on which you run your own operating system, technology stack, and applications.
				    
				  •   Containers are a lightweight virtualization technology that allow rapid replication and deployment of virtual servers. All containers run the same operating system. Docker is currently the most widely used container technology.
				    
				  •   A fundamental feature of the cloud is that “everything” can be delivered as a service and accessed over the Internet. A service is rented rather than owned and is shared with other users.
				    
				  •   Infrastructure as a service (IaaS) means that computing, storage, and other services are available in the cloud. There is no need to run your own physical servers.
				    
				  •   Platform as a service (PaaS) means using services provided by a cloud platform vendor to make it possible to auto-scale your software in response to demand.
				    
				  •   Software as a service (SaaS) means that application software is delivered as a service to users. This has important benefits for users, such as lower capital costs, and for software vendors, such as simpler deployment of new software releases.
				    
				  •   Multi-tenant systems are SaaS systems where all users share the same database, which may be adapted at run time to their individual needs. Multi-instance systems are SaaS applications where each user has their own separate database.
				    
				  •   The key architectural issues for cloud-based software are the cloud platform to be used, whether to use a multi-tenant or multi-instance database, scalability and resilience requirements, and whether to use objects or services as the basic components in the system. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gsywp9rcm8z785emyrtnk33t))
			- -
		- 6 Microservices Architecture
			- -
				- Q: What is a (micro)service? #flashcard
					- In practice, it was not easy to scale or move individual services without affecting other parts of the system.
					  
					  Amazon’s approach was to rethink what a service should be. They concluded that a service should be related to a single business function. Instead of relying on a shared database and other services in the system, services should be completely independent, with their own database. They should also manage their own user interface. Replacing or replicating a service should therefore be possible without having to change any other services in the system.
					  
					  This type of service has become known as a “microservice.” Microservices are small-scale, stateless services that have a single responsibility. Software products that use microservices are said to have a microservices architecture. If you need to create cloud-based software products that are adaptable, scalable, and resilient, then I recommend that you use a microservices architecture.
				- ([View Highlight](https://read.readwise.io/read/01gsyz049y7t1pqkkez1qmbbsj))
			- -
			- 6.3 RESTful services
				- -
					- Table 6.4 RESTful service principles
					  
					  Principle
					  
					  Explanation
					  
					  Use HTTP verbs
					  
					  The basic methods defined in the HTTP protocol (GET, PUT, POST, DELETE) must be used to access the operations made available by the service.
					  
					  Stateless services
					  
					  Services must never maintain internal state. As I have already explained, microservices are stateless, so fit with this principle.
					  
					  URI addressable
					  
					  All resources must have a URI, with a hierarchical structure, that is used to access subresources.
					  
					  Use XML or JSON
					  
					  Resources should normally be represented in JSON or XML or both. Other representations, such as audio and video representations, may be used if appropriate. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gsz07zqvr39r6yxh50aj4476))
				- -
				- -
					- What are the CRUD operations in RESTful? #flashcard
						- Table 6.5 RESTful service operations
						  
						  Action
						  
						  Implementation
						  
						  Create
						  
						  Implemented using HTTP POST, which creates the resource with the given URI. If the resource has already been created, an error is returned.
						  
						  Read
						  
						  Implemented using HTTP GET, which reads the resource and returns its value. GET operations should never update a resource so that successive GET operations with no intervening PUT operations always return the same value.
						  
						  Update
						  
						  Implemented using HTTP PUT, which modifies an existing resource. PUT should not be used for resource creation.
						  
						  Delete
						  
						  Implemented using HTTP DELETE, which makes the resource inaccessible using the specified URI. The resource may or may not be physically deleted.
					- ([View Highlight](https://read.readwise.io/read/01gsz0e0ds2vtzp2w0fwm2mkdx))
				- -
				- -
					- Are RESTful services asynchronous? #flashcard
						- As the HTML transfer protocol used by most RESTful services is a request/response protocol, RESTful services are normally synchronous services.
					- ([View Highlight](https://read.readwise.io/read/01gsz0mswdm0xqggb2a4xjjp0e))
				- -
				- -
					- When a system has a lot of small parts, it is more complicated to put it all together than if it was one big part. 
					  
					  Different teams decide which programming languages, databases, libraries, and other support software to use. This means that there is no one way to put the system together. Also, the parts may need to be changed quickly and if one team is responsible for updating all the parts at the same time, it can be slow. 
					  
					  Therefore, it is now common for the development team to be responsible for building the system and keeping it running. This is called DevOps, which means "Development" and "Operations" combined. #flashcard
						- When a system is composed of tens or even hundreds of microservices, deployment of the system is more complex than for monolithic systems. The service development teams decide which programming language, database, libraries, and other support software should be used to implement their service. Consequently, there is no “standard” deployment configuration for all services. Furthermore, services may change very quickly and there is the potential for a “deployment bottleneck” if a separate system admin team is faced with the problem of updating several services at the same time.
						  
						  Consequently, when a microservices architecture is used, it is now normal practice for the development team to be responsible for deployment and service management as well as software development. This approach is known as DevOps—a combination of “development” and “operations.”
					- tags:: [[ghost]]
					- ([View Highlight](https://read.readwise.io/read/01gsz0rh743e80e9jyvmwv6zfy))
				- -
				- -
					- Key points #flashcard
						- Key Points
						  
						  •   A microservice is an independent and self-contained software component that runs in its own process and communicates with other microservices using lightweight protocols.
						    
						  •   Microservices in a system can be implemented using different programming languages and database technologies.
						    
						  •   Microservices have a single responsibility and should be designed so that they can be easily changed without having to change other microservices in the system.
						    
						  •   Microservices architecture is an architectural style in which the system is constructed from communicating microservices. It is well suited to cloud-based systems where each microservice can run in its own container.
						    
						  •   The two most important responsibilities of architects of a microservices system are to decide how to structure the system into microservices and to decide how microservices should communicate and be coordinated.
						    
						  •   Communication and coordination decisions involve microservice communication protocols, data sharing, whether services should be centrally coordinated, and failure management.
						    
						  •   The RESTful architectural style is widely used in microservice-based systems. Services are designed so that the HTTP verbs—GET, POST, PUT, and DELETE—map onto the service operations.
						    
						  •   The RESTful style is based on digital resources that, in a microservices architecture, may be represented using XML or, more commonly, JSON.
						    
						  •   Continuous deployment is a process in which new versions of a service are put into production as soon as a service change has been made. It is a completely automated process that relies on automated testing to check that the new version is of production quality.
						    
						  •   If continuous deployment is used, you may need to maintain multiple versions of deployed services so that you can switch to an older version if problems are discovered in a newly deployed service.
					- ([View Highlight](https://read.readwise.io/read/01gsz12rdec4y729dna7n467jf))
				- -
				- -
					- •   *Building Microservices* This book is an excellent and readable overview of microservices and the issues to be considered when constructing microservices architectures. (S. Newman, O’Reilly, 2015)
					    
					  •   “Microservices” This is probably the most readable introduction to microservices that I have found. I highly recommend it. (J. Lewis and M. Fowler, 2014)
					    
					    [https://martinfowler.com/articles/microservices.html](https://martinfowler.com/articles/microservices.html) #flashcard
					- tags:: [[reference]]
					- ([View Highlight](https://read.readwise.io/read/01gsz1j41gf5x6jzj31pkfs227))
				- -
				- -
					- “RESTful Web Services: A Tutorial” Many tutorials on RESTful web services are available and naturally they are very similar. This tutorial is a comprehensive and clear introduction to the RESTful approach to web service implementation. (M. Vaqqas, 2014)
					  
					  [http://www.drdobbs.com/web-development/restful-web-services-a-tutorial/240169069](http://www.drdobbs.com/web-development/restful-web-services-a-tutorial/240169069) #flashcard
					- tags:: [[reference]]
					- ([View Highlight](https://read.readwise.io/read/01gsz1jrvymy7z25qvbnpp626p))
				- -
		- 7 Security and Privacy
			- -
				- Cloud-based security user’s preventions #flashcard
					- If you offer your product as a cloud-based service, you should include features that help users manage operational security and deal with security problems that may arise. For example:
					  
					  1.  Auto-logout addresses the common problem of users forgetting to log out from a computer used in a shared space. This feature reduces the chances of an unauthorized person gaining access to the system.
					    
					  2.  User command logging makes it possible to discover actions taken by users that have deliberately or accidentally damaged some system resources. This feature helps to diagnose problems and recover from them and also deters malicious legitimate users, as they know that their behavior will be logged.
					    
					  3.  Multifactor authentication reduces the chances of an intruder gaining access to the system using stolen credentials.
				- ([View Highlight](https://read.readwise.io/read/01gsz2z67b1bzp516s9tyqrerm))
			- -
			- -
				- Advantages of using federated identities for authentication: #flashcard
					- There are two advantages of using federated identities for authentication:
					  
					  1.  You don’t have to maintain your own database of passwords and other secret information. System attackers often try to gain access to this database, so if you maintain your own, you have to take stringent security precautions to protect it. Implementing and maintaining an authentication system are expensive processes for small product companies. Large companies, such as Google and Facebook, have the resources and the expertise to do this.
					    
					  2.  The identity provider may give additional information about users that can be used to personalize your service or to target advertising at users. Of course, when you set up a federated identity system with a major provider, then you have to ask users whether they are willing to share their information with you. There is no guarantee they will agree to this.
				- ([View Highlight](https://read.readwise.io/read/01gsz3gj4vs087yjwxxx0q8bze))
			- -
			- -
				- .. #flashcard
					- As an alternative to using a login/password pair, a commonly used approach to mobile authentication is to install an authentication token on the mobile device. When the app starts, the token is sent to the service provider to identify the user of the device. This approach to authentication is shown in [Figure 7.6](https://readwise.io/reader/document_raw_content/35544017#P7001016428000000000000000001359).
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/35544017/idf0200-01_png-f0200-01.png)
				- ([View Highlight](https://read.readwise.io/read/01gsz3ndkx5y78m8qy9xqsdjqs))
			- -
			- -
				- Key points #flashcard
					- Key Points
					  
					  •   Security is a technical concept that relates to a software system's ability to protect itself from malicious attacks that may threaten its availability, the integrity of the system and its data, and the theft of confidential information.
					    
					  •   Common types of attack on software products are injection attacks, cross-site scripting attacks, session hijacking attacks, denial-of-service attacks, and brute force attacks.
					    
					  •   Authentication may be based on something a user knows, something a user has, or some physical attribute of the user.
					    
					  •   Federated authentication involves devolving responsibility for authentication to a third party, such as Facebook or Google, or to a business's authentication service.
					    
					  •   Authorization involves controlling access to system resources based on the user's authenticated identity. Access control lists are the most commonly used mechanism to implement authorization.
					    
					  •   Symmetric encryption involves encrypting and decrypting information using the same secret key. Asymmetric encryption uses a key pair—a private key and a public key. Information encrypted using the public key can only be decrypted using the private key.
					    
					  •   A major issue in symmetric encryption is key exchange. The TLS protocol, which is used to secure web traffic, gets around this problem by using asymmetric encryption for transferring the information required to generate a shared key.
					    
					  •   If your product stores sensitive user data, you should encrypt that data when they are not in use.
					    
					  •   A key management system (KMS) stores encryption keys. Using a KMS is essential because a business may have to manage thousands or even millions of keys and may have to decrypt historical data that were encrypted using an obsolete encryption key.
					    
					  •   Privacy is a social concept that relates to how people feel about the release of their personal information to others. Different countries and cultures have different ideas about what information should and should not be private.
					    
					  •   Data protection laws have been passed in many countries to protect individual privacy. They require companies that manage user data to store them securely, to ensure that they are not used or sold without the permission of users, and to allow users to view and correct personal data held by the system.
				- ([View Highlight](https://read.readwise.io/read/01gsz4cq0c71vh4q2twp5xn8e7))
			- -
			- -
				- Key Points #flashcard
					- Key Points
					  
					  •   The most important quality attributes for most software products are reliability, security, availability, usability, responsiveness, and maintainability.
					    
					  •   To avoid introducing faults into your program, you should use programming practices that reduce the probability that you will make mistakes.
					    
					  •   You should always aim to minimize complexity in your programs. Complexity makes programs harder to understand. It increases the chances of programmer errors and makes the program more difficult to change.
					    
					  •   Design patterns are tried and tested solutions to commonly occurring problems. Using patterns is an effective way to reduce program complexity.
					    
					  •   Refactoring is the process of reducing the complexity of an existing program without changing its functionality. It is good practice to refactor your program regularly to make it easier to read and understand.
					    
					  •   Input validation involves checking all user inputs to ensure that they are in the format that is expected by your program. Input validation helps avoid the introduction of malicious code into your system and traps user errors that can pollute your database.
					    
					  •   Regular expressions are a way of defining patterns that can match a range of possible input strings. Regular expression matching is a compact and fast way of checking that an input string conforms to the rules you have defined.
					    
					  •   You should check that numbers have sensible values depending on the type of input expected. You should also check number sequences for feasibility.
					    
					  •   You should assume that your program may fail and manage these failures so that they have minimal impact on the user.
					    
					  •   Exception management is supported in most modern programming languages. Control is transferred to your own exception handler to deal with the failure when a program exception is detected.
					    
					  •   You should log user updates and maintain user data snapshots as your program executes. In the event of a failure, you can use these to recover the work that the user has done. You should also include ways of recognizing and recovering from external service failures.
				- ([View Highlight](https://read.readwise.io/read/01gsz7tstjvxg4ye9ske8jpqjc))
			- -
			- -
				- “McCabe’s Cyclomatic Complexity and Why We Don’t Use It”
				  
				  This post is a good explanation of the problems with the widely used cyclomatic complexity metric used to measure the decision complexity of code. As the author says, there is no simple measurement that can express complexity as a single number. (B. Hummel, 2014)
				  
				  https #flashcard
				- tags:: [[reference]]
				- ([View Highlight](https://read.readwise.io/read/01gsz7xnrc3m2mvx84fsfvf059))
			- -
		- 9 Testing
			- -
				- “The Art of Agile Development: Test-Driven Development” This is an online version of a chapter from the book The Art of Agile Development, a good description of test-driven development that goes into much more detail than I do here. Examples are in Java. (J. Shore, 2010)
				  
				  [http://www.jamesshore.com/Agile-Book/test_driven_development.html](http://www.jamesshore.com/Agile-Book/test_driven_development.html) #flashcard
				- tags:: [[reference]]
				- ([View Highlight](https://read.readwise.io/read/01gszh09r6jbvjm324k537x5ge))
			- -
			- -
				- •   “Introducing BDD” Behavior-driven design is an evolution of test-driven design where the focus of the testing process is the expected behavior of the software being tested. A stylized language can be used to describe behavior and tests derived from this description. I have never tried this approach, but it seems to get around some of the problems with TDD. (D. North, 2006)
				    
				    [https://dannorth.net/introducing-bdd/](https://dannorth.net/introducing-bdd/) #flashcard
				- tags:: [[reference]]
				- ([View Highlight](https://read.readwise.io/read/01gszh17xqxv4jnxgwkhgwn8fp))
			- -
		- 10 DevOps and Code Management
			- -
				- How does git know when there is a conflict? #flashcard
					- Git compares versions of files on a line-by-line basis. There is no conflict if developers have changed different lines in the file. If they have made changes to the same lines, however, then a merge conflict is signaled. Git highlights the lines where the conflict occurs, and it is up to the developers to resolve these conflicts
				- ([View Highlight](https://read.readwise.io/read/01gszhx2p779mnpbxv87048k8y))
			- -
			- -
				- About the reason for a pipeline #flashcard
					- In a continuous integration environment, developers have to make sure that they don’t “break the build.” Breaking the build means pushing code to the project repository, which when integrated, causes some of the system tests to fail. This holds up other developers. If this happens to you, your priority is to discover and fix the problem so that normal development can continue. To avoid breaking the build, you should always adopt an “integrate twice” approach to system integration. You should integrate and test on your own computer before pushing code to the project repository to trigger the integration server ([Figure 10.10](https://readwise.io/reader/document_raw_content/35544017#P7001016428000000000000000001E31)).
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/35544017/idf0313-01_png-f0313-01.png)
				- ([View Highlight](https://read.readwise.io/read/01gszj7zkxfxyqywksc2qsze3a))
			- -
			- -
				- Why containers? #flashcard
					- Continuous delivery means that, after making changes to a system, you ensure that the changed system is ready for delivery to customers. This means that you have to test it in a production environment to make sure that environmental factors do not cause system failures or slow down its performance. As well as feature tests, you should run load tests that show how the software behaves as the number of users increases. You may also run tests to check the throughput of transactions and your system’s response time.
					  
					  The simplest way to create a replica of a production environment is to run your software in a container, as I explained in [Chapter 5](https://readwise.io/reader/document_raw_content/35544017#P7001016428000000000000000000AFA). Your production environment is defined as a container, so to create a test environment
				- ([View Highlight](https://read.readwise.io/read/01gszjgevwk8y75b7ew7xsc1rf))
			- -
			- -
				- About continuous deployment feasibility #flashcard
					- Continuous deployment is obviously only practical for cloud-based systems. If your product is sold through an app store or downloaded from your website, continuous integration and delivery make sense. A working version is always available for release. If you update the downloadable version regularly, your customers can decide when to update the software on their computers or mobile devices
				- ([View Highlight](https://read.readwise.io/read/01gszjm6ky32j005jnpdzygg6e))
			- -
			- -
				- “What Is DevOps?” This blog post, written as DevOps was just starting to be used, is a thoughtful explanation of what DevOps means. It does not go into detail but encapsulates the essence of DevOps. (E. Mueller, 2010)
				  
				  [https://theagileadmin.com/what-is-dev/](https://theagileadmin.com/what-is-dev/) #flashcard
				- tags:: [[reference]]
				- ([View Highlight](https://read.readwise.io/read/01gszjxexj7cka0e3em6hd4d33))
			- -