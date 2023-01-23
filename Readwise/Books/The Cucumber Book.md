# The Cucumber Book

deck:: [[O'Reilly-Learning::The Cucumber Book]]\
author:: [[None]]\
full-title:: "The Cucumber Book"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781680502497/)
## Highlights
### Data Tables
- id:: 63c66a27-d25f-47c8-a255-ca7dc7ab7a9d
  
  Feature​:
     ​  ​Scenario​:
     ​  ​Given a board like this​:
     ​  | | 1 | 2 | 3 |
     ​  | 1 | | | |
     ​  | 2 | | | |
     ​  | 3 | | | |
     ​  When player x plays in row 2, column 1
     ​  ​Then the board should look like this​:
     ​  | | 1 | 2 | 3 |
     ​  | 1 | | | |
     ​  | 2 | x | | |
     ​  | 3 | | | | #flashcard
-
### Scenario Outline
- id:: 63c66a27-a1b8-4c89-bfa5-6d87a949f961
  
  Once you have a scenario outline with a few examples, it’s very easy to think of more examples, and even easier to add them. Before you know it, you have a huge, very comprehensive table of examples—and a problem.
     Why?
     On a system of any serious complexity, you can quite quickly start to experience what mathematicians call combinatorial explosion, where the number of different combinations of inputs and expected outputs becomes unmanageable. In trying to cover every possible eventuality, you end up with rows and rows of example data for Cucumber to execute. Remember that each of those little rows represents a whole scenario that might take several seconds to execute, and that can quickly start to add up. When your tests take longer to run, you slow down your feedback loop, making the whole team less productive as a result. #flashcard
-
- id:: 63c66a27-b228-4ddb-b4b8-4393250685bd
  
  Although this is a useful technique, be careful that your programmer’s instinct to reduce duplication at all costs doesn’t take over here.[17] If you move too much of the text of a step into the examples table, it can be very hard to read the flow of the scenario. Remember your goal is readability, so don’t take this too far, and always test your features by getting other people to regularly read them and give you feedback. #flashcard
-
### Working Together
- id:: 63c66a27-7986-4767-af42-f221c227f644
  
  Let’s rewrite the scenario without the passwords:
     ​  ​Scenario​: Check inbox
     ​  Given a User ​"Dave"​
     ​  And a User ​"Sue"​
     ​  And an email to ​"Dave"​ from ​"Sue"​
     ​  When I sign in as ​"Dave"​
     ​  Then I should see 1 email from ​"Sue"​ in my inbox
     This is definitely an improvement, making it easier to read and understand the essence of the scenario. Let’s try stripping away some more of the noise:
     ​  ​Scenario​: Check inbox
     ​  Given I have received an email from ​"Sue"​
     ​  When I sign in
     ​  Then I should see 1 email from ​"Sue"​ in my inbox
     Now we have a simple three-step scenario that’s clear and concise #flashcard
-
- id:: 63c66a27-1449-443c-9a23-5c4053bc3ca7
   Cucumber has to be a declarative language #flashcard 
    In computer programming, there are two contrasting styles for expressing the instructions you give to a computer to make it do something for you. These styles are called imperative programming and declarative programming.
     Imperative programming means using a sequence of commands for the computer to perform in a particular order. Ruby is an example of an imperative language: you write a program as a series of statements that Ruby runs one at a time, in order. A declarative program tells the computer what it should do without prescribing precisely how to do it. CSS is an example of a declarative language: you tell the computer what you want the various elements on a web page to look like, and you leave it to take care of the rest.
-
- id:: 63c66a27-0435-46f5-bb93-3040bbc54755
   Tienes que escribir el qué, no el cómo! #flashcard 
    Scenario​: Redirect user to originally requested page after logging in
     ​  Given I am an unauthenticated User
     ​  When I attempt to view some restricted content
     ​  Then I am shown a login form
     ​  When I authenticate with valid credentials
     ​  Then I should be shown the restricted content
     The beauty of this style is that it is not coupled to any specific implementation of the user interface
-
- id:: 63c66a27-55d4-4abc-a0a6-9b9769eaf8fd
   Puedes enlazar varios tests con un mismo step!!! #flashcard 
    It’s true that using declarative style will mean you have to write more step definitions, but you can keep the code in those step definitions short
-
### Caring for Your Tests
- id:: 63c66a27-18dd-468e-9d26-1f1fdba47e6b
  
  It might seem like stating the obvious, but having a lot of scenarios is by far the easiest way to give yourself a slow overall feature run. We’re not trying to suggest you give up on BDD and go back to cowboy coding, but we do suggest you treat a slow feature run as a red flag. Having lots of tests has other disadvantages than just waiting a long time for feedback. It’s hard to keep a large set of features organized, making them awkward for readers to navigate around. Maintenance is also harder on the underlying step definitions and support code.
     We find that teams that have a single humongous build also tend to have an architecture that could best be described as a big ball of mud. #flashcard
-
### 7. Step Definitions: On the Inside
- id:: 63c66a27-36a0-4b4c-a5a0-7e907e2b514e
   How is Cucumber used in the real life? #flashcard 
    Now we’re going to pick up this scenario and work outside-in, designing the system as we go, just as we would on a real project
-
### Sketching Out the Domain Model
- id:: 63c66a27-2f76-47ad-80ce-18ce358e8724
   Es mejor terminar de testear los steps del escenario que zambullirse en el TDD (un test funcional [escenario] fallido —> un nuevo ciclo en TDD) #flashcard 
    It’s tempting to pause here, move the Account class into a separate file, and start driving out the behavior we want using unit tests. We’re going to try to resist that temptation for now and stay on the outside of the Account class. If we can get a full tour through the scenario from this perspective, we’ll be more confident in the design of the class’s interface once we do step inside and start implementing it.
-
### Removing Duplication with Transforms
- id:: 63c66a27-479f-4ed8-aacc-5ea869d53909
  
  Transform(​/^\d+$/​) ​do​ |number|
     ​  number.to_i
     ​  ​end​ #flashcard
-