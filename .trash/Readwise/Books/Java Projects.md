# Java Projects

deck:: [[O'Reilly-Learning::Java Projects]]\
author:: [[None]]\
full-title:: "Java Projects"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/java-projects-/9781789131895/ibis_generated_cover_thumbnail.jpg)

## Highlights
### Integration tests
- 

Integration tests
     Integration tests are very similar to unit tests, and in most cases, novice programmers claim that they perform unit testing when they actually perform integration testing.
     Integration tests drive the code but do not test the individual classes (units) in isolation, mocking everything that the class may use. Rather, they test the functionality of most of the classes that are needed to perform a test. This way, the integration test does test that the classes are able to work together and not only satisfy their own specifications but also ensure that these specifications work together.
     In the integration test, the external world (like external services) and access to the database are mocked. That is because the integration tests are supposed to run on integration servers, in the same environment where the unit tests are executed, and there, these external interfaces may not be available. In most cases, databases are mocked using in-memory SQL, and external services are mocked using some mock classes. #flashcard 


    
-
- 

Spring provides a nice environment to execute such integration tests #flashcard 


    
-
### Getting started with Java
- 

the basic operation of JVM is almost as important as the language itself. Java is a compiled and interpreted language. It is a special beast that forges the best of both worlds. Before Java, there were interpreted and compiled languages. #flashcard 


    
-
### Executing jshell
- 

To compile the source code to bytecode, which is executable by JVM, we have to use the Java compiler named javac:
     javac HelloWorld.java
     This generates the java.class file in the current directory. This is a compiled code that can be executed as follows:
     $ java HelloWorld
     Hello World #flashcard 


    
-
