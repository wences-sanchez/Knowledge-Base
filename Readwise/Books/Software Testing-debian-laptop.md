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
- id:: 63639930-e468-40d4-86b3-143bb8639c7b
  
  The goal of a software tester is to find bugs. #flashcard
-
- id:: 63639930-5bdd-4b1e-8026-f8ad13a3ce4c
   How important it's to think how to break! #flashcard 
    If you're only testing things that should work and setting up your tests so they'll pass, you will miss the things that don't work. You will miss the bugs.
-
- id:: 63639930-9ceb-4a1a-b9aa-877764bc3a1e
  
  The goal of a software tester is to find bugs and find them as early as possible. #flashcard
-
- id:: 63639930-80c5-4b6b-8da6-d6f67fae5789
   What is the goal of a tester? #flashcard 
    The goal of a software tester is to find bugs, find them as early as possible, and make sure they get fixed.
-
- id:: 63639930-f345-470e-a750-c1e60cdd1ecc
  
  At first glance, it may appear that a software tester's job would be easier than a programmer's. Breaking code and finding bugs must surely be easier than writing the code in the first place. Surprisingly, it's not. #flashcard
-
### 2. The Software Development Process
- id:: 63639930-af01-48ea-aef2-85d6b96df874
   What is a software deliverable? #flashcard 
    The term used in the software industry to describe a software product component that's created and passed on to someone else is deliverable. The easiest way to explain what all these deliverables are is to organize them into major categories
-
- id:: 63639930-30b4-46ad-85ae-e9d5387a9b0a
   Testers' deliverables #flashcard 
    For the same reasons that programmers must plan and document their work, software testers must as well. It's not unheard of for a software test team to create more deliverables than the programmers.
-
- id:: 63639930-79b3-450f-b408-9fb0e86d3483
   Waterfall process and Testing... #flashcard 
    From a testing perspective, the waterfall model offers one huge advantage over the other models presented so far. Everything is carefully and thoroughly specified. By the time the software is delivered to the test group, every detail has been decided on, written down, and turned into software. From that, the test group can create an accurate plan and schedule. They know exactly what they're testing, and there's no question about whether something is a feature or a bug.But, with this advantage, comes a large disadvantage. Because testing occurs only at the end, a fundamental problem could creep in early on and not be detected until days before the scheduled product release. Remember from Chapter 1, “Software Testing Background,” how the cost of bugs increases over time? What's needed is a model that folds the testing tasks in earlier to find problems before they become too costly.
-
### 3. The Realities of Software Testing
- id:: 63639930-ce34-4d26-be54-88446f12ab80
  
  One key concept that software testers need to learn is how to reduce the huge domain of possible tests into a manageable set, and how to make wise risk-based decisions on what's important to test and what's not. #flashcard
-
- id:: 63639930-9290-4507-b31c-3fe5b6735adc
   How can you overcome the 'pesticide paradox'? #flashcard 
    To overcome the pesticide paradox, software testers must continually write new and different tests to exercise different parts of the program and find more bugs.
-
- id:: 63639930-825a-4bf4-9942-574952ae3c30
   Tester's tip #flashcard 
    Don't just report bad news. If you find a piece of code surprisingly bug free, tell the world. Pop into a programmer's cubicle occasionally just to chat. If all you ever do is report bad news, people will see you coming and will run and hide.
-
- id:: 63639930-7286-4b33-80bb-c3f4e0caede3
   What are Verification and Validation? #flashcard 
    Verification is the process confirming that something—software—meets its specification. Validation is the process confirming that it meets the user's requirements.
-
### 4. Examining the Specification
- id:: 63639930-b286-4fa8-8716-e70f1a6b9e58
   Note about the white-box tests #flashcard 
    There is a risk to white-box testing. It's very easy to become biased and fail to objectively test the software because you might tailor the tests to match the code's operation.
-
- id:: 63639930-613e-45c7-a812-7f2372777826
   Professional tip #flashcard 
    Tell your project team, “This is what I plan to test and submit bugs against.” You'll be amazed at how many details they'll immediately fill in.
-
- id:: 63639930-de51-4d86-ba22-1892bca74545
   What means quality, meanly? #flashcard 
    It's important to understand the customer's expectations. Remember that the definition of quality means “meeting the customer's needs.” As a tester, you must understand those needs to test that the software meets them.
-
- id:: 63639930-0770-45ac-a28b-02c3ba73612f
   Tip about long specs. #flashcard 
    If you review a portion of the spec and don't understand it, don't assume that it's correct and go on. Eventually, you'll have to use this specification to design your software tests, so you'll eventually have to understand it.
-
### 5. Testing the Software with Blinders On
- id:: 63639930-9e84-4774-9ee1-b3f110a50904
   Tip about being effective at testing #flashcard 
    Selecting test cases is the single most important task that software testers do. Improper selection can result in testing too much, testing too little, or testing the wrong things. Intelligently weighing the risks and reducing the infinite possibilities to a manageable effective set is where the magic is.
-
- id:: 63639930-b094-483c-bb77-d543641e3570
   Tip about 'test-to-pass' and 'test-to-fail' #flashcard 
    When designing and running your test cases, always run the test-to-pass cases first. It's important to see if the software fundamentally works before you throw the kitchen sink at it. You might be surprised how many bugs you find just using the software normally.
-
- id:: 63639930-c5d1-43ce-9351-6327cebf80cc
   Test input ideas #flashcard 
    So, with invalid, wrong, incorrect, and garbage data testing, have some fun. If the software wants numbers, give it letters. If it accepts only positive numbers, enter negative numbers. If it's date sensitive, see if it'll work correctly on the year 3000. Pretend to have “fat fingers” and press multiple keys at a time.
-
- id:: 63639930-84dc-4b0e-8256-c568ae0be1d4
   What is stress testing? #flashcard 
    Stress testing is running the software under less-than-ideal conditions—low memory, low disk space, slow CPUs, slow modems, and so on.
-
### 17. Planning Your Test Effort
- id:: 63639930-174e-4891-96ab-935386008a9c
   ¿Para qué hago el test plan si soy yo solo y el proyecto es corto y estamos en la era agile?
   Pues para pensar cómo voy a testear mi código. El documento que está en el GitHub es solo el resultado como deliverable del proyecto de pensarlo #flashcard 
    The test plan is a by-product of the detailed planning process that's undertaken to create it. It's the planning process that matters, not the resulting document.
-