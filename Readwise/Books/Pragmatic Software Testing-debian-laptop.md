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
- id:: 6363992b-10ec-4ae8-a327-9001db7b4f1b
  
  but in reality, most of our work as test professionals is constrained by time (and often money) too. For this reason, I suggest time constraints for each exercise #flashcard
-
### 1. What Does It Mean to Be Pragmatic?
- id:: 6363992b-bde5-4757-bddf-3559c17ba2ea
  
  On most projects I’ve worked on, I’ve typically wanted to do the following: #flashcard
-
- id:: 6363992b-74a3-47e1-977e-7e20e9f14f5e
   What does ‘effective' mean? #flashcard 
    Webster’s dictionary defines the word effective as “producing a decided, decisive, or desired result; impressive.” So, to be an effective software tester, you must decide what results you desire from your testing efforts.
-
- id:: 6363992b-ca1e-4fa6-9543-1dc6478a026f
   What does “efficient” mean? #flashcard 
    Likewise, Webster’s defines efficient as “productive of the desired effect; especially to be productive without waste.” So, to be an efficient tester, you must allocate resources (time and money) appropriately.
-
- id:: 6363992b-9789-4584-a1dc-70322c7f709b
   What's not testing? #flashcard 
    Let’s start with what it’s not: Software testing is not about proving conclusively that the software is free from any defects, or even about discovering all the defects. Such a mission for a test team is truly impossible to achieve.
-
- id:: 6363992b-d07d-49a2-9c8b-0c390fc5dc43
   Boris Beizer identified five phases of a tester’s mental life: #flashcard 
    Phase 0: There’s no difference between testing and debugging. Other than in support of debugging, testing has no purpose.Phase 1: The purpose of testing is to show that the software works.Phase 2: The purpose of testing is to show that the software doesn’t work.Phase 3: The purpose of testing is not to prove anything, but to reduce the perceived risk of the software not working to an acceptable value.Phase 4: Testing is not an act. It is a mental discipline that results in low-risk software without much testing effort.
-
### 3. Aligning Testing with the Project
- id:: 6363992b-b9b7-4eb6-9e83-f152bfc93a89
   Phases of testing: #flashcard 
    The first phase or level is often called unit, component, or subsystem test. Here, you test portions of the system as they are created, looking for bugs in the individual pieces of the system under test before these pieces are integrated.In the second phase or level of testing, often called integration (and less frequently, string) test, you test collections of interoperating or communicating units, subsystems, or components, looking for bugs in the relationships and interfaces between pairs and groups of these pieces of the system under test as the pieces come together.In the third phase or level of testing, often called system test, you test the entire system, looking for bugs in the overall and particular behaviors, functions, and responses of the system under test as a whole.In the fourth phase or level of testing, often called acceptance or pilot test, you generally are no longer looking for bugs. Rather, the objective is to demonstrate that the product is ready for deployment or release.
-
- id:: 6363992b-9bc5-49d0-907a-d2f056f9926d
   About V-Model estimations. #flashcard 
    While this model is intuitive and in many cases familiar to testers, developers, and managers, it has some weak spots. For one, it is usually schedule- and budget-driven. That is, when plans are flawed and money runs out, it’s usually testing that is cut back, since most of the testing happens at the end. For large projects, the chances of perfect planning 6, 12, or even 18 months or longer in advance are very low. That said, this model beats chaos.
-
### 4. Understanding Test Strategies, Tactics, and Design
- id:: 6363992b-4faf-423a-84ce-fc491b3e51d1
   Definition of Regression: #flashcard 
    Regression is the misbehavior of a previously correct function, attribute, or feature. The word is also used to mean the discovery of a previously undiscovered bug while running a previously run test. Regression is generally associated with some change to the system, such as adding a feature or fixing a bug.
-
### 12. Use Cases, Live Data, and Decision Tables
- id:: 6363992b-3c9d-4bc8-b732-cd5e3edc2430
   What techniques should you combine with Equivalence Classes? #flashcard 
    You can and should combine the use case and scenario technique with equivalence classes to make sure that every equivalence class is covered. You can also use boundary value analysis to create challenging tests.
-
- id:: 6363992b-0d39-4fe4-8ad1-3c58bf05a41d
   Format of Decision Table #flashcard 
    The table is read columnwise. The leftmost column specifies first the conditions, then the actions. The conditions listed are those that influence the behavior of the system for the particular transaction under consideration. The actions listed are those actions the system might carry out depending on the conditions when handling this transaction. Each subsequent column to the right indicates, under the specified combination of conditions, which specified actions should and shouldn’t take place.The dashes (-) indicate conditions that aren’t reached as part of this rule.
-
### 14. State Transition Diagrams
- id:: 6363992b-4238-469d-b232-f9552416a5aa
   Sobre tablas de estado #flashcard 
    State TablesA problem with using state transition diagrams is that they don’t show all possible combinations of states and events. Consider an e-commerce system. Unless the programmer takes steps to avoid it, the user can trigger both legal and illegal events by clicking buttons on the screen.
-