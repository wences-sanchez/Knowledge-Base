title:: Readwise/Effective Software Testing: A developer's guide (highlights)
deck:: [[O'Reilly-Learning::Effective Software Testing: A developer's guide]]
author:: [[Maurício Aniche]]
full-title:: "Effective Software Testing: A developer's guide"
category:: #books

tags:: o'reilly-learning qa

- Highlights first synced by [[Readwise]] [[Sunday, 08-01-2023]]
	- -
		- About the different types of tests #flashcard
		  id:: a417f339-90be-43b7-8d5f-dc6167370291
			- ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/IFC.png-IFC.png)
			  
			  The different techniques a developer should use to effectively and systematically test a software system
		- ([View Highlight](https://read.readwise.io/read/01gp0wjxhxhatyehsz61a76466))
	- -
	- -
		- About software testing in general #flashcard
		  id:: 4e6baf5a-ec80-4223-9203-d7bbd11fea0f
			- Put simply, testing is nothing but executing a piece of software to see if it behaves as expected. But testing is also hard. Its difficulty surfaces when thinking about the full set of test cases to be designed and executed. Out of the infinitely many possible test cases, which one should you write? Did you do enough testing to move the system to production? What extra tests do you need? Why these tests? And, if you need to change the system, how should you set up the test suite so that it supports rather than impedes future change?
		- ([View Highlight](https://read.readwise.io/read/01gp0wz1fkmcc13hr9kexyh53v))
	- -
	- -
		- Effective and Systematic testing #flashcard
		  id:: 39a100cf-cfad-4d96-9573-cfffe97862a6
			- I have been using two words to describe how I expect a developer to test: *effectively* and *systematically*. Being *effective* means we focus on writing the right tests. Software testing is all about trade-offs. Testers want to maximize the number of bugs they find while minimizing the effort required to find the bugs. How do we achieve this? By knowing what to test.
			  
			  All the techniques I present in this book have a clear beginning (what to test) and a clear end (when to stop). Of course, I do not mean your systems will be bug-free if you follow these techniques. As a community, we still do not know how to build bug-free systems. But I can confidently say that the number of bugs will be reduced, hopefully to tolerable levels.
			  
			  Being *systematic* means that for a given piece of code, any developer should come up with the same test suite. Testing often happens in an ad hoc manner. Developers engineer the test cases that come to mind. It is common to see two developers developing different test suites for the same program. We should be able to systematize our processes to reduce the dependency on the developer who is doing the job.
		- ([View Highlight](https://read.readwise.io/read/01gp12jm3bewp0y7tfahs1rczf))
	- -
	- -
		- Systematic testing is a way of structure your tests just in an organised way for being more efficient in your work of software testing.
		  id:: 5ce802c8-f5b6-471a-a113-9b11359ec46c
		  If you didn’t apply systematic testing, you would probably miss some important cases of failure. #flashcard
			- 1.1 In your own words, explain what systematic testing is and how it is different from non-systematic testing.
		- ([View Highlight](https://read.readwise.io/read/01gp39acrd1h8nmfx9zp0nssqt))
	- -
	- -
		- Validation #flashcard
		  id:: 4a26e8d6-9d4a-4700-8e89-0c23df71f984
			- 1.2 Kelly, a very experienced software tester, visits Books!, a social network focused on matching people based on the books they read. Users do not report bugs often, as the Books! developers have strong testing practices in place. However, users say that the software is not delivering what it promises. What testing principle applies here?
		- ([View Highlight](https://read.readwise.io/read/01gp39psbaj5vvsefzdm00zdn0))
	- -
	- -
		- B) #flashcard
		  id:: 07b25d00-3bd9-4b96-b270-69e7efb5dff4
			- 1.3 Suzanne, a junior software tester, has just joined a very large online payment company in the Netherlands. As her first task, Suzanne analyzes the past two years’ worth of bug reports. She observes that more than 50% of the bugs happen in the international payments module. Suzanne promises her manager that she will design test cases that completely cover the international payments module and thus find all the bugs.
			  
			  Which of the following testing principles may explain why this is not possible?
			  
			  A) Pesticide paradox
			  
			  B) Exhaustive testing
			  
			  C) Test early
			  
			  D) Defect clustering
		- ([View Highlight](https://read.readwise.io/read/01gp39rn3jw8wr72sgqy4cn663))
	- -
	- -
		- B) #flashcard
		  id:: 15a207e1-69b0-40a4-b085-ab90123a2b21
			- 1.4 John strongly believes in unit testing. In fact, this is the only type of testing he does for any project he’s part of. Which of the following testing principles will *not* help convince John that he should move away from his “only unit testing” approach?
			  
			  A) Pesticide paradox
			  
			  B) Tests are context-dependent
			  
			  C) Absence-of-errors fallacy
			  
			  D) Test early
		- ([View Highlight](https://read.readwise.io/read/01gp39sf8s0r8fwvespa3xvpzr))
	- -
	- -
		- A) #flashcard
		  id:: 4399f537-ff4d-475f-82d5-70142371ec57
			- 1.5 Sally just started some consultancy for a company that develops a mobile app to help people keep up with their daily exercises. The development team members are fans of automated software testing and, more specifically, unit tests. They have high unit test code coverage (>95% branch coverage), but users still report a significant number of bugs.
			  
			  Sally, who is well versed in software testing, explains a testing principle to the team. Which of the following principles did she talk about?
			  
			  A) Pesticide paradox
			  
			  B) Exhaustive testing
			  
			  C) Test early
			  
			  D) Defect clustering
		- ([View Highlight](https://read.readwise.io/read/01gp39zpr0nnjnqqsc22s65qbn))
	- -
	- -
		- D) #flashcard
		  id:: dd521b4f-f3f1-4039-bc8b-56aef112cc97
			- 1.6 Consider this requirement: “A web shop runs a batch job, once a day, to deliver all orders that have been paid. It also sets the delivery date according to whether the order is from an international customer. Orders are retrieved from an external database. Orders that have been paid are then sent to an external web service.”
			  
			  As a tester, you have to decide which test level (unit, integration, or system) to apply. Which of the following statements is true?
			  
			  A) Integration tests, although more complicated (in terms of automation) than unit tests, would provide more help in finding bugs in the communication with the web service and/or the communication with the database.
			  
			  B) Given that unit tests could be easily written (by using mocks) and would cover as much as integration tests would, unit tests are the best option for any situation.
			  
			  C) The most effective way to find bugs in this code is through system tests. In this case, the tester should run the entire system and exercise the batch process. Because this code can easily be mocked, system tests would also be cheap.
			  
			  D) While all the test levels can be used for this problem, testers are more likely to find more bugs if they choose one level and explore all the possibilities and corner cases there.
		- ([View Highlight](https://read.readwise.io/read/01gp3a413ntyytpe86y03an8b9))
	- -
	- -
		- C) #flashcard
		  id:: ff90f7e8-bc93-44c0-88e3-4c546ed3db7a
			- 1.7 Delft University of Technology (TU Delft) has built in-house software to handle employee payroll. The application uses Java web technologies and stores data in a Postgres database. The application frequently retrieves, modifies, and inserts large amounts of data. All this communication is done by Java classes that send (complex) SQL queries to the database.
			  
			  As testers, we know that a bug can be anywhere, including in the SQL queries. We also know that there are many ways to exercise our system. Which one of the following is *not* a good option to detect bugs in SQL queries?
			  
			  A) Unit testing
			  
			  B) Integration testing
			  
			  C) System testing
			  
			  D) Stress testing
		- ([View Highlight](https://read.readwise.io/read/01gp3af02h36kbxnfgnxkfp0ep))
	- -
	- -
		- 1.8 Choosing the level of a test involves a trade-off, because each test level has advantages and disadvantages. Which one of the following is the main advantage of a test at the system level?
		  id:: 69ed87a2-091c-4082-95be-3a574c6781fa
		  
		  A) The interaction with the system is much closer to reality.
		  
		  B) In a continuous integration environment, system tests provide real feedback to developers.
		  
		  C) Because system tests are never flaky, they provide developers with more stable feedback.
		  
		  D) A system test is written by product owners, making it closer to reality. #flashcard
			- A) The interaction with the system is much closer to reality.
		- ([View Highlight](https://read.readwise.io/read/01gp3ah5v43fjcqw7xrsbdmn25))
	- -
	- -
		- 1.9 What is the main reason the number of recommended system tests in the testing pyramid is smaller than the number of unit tests?
		  id:: d4e60f17-c930-462c-ba61-ba7dbddf1f3b
		  
		  A) Unit tests are as good as system tests.
		  
		  B) System tests tend to be slow and are difficult to make deterministic.
		  
		  C) There are no good tools for system tests.
		  
		  D) System tests do not provide developers with enough quality feedback. #flashcard
			- B) System tests tend to be slow and are difficult to make deterministic.
		- ([View Highlight](https://read.readwise.io/read/01gp3ajfjz1yjawzhdv681w58a))
	- -
	- 2 Specification-based testing
		- -
			- The exhaustive tests are written after the code. Furthermore, when a developer codes, he codes requirement by requirement, and pushes his code like that, and the pipeline makes the code go directly to production, because the tests all pass. #flashcard
			  id:: b813cb78-c54b-4116-8e03-3f318b8e033e
				- The developer writes the implementation code, guided by test-driven development (TDD) cycles, and always ensures that the code is testable. With all the classes ready, the developer switches to “testing mode.” It is time to systematically look for bugs. This is where specification testing fits in: it is the first testing technique I recommend using once you’re in testing mode.
			- ([View Highlight](https://read.readwise.io/read/01gp3ayem2sd8jnaecabqvctrs))
		- -
		- 2.1 The requirements say it all
			- -
				- 2.1.1 Step 1: Understanding the requirements, inputs, and outputs #flashcard
				  id:: d3a70797-7af6-4372-b6c9-475ee1820c38
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3cjkspekbenncvgyfkjgb6))
			- -
			- -
				- Regardless of how your requirements are written (or even if they are only in your mind), they include three parts. First is what the program/method must do: its business rules. Second, the program receives data as inputs. Inputs are a fundamental part of our reasoning, as it is through them that we can test the different cases. Third, reasoning about the output will help us better understand what the program does and how the inputs are converted to the expected output. #flashcard
				  id:: 12b034dd-31a9-49dc-9f5c-2d34bd74022b
				- ([View Highlight](https://read.readwise.io/read/01gp3ceqk03gfaznd22y75xtej))
			- -
			- -
				- 2.1.2 Step 2: Explore what the program does for various inputs #flashcard
				  id:: 5929818b-9adf-46e7-be27-0e18f62d9603
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3ck13jf4jvs06k0prb17sw))
			- -
			- -
				- I stop this exploration phase when I have a clear mental model of how the program should work. Note that I do not expect you to perform the same exploration I did—it is personal and guided by my hypothesis about the program. Also note that I did not explore any corner cases; that comes later. At this moment, I am only interested in better understanding the program. #flashcard
				  id:: a698a8e7-4319-49a4-a10b-8f7c6f8444f0
				- ([View Highlight](https://read.readwise.io/read/01gp3d8e6wqe2z5kj5t70nne92))
			- -
			- -
				- 2.1.3 Step 3: Explore possible inputs and outputs, and identify partitions #flashcard
				  id:: 6ae30c06-c5c1-4308-86a4-0aa7d35d8e88
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3dnabckh0daymp2xa0n4sp))
			- -
			- -
				- In the case of our example, for testing purposes, the input “abcd” with `open` tag “a” and `close` tag “d”, which makes the program return “bc”, is the same as the input “xyzw” with `open` tag “x” and `close` tag “w”. You change the letters, but you expect the program to do the same thing for both inputs. Given your resource constraints, you will test just one of these inputs (it does not matter which), and you will trust that this single case represents that entire class of inputs. In testing terminology, we say that these two inputs are *equivalent*. #flashcard
				  id:: e501c6fb-d12d-4563-9f80-4454d42ab44c
				- ([View Highlight](https://read.readwise.io/read/01gp3dqbsh11ffejjcw134xzq5))
			- -
			- -
				- How to design systematic equivalence sets? #flashcard
				  id:: 03d704a3-205e-41c3-b570-5a99b2d29625
					- A systematic way to do such an exploration is to think of the following:
					  
					  1.  Each input individually: “What are the possible classes of inputs I can provide?”
					    
					  2.  Each input in combination with other inputs: “What combinations can I try between the `open` and `close` tags?”
					    
					  3.  The different classes of output expected from this program: “Does it return arrays? Can it return an empty array? Can it return nulls?”
				- ([View Highlight](https://read.readwise.io/read/01gp3drpk4s50v7g2aw62dypq6))
			- -
			- -
				- 2.1.4 Step 4: Analyze the boundaries #flashcard
				  id:: c5f50dc7-8f83-432e-823f-6b599bf28bb9
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3e25qvymje8fhc1xzkn478))
			- -
			- -
				- 2.1.5 Step 5: Devise test cases #flashcard
				  id:: b866beb4-bf57-4063-885b-37b21b6226fb
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3efgs9nqcnydcrxkn18skf))
			- -
			- -
				- We end up with 21 tests. Note that deriving them did not require much creativity: the process we followed was systematic. This is the idea! #flashcard
				  id:: e6c03532-c8ac-43b7-aa98-997a31f63785
				- ([View Highlight](https://read.readwise.io/read/01gp3fdqgxjtabpttaswmscx12))
			- -
			- -
				- 2.1.6 Step 6: Automate the test cases #flashcard
				  id:: 97b3c564-8fb5-4111-acd8-fca79a343ae0
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3fe0k8ykqhs1jy5x261exa))
			- -
			- -
				- 2.1.7 Step 7: Augment the test suite with creativity and experience #flashcard
				  id:: 9a915f5c-d1f7-4fbe-8960-ffcd9279b32a
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gp3fpaqszmqcs3aeprybrzqs))
			- -
			- 2.2 Specification-based testing in a nutshell
				- -
					- Specification-based testing in a nutshell #flashcard
					  id:: 87dd614f-ee87-43ca-97d6-ad99c5aa4331
						- ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/x02-04.png-02-04.png)
						  
						  Figure 2.4 The seven steps I propose to derive test cases based on specifications. The solid arrows indicate the standard path to follow. The dashed arrows indicate that, as always, the process should be iterative, so in practice you’ll go back and forth until you are confident about the test suite you’ve created.
						  
						  The steps are as follows:
						  
						  1.  *Understand the requirement, inputs, and outputs.* We need an overall idea of what we are about to test. Read the requirements carefully. What should the program do? What should it not do? Does it handle specific corner cases? Identify the input and output variables in play, their types (integers, strings, and so on), and their input domain (for example, is the variable a number that must be between 5 and 10?). Some of these characteristics can be found in the program’s specification; others may not be stated explicitly. Try to understand the nitty-gritty details of the requirements.
						    
						  2.  *Explore the program.* If you did not write the program yourself, a very good way to determine what it does (besides reading the documentation) is to play with it. Call the program under test with different inputs and see what it produces as output. Continue until you are sure your mental model matches what the program does. This exploration does not have to be (and should not be) systematic. Rather, focus on increasing your understanding. Remember that you are still not testing the program.
						    
						  3.  *Judiciously explore the possible inputs and outputs, and identify the partitions.* Identifying the correct partitions is the hardest part of testing. If you miss one, you may let a bug slip through. I propose three steps to identify the partitions:
						    
						    a) Look at each input variable individually. Explore its type (is it an integer? is it a string?) and the range of values it can receive (can it be null? is it a number ranging from 0 to 100? does it allow negative numbers?).
						    
						    b) Look at how each variable may interact with another. Variables often have dependencies or put constraints on each other, and those should be tested.
						    
						    c) Explore the possible types of outputs, and make sure you are testing them all. While exploring the inputs and outputs, pay attention to any implicit (business) rules, logic, or expected behavior.
						    
						  4.  *Identify the boundaries.* Bugs love boundaries, so be extra thorough here. Analyze the boundaries of all the partitions you devised in the previous step. Identify the relevant ones, and add them to the list.
						    
						  5.  *Devise test cases based on the partitions and boundaries.* The basic idea is to combine all the partitions in the different categories to test all possible combinations of inputs. However, combining them all may be too expensive, so part of the task is to reduce the number of combinations. The common strategy is to test exceptional behavior only once and not combine it with the other partitions.
						    
						  6.  *Automate the test cases.* A test is only a test when it is automated. Therefore, the goal is to write (JUnit) automated tests for all the test cases you just devised. This means identifying concrete input values for them and having a clear expectation of what the program should do (the output). Remember that test code is code, so reduce duplication and ensure that the code is easy to read and that the different test cases are easily identifiable in case one fails.
						    
						  7.  *Augment the test suite with creativity and experience.* Perform some final checks. Revisit all the tests you created, using your experience and creativity. Did you miss something? Does your gut feeling tell you that the program may fail in a specific case? If so, add a new test case.
					- ([View Highlight](https://read.readwise.io/read/01gp3g6h6mb0nrkhfse7kkndmd))
				- -
			- 2.4 Specification-based testing in the real world
				- -
					- The process should be iterative, not sequential
					  id:: f9741607-26a7-489a-b68d-413aa634c732
					  
					  Describing iterative processes in writing is challenging. My explanation may have given you the impression that this process is fully sequential and that you move to the next step only when you have completed the previous one. However, the entire process is meant to be iterative. In practice, I go back and forth between the different steps. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gp3j35vdvx85e0w8r9r9ytcq))
				- -
				- -
					- Approach for specification testing #flashcard
					  id:: 486749cf-6a1b-4aa0-9559-004a4aa6b809
						- I propose a seven-step approach for specification testing: (1) understand the requirements, (2) explore the program if you do not know much about it, (3) judiciously analyze the properties of the inputs and outputs and identify the partitions, (4) analyze the boundaries, (5) devise concrete test cases, (6) implement the concrete test cases as automated (JUnit) tests, and (7) use creativity and experience to augment the test suite.
					- ([View Highlight](https://read.readwise.io/read/01gp65rwyp9v0mag79a47ghvfw))
				- -
- New highlights added [[Monday, 23-01-2023]] at 9:23 AM
	- -
		- Structural testing in a nutshell
		  id:: f711b294-1cd0-46c6-9a16-0386ae07e02a
		  
		  Based on what we just did, let me define a simple approach that any developer can follow (see figure 3.4):
		  
		  1.  Perform *specification-based testing*, as discussed in the previous chapter.
		    
		  2.  *Read the implementation*, and understand the main coding decisions made by the developer.
		    
		  3.  Run the devised test suite with a *code coverage tool*.
		    
		  4.  For each piece of code that is *not* covered:
		    
		    a) *Understand* why that piece of code was not tested. Why didn’t you see this test case during specification-based testing? Consult with the requirements engineer if you need more clarity.
		    
		    b) *Decide* whether the piece of code deserves a test. Testing or not testing that piece of code is now a conscious decision on your part.
		    
		    c) If a test is needed, *implement an automated test case* that covers the missing piece.
		    
		  5.  Go back to the source code and *look for other interesting tests you can devise* based on the code. For each identified piece of the code, perform the substeps of step 4.
		    
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/x03-04.png-03-04.png) #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gq4qeh3csmj914f7hewrke0m))
	- -
	- -
		- What is line coverage? #flashcard
			- A developer who aims to achieve line coverage wants at least one test case that covers the line under test. It does not matter if that line contains a complex `if` statement full of conditions. If a test touches that line in any way, the developer can count the line as covered.
		- ([View Highlight](https://read.readwise.io/read/01gq4qh54fzf0xg68938td0r5m))
	- -
	- -
		- What is branch coverage? #flashcard
		  id:: 77bf4039-0cdb-4005-8b18-041aca62e764
			- Branch coverage takes into consideration the fact that branching instructions (`if`s, `for`s, `while`s, and so on) make the program behave in different ways, depending how the instruction is evaluated. For a simple `if(a` `&&` `b)` statement, having a test case T1 that makes the `if` statement `true` and another test case T2 that makes the statement `false` is enough to consider the branch covered.
			  
			  Figure 3.5 illustrates a control-flow graph (CFG) of the `CountWords` program. You can see that for each `if` instruction, two edges come out of the node: one representing where the flow goes if the statement is evaluated to `true` and another representing where the program goes if the statement is evaluated to `false`. Covering all the edges in the graph means achieving 100% branch coverage.
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/x03-05.png-03-05.png)
		- ([View Highlight](https://read.readwise.io/read/01gq4qw4ensqgrtpst730102te))
	- -
	- -
		- What is condition + branch coverage? #flashcard
		  id:: 4900345f-e70c-4403-92f6-bad8e43773df
			- Condition + branch coverage considers not only possible branches but also each condition of each branch statement. For example, the first `if` statement in the `CountWords` program contains three conditions: `!Character.isLetter(str.charAt(i))`, `last` `==` `'s'`, and `last` `==` `'r'`. Therefore, a developer aiming for condition + branch coverage should create a test suite that exercises each of those individual conditions being evaluated to `true` and `false` at least once *and* the entire branch statement being `true` and `false` at least once.
			  
			  Note that blindly looking only at the conditions (and ignoring how they are combined) may result in test suites that do not cover everything. Imagine a simple `if(A` `||` `B)`. A test suite composed of two tests (T1 that makes A `true` and B `false` and T2 that makes A `false` and B `true`) covers the two conditions, as each condition is exercised as `true` and `false`. However, the test suite does not fully cover the branch, as in both tests, the evaluation of the entire `if` statement is always `true`. This is why we use condition + branch coverage, and not only (basic) condition coverage.
			  
			  In the extended CFG in figure 3.6, branch nodes contain only a single condition. The complicated `if` is broken into three nodes.
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/x03-06.png-03-06.png)
			  
			  Figure 3.6 The extended control-flow graph of the `CountWords` program. Each condition is in its own node. Covering all the edges in the graph means achieving 100% condition + branch coverage.
		- ([View Highlight](https://read.readwise.io/read/01gq4r0gkgxj4b13qmxd8dpndd))
	- -
	- -
		- What is path coverage? #flashcard
		  id:: b50f9b9b-8409-418f-9b2f-5f8529c1adc2
			- A developer aiming for path coverage covers *all* the possible paths of execution of the program. While ideally this is the strongest criterion, it is often impossible or too expensive to achieve. In a single program with three conditions, where each condition could be independently evaluated to `true` or `false`, we would have 23 = 8 paths to cover. In a program with 10 conditions, the total number of combinations would be 210 = 1024. In other words, we would need to devise more than a thousand tests!
			  
			  Path coverage also gets more complicated for programs with loops. In a program with an unbounded loop, the loop might iterate hundreds of times. A rigorous tester aiming for path coverage would have to try the program with the loop executing one time, two times, three times, and so on.
		- ([View Highlight](https://read.readwise.io/read/01gq4r4346tvggsa6r7mr6s1bj))
	- -
	- -
		- The MC/DC criterion looks at combinations of conditions, as path coverage does. However, instead of testing *all* possible combinations, we identify the *important* combinations that need to be tested. MC/DC exercises each of these conditions so that it can, independently of the other conditions, affect the outcome of the entire decision. Every possible condition of each parameter must influence the outcome at least once. (For details, read Kelly Hayhurst’s 2001 paper.) #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gq4rbejdpg9mzw7rzn40zb7g))
	- -
	- -
		- Note I have a video on YouTube that explains MC/DC visually: [www.youtube.com/watch?v=HzmnCVaICQ4](http://www.youtube.com/watch?v=HzmnCVaICQ4). #flashcard
		  id:: f2923b54-1953-4b2f-9767-d563ed819f0a
		- ([View Highlight](https://read.readwise.io/read/01gq4rq40etx0xs2988q2d32cr))
	- -
	- -
		- How do you test a loop? #flashcard
		  id:: 5e99169f-6fef-4666-8535-f6472ceba3e3
			- Given that exhaustive testing is impossible, testers often rely on the *loop boundary adequacy criterion* to decide when to stop testing a loop. A test suite satisfies this criterion if and only if for every loop
			  
			  •   There is a test case that exercises the loop zero times.
			    
			  •   There is a test case that exercises the loop once.
			    
			  •   There is a test case that exercises the loop multiple times.
			    
			  
			  Pragmatically speaking, my experience shows that the main challenge comes when devising the test case for the loop being executed multiple times. Should the test case force the loop to iterate 2, 5, or 10 times? This decision requires a good understanding of the program and its requirement. With optimal understanding of the specs, you should be able to devise good tests for the loop. Do not be afraid to create two or more tests for the “multiple times” case. Do whatever you need to do to ensure that the loop works as expected.
		- ([View Highlight](https://read.readwise.io/read/01gq4rv8twd8c37sv26bpg888z))
	- -
	- -
		- ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/x03-07.png-03-07.png)
		  id:: 0b2853a0-d605-45be-839a-0fa2c6c2270d
		  
		  Figure 3.7 The different coverage criteria and their subsumption relations
		  
		  Branch coverage subsumes line coverage, which means 100% branch coverage always implies 100% line coverage. However, 100% line coverage does not imply 100% branch coverage. Moreover, 100% condition + branch coverage always implies 100% branch coverage and 100% line coverage. Following this train of thought, we see that path coverage subsumes all other criteria. This is logical as path coverage covers all possible paths of the program. Next, we see that MC/DC is stronger than condition + branch coverage, as MC/DC ensures the independence of each condition. And condition + branch coverage subsumes both branch and condition coverage independently. Finally, all other criteria, except basic condition coverage, subsume line coverage, which is the weakest criterion in the figure #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gq4rz5235mz671rea0atr2bs))
	- -
	- -
		- My rule of thumb is branch coverage: I always try to at least reach all the branches of the program. Whenever I see a more complicated expression, I evaluate the need for condition + branch coverage. If I see an even more complex expression, I consider MC/DC. #flashcard
		  id:: dfdec787-6180-47df-9d23-dcf75d800af5
		- ([View Highlight](https://read.readwise.io/read/01gq4sqsyfqkkx5s71ymcjbckz))
	- -
	- -
		- Note Arie van Deursen offers a clear answer on Stack Overflow about the differences between design-by-contract and validation, and I strongly recommend that you check it out: [https://stackoverflow.com/a/5452329](https://stackoverflow.com/a/5452329). #flashcard
		  id:: eed084e9-de6a-4a85-8bcb-4e98d30bdf9a
		- ([View Highlight](https://read.readwise.io/read/01gq50d8ccbda1vbm6337g10jr))
	- -
	- -
		- About asserts vs exceptions #flashcard
		  id:: 62a25856-ac3c-4106-895e-e367a0049508
			- Here is my rule of thumb:
			  
			  •   If I am modeling the contracts of a library or utility class, I favor exceptions, following the wisdom of the most popular libraries.
			    
			  •   If I am modeling business classes and their interactions and I know that the data was cleaned up in previous layers (say, in the controller of a Model-View-Controller [MVC] architecture), I favor assertions. The data was already validated, and I am sure they start their work with valid data. I do not expect pre-conditions or post-conditions to be violated, so I prefer to use the `assert` instruction. It will throw an `AssertionError`, which will halt execution. I also ensure that my final user does not see an exception stack trace but instead is shown a more elegant error page.
			    
			  •   If I am modeling business classes but I am not sure whether the data was already cleaned up, I go for exceptions.
		- ([View Highlight](https://read.readwise.io/read/01gq50m7fadx10drced8pmtge1))
	- -
	- -
		- About design-by-contract VS testing #flashcard
			- I also want to highlight that design-by-contract does not replace the need for testing. Why? Because, to the best of my knowledge and experience, you cannot express all the expected behavior of a piece of code solely with pre-conditions, post-conditions, and invariants. In practice, I suggest that you design contracts to ensure that classes can communicate with each other without fear, and test to ensure that the behavior of the class is correct.
		- ([View Highlight](https://read.readwise.io/read/01gq50y0qhg91vm684pbjxc6h7))
	- -
	- -
		- let me again discuss the difference between validation and pre-conditions. Validation is what you do to ensure that the data is valid. Pre-conditions explicitly state under what conditions a method can be invoked. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gq511p4b14k376ra6qy0qjjw))
	- -
	- 5 Property-based testing
		- -
			- About property-based testing #flashcard
			  id:: 36d447b8-73f2-47e8-920a-0c233185ef30
				- Pay attention to these two points:
				  
				  1.  Ask yourself, “Am I exercising the property as closely as possible to the real world?” If you come up with input data that will be wildly different from what you expect in the real world, it may not be a good test.
				    
				  2.  Do all the partitions have the same likelihood of being exercised by your test? In the example, the element to be found is sometimes before and sometimes after the start index. If you write a test in which, say, 95% of the inputs have the element before the start index, you may be biasing your test too much. You want all the partitions to have the same likelihood of being exercised.
				    
				    In the example code, given that both `indexToAddElement` and `startIndex` are random numbers between 0 and 99, we expect about a 50-50 split between the partitions. When you are unsure about the distribution, add some debugging instructions and see what inputs or partitions your test generates or exercises.
			- ([View Highlight](https://read.readwise.io/read/01gq5780d2egrte9zt8a9v6yse))
		- -
		- -
			- 😅 #flashcard
				- A developer who did not read the chapters on specification-based testing and structural testing would come up with at least three tests: one to ensure that `add()` adds the product to the cart, another to ensure that the method behaves correctly when the same product is added twice, and one to ensure that `remove()` indeed removes the product from the basket. Then they would probably add a few tests for the exceptional cases (which in this class are clearly specified in the contracts).
			- tags:: [[favorite]]
			- ([View Highlight](https://read.readwise.io/read/01gq57bxtzj7e0ahq89p7s7nex))
		- -
		- -
			- Property-based testing seems much fancier than example-based testing. It also explores the input domain much better. Should we only use property-based testing from now on?
			  id:: 04841894-9aa2-4b51-b564-d89485ab443b
			  
			  In practice, I mix example-based testing and property-based testing. In the testing workflow I propose, I use example-based testing when doing specification-based and structural testing. Example-based tests are naturally simpler than property-based tests, and they require less creativity to automate. I like that: their simplicity allows me to focus on understanding the requirements and engineer better test cases. When I am done with both testing techniques and have a much better grasp of the program under test, I evaluate which test cases would be better as property-based tests. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gq584p3k8d4m5xcfvtqzj0sw))
		- -
		- 6 Test doubles and mocks
			- -
				- Note While some of the schools of thought in testing prefer to see mocks as a design technique, in this book, I talk about stubs and mocks mostly from a testing perspective, as our goal is to use mocks to ease our lives when looking for bugs. If you are interested in mocking as a design technique, I strongly recommend Freeman and Pryce’s 2009 book, which is the canonical reference for the subject. #flashcard
				  id:: 17bf02a1-27c5-4386-9c23-187e3ba944ef
				- ([View Highlight](https://read.readwise.io/read/01gq58qxc0w6m7qqefwnk23sb0))
			- -
			- -
				- Dummy objects are passed to the class under test but never used. This is common in business applications where you need to fill a long list of parameters, but the test exercises only a few of them. Think of a unit test for a `Customer` class. Maybe this class depends on several other classes like `Address`, `Email`, and so on. Maybe a specific test case A wants to exercise a behavior, and this behavior does not care which `Address` this `Customer` has. In this case, a tester can set up a dummy `Address` object and pass it to the `Customer` class. #flashcard
				  id:: 261698fd-ba3f-488b-be54-b042842d6fdf
				- ([View Highlight](https://read.readwise.io/read/01gq58tzw2k102rxfrk6mjmdr4))
			- -
			- -
				- Fake objects have real working implementations of the class they simulate. However, they usually do the same task in a much simpler way. Imagine a fake database class that uses an array list instead of a real database. This fake object is simpler to control than the real database. A common example in real life is to use a simpler database during testing.
				  id:: 02087a0e-2cb5-4fbd-80d5-087580211520
				  
				  In the Java world, developers like to use HSQLDB (HyperSQL database, [http://hsqldb.org](http://hsqldb.org)), an in-memory database that is much faster and easier to set up in the test code than a real database. We will talk more about in-memory databases when we discuss integration testing in chapter 9. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq58vfa1xm2hzpadd0p2q5x5))
			- -
			- -
				- Stubs provide hard-coded answers to the calls performed during the test. Unlike fake objects, stubs do not have a working implementation. If the code calls a stubbed method `getAllInvoices`, the stub will return a hard-coded list of invoices.
				  id:: e912696d-3e56-4803-8ad4-e8fd0df50c22
				  
				  Stubs are the most popular type of simulation. In most cases, all you need from a dependency is for it to return a value so the method under test can continue its execution. If we were testing a method that depends on this `getAllInvoices` method, we could stub it to return an empty list, then return a list with one element, then return a list with many elements, and so on. This would enable us to assert how the method under test would work for lists of various lengths being returned from the database. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq590tvfybtfjkn7gtqm6eky))
			- -
			- -
				- Mock objects act like stubs in the sense that you can configure how they reply if a method is called: for example, to return a list of invoices when `getAllInvoices` is called. However, mocks go beyond that. They save all the interactions and allow you to make assertions afterward. For example, maybe we only want the `getAllInvoices` method to be called once. If the method is called twice by the class under test, this is a bug, and the test should fail. At the end of our test, we can write an assertion along the lines of “verify that `getAllInvoices` was called just once.”
				  id:: f7e11c71-07ff-4b85-a457-31c091ca4e77
				  
				  Mocking frameworks let you assert all sorts of interactions, such as “the method was never called with this specific parameter” or “the method was called twice with parameter A and once with parameter B.” Mocks are also popular in industry since they can provide insight into how classes interact. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq5945263bbgxn66zps5xckt))
			- -
			- -
				- As the name suggests, spies spy on a dependency. They wrap themselves around the real object and observe its behavior. Strictly speaking, we are not simulating the object but rather recording all the interactions with the underlying object we are spying on.
				  id:: b92b68db-8d5b-4f57-b7d2-cf724f750130
				  
				  Spies are used in very specific contexts, such as when it is much easier to use the real implementation than a mock but you still want to assert how the method under test interacts with the dependency. Spies are less common in the wild. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq5951680gakrhxm6202nv1z))
			- -
			- -
				- Note This idea of classes not instantiating their dependencies by themselves but instead receiving them is a popular design technique. It allows us to inject mocks and also makes the production code more flexible. This idea is also known as *dependency injection*. If you want to dive into the topic, I suggest *Dependency Injection: Principles, Practices, and Patterns* by Steven van Deursen and Mark Seemann (2019). #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq59wpj2p53m5fq8xx8amcqs))
			- -
			- -
				- To learn more about the differences between mocks and stubs, see the article “Mocks Aren’t Stubs,” by Martin Fowler (2007). #flashcard
				  id:: e778f795-f442-4162-a040-39a036e2bff9
				- ([View Highlight](https://read.readwise.io/read/01gq5apf9q18srp1gz8eatg0tr))
			- -
			- -
				- I have been talking a lot about the advantages of mocks. However, as I hinted before, a common (and heated) discussion among practitioners is whether to use mocks. Let’s look at possible disadvantages.
				  id:: 337281bc-e2d3-4dfc-8883-4eb8642a713a
				  
				  Some developers strongly believe that using mocks may lead to test suites that *test the mock, not the code*. That can happen. When you use mocks, you are naturally making your test less realistic. In production, your code will use the concrete implementation of the class you mocked during the test. Something may go wrong in the way the classes communicate in production, for example, and you may miss it because you mocked them.
				  
				  Consider a class `A` that depends on class `B`. Suppose class `B` offers a method `sum()` that always returns positive numbers (that is, the post-condition of `sum()`). When testing class `A`, the developer decides to mock `B`. Everything seems to work. Months later, a developer changes the post-conditions of `B`’s `sum()`: now it also returns negative numbers. In a common development workflow, a developer would apply these changes in `B` and update `B`’s tests to reflect the change. It is easy to forget to check whether `A` handles this new post-condition well. Even worse, `A`’s test suite will still pass! `A` mocks `B`, and the mock does not know that `B` changed. In large-scale software, it can be easy to lose control of your mocks in the sense that mocks may not represent the real contract of the class.
				  
				  For mock objects to work well on a large scale, developers must design careful (and hopefully stable) contracts. If contracts are well designed and stable, you do not need to be afraid of mocks. And although we use the example of a contract break as a disadvantage of mocks, it is part of the coder’s job to find the dependencies of the contract change and check that the new contract is covered, mocks or not.
				  
				  Another disadvantage is that tests that use mocks are naturally more coupled with the code they test than tests that do not use mocks. Think of all the tests we have written without mocks. They call a method, and they assert the output. They do not know anything about the actual implementation of the method. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq5bg86xa80kp4yd8sh6jtqv))
			- -
			- -
				- Pragmatically, developers often mock or stub the following types of dependencies:
				  
				  •   *Dependencies that are too slow* —If the dependency is too slow for any reason, it might be a good idea to simulate it. We do not want slow test suites. Therefore, I mock classes that deal with databases or web services. Note that I still do integration tests to ensure that these classes work properly, but I use mocks for all the other classes that depend on these slow classes.
				    
				  •   *Dependencies that communicate with external infrastructure* —If the dependency talks to (external) infrastructure, it may be too slow or too complex to set up the required infrastructure. So, I apply the same principle: whenever testing a class that depends on a class that handles external infrastructure, I mock the dependency (as we mocked the `IssuedInvoices` class when testing the `InvoiceFilter` class). I then write integration tests for these classes.
				    
				  •   *Cases that are hard to simulate* —If we want to force the dependency to behave in a hard-to-simulate way, mocks or stubs can help. A common example is when we would like the dependency to throw an exception. Forcing an exception might be tricky when using the real dependency but is easy to do with a stub. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq5bx5y8asq5vx5b0gafcear))
			- -
			- -
				- On the other hand, developers tend not to mock or stub the following dependencies:
				  id:: 2ced58f2-b9d8-4d24-baf9-f64985561cfc
				  
				  •   *Entities* —Entities are classes that represent business concepts. They consist primarily of data and methods that manipulate this data. Think of the `Invoice` class in this chapter or the `ShoppingCart` class from previous chapters. In business systems, entities commonly depend on other entities. This means, whenever testing an entity, we need to instantiate other entities.
				    
				    For example, to test a `ShoppingCart`, we may need to instantiate `Product`s and `Item`s. One possibility would be to mock the `Product` class when the focus is to test the `ShoppingCart`. However, this is not something I recommend. Entities are classes that are simple to manipulate. Mocking them may require more work. Therefore, I prefer to never mock them. If my test needs three entities, I instantiate them.
				    
				    I make exceptions for heavy entities. Some entities require dozens of other entities. Think of a complex `Invoice` class that depends on 10 other entities: `Customer`, `Product`, and so on. Mocking this complex `Invoice` class may be easier.
				    
				  •   *Native libraries and utility methods* —It is also not common to mock or stub libraries that come with our programming language and utility methods. For example, why would we mock `ArrayList` or a call to `String.format`? Unless you have a very good reason, avoid mocking them.
				    
				  •   *Things that are simple enough* —Simple classes may not be worth mocking. If you feel a class is too simple to be mocked, it probably is. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq5bwxwhnhnb734v7hwjr1h1))
			- -
			- -
				- You do not have to (and should not) mock everything, even when you decide to go for mocks. Only mock what is necessary. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gq5cjzjdb14p8ybv5y9wnkvd))
			- -
		- 7 Designing for testability
		- 8 Test-driven development
			- -
				- Note You may wonder about corner cases: What about an empty string? or null? Those cases are worth testing. However, when doing TDD, I first focus on the happy path and the business rules; I consider corners and boundaries later.
				  
				  Remember, we are not in testing mode. We are in development mode, coming up with inputs and outputs (or test cases) that will guide us through the implementation. In the development flow I introduced in figure 1.4, TDD is part of “testing to guide development.” When we are finished with the implementation, we can dive into rigorous testing using all the techniques we have discussed. #flashcard
				- tags:: [[favorite]]
				- ([View Highlight](https://read.readwise.io/read/01gq5dfyq5whjkc4x0b5m92yrb))
			- -
			- -
				- 8.3.5 Other schools of TDD #flashcard
				- tags:: [[h4]]
				- ([View Highlight](https://read.readwise.io/read/01gq5fb116pjfzdabvv5d3sr8g))
			- -
			- -
				- About the different schools of TDD #flashcard
					- I suggest that you learn more about both schools. Both have good points, and combining them makes sense. I recommend Mancuso’s 2018 talk, which elaborates on the differences between the schools and how the approaches can be used.
				- ([View Highlight](https://read.readwise.io/read/01gq5fxe10km4rc1ce13834kf6))
			- -
		- 9 Writing larger tests
		- 10 Test code quality
			- -
				- A *fixture* is the set of input values used to exercise the component under test #flashcard
				  id:: 0bd8ba26-022f-4724-aab4-50fcec8bff1d
				- ([View Highlight](https://read.readwise.io/read/01gq5jtf7jh6n26c5k1bqhafty))
			- -