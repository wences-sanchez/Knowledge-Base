# Complete Guide to Test Automation

deck:: [[O'Reilly-Learning::Complete Guide to Test Automation]]\
author:: [[Arnon Axelrod]]\
full-title:: "Complete Guide to Test Automation"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781484238325/)

## Highlights
### 1. The Value of Test Automation
- 
 Define Test Automation briefly #flashcard 
    “Using software to help in testing of another software,”

    
-
### 2. From Manual to Automated Testing
- 
 Is test automation just about repetition? #flashcard 
    If it was that simple, then we wouldn’t need this book (and I probably had to find another job…). But in practice, things are not so trivial. Even though a big part of executing regression tests is highly repetitive, there is at least one very important part that is not repetitive whatsoever, and this part constitutes the entire essence of executing the tests. This non-repetitive part is the part of detecting the errors! While it’s simple to record the actions that the manual tester does and replay them, it’s much trickier to detect bugs in an automated manner.

    
-
- 
 Why we can't rely on machines to do the tests for us. #flashcard 
    When we execute tests manually, we rarely think about these changes as an issue. Often the changes are minor enough that if we use our judgment and common sense, we can still relate the words that describe the test steps to the new behavior of the application, even if they don’t exactly match anymore. We use this judgment and common sense that is based on our domain knowledge, communication with other team members, experience, etc., in order to assess whether a change is a bug or an improvement. However, a machine lacks any of these skills, and therefore it treats legitimate changes and bugs equally.

    
-
- 
 Why automate it all is not a good idea 😢. #flashcard 
    instead of reflecting only the specific information that is important to test, then your tests will fail much too often due to legitimate changes, rather than on real bugs. In other words, the ratio between false positives and real failures will be too high, which makes them less reliable

    
-
- 
 Another reason in favor of manual testing #flashcard 
    The bottom line is that the effort you’ll need to make in order to investigate the failures and to maintain the tests (re-record or fix them) will very likely go beyond the cost of manually executing the tests.

    
-
- 
 When is the best time to report a test? #flashcard 
    how would it change the way you use your test automation when developing the next version, feature, or user story (see sidebar)? Would you still run it only nightly and investigate the failures the next morning? When you’ll find a bug, will you just report it in your bug tracking system and wait until the end of the quarterly release cycle for the developers to fix it? I hope that your answer is “No”!

    
-
- 

Remember that the sweet spot of automated testing is not to find as many bugs as possible, but rather to provide fast feedback about whether the system behaves in the way we expect, as defined in the tests. #flashcard 


    
-
- 
 About automated tests modularity #flashcard 
    A test automation system is usually more than just a plain collection of test scripts, but it can, and should be built in a modular fashion, where some pieces contain the fine details, and the scripts are only a composition of these pieces.

    
-
### 3. People and Tools
- 

it is highly recommended to use the same programming language that the other developers in the team use. For unit testing, this decision is obvious, both because it’s the most straightforward way, and also because usually unit tests are written by the same developers that write the code of the system. However, this is recommended also for other types of automation tests. The main reasons for this is knowledge transfer, collaboration, and reuse of tools and utilities #flashcard 


    
-
### 10. Designing the First Test Case
- 

when you come to design a test case, you should think about this test case as a scientific claim. The claim is a sentence that can be either true or false. This claim is what we’ll try to refute in the test, so the first thing that you have to do when designing a test case is to phrase that claim. At this point, I open my favorite text editor and write down this phrase. #flashcard 


    
-
- 
 About getters and setters in Selenium #flashcard 
    Hide Selenium details inside the page object class. For example, if you have a Submit button on the page, instead of having a public property (or a getter method) that returns IWebElement for that button, put a void Submit() method on the object that finds the button and clicks it internally.

    
-
- 
 About methods in the Page Object Pattern #flashcard 
    for a LoginPage class, instead of exposing getters and setters for UserName and Password, and method to click the Submit button, I prefer to have one method Login

    
-
- 
 About modelling with Page Object Pattern.
   [Hint]: Re-use subclasses #flashcard 
    Despite its name, “Page Object” should not correspond only to whole pages. Instead, it’s recommended to decompose a page into subpages or views, according to the logical layout of the page. For example, a typical email application can have a MainPage object containing properties for the toolbar, the folders tree, the list of headers, and the preview pane. Each of these views should have its own Page Object. This idea can even be repeated in a nested manner

    
-
- 
 What can you do when there are views in the Page Object Pattern that appear in different places in the application, but with slight differences?
   Or, what about when there are similar views which part of them is fixed and other parts changes according to their type? #flashcard 
    In these cases, consider using abstract classes containing the fixed parts of regular properties, and the different parts as abstract properties. Then create derived classes for each type.

    
-
### 14. Adding More Tests
- 
 Methodology of test process #flashcard 
    Plan the test as a claim and an experiment that proves or refutes it.
     Translate the experiment steps into classes and methods, and make the code compile, even though the methods are not really implemented yet (they just throw NotImplementedException).
     Run the test, and implement the first method that throws NotImplementedException.
     Repeat the last step until the test passes.

    
-
### 19. Where to Go from Here
- 

instead of spending a couple of years in each role, probably the best way is to spend a couple of years in a team where everyone does everything (dev, testing, DevOps, etc.) or at least a multidisciplinary team that works in a tight collaboration. #flashcard 


    
-
