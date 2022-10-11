title:: Pragmatic Software Testing (highlights)
author:: [[]]
full-title:: "Pragmatic Software Testing"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- Introduction
		- -
		- but in reality, most of our work as test professionals is constrained by time (and often money) too. For this reason, I suggest time constraints for each exercise #ñspace
		- -
	- 1. What Does It Mean to Be Pragmatic?
		- -
		- On most projects I’ve worked on, I’ve typically wanted to do the following: #ñspace
		- -
		- -
		- What does ‘effective' mean? #car
			- Webster’s dictionary defines the word effective as “producing a decided, decisive, or desired result; impressive.” So, to be an effective software tester, you must decide what results you desire from your testing efforts.
		- -
		- -
		- What does “efficient” mean? #car
			- Likewise, Webster’s defines efficient as “productive of the desired effect; especially to be productive without waste.” So, to be an efficient tester, you must allocate resources (time and money) appropriately.
		- -
		- -
		- What's not testing? #car
		  id:: 6340152e-1cd8-459a-a678-6b99e5aaed9b
			- Let’s start with what it’s not: Software testing is not about proving conclusively that the software is free from any defects, or even about discovering all the defects. Such a mission for a test team is truly impossible to achieve.
		- -
		- -
		- Boris Beizer identified five phases of a tester’s mental life: #car
		  id:: 6340152e-5e20-4bbb-8cb6-e899f2c561a8
			- Phase 0: There’s no difference between testing and debugging. Other than in support of debugging, testing has no purpose.Phase 1: The purpose of testing is to show that the software works.Phase 2: The purpose of testing is to show that the software doesn’t work.Phase 3: The purpose of testing is not to prove anything, but to reduce the perceived risk of the software not working to an acceptable value.Phase 4: Testing is not an act. It is a mental discipline that results in low-risk software without much testing effort.
		- -
	- 3. Aligning Testing with the Project
		- -
		- Phases of testing: #car
			- The first phase or level is often called unit, component, or subsystem test. Here, you test portions of the system as they are created, looking for bugs in the individual pieces of the system under test before these pieces are integrated.In the second phase or level of testing, often called integration (and less frequently, string) test, you test collections of interoperating or communicating units, subsystems, or components, looking for bugs in the relationships and interfaces between pairs and groups of these pieces of the system under test as the pieces come together.In the third phase or level of testing, often called system test, you test the entire system, looking for bugs in the overall and particular behaviors, functions, and responses of the system under test as a whole.In the fourth phase or level of testing, often called acceptance or pilot test, you generally are no longer looking for bugs. Rather, the objective is to demonstrate that the product is ready for deployment or release.
		- -
		- -
		- About V-Model estimations. #car
		  id:: 6340152e-277d-44a1-afb2-cd23282919ad
			- While this model is intuitive and in many cases familiar to testers, developers, and managers, it has some weak spots. For one, it is usually schedule- and budget-driven. That is, when plans are flawed and money runs out, it’s usually testing that is cut back, since most of the testing happens at the end. For large projects, the chances of perfect planning 6, 12, or even 18 months or longer in advance are very low. That said, this model beats chaos.
		- -
	- 4. Understanding Test Strategies, Tactics, and Design
		- -
		- Definition of Regression: #car
		  id:: 6340152e-f2c3-4a4a-a7d3-f5b62e47c1ae
			- Regression is the misbehavior of a previously correct function, attribute, or feature. The word is also used to mean the discovery of a previously undiscovered bug while running a previously run test. Regression is generally associated with some change to the system, such as adding a feature or fixing a bug.
		- -
	- 12. Use Cases, Live Data, and Decision Tables
		- -
		- What techniques should you combine with Equivalence Classes? #car
			- You can and should combine the use case and scenario technique with equivalence classes to make sure that every equivalence class is covered. You can also use boundary value analysis to create challenging tests.
		- -
		- -
		- Format of Decision Table #car
			- The table is read columnwise. The leftmost column specifies first the conditions, then the actions. The conditions listed are those that influence the behavior of the system for the particular transaction under consideration. The actions listed are those actions the system might carry out depending on the conditions when handling this transaction. Each subsequent column to the right indicates, under the specified combination of conditions, which specified actions should and shouldn’t take place.The dashes (-) indicate conditions that aren’t reached as part of this rule.
		- -
	- 14. State Transition Diagrams
		- -
		- Sobre tablas de estado #car
			- State TablesA problem with using state transition diagrams is that they don’t show all possible combinations of states and events. Consider an e-commerce system. Unless the programmer takes steps to avoid it, the user can trigger both legal and illegal events by clicking buttons on the screen.
		- -