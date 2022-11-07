# Advanced Software Testing - Vol. 1, 2nd Edition

deck:: [[O'Reilly-Learning::Advanced Software Testing - Vol. 1, 2nd Edition]]\
author:: [[None]]\
full-title:: "Advanced Software Testing - Vol. 1, 2nd Edition"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/advanced-software-testing/9781457189517/ibis_generated_cover_thumbnail.jpg)
## Highlights
### 1 Testing Process
- id:: 6363990c-574d-4047-b433-dfb0af7737dd
  
  when you’re documenting the tests, keep in mind that you might not be documenting them just for yourself. What other testers will need to run them? Will the tests be reviewed by other project stakeholders? #flashcard
-
### 2 Test Management: Responsibilities for the Test Analyst
- id:: 6363990c-b4c1-4c83-81b1-9b6d3a758072
  
  In some cases, values are not independent, in that the selection of one value from one subset constrains the choice in another subset #flashcard
-
- id:: 6363990c-3185-474c-80c0-41b94ffbffee
  
  for those partitions that are ordered values, we select the minimum and maximum values—the boundary values—as test values. This technique can be applied at any level of testing. It can even be used during white-box testing when looking at loops, when looking at data structures such as lists and arrays, and during non-functional testing for boundaries in memory usage and performance. #flashcard
-
- id:: 6363990c-dd5a-4321-bbd5-5db7ef02b831
  
  When used properly, this technique will find situations where boundaries are in the wrong place, boundaries are just plain missing, or undesired boundaries exist #flashcard
-
- id:: 6363990b-bc9d-442a-be51-ad3912588e72
  
  Conceptually, boundary value analysis is about testing the edges of equivalence classes #flashcard
-
- id:: 6363990b-ec84-4187-b682-4a385ec2c5b9
  
  So, do all equivalence classes have boundary values? No, definitely not. Boundary value analysis is an extension of equivalence partitioning that applies only when the members of an equivalence class are ordered. #flashcard
-
- id:: 6363990b-8de0-41c5-9789-d6bb7a391044
  
  Notice that the number of columns—i.e., the number of business rules—is equal to 2 raised to the power of the number of conditions #flashcard
-
- id:: 6363990b-9afc-4ea4-9775-b5f54da1e21d
  
  To combine two or more columns, look for two or more columns that result in the same combination of actions. #flashcard  #qa
-
- id:: 6363990b-ac18-4725-ba75-400600391731
   What does a cause-effect graph look like? #flashcard 
    Cause-effect graphs are simply pictorial representations of the same business logic that is shown in a decision table.
-
### 3 Test Techniques
- id:: 6363990b-8ee3-4b0e-a123-80904e4b7e11
  
  An oracle should not be the code, because otherwise we are only testing whether the compiler works. #flashcard
-
- id:: 6363990b-bad5-488f-a249-380604a34826
  
  It’s important to remember that fulfilling coverage criteria for a particular test design technique does not mean that your tests are in any way complete or exhaustive. Instead, it means that the model has run out of useful tests to suggest, based on that technique. #flashcard
-
- id:: 6363990b-3fe7-478b-9600-d8df3be2f295
   About Equivalence Partitioning #flashcard 
    This technique is also very useful in constructing smoke tests, though testing of some of the less-risky partitions frequently is omitted in smoke tests.
-
- id:: 6363990b-3692-4c58-ac28-a96305dfb068
  
  If the conditions are not sufficient, but we must also refer to what conditions have existed in the past, then we’ll want to use state-based testing #flashcard
-