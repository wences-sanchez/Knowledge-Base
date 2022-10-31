title:: Java Projects (highlights)
deck:: [[O'Reilly-Learning::Java Projects]]
author:: [[]]
full-title:: "Java Projects"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Integration tests
		- -
			- Integration tests
			  id:: a9ec1f24-fd40-44bd-917b-50e409b748d4
			                
			            
			            
			                
			  Integration tests are very similar to unit tests, and in most cases, novice programmers claim that they perform unit testing when they actually perform integration testing.
			  Integration tests drive the code but do not test the individual classes (units) in isolation, mocking everything that the class may use. Rather, they test the functionality of most of the classes that are needed to perform a test. This way, the integration test does test that the classes are able to work together and not only satisfy their own specifications but also ensure that these specifications work together.
			  In the integration test, the external world (like external services) and access to the database are mocked. That is because the integration tests are supposed to run on integration servers, in the same environment where the unit tests are executed, and there, these external interfaces may not be available. In most cases, databases are mocked using in-memory SQL, and external services are mocked using some mock classes. #flashcard
		- -
		- -
			- Spring provides a nice environment to execute such integration tests #flashcard
			  id:: 208653c7-355d-4d25-aa60-8f42b3d8a098
		- -
	- Getting started with Java
		- -
			- the basic operation of JVM is almost as important as the language itself. Java is a compiled and interpreted language. It is a special beast that forges the best of both worlds. Before Java, there were interpreted and compiled languages. #flashcard
			  id:: 54f5126c-3379-422f-a9ef-a9bb15f16fc2
		- -
	- Executing jshell
		- -
			- To compile the source code to bytecode, which is executable by JVM, we have to use the Java compiler named javac:
			  id:: 635faa2f-8675-49a9-b935-6ebef77aedf4
			  
			  javac HelloWorld.java
			  This generates the java.class file in the current directory. This is a compiled code that can be executed as follows:
			  
			  $ java HelloWorld
			  Hello World #flashcard
		- -