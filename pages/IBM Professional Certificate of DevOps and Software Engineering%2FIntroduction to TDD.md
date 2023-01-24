public:: true
tags:: #Coursera #IBM-DevOps #DevOps
deck:: [[Coursera::IBM DevOps::Introduction to TDD]]

-
- ## Tasks {{renderer :todomaster}}
	- DONE Week 1
	  id:: 63ce7392-cf1f-40bc-93e8-b0f4eb2bb361
	  :LOGBOOK:
	  CLOCK: [2023-01-23 Mon 12:47:06]--[2023-01-23 Mon 13:55:02] =>  01:07:56
	  :END:
	- DOING Week 2
	  id:: 63cfbc8e-bc6b-40ef-9426-5259d701627a
	  :LOGBOOK:
	  CLOCK: [2023-01-24 Tue 12:13:44]
	  :END:
	- TODO Week 3
	- TODO Week 4
-
- # Week 1
	- ## Welcome
	- ## Introduction to Testing
		- ### The Importance of Testing
			- > "If it's worth building, it's worth testing.
			  If it's not worth testing, why are you wasting your time working on it?
			  -- Scott Ambler, agiledata.org
			- TDD is crucial for CD
		- ### Why Developers don't test
			- Make sure that the tests pass before writing any new code
			- The time that you are spending now in testing or TDD will save you hours and hours of later debugging
			- Even when your code is good, you'll depend on third-party dependencies that could break your code -- So test is important!
		- ### Testing Levels and Release Cycle
			- At the lowest level, it's **unit testing**
				- The purpose of this level is to validate that each unit performs as designed
				- It requires close knowledge of the code
				- These are the tests that run when you integrate your code to let you if you broke something.
			- At the next level, it's **Integration Testing**
				- You combine different units to see how they work and behave together correctly
				- This is the level of Behaviour Driven Development. You are testing the behaviour.
			- Next, **System Tests**
				- At this level, the entire software process is being tested
				- We make sure that the system works like in production
			- Finally, it's **Acceptance Tests**
				- The system is tested for acceptability.
				- The purpose of this test is to evaluate the system's compliance with the business requierements
				- At this point, we want to ensure the validation of our code which we've already developed (until now).
			- ![image.png](../assets/image_1674476138370_0.png)
			- ![image.png](../assets/image_1674476191183_0.png)
		- ### TDD and BDD
			- **BDD**
				- Focuses on the behavior of the system from the outside
				- NOT the minutia of how the system works from the inside
				- It's great for integration testing
				- Uses a syntax that can be understood by both developers and stakeholders
			- **TDD**
				- Focuses on how the system works from the inside
				- Tests drive the design
				- It keeps you focused on the purpose of the code
			- BDD is for integration and acceptance testing
			- TDD is for driving your development by writing your tests first
			- BDD ensures that you are building the "right thing"
			- TDD ensures that you are building the "thing right"
			- ![image.png](../assets/image_1674476762901_0.png)
		- ### Testing Case Study
			- It's important to use fixtures that are strange to the use case. Such as `True` or `None` or `"stfr"`
			- ![image.png](../assets/image_1674477384725_0.png)
			- You must code **defensively**. Because your code will be called from unkwon methods.
		-
		- ### Questions
			- Why do developers need both test driven development (TDD) and behavior driven development (BDD)?
			  id:: 63ce8264-4df7-4ace-9e69-e6d73dff5ef9
			  
			  [ ] Developers use both TDD and BDD to communicate with clients.
			  
			  [ ] TDD and BDD together ensure that you are building the software right.
			  
			  [ ]TDD and BDD complement each other in the development process.
			  
			  [ ] Developers use both TDD and BDD to perform acceptance testing. #flashcard
				- **[x] TDD and BDD complement each other in the development process.**
-
- # Week 2
	- ## Introduction to Test Driven Development
		- ### Benefits of Test Driven Development
			- TDD means that your unit test cases drive the design of your code while developing
				- It's a design approach to code.
				- Because you have to think as a customer, externally, of your code.
			-
-
-
-
-
-
-
-