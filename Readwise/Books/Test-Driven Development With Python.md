# Test-Driven Development With Python

deck:: [[O'Reilly-Learning::Test-Driven Development With Python]]\
author:: [[None]]\
full-title:: "Test-Driven Development With Python"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781449365141/)
## Highlights
### 3. Testing a Simple Home Page with Unit Tests
- id:: 63c66a26-6ae6-444a-8bf4-3e9a3e27db37
   Unit Tests VS Functional Tests #flashcard 
    Unit Tests, and How They Differ from Functional Tests
     As with so many of the labels we put on things, the line between unit tests and functional tests can become a little blurry at times. The basic distinction, though, is that functional tests test the application from the outside, from the point of view of the user. Unit tests test the application from the inside, from the point of view of the programmer.
-
- id:: 63c66a26-0192-49b3-89af-677f5489c4a6
  
  The TDD approach I’m following wants our application to be covered by both types of test. Our workflow will look a bit like this:
     We start by writing a functional test, describing the new functionality from the user’s point of view.
     Once we have a functional test that fails, we start to think about how to write code that can get it to pass (or at least to get past its current failure). We now use one or more unit tests to define how we want our code to behave—the idea is that each line of production code we write should be tested by (at least) one of our unit tests.
     Once we have a failing unit test, we write the smallest amount of application code we can, just enough to get the unit test to pass. We may iterate between steps 2 and 3 a few times, until we think the functional test will get a little further.
     Now we can rerun our functional tests and see if they pass, or get a little further. That may prompt us to write some new unit tests, and some new code, and so on.
     You can see that, all the way through, the functional tests are driving what development we do from a high level, while the unit tests drive what we do at a low level.
     Does that seem slightly redundant? Sometimes it can feel that way, but functional tests and unit tests do really have very different objectives, and they will usually end up looking quite different.
     NOTE
     Functional tests should help you build an application with the right functionality, and guarantee you never accidentally break it. Unit tests should help you to write code that’s clean and bug free. #flashcard
-