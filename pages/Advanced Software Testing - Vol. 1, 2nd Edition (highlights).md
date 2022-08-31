title:: Advanced Software Testing - Vol. 1, 2nd Edition (highlights)
author:: [[]]
full-title:: "Advanced Software Testing - Vol. 1, 2nd Edition"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- 1 Testing Process
		- -
		- when you’re documenting the tests, keep in mind that you might not be documenting them just for yourself. What other testers will need to run them? Will the tests be reviewed by other project stakeholders? #space
		- -
	- 2 Test Management: Responsibilities for the Test Analyst
		- -
		- In some cases, values are not independent, in that the selection of one value from one subset constrains the choice in another subset #space
		- -
		- -
		- for those partitions that are ordered values, we select the minimum and maximum values—the boundary values—as test values. This technique can be applied at any level of testing. It can even be used during white-box testing when looking at loops, when looking at data structures such as lists and arrays, and during non-functional testing for boundaries in memory usage and performance. #space
		- -
		- -
		- When used properly, this technique will find situations where boundaries are in the wrong place, boundaries are just plain missing, or undesired boundaries exist #space
		- -
		- -
		- Conceptually, boundary value analysis is about testing the edges of equivalence classes #space
		- -
		- -
		- So, do all equivalence classes have boundary values? No, definitely not. Boundary value analysis is an extension of equivalence partitioning that applies only when the members of an equivalence class are ordered. #space
		- -
		- -
		- Notice that the number of columns—i.e., the number of business rules—is equal to 2 raised to the power of the number of conditions #space
		- -
		- -
		- To combine two or more columns, look for two or more columns that result in the same combination of actions. #space
			- #[[qa]]
		- -
		- -
		- What does a cause-effect graph look like? #card
			- Cause-effect graphs are simply pictorial representations of the same business logic that is shown in a decision table.
		- -
	- 3 Test Techniques
		- -
		- An oracle should not be the code, because otherwise we are only testing whether the compiler works. #space
		- -
		- -
		- It’s important to remember that fulfilling coverage criteria for a particular test design technique does not mean that your tests are in any way complete or exhaustive. Instead, it means that the model has run out of useful tests to suggest, based on that technique. #space
		- -
		- -
		- About Equivalence Partitioning #card
			- This technique is also very useful in constructing smoke tests, though testing of some of the less-risky partitions frequently is omitted in smoke tests.
		- -
		- -
		- If the conditions are not sufficient, but we must also refer to what conditions have existed in the past, then we’ll want to use state-based testing #space
		- -