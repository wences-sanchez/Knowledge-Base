title:: Software Testing (highlights)
author:: [[]]
full-title:: "Software Testing"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- 1. Software Testing Background
		- -
		- The goal of a software tester is to find bugs. #ñspace
		- -
		- -
		- How important it's to think how to break! #car
			- If you're only testing things that should work and setting up your tests so they'll pass, you will miss the things that don't work. You will miss the bugs.
		- -
		- -
		- The goal of a software tester is to find bugs and find them as early as possible. #ñspace
		- -
		- -
		- What is the goal of a tester? #car
			- The goal of a software tester is to find bugs, find them as early as possible, and make sure they get fixed.
		- -
		- -
		- At first glance, it may appear that a software tester's job would be easier than a programmer's. Breaking code and finding bugs must surely be easier than writing the code in the first place. Surprisingly, it's not. #ñspace
		- -
	- 2. The Software Development Process
		- -
		- What is a software deliverable? #car
		  id:: 63401535-142e-498e-8e2c-53f373719987
			- The term used in the software industry to describe a software product component that's created and passed on to someone else is deliverable. The easiest way to explain what all these deliverables are is to organize them into major categories
		- -
		- -
		- Testers' deliverables #car
		  id:: 63401535-8bbf-4c63-82db-b9eaf893c05b
			- For the same reasons that programmers must plan and document their work, software testers must as well. It's not unheard of for a software test team to create more deliverables than the programmers.
		- -
		- -
		- Waterfall process and Testing... #car
		  id:: 63401535-c8f6-4383-b819-fccc57e6fb08
			- From a testing perspective, the waterfall model offers one huge advantage over the other models presented so far. Everything is carefully and thoroughly specified. By the time the software is delivered to the test group, every detail has been decided on, written down, and turned into software. From that, the test group can create an accurate plan and schedule. They know exactly what they're testing, and there's no question about whether something is a feature or a bug.But, with this advantage, comes a large disadvantage. Because testing occurs only at the end, a fundamental problem could creep in early on and not be detected until days before the scheduled product release. Remember from Chapter 1, “Software Testing Background,” how the cost of bugs increases over time? What's needed is a model that folds the testing tasks in earlier to find problems before they become too costly.
		- -
	- 3. The Realities of Software Testing
		- -
		- One key concept that software testers need to learn is how to reduce the huge domain of possible tests into a manageable set, and how to make wise risk-based decisions on what's important to test and what's not. #ñspace
		- -
		- -
		- How can you overcome the 'pesticide paradox'? #car
		  id:: 63401535-c89b-4970-8fb6-32ead045cb6e
			- To overcome the pesticide paradox, software testers must continually write new and different tests to exercise different parts of the program and find more bugs.
		- -
		- -
		- Tester's tip #car
		  id:: 63401535-f654-465e-a421-b061fbb96ffe
			- Don't just report bad news. If you find a piece of code surprisingly bug free, tell the world. Pop into a programmer's cubicle occasionally just to chat. If all you ever do is report bad news, people will see you coming and will run and hide.
		- -
		- -
		- What are Verification and Validation? #car
			- Verification is the process confirming that something—software—meets its specification. Validation is the process confirming that it meets the user's requirements.
		- -
	- 4. Examining the Specification
		- -
		- Note about the white-box tests #car
		  id:: 63401535-072f-4023-b450-67e0d4ae96a6
			- There is a risk to white-box testing. It's very easy to become biased and fail to objectively test the software because you might tailor the tests to match the code's operation.
		- -
		- -
		- Professional tip #car
		  id:: 63401535-0a1c-4a1c-9083-b9f73199d562
			- Tell your project team, “This is what I plan to test and submit bugs against.” You'll be amazed at how many details they'll immediately fill in.
		- -
		- -
		- What means quality, meanly? #car
			- It's important to understand the customer's expectations. Remember that the definition of quality means “meeting the customer's needs.” As a tester, you must understand those needs to test that the software meets them.
		- -
		- -
		- Tip about long specs. #car
			- If you review a portion of the spec and don't understand it, don't assume that it's correct and go on. Eventually, you'll have to use this specification to design your software tests, so you'll eventually have to understand it.
		- -
	- 5. Testing the Software with Blinders On
		- -
		- Tip about being effective at testing #car
			- Selecting test cases is the single most important task that software testers do. Improper selection can result in testing too much, testing too little, or testing the wrong things. Intelligently weighing the risks and reducing the infinite possibilities to a manageable effective set is where the magic is.
		- -
		- -
		- Tip about 'test-to-pass' and 'test-to-fail' #car
			- When designing and running your test cases, always run the test-to-pass cases first. It's important to see if the software fundamentally works before you throw the kitchen sink at it. You might be surprised how many bugs you find just using the software normally.
		- -
		- -
		- Test input ideas #car
			- So, with invalid, wrong, incorrect, and garbage data testing, have some fun. If the software wants numbers, give it letters. If it accepts only positive numbers, enter negative numbers. If it's date sensitive, see if it'll work correctly on the year 3000. Pretend to have “fat fingers” and press multiple keys at a time.
		- -
		- -
		- What is stress testing? #car
			- Stress testing is running the software under less-than-ideal conditions—low memory, low disk space, slow CPUs, slow modems, and so on.
		- -
	- 17. Planning Your Test Effort
		- -
		- ¿Para qué hago el test plan si soy yo solo y el proyecto es corto y estamos en la era agile?
		  id:: 63401535-bf6b-4c60-a559-ef7cbe224b30
		  Pues para pensar cómo voy a testear mi código. El documento que está en el GitHub es solo el resultado como deliverable del proyecto de pensarlo #car
			- The test plan is a by-product of the detailed planning process that's undertaken to create it. It's the planning process that matters, not the resulting document.
		- -