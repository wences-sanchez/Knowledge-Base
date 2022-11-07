title:: Test-Driven Development With Python (highlights)
deck:: [[O'Reilly-Learning::Test-Driven Development With Python]]
author:: [[]]
full-title:: "Test-Driven Development With Python"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 3. Testing a Simple Home Page with Unit Tests
		- -
			- Unit Tests VS Functional Tests #flashcard
			  id:: ffe14d5b-9a13-4e87-a297-8a8dca87e917
				- Unit Tests, and How They Differ from Functional Tests
				  As with so many of the labels we put on things, the line between unit tests and functional tests can become a little blurry at times. The basic distinction, though, is that functional tests test the application from the outside, from the point of view of the user. Unit tests test the application from the inside, from the point of view of the programmer.
		- -
		- -
			- The TDD approach I’m following wants our application to be covered by both types of test. Our workflow will look a bit like this:
			  id:: f5d56a03-4e85-4224-aa60-72e2b5575af1
			  
			  We start by writing a functional test, describing the new functionality from the user’s point of view.
			  Once we have a functional test that fails, we start to think about how to write code that can get it to pass (or at least to get past its current failure). We now use one or more unit tests to define how we want our code to behave—the idea is that each line of production code we write should be tested by (at least) one of our unit tests.
			  Once we have a failing unit test, we write the smallest amount of application code we can, just enough to get the unit test to pass. We may iterate between steps 2 and 3 a few times, until we think the functional test will get a little further.
			  Now we can rerun our functional tests and see if they pass, or get a little further. That may prompt us to write some new unit tests, and some new code, and so on.
			  You can see that, all the way through, the functional tests are driving what development we do from a high level, while the unit tests drive what we do at a low level.
			  
			  Does that seem slightly redundant? Sometimes it can feel that way, but functional tests and unit tests do really have very different objectives, and they will usually end up looking quite different.
			  
			  NOTE
			  Functional tests should help you build an application with the right functionality, and guarantee you never accidentally break it. Unit tests should help you to write code that’s clean and bug free. #flashcard
		- -