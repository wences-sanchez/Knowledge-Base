tags:: #Udacity, Cloud Development
deck:: [[Cloud Development Nanodegree::Full Stack Apps on AWS]]

-
- ## 1. Cloud Basics and Parts of a Cloud #flashcard
  id:: 63db7934-5429-44cc-bd99-8d52a580cf60
	- ### Defining Our Cloud
		- Cloud can be used for a variety of purposes:
			- Store data of all users into a central store
			- Scale our data store
			- Compute very hard math and cost problems
			- Parallelize compute power
			-
- ## 2. Monolithic vs. Loosely Coupled Systems #flashcard
  id:: 63db7934-95fa-4c61-a0c1-a461024191b2
	- Traditionally, the different features were inside a single web server
	- Often, those systems were **tightly coupled**.
		- Tightly coupled systems are **quick to stand-up**, but may result in higher **Technical Debt**.
	- It's a much better idea to use **loosely coupled** systems
		- Loosely coupled systems require more time upfront but are generally easier to improve upon.
	- What are microservices? #flashcard
	  id:: 63566061-94db-47f9-b52e-86e1f31ddcc7
		- Microservices are individual specialized systems (software deployed on specialized infrastructure) designed to accomplish a specific task.  Specific tasks may include things like authentication, image processing, or data management.
-
- ## 3. Request Response and APIs #flashcard
  id:: 63db7934-b8ee-4c36-9336-ac9f6f7ec4ce
	- ### Request Response and APIs
		- ![image.png](../assets/image_1675243528825_0.png)
		-
	- ### HTTP Responses
		- Some common Status Codes
			- 200 Success
			- 400 Bad Request
			- 401 Unauthorized
			- 403 Forbidden
			- 404 Not Found
			- 500 Internal Server Error
			- ....many more
			- It's important to specify each status in our code
			- https://www.restapitutorial.com/httpstatuscodes.html
-
-
-