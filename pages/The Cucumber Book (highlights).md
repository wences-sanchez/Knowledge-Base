title:: The Cucumber Book (highlights)
deck:: [[O'Reilly-Learning::The Cucumber Book]]
author:: [[]]
full-title:: "The Cucumber Book"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Data Tables
		- -
			- Feature​:
			  id:: 64f21c00-c1e5-476c-9955-af109751702c
			  ​ 	  ​Scenario​:
			  ​ 	    ​Given a board like this​:
			  ​ 	      |   | 1 | 2 | 3 |
			  ​ 	      | 1 |   |   |   |
			  ​ 	      | 2 |   |   |   |
			  ​ 	      | 3 |   |   |   |
			  ​ 	    When player x plays in row 2, column 1
			  ​ 	    ​Then the board should look like this​:
			  ​ 	      |   | 1 | 2 | 3 |
			  ​ 	      | 1 |   |   |   |
			  ​ 	      | 2 | x |   |   |
			  ​ 	      | 3 |   |   |   | #flashcard
		- -
	- Scenario Outline
		- -
			- Once you have a scenario outline with a few examples, it’s very easy to think of more examples, and even easier to add them. Before you know it, you have a huge, very comprehensive table of examples—and a problem.
			  id:: bb128a52-e5e1-4367-a8e6-98fd1d34e8f6
			  
			  Why?
			  
			  On a system of any serious complexity, you can quite quickly start to experience what mathematicians call combinatorial explosion, where the number of different combinations of inputs and expected outputs becomes unmanageable. In trying to cover every possible eventuality, you end up with rows and rows of example data for Cucumber to execute. Remember that each of those little rows represents a whole scenario that might take several seconds to execute, and that can quickly start to add up. When your tests take longer to run, you slow down your feedback loop, making the whole team less productive as a result. #flashcard
		- -
		- -
			- Although this is a useful technique, be careful that your programmer’s instinct to reduce duplication at all costs doesn’t take over here.[17] If you move too much of the text of a step into the examples table, it can be very hard to read the flow of the scenario. Remember your goal is readability, so don’t take this too far, and always test your features by getting other people to regularly read them and give you feedback. #flashcard
			  id:: bb2b387f-99db-4b31-ba06-63dae970de17
		- -
	- Working Together
		- -
			- Let’s rewrite the scenario without the passwords:
			  id:: 4c6d989d-d03a-4392-bb8c-dbb84707618f
			  
			  ​ 	​Scenario​: Check inbox
			  ​ 	  Given a User ​"Dave"​
			  ​ 	  And a User ​"Sue"​
			  ​ 	  And an email to ​"Dave"​ from ​"Sue"​
			  ​ 	  When I sign in as ​"Dave"​
			  ​ 	  Then I should see 1 email from ​"Sue"​ in my inbox
			  This is definitely an improvement, making it easier to read and understand the essence of the scenario. Let’s try stripping away some more of the noise:
			  
			  ​ 	​Scenario​: Check inbox
			  ​ 	  Given I have received an email from ​"Sue"​
			  ​ 	  When I sign in
			  ​ 	  Then I should see 1 email from ​"Sue"​ in my inbox
			  Now we have a simple three-step scenario that’s clear and concise #flashcard
		- -
		- -
			- Cucumber has to be a declarative language #flashcard
			  id:: 4ca3c984-c7f0-460c-9164-800c6d36e2a3
				- In computer programming, there are two contrasting styles for expressing the instructions you give to a computer to make it do something for you. These styles are called imperative programming and declarative programming.
				  
				  Imperative programming means using a sequence of commands for the computer to perform in a particular order. Ruby is an example of an imperative language: you write a program as a series of statements that Ruby runs one at a time, in order. A declarative program tells the computer what it should do without prescribing precisely how to do it. CSS is an example of a declarative language: you tell the computer what you want the various elements on a web page to look like, and you leave it to take care of the rest.
		- -
		- -
			- Tienes que escribir el qué, no el cómo! #flashcard
			  id:: c0d34c99-645a-4df9-ac96-55acdcee7719
				- Scenario​: Redirect user to originally requested page after logging in
				  ​ 	  Given I am an unauthenticated User
				  ​ 	  When I attempt to view some restricted content
				  ​ 	  Then I am shown a login form
				  ​ 	  When I authenticate with valid credentials
				  ​ 	  Then I should be shown the restricted content
				  The beauty of this style is that it is not coupled to any specific implementation of the user interface
		- -
		- -
			- Puedes enlazar varios tests con un mismo step!!! #flashcard
			  id:: 3d23ce76-bab6-4c7d-97b6-f42f0d9efa76
				- It’s true that using declarative style will mean you have to write more step definitions, but you can keep the code in those step definitions short
		- -
	- Caring for Your Tests
		- -
			- It might seem like stating the obvious, but having a lot of scenarios is by far the easiest way to give yourself a slow overall feature run. We’re not trying to suggest you give up on BDD and go back to cowboy coding, but we do suggest you treat a slow feature run as a red flag. Having lots of tests has other disadvantages than just waiting a long time for feedback. It’s hard to keep a large set of features organized, making them awkward for readers to navigate around. Maintenance is also harder on the underlying step definitions and support code.
			  id:: 4bc2045a-987e-4bb4-b676-10aed8b6e8bc
			  
			  We find that teams that have a single humongous build also tend to have an architecture that could best be described as a big ball of mud. #flashcard
		- -
	- 7. Step Definitions: On the Inside
		- -
			- How is Cucumber used in the real life? #flashcard
			  id:: d1e90621-22fb-462d-b116-b21c53127c6d
				- Now we’re going to pick up this scenario and work outside-in, designing the system as we go, just as we would on a real project
		- -
	- Sketching Out the Domain Model
		- -
			- Es mejor terminar de testear los steps del escenario que zambullirse en el TDD (un test funcional [escenario] fallido —> un nuevo ciclo en TDD) #flashcard
			  id:: 412e1b47-6d54-4d61-9e78-5adbfd773785
				- It’s tempting to pause here, move the Account class into a separate file, and start driving out the behavior we want using unit tests. We’re going to try to resist that temptation for now and stay on the outside of the Account class. If we can get a full tour through the scenario from this perspective, we’ll be more confident in the design of the class’s interface once we do step inside and start implementing it.
		- -
	- Removing Duplication with Transforms
		- -
			- Transform(​/^\d+$/​) ​do​ |number|
			  id:: 6238d548-dd04-4c9c-aebb-ed497ca6fe96
			  ​ 	  number.to_i
			  ​ 	​end​ #flashcard
		- -