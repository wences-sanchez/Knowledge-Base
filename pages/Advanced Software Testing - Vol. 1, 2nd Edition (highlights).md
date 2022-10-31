title:: Advanced Software Testing - Vol. 1, 2nd Edition (highlights)
deck:: [[O'Reilly-Learning::Advanced Software Testing - Vol. 1, 2nd Edition]]
author:: [[]]
full-title:: "Advanced Software Testing - Vol. 1, 2nd Edition"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 1 Testing Process
		- -
			- when you’re documenting the tests, keep in mind that you might not be documenting them just for yourself. What other testers will need to run them? Will the tests be reviewed by other project stakeholders? #flashcard
		- -
	- 2 Test Management: Responsibilities for the Test Analyst
		- -
			- In some cases, values are not independent, in that the selection of one value from one subset constrains the choice in another subset #flashcard
		- -
		- -
			- for those partitions that are ordered values, we select the minimum and maximum values—the boundary values—as test values. This technique can be applied at any level of testing. It can even be used during white-box testing when looking at loops, when looking at data structures such as lists and arrays, and during non-functional testing for boundaries in memory usage and performance. #flashcard
		- -
		- -
			- When used properly, this technique will find situations where boundaries are in the wrong place, boundaries are just plain missing, or undesired boundaries exist #flashcard
		- -
		- -
			- Conceptually, boundary value analysis is about testing the edges of equivalence classes #flashcard
			  id:: a9a2d274-6a02-40d6-9d9c-d8312156c63e
		- -
		- -
			- So, do all equivalence classes have boundary values? No, definitely not. Boundary value analysis is an extension of equivalence partitioning that applies only when the members of an equivalence class are ordered. #flashcard
			  id:: e872dab9-6c92-4238-b258-bc4441e02873
		- -
		- -
			- Notice that the number of columns—i.e., the number of business rules—is equal to 2 raised to the power of the number of conditions #flashcard
			  id:: 67c9fbdf-260e-4a3b-a514-ccc6b6267d4e
		- -
		- -
			- To combine two or more columns, look for two or more columns that result in the same combination of actions. #flashcard
			  id:: 6f2aa3a7-c21a-4631-8140-ebcc05464223
			- tags:: [[qa]]
		- -
		- -
			- What does a cause-effect graph look like? #flashcard
				- Cause-effect graphs are simply pictorial representations of the same business logic that is shown in a decision table.
		- -
	- 3 Test Techniques
		- -
			- An oracle should not be the code, because otherwise we are only testing whether the compiler works. #flashcard
			  id:: 504d3008-8adb-442a-9ae7-66dabb53c32a
		- -
		- -
			- It’s important to remember that fulfilling coverage criteria for a particular test design technique does not mean that your tests are in any way complete or exhaustive. Instead, it means that the model has run out of useful tests to suggest, based on that technique. #flashcard
		- -
		- -
			- About Equivalence Partitioning #flashcard
				- This technique is also very useful in constructing smoke tests, though testing of some of the less-risky partitions frequently is omitted in smoke tests.
		- -
		- -
			- If the conditions are not sufficient, but we must also refer to what conditions have existed in the past, then we’ll want to use state-based testing #flashcard
		- -