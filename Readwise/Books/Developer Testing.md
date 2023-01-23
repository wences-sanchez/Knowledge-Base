# Developer Testing

deck:: [[O'Reilly-Learning::Developer Testing]]\
author:: [[None]]\
full-title:: "Developer Testing"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/developer-testing-building/9780134291109/ibis_generated_cover_thumbnail.jpg)
## Highlights
### About the Author
- id:: 63c669f4-f70f-44e7-86f1-f1d7287592c9
   That’s what I want to become 😃 #flashcard 
    Twenty-five years later, Alexander still writes code and remains a developer at heart.
-
### Chapter 1. Developer Testing
- id:: 63c669f4-c80f-4728-b4d4-4dbbe4cd7685
   What’s the reason why the tester shouldn’t be the same person than the developer? #flashcard 
    Some types of testing require specific skills or some distance from the tested software in order to mitigate any bias its creators may be subject to. This is why testing is a separate area of expertise.
-
- id:: 63c669f4-2ac9-40ea-b415-bc7619ca2a39
   Who should write the unit tests? #flashcard 
    Nevertheless, unit tests are 100 percent developer-owned.
-
- id:: 63c669f4-c1ac-4eff-9e30-937dceda6a34
   How would you fix a new bug issue in a maintenance project? #flashcard 
    A well-proven technique for fixing bugs is restraining oneself from rushing ahead to implement a fix, and first writing a test that’ll fail because of the bug’s presence. In the absence of the bug, that test would pass. Once the test is in place, the bug is fixed. If the fix is correct, the test passes.
-
- id:: 63c669f4-8849-40b6-b422-ad9a310b9707
  
  performed by developers in a cross-functional team #flashcard
-
- id:: 63c669f4-7f91-4c52-bed5-10029ff8c222
  
  Therefore, this book recurrently returns to the topic of collaboration between team members who are better at writing the code and team members who are better at testing it. #flashcard
-
### Chapter 2. Testing Objectives, Styles, and Roles
- id:: 63c669f4-8d07-434d-8532-f5d4b1933ca4
  
  By now it should be obvious that developer testing, as described in this book, is testing meant to support. #flashcard
-
- id:: 63c669f4-0461-404e-8784-d7202191b6fe
   About the Tester role in Agile #flashcard 
    In agile testing, the role of the tester is shifted from reactive to proactive. Instead of writing test cases, waiting for something to test, or executing manual tests, the tester becomes the team’s quality champion and contributes to a successful release in any way she can. For example, by helping the customer or product owner to specify desired functionality, by making sure that testing activities are taken into account during planning and estimation meetings, by educating and assisting the developers in test design and test automation, or by pair programming or pair testing.
-
- id:: 63c669f4-0dc8-4bc7-8c35-e713260355b1
   What are the differences between Traditional and Agile mind-sets? #flashcard 
    The wording is important here. In traditional testing, tests are supposed to be planned and created in parallel with the development. The difference is that collaboration, joint planning, and common success/completion criteria aren’t emphasized.
-
- id:: 63c669f4-58e6-4406-94c7-f04e505d30a9
   Just talking seriously about QA and what should be your attitude #flashcard 
    You know what? None of these factors really matter. If you’re the only developer, or your team doesn’t have any testers, or you’re being rushed by others, or the system is old and crappy, your quality assurance process is the only one you have, and it will make or break your software.
-
### Chapter 3. The Testing Vocabulary
- id:: 63c669f4-9e51-4861-90d7-3b6ddff3bfff
  
  All developers sometimes make mistakes. These are known as errors in the language of testing. #flashcard
-
- id:: 63c669f4-dd0b-4b82-a4d5-1b9b6ad9f140
  
  Errors lead to defects in the software #flashcard
-
- id:: 63c669f4-3858-4911-a0ff-b49b883f9a7f
  
  Defects/bugs may lead to software failures. Not all of them do, though. A defect in code that’s never executed won’t cause a failure. #flashcard
-
- id:: 63c669f4-0dbb-402e-95f3-5f09c5eb39ed
   What are system tests? #flashcard 
    Systems are made up of finished and integrated building blocks. They may be components or other systems. System testing is the activity of verifying that the entire system works. System tests are often executed from a black box perspective
-
- id:: 63c669f4-cd56-46c7-8692-dac58aaadd8f
  
  He suggested defining a component’s behavior as the outcome produced by its functionality under certain preconditions. #flashcard
-
- id:: 63c669f4-ae0b-49c7-a714-3e7b1bec8111
  
  FIGURE 3.3 Agile Testing Quadrants as presented in the book More Agile Testing by Lisa Crispin and Janet Gregory (2014). #flashcard
-
- id:: 63c669f4-daa3-4d25-84fa-f0f914764e77
   What are negative tests? #flashcard 
    The purpose of negative testing is to verify that the system behaves correctly if supplied with invalid values and that it doesn’t generate any unexpected results. What outcome to expect depends on the test level. At the system level, we generally want the system to “do the right thing”: either reject the faulty input in a user-friendly manner, or recover somehow. At the unit level, throwing an exception may be the right thing to do. For example, if a function exercised with a unit test expects a positive number and throws an IllegalArgumentException or ArgumentOutOfRangeException in a negative test that may be fine. What’s important is that the developer has anticipated the scenario.
-
- id:: 63c669f4-5a62-4a53-b423-0c2d23f32881
  
  Integration tests verify that components/systems can talk to each other, but sometimes the term is used to describe tests that are somewhere between unit tests and system tests. #flashcard
-
### Chapter 4. Testability from a Developer’s Perspective
- id:: 63c669f4-2d31-40ea-b993-1afcfeff2b2c
  
  However, estimating progress for software that has no tests (because of poor testability) ranges between best guesses and wishful thinking. A developer who believes he is “95 percent finished” with a feature has virtually no way of telling what fraction of seemingly unrelated functionality he has broken along the way and how much time it’ll take to fix these regressions and the remaining “5 percent”. A suite of tests makes this situation more manageable. Again, if the feature is supposedly “95 percent finished” and all tests for the new functionality pass, as well as those that exercise the rest of the system, the estimate is much more credible. Now the uncertainty is reduced to potential surprises in the remaining work, not to random regressions that may pop up anywhere in the system #flashcard
-
- id:: 63c669f4-213b-4b43-9156-a95e635f8919
  
  Changing software that has no tests makes the average developer uncomfortable and afraid (and it should). Fear is easily observed in code. It manifests itself as duplication—the safe way to avoid breaking something that works. #flashcard
-