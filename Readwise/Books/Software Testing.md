# Software Testing

deck:: [[O'Reilly-Learning::Software Testing]]\
author:: [[None]]\
full-title:: "Software Testing"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/software-testing-second/0672327988/ibis_generated_cover_thumbnail.jpg)
## Highlights
### 1. Software Testing Background
- id:: 63c66a24-bf3d-4ec6-8b83-57c1295ebe10
  
  The goal of a software tester is to find bugs. #flashcard
-
- id:: 63c66a24-08fb-4731-9389-56e2c9f6725d
   How important it's to think how to break! #flashcard 
    If you're only testing things that should work and setting up your tests so they'll pass, you will miss the things that don't work. You will miss the bugs.
-
- id:: 63c66a24-238f-4dcb-828a-011567e87d93
  
  The goal of a software tester is to find bugs and find them as early as possible. #flashcard
-
- id:: 63c66a24-fa6b-4c2f-8194-35d8aa4f4e69
   What is the goal of a tester? #flashcard 
    The goal of a software tester is to find bugs, find them as early as possible, and make sure they get fixed.
-
- id:: 63c66a24-1758-4e92-88c4-0522542b2270
  
  At first glance, it may appear that a software tester's job would be easier than a programmer's. Breaking code and finding bugs must surely be easier than writing the code in the first place. Surprisingly, it's not. #flashcard
-
### 2. The Software Development Process
- id:: 63c66a24-d04a-493a-a96a-48a2d7768797
   What is a software deliverable? #flashcard 
    The term used in the software industry to describe a software product component that's created and passed on to someone else is deliverable. The easiest way to explain what all these deliverables are is to organize them into major categories
-
- id:: 63c66a24-8652-48c3-97de-1e03d01de6a5
   Testers' deliverables #flashcard 
    For the same reasons that programmers must plan and document their work, software testers must as well. It's not unheard of for a software test team to create more deliverables than the programmers.
-
- id:: 63c66a24-578b-4455-a1bf-134773aacbbc
   Waterfall process and Testing... #flashcard 
    From a testing perspective, the waterfall model offers one huge advantage over the other models presented so far. Everything is carefully and thoroughly specified. By the time the software is delivered to the test group, every detail has been decided on, written down, and turned into software. From that, the test group can create an accurate plan and schedule. They know exactly what they're testing, and there's no question about whether something is a feature or a bug.But, with this advantage, comes a large disadvantage. Because testing occurs only at the end, a fundamental problem could creep in early on and not be detected until days before the scheduled product release. Remember from Chapter 1, “Software Testing Background,” how the cost of bugs increases over time? What's needed is a model that folds the testing tasks in earlier to find problems before they become too costly.
-
### 3. The Realities of Software Testing
- id:: 63c66a24-4a89-4c81-9893-69d85e8354ab
  
  One key concept that software testers need to learn is how to reduce the huge domain of possible tests into a manageable set, and how to make wise risk-based decisions on what's important to test and what's not. #flashcard
-
- id:: 63c66a24-263e-424b-800e-06b951dbef9c
   How can you overcome the 'pesticide paradox'? #flashcard 
    To overcome the pesticide paradox, software testers must continually write new and different tests to exercise different parts of the program and find more bugs.
-
- id:: 63c66a24-d03b-4252-83d1-cb39944c60cd
   Tester's tip #flashcard 
    Don't just report bad news. If you find a piece of code surprisingly bug free, tell the world. Pop into a programmer's cubicle occasionally just to chat. If all you ever do is report bad news, people will see you coming and will run and hide.
-
- id:: 63c66a24-b81e-46ec-96e1-7646573c0540
   What are Verification and Validation? #flashcard 
    Verification is the process confirming that something—software—meets its specification. Validation is the process confirming that it meets the user's requirements.
-
### 4. Examining the Specification
- id:: 63c66a24-a5a7-4169-8614-6ce8ab937ac5
   Note about the white-box tests #flashcard 
    There is a risk to white-box testing. It's very easy to become biased and fail to objectively test the software because you might tailor the tests to match the code's operation.
-
- id:: 63c66a24-6f2f-40c9-9c61-fac562771866
   Professional tip #flashcard 
    Tell your project team, “This is what I plan to test and submit bugs against.” You'll be amazed at how many details they'll immediately fill in.
-
- id:: 63c66a24-0894-4a6b-9487-85e51c2f2baa
   What means quality, meanly? #flashcard 
    It's important to understand the customer's expectations. Remember that the definition of quality means “meeting the customer's needs.” As a tester, you must understand those needs to test that the software meets them.
-
- id:: 63c66a24-be51-4829-97db-0519c4b904b3
   Tip about long specs. #flashcard 
    If you review a portion of the spec and don't understand it, don't assume that it's correct and go on. Eventually, you'll have to use this specification to design your software tests, so you'll eventually have to understand it.
-
### 5. Testing the Software with Blinders On
- id:: 63c66a24-0b82-44cd-8e4d-17e60d5fb6cc
   Tip about being effective at testing #flashcard 
    Selecting test cases is the single most important task that software testers do. Improper selection can result in testing too much, testing too little, or testing the wrong things. Intelligently weighing the risks and reducing the infinite possibilities to a manageable effective set is where the magic is.
-
- id:: 63c66a24-8181-40a6-a517-b4d4ec4f7a79
   Tip about 'test-to-pass' and 'test-to-fail' #flashcard 
    When designing and running your test cases, always run the test-to-pass cases first. It's important to see if the software fundamentally works before you throw the kitchen sink at it. You might be surprised how many bugs you find just using the software normally.
-
- id:: 63c66a24-8b55-4256-9617-9beb44a98c54
   Test input ideas #flashcard 
    So, with invalid, wrong, incorrect, and garbage data testing, have some fun. If the software wants numbers, give it letters. If it accepts only positive numbers, enter negative numbers. If it's date sensitive, see if it'll work correctly on the year 3000. Pretend to have “fat fingers” and press multiple keys at a time.
-
- id:: 63c66a24-bdc3-4e05-b20a-f50c4e6360e5
   What is stress testing? #flashcard 
    Stress testing is running the software under less-than-ideal conditions—low memory, low disk space, slow CPUs, slow modems, and so on.
-
### 17. Planning Your Test Effort
- id:: 63c66a24-fdd9-4601-8292-ff7f1da061d1
   ¿Para qué hago el test plan si soy yo solo y el proyecto es corto y estamos en la era agile?
   Pues para pensar cómo voy a testear mi código. El documento que está en el GitHub es solo el resultado como deliverable del proyecto de pensarlo #flashcard 
    The test plan is a by-product of the detailed planning process that's undertaken to create it. It's the planning process that matters, not the resulting document.
-