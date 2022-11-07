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
- id:: 63639917-91c7-4154-ae36-0e8751781198
   That’s what I want to become 😃 #flashcard 
    Twenty-five years later, Alexander still writes code and remains a developer at heart.
-
### Chapter 1. Developer Testing
- id:: 63639917-f542-4e5b-aa72-82695d47f5a9
   What’s the reason why the tester shouldn’t be the same person than the developer? #flashcard 
    Some types of testing require specific skills or some distance from the tested software in order to mitigate any bias its creators may be subject to. This is why testing is a separate area of expertise.
-
- id:: 63639917-1091-4aa8-a493-f1edc93e67d2
   Who should write the unit tests? #flashcard 
    Nevertheless, unit tests are 100 percent developer-owned.
-
- id:: 63639917-5cf2-4067-95e2-5e0ad0479927
   How would you fix a new bug issue in a maintenance project? #flashcard 
    A well-proven technique for fixing bugs is restraining oneself from rushing ahead to implement a fix, and first writing a test that’ll fail because of the bug’s presence. In the absence of the bug, that test would pass. Once the test is in place, the bug is fixed. If the fix is correct, the test passes.
-
- id:: 63639917-cdd8-4376-a04d-8b0e955ac333
  
  performed by developers in a cross-functional team #flashcard
-
- id:: 63639917-3ad2-4828-88f7-cb09f1dfe312
  
  Therefore, this book recurrently returns to the topic of collaboration between team members who are better at writing the code and team members who are better at testing it. #flashcard
-
### Chapter 2. Testing Objectives, Styles, and Roles
- id:: 63639917-5220-48ef-a4d8-2bcf5f658716
  
  By now it should be obvious that developer testing, as described in this book, is testing meant to support. #flashcard
-
- id:: 63639917-1f0b-4f1d-9cc9-2c5dc9241763
   About the Tester role in Agile #flashcard 
    In agile testing, the role of the tester is shifted from reactive to proactive. Instead of writing test cases, waiting for something to test, or executing manual tests, the tester becomes the team’s quality champion and contributes to a successful release in any way she can. For example, by helping the customer or product owner to specify desired functionality, by making sure that testing activities are taken into account during planning and estimation meetings, by educating and assisting the developers in test design and test automation, or by pair programming or pair testing.
-
- id:: 63639917-95db-4766-bd47-cbfe1a15518b
   What are the differences between Traditional and Agile mind-sets? #flashcard 
    The wording is important here. In traditional testing, tests are supposed to be planned and created in parallel with the development. The difference is that collaboration, joint planning, and common success/completion criteria aren’t emphasized.
-
- id:: 63639917-ae60-4527-85f4-2c4cd2782b1f
   Just talking seriously about QA and what should be your attitude #flashcard 
    You know what? None of these factors really matter. If you’re the only developer, or your team doesn’t have any testers, or you’re being rushed by others, or the system is old and crappy, your quality assurance process is the only one you have, and it will make or break your software.
-
### Chapter 3. The Testing Vocabulary
- id:: 63639917-cb0f-4b29-a00f-3214285dbb51
  
  All developers sometimes make mistakes. These are known as errors in the language of testing. #flashcard
-
- id:: 63639917-3d1e-41e8-84c4-be222fa6df71
  
  Errors lead to defects in the software #flashcard
-
- id:: 63639917-c58e-42e4-b1ff-4c4565150fc0
  
  Defects/bugs may lead to software failures. Not all of them do, though. A defect in code that’s never executed won’t cause a failure. #flashcard
-
- id:: 63639917-f0cd-49b1-bc3c-0dae93e0c47f
   What are system tests? #flashcard 
    Systems are made up of finished and integrated building blocks. They may be components or other systems. System testing is the activity of verifying that the entire system works. System tests are often executed from a black box perspective
-
- id:: 63639917-7746-4a33-a6d1-2ac9f5edbcf3
  
  He suggested defining a component’s behavior as the outcome produced by its functionality under certain preconditions. #flashcard
-
- id:: 63639917-e688-4b62-9a7c-afb2e455d487
  
  FIGURE 3.3 Agile Testing Quadrants as presented in the book More Agile Testing by Lisa Crispin and Janet Gregory (2014). #flashcard
-
- id:: 63639917-1831-4ca5-b65f-644c57177b04
   What are negative tests? #flashcard 
    The purpose of negative testing is to verify that the system behaves correctly if supplied with invalid values and that it doesn’t generate any unexpected results. What outcome to expect depends on the test level. At the system level, we generally want the system to “do the right thing”: either reject the faulty input in a user-friendly manner, or recover somehow. At the unit level, throwing an exception may be the right thing to do. For example, if a function exercised with a unit test expects a positive number and throws an IllegalArgumentException or ArgumentOutOfRangeException in a negative test that may be fine. What’s important is that the developer has anticipated the scenario.
-
- id:: 63639917-d862-44c0-9547-ed83c133f012
  
  Integration tests verify that components/systems can talk to each other, but sometimes the term is used to describe tests that are somewhere between unit tests and system tests. #flashcard
-
### Chapter 4. Testability from a Developer’s Perspective
- id:: 63639917-78ff-4b10-bc9e-c63bc30f4fc9
  
  However, estimating progress for software that has no tests (because of poor testability) ranges between best guesses and wishful thinking. A developer who believes he is “95 percent finished” with a feature has virtually no way of telling what fraction of seemingly unrelated functionality he has broken along the way and how much time it’ll take to fix these regressions and the remaining “5 percent”. A suite of tests makes this situation more manageable. Again, if the feature is supposedly “95 percent finished” and all tests for the new functionality pass, as well as those that exercise the rest of the system, the estimate is much more credible. Now the uncertainty is reduced to potential surprises in the remaining work, not to random regressions that may pop up anywhere in the system #flashcard
-
- id:: 63639917-ca3b-4652-a277-8ac594ab3e91
  
  Changing software that has no tests makes the average developer uncomfortable and afraid (and it should). Fear is easily observed in code. It manifests itself as duplication—the safe way to avoid breaking something that works. #flashcard
-