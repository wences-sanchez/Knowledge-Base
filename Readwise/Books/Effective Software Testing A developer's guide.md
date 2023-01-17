# Effective Software Testing: A developer's guide

deck:: [[Other-Books::Effective Software Testing: A developer's guide]]\
author:: [[Maurício Aniche]]\
full-title:: "Effective Software Testing: A developer's guide"\
category:: #books\
\
tags:: o'reilly-learning qa  

![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/cover-cover.jpeg)

## Highlights
- 
 About the different types of tests #flashcard 
    ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/IFC.png-IFC.png)
     The different techniques a developer should use to effectively and systematically test a software system

    ([View Highlight](https://read.readwise.io/read/01gp0wjxhxhatyehsz61a76466))
-
- 
 About software testing in general #flashcard 
    Put simply, testing is nothing but executing a piece of software to see if it behaves as expected. But testing is also hard. Its difficulty surfaces when thinking about the full set of test cases to be designed and executed. Out of the infinitely many possible test cases, which one should you write? Did you do enough testing to move the system to production? What extra tests do you need? Why these tests? And, if you need to change the system, how should you set up the test suite so that it supports rather than impedes future change?

    ([View Highlight](https://read.readwise.io/read/01gp0wz1fkmcc13hr9kexyh53v))
-
- 
 Effective and Systematic testing #flashcard 
    I have been using two words to describe how I expect a developer to test: *effectively* and *systematically*. Being *effective* means we focus on writing the right tests. Software testing is all about trade-offs. Testers want to maximize the number of bugs they find while minimizing the effort required to find the bugs. How do we achieve this? By knowing what to test.
     All the techniques I present in this book have a clear beginning (what to test) and a clear end (when to stop). Of course, I do not mean your systems will be bug-free if you follow these techniques. As a community, we still do not know how to build bug-free systems. But I can confidently say that the number of bugs will be reduced, hopefully to tolerable levels.
     Being *systematic* means that for a given piece of code, any developer should come up with the same test suite. Testing often happens in an ad hoc manner. Developers engineer the test cases that come to mind. It is common to see two developers developing different test suites for the same program. We should be able to systematize our processes to reduce the dependency on the developer who is doing the job.

    ([View Highlight](https://read.readwise.io/read/01gp12jm3bewp0y7tfahs1rczf))
-
- 
 Systematic testing is a way of structure your tests just in an organised way for being more efficient in your work of software testing.
   If you didn’t apply systematic testing, you would probably miss some important cases of failure. #flashcard 
    1.1 In your own words, explain what systematic testing is and how it is different from non-systematic testing.

    ([View Highlight](https://read.readwise.io/read/01gp39acrd1h8nmfx9zp0nssqt))
-
- 
 Validation #flashcard 
    1.2 Kelly, a very experienced software tester, visits Books!, a social network focused on matching people based on the books they read. Users do not report bugs often, as the Books! developers have strong testing practices in place. However, users say that the software is not delivering what it promises. What testing principle applies here?

    ([View Highlight](https://read.readwise.io/read/01gp39psbaj5vvsefzdm00zdn0))
-
- 
 B) #flashcard 
    1.3 Suzanne, a junior software tester, has just joined a very large online payment company in the Netherlands. As her first task, Suzanne analyzes the past two years’ worth of bug reports. She observes that more than 50% of the bugs happen in the international payments module. Suzanne promises her manager that she will design test cases that completely cover the international payments module and thus find all the bugs.
     Which of the following testing principles may explain why this is not possible?
     A) Pesticide paradox
     B) Exhaustive testing
     C) Test early
     D) Defect clustering

    ([View Highlight](https://read.readwise.io/read/01gp39rn3jw8wr72sgqy4cn663))
-
- 
 B) #flashcard 
    1.4 John strongly believes in unit testing. In fact, this is the only type of testing he does for any project he’s part of. Which of the following testing principles will *not* help convince John that he should move away from his “only unit testing” approach?
     A) Pesticide paradox
     B) Tests are context-dependent
     C) Absence-of-errors fallacy
     D) Test early

    ([View Highlight](https://read.readwise.io/read/01gp39sf8s0r8fwvespa3xvpzr))
-
- 
 A) #flashcard 
    1.5 Sally just started some consultancy for a company that develops a mobile app to help people keep up with their daily exercises. The development team members are fans of automated software testing and, more specifically, unit tests. They have high unit test code coverage (>95% branch coverage), but users still report a significant number of bugs.
     Sally, who is well versed in software testing, explains a testing principle to the team. Which of the following principles did she talk about?
     A) Pesticide paradox
     B) Exhaustive testing
     C) Test early
     D) Defect clustering

    ([View Highlight](https://read.readwise.io/read/01gp39zpr0nnjnqqsc22s65qbn))
-
- 
 D) #flashcard 
    1.6 Consider this requirement: “A web shop runs a batch job, once a day, to deliver all orders that have been paid. It also sets the delivery date according to whether the order is from an international customer. Orders are retrieved from an external database. Orders that have been paid are then sent to an external web service.”
     As a tester, you have to decide which test level (unit, integration, or system) to apply. Which of the following statements is true?
     A) Integration tests, although more complicated (in terms of automation) than unit tests, would provide more help in finding bugs in the communication with the web service and/or the communication with the database.
     B) Given that unit tests could be easily written (by using mocks) and would cover as much as integration tests would, unit tests are the best option for any situation.
     C) The most effective way to find bugs in this code is through system tests. In this case, the tester should run the entire system and exercise the batch process. Because this code can easily be mocked, system tests would also be cheap.
     D) While all the test levels can be used for this problem, testers are more likely to find more bugs if they choose one level and explore all the possibilities and corner cases there.

    ([View Highlight](https://read.readwise.io/read/01gp3a413ntyytpe86y03an8b9))
-
- 
 C) #flashcard 
    1.7 Delft University of Technology (TU Delft) has built in-house software to handle employee payroll. The application uses Java web technologies and stores data in a Postgres database. The application frequently retrieves, modifies, and inserts large amounts of data. All this communication is done by Java classes that send (complex) SQL queries to the database.
     As testers, we know that a bug can be anywhere, including in the SQL queries. We also know that there are many ways to exercise our system. Which one of the following is *not* a good option to detect bugs in SQL queries?
     A) Unit testing
     B) Integration testing
     C) System testing
     D) Stress testing

    ([View Highlight](https://read.readwise.io/read/01gp3af02h36kbxnfgnxkfp0ep))
-
- 
 1.8 Choosing the level of a test involves a trade-off, because each test level has advantages and disadvantages. Which one of the following is the main advantage of a test at the system level?
   A) The interaction with the system is much closer to reality.
   B) In a continuous integration environment, system tests provide real feedback to developers.
   C) Because system tests are never flaky, they provide developers with more stable feedback.
   D) A system test is written by product owners, making it closer to reality. #flashcard 
    A) The interaction with the system is much closer to reality.

    ([View Highlight](https://read.readwise.io/read/01gp3ah5v43fjcqw7xrsbdmn25))
-
- 
 1.9 What is the main reason the number of recommended system tests in the testing pyramid is smaller than the number of unit tests?
   A) Unit tests are as good as system tests.
   B) System tests tend to be slow and are difficult to make deterministic.
   C) There are no good tools for system tests.
   D) System tests do not provide developers with enough quality feedback. #flashcard 
    B) System tests tend to be slow and are difficult to make deterministic.

    ([View Highlight](https://read.readwise.io/read/01gp3ajfjz1yjawzhdv681w58a))
-
#### 2 Specification-based testing
- 
 The exhaustive tests are written after the code. Furthermore, when a developer codes, he codes requirement by requirement, and pushes his code like that, and the pipeline makes the code go directly to production, because the tests all pass. #flashcard 
    The developer writes the implementation code, guided by test-driven development (TDD) cycles, and always ensures that the code is testable. With all the classes ready, the developer switches to “testing mode.” It is time to systematically look for bugs. This is where specification testing fits in: it is the first testing technique I recommend using once you’re in testing mode.

    ([View Highlight](https://read.readwise.io/read/01gp3ayem2sd8jnaecabqvctrs))
-
##### 2.1 The requirements say it all
- 

2.1.1 Step 1: Understanding the requirements, inputs, and outputs #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3cjkspekbenncvgyfkjgb6))
-
- 

Regardless of how your requirements are written (or even if they are only in your mind), they include three parts. First is what the program/method must do: its business rules. Second, the program receives data as inputs. Inputs are a fundamental part of our reasoning, as it is through them that we can test the different cases. Third, reasoning about the output will help us better understand what the program does and how the inputs are converted to the expected output. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gp3ceqk03gfaznd22y75xtej))
-
- 

2.1.2 Step 2: Explore what the program does for various inputs #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3ck13jf4jvs06k0prb17sw))
-
- 

I stop this exploration phase when I have a clear mental model of how the program should work. Note that I do not expect you to perform the same exploration I did—it is personal and guided by my hypothesis about the program. Also note that I did not explore any corner cases; that comes later. At this moment, I am only interested in better understanding the program. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gp3d8e6wqe2z5kj5t70nne92))
-
- 

2.1.3 Step 3: Explore possible inputs and outputs, and identify partitions #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3dnabckh0daymp2xa0n4sp))
-
- 

In the case of our example, for testing purposes, the input “abcd” with `open` tag “a” and `close` tag “d”, which makes the program return “bc”, is the same as the input “xyzw” with `open` tag “x” and `close` tag “w”. You change the letters, but you expect the program to do the same thing for both inputs. Given your resource constraints, you will test just one of these inputs (it does not matter which), and you will trust that this single case represents that entire class of inputs. In testing terminology, we say that these two inputs are *equivalent*. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gp3dqbsh11ffejjcw134xzq5))
-
- 
 How to design systematic equivalence sets? #flashcard 
    A systematic way to do such an exploration is to think of the following:
     1. Each input individually: “What are the possible classes of inputs I can provide?”
     2. Each input in combination with other inputs: “What combinations can I try between the `open` and `close` tags?”
     3. The different classes of output expected from this program: “Does it return arrays? Can it return an empty array? Can it return nulls?”

    ([View Highlight](https://read.readwise.io/read/01gp3drpk4s50v7g2aw62dypq6))
-
- 

2.1.4 Step 4: Analyze the boundaries #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3e25qvymje8fhc1xzkn478))
-
- 

2.1.5 Step 5: Devise test cases #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3efgs9nqcnydcrxkn18skf))
-
- 

We end up with 21 tests. Note that deriving them did not require much creativity: the process we followed was systematic. This is the idea! #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gp3fdqgxjtabpttaswmscx12))
-
- 

2.1.6 Step 6: Automate the test cases #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3fe0k8ykqhs1jy5x261exa))
-
- 

2.1.7 Step 7: Augment the test suite with creativity and experience #flashcard  #h4 


    ([View Highlight](https://read.readwise.io/read/01gp3fpaqszmqcs3aeprybrzqs))
-
##### 2.2 Specification-based testing in a nutshell
- 
 Specification-based testing in a nutshell #flashcard 
    ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/24323188/x02-04.png-02-04.png)
     Figure 2.4 The seven steps I propose to derive test cases based on specifications. The solid arrows indicate the standard path to follow. The dashed arrows indicate that, as always, the process should be iterative, so in practice you’ll go back and forth until you are confident about the test suite you’ve created.
     The steps are as follows:
     1. *Understand the requirement, inputs, and outputs.* We need an overall idea of what we are about to test. Read the requirements carefully. What should the program do? What should it not do? Does it handle specific corner cases? Identify the input and output variables in play, their types (integers, strings, and so on), and their input domain (for example, is the variable a number that must be between 5 and 10?). Some of these characteristics can be found in the program’s specification; others may not be stated explicitly. Try to understand the nitty-gritty details of the requirements.
     2. *Explore the program.* If you did not write the program yourself, a very good way to determine what it does (besides reading the documentation) is to play with it. Call the program under test with different inputs and see what it produces as output. Continue until you are sure your mental model matches what the program does. This exploration does not have to be (and should not be) systematic. Rather, focus on increasing your understanding. Remember that you are still not testing the program.
     3. *Judiciously explore the possible inputs and outputs, and identify the partitions.* Identifying the correct partitions is the hardest part of testing. If you miss one, you may let a bug slip through. I propose three steps to identify the partitions:
     a) Look at each input variable individually. Explore its type (is it an integer? is it a string?) and the range of values it can receive (can it be null? is it a number ranging from 0 to 100? does it allow negative numbers?).
     b) Look at how each variable may interact with another. Variables often have dependencies or put constraints on each other, and those should be tested.
     c) Explore the possible types of outputs, and make sure you are testing them all. While exploring the inputs and outputs, pay attention to any implicit (business) rules, logic, or expected behavior.
     4. *Identify the boundaries.* Bugs love boundaries, so be extra thorough here. Analyze the boundaries of all the partitions you devised in the previous step. Identify the relevant ones, and add them to the list.
     5. *Devise test cases based on the partitions and boundaries.* The basic idea is to combine all the partitions in the different categories to test all possible combinations of inputs. However, combining them all may be too expensive, so part of the task is to reduce the number of combinations. The common strategy is to test exceptional behavior only once and not combine it with the other partitions.
     6. *Automate the test cases.* A test is only a test when it is automated. Therefore, the goal is to write (JUnit) automated tests for all the test cases you just devised. This means identifying concrete input values for them and having a clear expectation of what the program should do (the output). Remember that test code is code, so reduce duplication and ensure that the code is easy to read and that the different test cases are easily identifiable in case one fails.
     7. *Augment the test suite with creativity and experience.* Perform some final checks. Revisit all the tests you created, using your experience and creativity. Did you miss something? Does your gut feeling tell you that the program may fail in a specific case? If so, add a new test case.

    ([View Highlight](https://read.readwise.io/read/01gp3g6h6mb0nrkhfse7kkndmd))
-
##### 2.4 Specification-based testing in the real world
- 

The process should be iterative, not sequential
     Describing iterative processes in writing is challenging. My explanation may have given you the impression that this process is fully sequential and that you move to the next step only when you have completed the previous one. However, the entire process is meant to be iterative. In practice, I go back and forth between the different steps. #flashcard 


    ([View Highlight](https://read.readwise.io/read/01gp3j35vdvx85e0w8r9r9ytcq))
-
- 
 Approach for specification testing #flashcard 
    I propose a seven-step approach for specification testing: (1) understand the requirements, (2) explore the program if you do not know much about it, (3) judiciously analyze the properties of the inputs and outputs and identify the partitions, (4) analyze the boundaries, (5) devise concrete test cases, (6) implement the concrete test cases as automated (JUnit) tests, and (7) use creativity and experience to augment the test suite.

    ([View Highlight](https://read.readwise.io/read/01gp65rwyp9v0mag79a47ghvfw))
-
