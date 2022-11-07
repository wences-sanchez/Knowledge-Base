title:: Software Testing (highlights)
deck:: [[O'Reilly-Learning::Software Testing]]
author:: [[]]
full-title:: "Software Testing"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 1. Software Testing Background
		- -
			- The goal of a software tester is to find bugs. #flashcard
			  id:: 2b953420-622d-46ac-95af-b39083650b8a
		- -
		- -
			- How important it's to think how to break! #flashcard
			  id:: 4b7a4e6f-e0d2-4c01-936c-bedf090756da
				- If you're only testing things that should work and setting up your tests so they'll pass, you will miss the things that don't work. You will miss the bugs.
		- -
		- -
			- The goal of a software tester is to find bugs and find them as early as possible. #flashcard
			  id:: 4005c105-02a8-445e-ad34-e99fb5a23098
		- -
		- -
			- What is the goal of a tester? #flashcard
			  id:: ca199f4e-bf12-493f-8a4a-e388e86a21a1
				- The goal of a software tester is to find bugs, find them as early as possible, and make sure they get fixed.
		- -
		- -
			- At first glance, it may appear that a software tester's job would be easier than a programmer's. Breaking code and finding bugs must surely be easier than writing the code in the first place. Surprisingly, it's not. #flashcard
			  id:: c34e8bc1-9123-459f-9a3e-2fa88adea7bb
		- -
	- 2. The Software Development Process
		- -
			- What is a software deliverable? #flashcard
			  id:: b2ee49c7-523f-4e47-9184-d08a7ff84e26
				- The term used in the software industry to describe a software product component that's created and passed on to someone else is deliverable. The easiest way to explain what all these deliverables are is to organize them into major categories
		- -
		- -
			- Testers' deliverables #flashcard
			  id:: 61048ca4-ede8-4e11-9840-c57a9183a7de
				- For the same reasons that programmers must plan and document their work, software testers must as well. It's not unheard of for a software test team to create more deliverables than the programmers.
		- -
		- -
			- Waterfall process and Testing... #flashcard
			  id:: ee0983e1-4bee-47fc-8459-1acc56cc183a
				- From a testing perspective, the waterfall model offers one huge advantage over the other models presented so far. Everything is carefully and thoroughly specified. By the time the software is delivered to the test group, every detail has been decided on, written down, and turned into software. From that, the test group can create an accurate plan and schedule. They know exactly what they're testing, and there's no question about whether something is a feature or a bug.But, with this advantage, comes a large disadvantage. Because testing occurs only at the end, a fundamental problem could creep in early on and not be detected until days before the scheduled product release. Remember from Chapter 1, “Software Testing Background,” how the cost of bugs increases over time? What's needed is a model that folds the testing tasks in earlier to find problems before they become too costly.
		- -
	- 3. The Realities of Software Testing
		- -
			- One key concept that software testers need to learn is how to reduce the huge domain of possible tests into a manageable set, and how to make wise risk-based decisions on what's important to test and what's not. #flashcard
			  id:: e1acf2c5-90e7-4449-97b2-f795a1d62058
		- -
		- -
			- How can you overcome the 'pesticide paradox'? #flashcard
			  id:: 8e56cda8-1472-4cde-993a-48de8c93f665
				- To overcome the pesticide paradox, software testers must continually write new and different tests to exercise different parts of the program and find more bugs.
		- -
		- -
			- Tester's tip #flashcard
			  id:: 41c5bc7c-71d1-409f-9e04-776ab22c44f7
				- Don't just report bad news. If you find a piece of code surprisingly bug free, tell the world. Pop into a programmer's cubicle occasionally just to chat. If all you ever do is report bad news, people will see you coming and will run and hide.
		- -
		- -
			- What are Verification and Validation? #flashcard
			  id:: ea554f66-7052-4acd-aa63-15eb548cce4b
				- Verification is the process confirming that something—software—meets its specification. Validation is the process confirming that it meets the user's requirements.
		- -
	- 4. Examining the Specification
		- -
			- Note about the white-box tests #flashcard
			  id:: 7723e3e3-7eb2-433c-b011-48761f0f2679
				- There is a risk to white-box testing. It's very easy to become biased and fail to objectively test the software because you might tailor the tests to match the code's operation.
		- -
		- -
			- Professional tip #flashcard
			  id:: 82b48d47-1dc9-4b94-972f-78de003c8265
				- Tell your project team, “This is what I plan to test and submit bugs against.” You'll be amazed at how many details they'll immediately fill in.
		- -
		- -
			- What means quality, meanly? #flashcard
			  id:: b2d33868-b15d-46b5-a2b1-5afde0d565ac
				- It's important to understand the customer's expectations. Remember that the definition of quality means “meeting the customer's needs.” As a tester, you must understand those needs to test that the software meets them.
		- -
		- -
			- Tip about long specs. #flashcard
			  id:: cdc16a35-7b0c-400f-b326-a6e9d5a90803
				- If you review a portion of the spec and don't understand it, don't assume that it's correct and go on. Eventually, you'll have to use this specification to design your software tests, so you'll eventually have to understand it.
		- -
	- 5. Testing the Software with Blinders On
		- -
			- Tip about being effective at testing #flashcard
			  id:: d31b8ca6-e0f5-4bd1-831a-aeaa98dd01d0
				- Selecting test cases is the single most important task that software testers do. Improper selection can result in testing too much, testing too little, or testing the wrong things. Intelligently weighing the risks and reducing the infinite possibilities to a manageable effective set is where the magic is.
		- -
		- -
			- Tip about 'test-to-pass' and 'test-to-fail' #flashcard
			  id:: f1dd5ab3-3d44-4fc5-88c8-b7fbbe21dc30
				- When designing and running your test cases, always run the test-to-pass cases first. It's important to see if the software fundamentally works before you throw the kitchen sink at it. You might be surprised how many bugs you find just using the software normally.
		- -
		- -
			- Test input ideas #flashcard
			  id:: 2772b422-e1df-4021-9ab7-a0f9aee5136d
				- So, with invalid, wrong, incorrect, and garbage data testing, have some fun. If the software wants numbers, give it letters. If it accepts only positive numbers, enter negative numbers. If it's date sensitive, see if it'll work correctly on the year 3000. Pretend to have “fat fingers” and press multiple keys at a time.
		- -
		- -
			- What is stress testing? #flashcard
			  id:: 876d00a5-fc9b-4ea3-b576-09a0c3a167f4
				- Stress testing is running the software under less-than-ideal conditions—low memory, low disk space, slow CPUs, slow modems, and so on.
		- -
	- 17. Planning Your Test Effort
		- -
			- ¿Para qué hago el test plan si soy yo solo y el proyecto es corto y estamos en la era agile?
			  id:: 47930521-3ba9-4941-8036-7a2b248ef0d7
			  Pues para pensar cómo voy a testear mi código. El documento que está en el GitHub es solo el resultado como deliverable del proyecto de pensarlo #flashcard
				- The test plan is a by-product of the detailed planning process that's undertaken to create it. It's the planning process that matters, not the resulting document.
		- -