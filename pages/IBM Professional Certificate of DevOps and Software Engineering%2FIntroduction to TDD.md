tags:: #Coursera #IBM-DevOps #DevOps
deck:: [[Coursera::IBM DevOps::Introduction to TDD]]

-
- ## Tasks
	- DOING Week 1
	  :LOGBOOK:
	  CLOCK: [2023-01-23 Mon 12:47:06]
	  :END:
	- TODO Week 2
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
				- At this level, the entire software