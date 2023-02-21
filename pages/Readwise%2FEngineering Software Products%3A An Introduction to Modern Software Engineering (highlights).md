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