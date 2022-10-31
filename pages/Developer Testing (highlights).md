title:: Developer Testing (highlights)
deck:: [[O'Reilly-Learning::Developer Testing]]
author:: [[]]
full-title:: "Developer Testing"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- About the Author
		- -
			- That’s what I want to become 😃 #flashcard
			  id:: d417ce5f-7283-4ad7-ad65-a178d96995c1
				- Twenty-five years later, Alexander still writes code and remains a developer at heart.
		- -
	- Chapter 1. Developer Testing
		- -
			- What’s the reason why the tester shouldn’t be the same person than the developer? #flashcard
			  id:: 9845db7e-68c2-4424-83a5-ec45a5ef0e8f
				- Some types of testing require specific skills or some distance from the tested software in order to mitigate any bias its creators may be subject to. This is why testing is a separate area of expertise.
		- -
		- -
			- Who should write the unit tests? #flashcard
			  id:: c316409f-6dae-400b-ad21-3567ae6cda57
				- Nevertheless, unit tests are 100 percent developer-owned.
		- -
		- -
			- How would you fix a new bug issue in a maintenance project? #flashcard
			  id:: 6bf4eba7-3a91-4c1a-82e5-2198cdee7e76
				- A well-proven technique for fixing bugs is restraining oneself from rushing ahead to implement a fix, and first writing a test that’ll fail because of the bug’s presence. In the absence of the bug, that test would pass. Once the test is in place, the bug is fixed. If the fix is correct, the test passes.
		- -
		- -
			- performed by developers in a cross-functional team #flashcard
			  id:: 3e1d2ad0-0314-43ce-a085-0b7e20ac372b
		- -
		- -
			- Therefore, this book recurrently returns to the topic of collaboration between team members who are better at writing the code and team members who are better at testing it. #flashcard
			  id:: c8ddc803-8357-4a76-9a81-f92a060a2bc6
		- -
	- Chapter 2. Testing Objectives, Styles, and Roles
		- -
			- By now it should be obvious that developer testing, as described in this book, is testing meant to support. #flashcard
			  id:: c7755a17-5221-4cd3-a370-a8f51e7baf66
		- -
		- -
			- About the Tester role in Agile #flashcard
			  id:: 020fc8f8-e152-4569-831f-c94c0a76b8fd
				- In agile testing, the role of the tester is shifted from reactive to proactive. Instead of writing test cases, waiting for something to test, or executing manual tests, the tester becomes the team’s quality champion and contributes to a successful release in any way she can. For example, by helping the customer or product owner to specify desired functionality, by making sure that testing activities are taken into account during planning and estimation meetings, by educating and assisting the developers in test design and test automation, or by pair programming or pair testing.
		- -
		- -
			- What are the differences between Traditional and Agile mind-sets? #flashcard
			  id:: 4a206f33-6fe7-4829-80fb-cc5754da4226
				- The wording is important here. In traditional testing, tests are supposed to be planned and created in parallel with the development. The difference is that collaboration, joint planning, and common success/completion criteria aren’t emphasized.
		- -
		- -
			- Just talking seriously about QA and what should be your attitude #flashcard
			  id:: cc824a66-e064-4cdf-b3dc-420d355bc0b8
				- You know what? None of these factors really matter. If you’re the only developer, or your team doesn’t have any testers, or you’re being rushed by others, or the system is old and crappy, your quality assurance process is the only one you have, and it will make or break your software.
		- -
	- Chapter 3. The Testing Vocabulary
		- -
			- All developers sometimes make mistakes. These are known as errors in the language of testing. #flashcard
			  id:: 185df20b-3096-496d-8ff3-d6f977bdf5b7
		- -
		- -
			- Errors lead to defects in the software #flashcard
			  id:: aa502e20-7ea8-4441-adf2-ec231f2f6681
		- -
		- -
			- Defects/bugs may lead to software failures. Not all of them do, though. A defect in code that’s never executed won’t cause a failure. #flashcard
			  id:: b75d282a-3cc4-4ab7-9873-58357053c6a6
		- -
		- -
			- What are system tests? #flashcard
			  id:: 2b457781-3939-428b-9a09-85d2969df14d
				- Systems are made up of finished and integrated building blocks. They may be components or other systems. System testing is the activity of verifying that the entire system works. System tests are often executed from a black box perspective
		- -
		- -
			- He suggested defining a component’s behavior as the outcome produced by its functionality under certain preconditions. #flashcard
			  id:: 7bf094bc-206d-482f-ad45-5d025d413580
		- -
		- -
			- FIGURE 3.3 Agile Testing Quadrants as presented in the book More Agile Testing by Lisa Crispin and Janet Gregory (2014). #flashcard
			  id:: 38c84310-3a0c-4646-8154-b443f8c885a6
		- -
		- -
			- What are negative tests? #flashcard
			  id:: 5888be78-1562-44eb-af9f-f6df40d7b610
				- The purpose of negative testing is to verify that the system behaves correctly if supplied with invalid values and that it doesn’t generate any unexpected results. What outcome to expect depends on the test level. At the system level, we generally want the system to “do the right thing”: either reject the faulty input in a user-friendly manner, or recover somehow. At the unit level, throwing an exception may be the right thing to do. For example, if a function exercised with a unit test expects a positive number and throws an IllegalArgumentException or ArgumentOutOfRangeException in a negative test that may be fine. What’s important is that the developer has anticipated the scenario.
		- -
		- -
			- Integration tests verify that components/systems can talk to each other, but sometimes the term is used to describe tests that are somewhere between unit tests and system tests. #flashcard
			  id:: 02e3c215-d4f3-4b28-98ad-d21f315a2893
		- -
	- Chapter 4. Testability from a Developer’s Perspective
		- -
			- However, estimating progress for software that has no tests (because of poor testability) ranges between best guesses and wishful thinking. A developer who believes he is “95 percent finished” with a feature has virtually no way of telling what fraction of seemingly unrelated functionality he has broken along the way and how much time it’ll take to fix these regressions and the remaining “5 percent”. A suite of tests makes this situation more manageable. Again, if the feature is supposedly “95 percent finished” and all tests for the new functionality pass, as well as those that exercise the rest of the system, the estimate is much more credible. Now the uncertainty is reduced to potential surprises in the remaining work, not to random regressions that may pop up anywhere in the system #flashcard
			  id:: 978dbfb1-29e7-4b84-8c71-7a575f04c242
		- -
		- -
			- Changing software that has no tests makes the average developer uncomfortable and afraid (and it should). Fear is easily observed in code. It manifests itself as duplication—the safe way to avoid breaking something that works. #flashcard
			  id:: de1a3b82-9b79-4d81-90ad-278f3ca07cd0
		- -