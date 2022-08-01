- ## Week 1
	- ### Lesson 1: Introduction to Testing
		- **Verification** VS **Validation** #spaced
			- **Validation** is when we make sure that the actual product against the expected result from the user's perspective. It's a dynamic testing. It answers the question:
				- > Are we building the right product?
			- **Verification** is when we check that the software is free from bugs, technically speaking. Upon our internal requirements. It answers the question:
				- > Are we building the product right?
		- According to **Turing's halting problem**, it is theoretically not possible at all to check a perfect verification of one program by having another one checking it. #Curiosities
		- ![image.png](../assets/image_1659351422358_0.png)
	- ### Lesson 2: Why and How we Test
		- Types of tests: #spaced
			- **Unit tests:** testing individual classes / functions
			- **Integration tests:** testing packages / subsystems
			- **System tests:** testing the entire system
		- Even with **TDD**, there is *re-test* when you modify your code.
		- The function f(x) of a program is not continuous, so we can't derive its output (unlike other engineering fields) to test it. #Curiosities
		- *Optimistic* VS *Pessimistic* **testing** #flaschard
			- Optimistic means that the system gives you a lot of outputs. An
				- > They say your program is right, when in fact it may be wrong in some cases.
			- Pessimistic means that the system gives you a lot of false negatives that you (the human) have to discard.
				- > They'll say your program is wrong when in fact your program may be right.
				-
		-
		- #### Questions
			- ##### Pregunta 3
			- Is testing a (primarily) optimistic or pessimistic verification technique?
			  
			  [ ] Optimistic
			  [ ] Pessimistic
			  #flaschard
				- [X] Optimistic
				  For the most part, testing is 'optimistic,' meaning that it will state that your program is correct when in fact it is incorrect for certain inputs.  Testing can be pessimistic, but only if the tests are incorrectly specified. If a tester incorrectly states the outcome of the test, then that test may incorrectly flag a program as misbehaving.
		-
		-