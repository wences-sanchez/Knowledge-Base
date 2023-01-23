# Pragmatic Software Testing

deck:: [[O'Reilly-Learning::Pragmatic Software Testing]]\
author:: [[None]]\
full-title:: "Pragmatic Software Testing"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/pragmatic-software-testing/9780470127902/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Introduction
- id:: 63c66a19-415c-456f-aa30-137200b3e181
  
  but in reality, most of our work as test professionals is constrained by time (and often money) too. For this reason, I suggest time constraints for each exercise #flashcard
-
### 1. What Does It Mean to Be Pragmatic?
- id:: 63c66a19-495c-4be8-be25-a517d2393f41
  
  On most projects I’ve worked on, I’ve typically wanted to do the following: #flashcard
-
- id:: 63c66a19-adf8-4e9d-917f-86a18afbb8ae
   What does ‘effective' mean? #flashcard 
    Webster’s dictionary defines the word effective as “producing a decided, decisive, or desired result; impressive.” So, to be an effective software tester, you must decide what results you desire from your testing efforts.
-
- id:: 63c66a19-fc14-4f5e-aecd-982a8d4fb4d4
   What does “efficient” mean? #flashcard 
    Likewise, Webster’s defines efficient as “productive of the desired effect; especially to be productive without waste.” So, to be an efficient tester, you must allocate resources (time and money) appropriately.
-
- id:: 63c66a19-d49a-46b9-9976-f597ae26a756
   What's not testing? #flashcard 
    Let’s start with what it’s not: Software testing is not about proving conclusively that the software is free from any defects, or even about discovering all the defects. Such a mission for a test team is truly impossible to achieve.
-
- id:: 63c66a19-1410-44e0-ba6e-155c14abf8cc
   Boris Beizer identified five phases of a tester’s mental life: #flashcard 
    Phase 0: There’s no difference between testing and debugging. Other than in support of debugging, testing has no purpose.Phase 1: The purpose of testing is to show that the software works.Phase 2: The purpose of testing is to show that the software doesn’t work.Phase 3: The purpose of testing is not to prove anything, but to reduce the perceived risk of the software not working to an acceptable value.Phase 4: Testing is not an act. It is a mental discipline that results in low-risk software without much testing effort.
-
### 3. Aligning Testing with the Project
- id:: 63c66a19-7218-4b81-885b-4ad879a3289f
   Phases of testing: #flashcard 
    The first phase or level is often called unit, component, or subsystem test. Here, you test portions of the system as they are created, looking for bugs in the individual pieces of the system under test before these pieces are integrated.In the second phase or level of testing, often called integration (and less frequently, string) test, you test collections of interoperating or communicating units, subsystems, or components, looking for bugs in the relationships and interfaces between pairs and groups of these pieces of the system under test as the pieces come together.In the third phase or level of testing, often called system test, you test the entire system, looking for bugs in the overall and particular behaviors, functions, and responses of the system under test as a whole.In the fourth phase or level of testing, often called acceptance or pilot test, you generally are no longer looking for bugs. Rather, the objective is to demonstrate that the product is ready for deployment or release.
-
- id:: 63c66a19-ff13-4298-a511-843105a5467f
   About V-Model estimations. #flashcard 
    While this model is intuitive and in many cases familiar to testers, developers, and managers, it has some weak spots. For one, it is usually schedule- and budget-driven. That is, when plans are flawed and money runs out, it’s usually testing that is cut back, since most of the testing happens at the end. For large projects, the chances of perfect planning 6, 12, or even 18 months or longer in advance are very low. That said, this model beats chaos.
-
### 4. Understanding Test Strategies, Tactics, and Design
- id:: 63c66a19-1eca-4cba-ad7b-565d0a8a7943
   Definition of Regression: #flashcard 
    Regression is the misbehavior of a previously correct function, attribute, or feature. The word is also used to mean the discovery of a previously undiscovered bug while running a previously run test. Regression is generally associated with some change to the system, such as adding a feature or fixing a bug.
-
### 12. Use Cases, Live Data, and Decision Tables
- id:: 63c66a19-d7c7-49a5-8f54-123c8fea76b7
   What techniques should you combine with Equivalence Classes? #flashcard 
    You can and should combine the use case and scenario technique with equivalence classes to make sure that every equivalence class is covered. You can also use boundary value analysis to create challenging tests.
-
- id:: 63c66a19-3da8-4bac-8394-db4dc4fe63e6
   Format of Decision Table #flashcard 
    The table is read columnwise. The leftmost column specifies first the conditions, then the actions. The conditions listed are those that influence the behavior of the system for the particular transaction under consideration. The actions listed are those actions the system might carry out depending on the conditions when handling this transaction. Each subsequent column to the right indicates, under the specified combination of conditions, which specified actions should and shouldn’t take place.The dashes (-) indicate conditions that aren’t reached as part of this rule.
-
### 14. State Transition Diagrams
- id:: 63c66a19-4f75-44a5-836d-1faf5b6fe98a
   Sobre tablas de estado #flashcard 
    State TablesA problem with using state transition diagrams is that they don’t show all possible combinations of states and events. Consider an e-commerce system. Unless the programmer takes steps to avoid it, the user can trigger both legal and illegal events by clicking buttons on the screen.
-