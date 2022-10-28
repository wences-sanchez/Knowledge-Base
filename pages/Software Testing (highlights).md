title:: Software Testing (highlights)
author:: [[]]
full-title:: "Software Testing"
category:: #books

tags:: #[[O'Reilly-Learning]]

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- 1. Software Testing Background
		- The goal of a software tester is to find bugs.
		- If you're only testing things that should work and setting up your tests so they'll pass, you will miss the things that don't work. You will miss the bugs.
			- **Note**: How important it's to think how to break!
		- The goal of a software tester is to find bugs and find them as early as possible.
		- The goal of a software tester is to find bugs, find them as early as possible, and make sure they get fixed.
			- **Note**: What is the goal of a tester?
		- At first glance, it may appear that a software tester's job would be easier than a programmer's. Breaking code and finding bugs must surely be easier than writing the code in the first place. Surprisingly, it's not.
	- 2. The Software Development Process
		- The term used in the software industry to describe a software product component that's created and passed on to someone else is deliverable. The easiest way to explain what all these deliverables are is to organize them into major categories
			- **Note**: What is a software deliverable?
		- For the same reasons that programmers must plan and document their work, software testers must as well. It's not unheard of for a software test team to create more deliverables than the programmers.
			- **Note**: Testers' deliverables
		- From a testing perspective, the waterfall model offers one huge advantage over the other models presented so far. Everything is carefully and thoroughly specified. By the time the software is delivered to the test group, every detail has been decided on, written down, and turned into software. From that, the test group can create an accurate plan and schedule. They know exactly what they're testing, and there's no question about whether something is a feature or a bug.But, with this advantage, comes a large disadvantage. Because testing occurs only at the end, a fundamental problem could creep in early on and not be detected until days before the scheduled product release. Remember from Chapter 1, “Software Testing Background,” how the cost of bugs increases over time? What's needed is a model that folds the testing tasks in earlier to find problems before they become too costly.
			- **Note**: Waterfall process and Testing...
	- 3. The Realities of Software Testing
		- One key concept that software testers need to learn is how to reduce the huge domain of possible tests into a manageable set, and how to make wise risk-based decisions on what's important to test and what's not.
		- To overcome the pesticide paradox, software testers must continually write new and different tests to exercise different parts of the program and find more bugs.
			- **Note**: How can you overcome the 'pesticide paradox'?
		- Don't just report bad news. If you find a piece of code surprisingly bug free, tell the world. Pop into a programmer's cubicle occasionally just to chat. If all you ever do is report bad news, people will see you coming and will run and hide.
			- **Note**: Tester's tip
		- Verification is the process confirming that something—software—meets its specification. Validation is the process confirming that it meets the user's requirements.
			- **Note**: What are Verification and Validation?
	- 4. Examining the Specification
		- There is a risk to white-box testing. It's very easy to become biased and fail to objectively test the software because you might tailor the tests to match the code's operation.
			- **Note**: Note about the white-box tests
		- Tell your project team, “This is what I plan to test and submit bugs against.” You'll be amazed at how many details they'll immediately fill in.
			- **Note**: Professional tip
		- It's important to understand the customer's expectations. Remember that the definition of quality means “meeting the customer's needs.” As a tester, you must understand those needs to test that the software meets them.
			- **Note**: What means quality, meanly?
		- If you review a portion of the spec and don't understand it, don't assume that it's correct and go on. Eventually, you'll have to use this specification to design your software tests, so you'll eventually have to understand it.
			- **Note**: Tip about long specs.
	- 5. Testing the Software with Blinders On
		- Selecting test cases is the single most important task that software testers do. Improper selection can result in testing too much, testing too little, or testing the wrong things. Intelligently weighing the risks and reducing the infinite possibilities to a manageable effective set is where the magic is.
			- **Note**: Tip about being effective at testing
		- When designing and running your test cases, always run the test-to-pass cases first. It's important to see if the software fundamentally works before you throw the kitchen sink at it. You might be surprised how many bugs you find just using the software normally.
			- **Note**: Tip about 'test-to-pass' and 'test-to-fail'
		- So, with invalid, wrong, incorrect, and garbage data testing, have some fun. If the software wants numbers, give it letters. If it accepts only positive numbers, enter negative numbers. If it's date sensitive, see if it'll work correctly on the year 3000. Pretend to have “fat fingers” and press multiple keys at a time.
			- **Note**: Test input ideas
		- Stress testing is running the software under less-than-ideal conditions—low memory, low disk space, slow CPUs, slow modems, and so on.
			- **Note**: What is stress testing?
	- 17. Planning Your Test Effort
		- The test plan is a by-product of the detailed planning process that's undertaken to create it. It's the planning process that matters, not the resulting document.
			- **Note**: ¿Para qué hago el test plan si soy yo solo y el proyecto es corto y estamos en la era agile?
			  Pues para pensar cómo voy a testear mi código. El documento que está en el GitHub es solo el resultado como deliverable del proyecto de pensarlo