# Test-Driven Python Development

deck:: [[O'Reilly-Learning::Test-Driven Python Development]]\
author:: [[None]]\
full-title:: "Test-Driven Python Development"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/test-driven-python-development/9781783987924/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Understanding test-driven development
- id:: 63c66a26-1f51-4c9f-9cec-3f40f51dbbda
   Why unit tests? #flashcard 
    At this point, a valid question would be to ask why we need unit testing at all. Why not write only integration tests, where a single test could check so many parts of the application at once? The reason is that integration tests do not pinpoint the location of failure. A failing integration test could have an error in the UI, or in the logic, or somewhere in the way data is read or written. It will take a lot of investigation to see where the error is and fix it.
-
- id:: 63c66a26-f808-4132-993c-5bc759d2ff01
   Rhythm of TDD #flashcard 
    Developers who are familiar with TDD usually go through this cycle many times an hour, implementing small steps of functionality each time.
-
- id:: 63c66a26-f10e-4088-9cfa-6fff8022c5a4
  
  As we can see, unit testing is a general term, whereas developer testing is a specific subset of unit testing, and TDD is a specific form of developer testing. #flashcard
-
- id:: 63c66a26-c65c-4ab8-8c1f-947a93859043
   About TDD philosophy. #flashcard 
    the main focus of TDD is not really about testing. The simple act of writing a test before the implementation changes the way we think when we implement the corresponding functionality. The resulting code is more testable, usually has a simple and elegant design, and is more maintainable and readable.
-
- id:: 63c66a26-3870-421c-b8e8-35285e2e9e09
   What is TDD about. #flashcard 
    NOTE
     TDD is about writing better, cleaner, more maintainable code, and only incidentally about testing.
-
- id:: 63c66a26-77f8-42ba-90b8-e1765c0bc50a
  
  Thus, one can say that TDD is all about writing better code, and it is just a happy side effect that we end up with a fully automated test suite as an outcome. #flashcard
-
### Using TDD to build a stock alert application
- id:: 63c66a26-690e-4053-9452-7b6897654705
  
  The unittest framework will pick up any method that starts with test #flashcard
-
- id:: 63c66a26-8f13-40af-85fa-01663dd5e850
  
  Rather than coming up with a very comprehensive list of functionality, we're going to focus on tiny bits of functionality, one at a time. #flashcard
-
- id:: 63c66a26-2b58-487f-bc75-87e21e498b87
   Failure VS Error #flashcard 
    There are two reasons why a test might not pass: It might have failed or it might have caused an error. There is a small difference between these two. A failure indicates that we expected some outcome (usually via an assert), but got something else. For example, in our test, we are asserting that stock.price is None. Suppose stock.price has some other value apart from None, then the test will fail.
     An error indicates that something unexpected happened, usually an unexpected exception was raised. In our previous example, we got an error because the Stock class has not yet been defined.
-
- id:: 63c66a26-922e-48f5-a3e4-e5a6f382b4a4
   What does '__name__' mean in Python??? #flashcard 
    The last segment checks if the module was executed directly from the command line. In such a case, the __name__ variable will have the value __main__
-
### Reorganizing the test code
- id:: 63c66a26-1618-4a5e-a186-389b7444686c
   Why is '__main__' used in Python??? #flashcard 
    The reason we need to wrap this function call inside the conditional is because this part does not get executed if the module is imported into another file.
-
- id:: 63c66a26-3d2e-42ca-be4b-1f8438ba53ed
  
  from ..stock import Stock #flashcard
-
- id:: 63c66a26-4855-45f1-bfd1-7e0771eda787
  
  Including a call to unittest.main() works well with individual scripts since it allows us to run the tests by simply executing the file. However, it is not a very scalable solution. If we have hundreds of files, we would like to run all the tests at once, and not have to execute each file individually. #flashcard
-
- id:: 63c66a26-f25e-4b6e-9564-9354aa750eec
  
  python3 -m unittest #flashcard
-
### 2. Red-Green-Refactor – The TDD Cycle
- id:: 63c66a26-8390-4a77-816d-9e3eef251506
  
  in TDD, tests are nothing but requirements. Each time we write a test and implement code to make it pass, what we actually do is make the code meet some requirement. Looking at it another way, tests are just executable requirement specifications. #flashcard
-
### Arrange-Act-Assert
- id:: 63c66a26-7eef-4054-8a2e-2bd2822fa6fc
   Body of a test (without setup) #flashcard 
    This test follows the pattern of Arrange-Act-Assert.
     Arrange: Set up the context for the test. In this case, we create a Stock object. In other tests, it may involve creating multiple objects or hooking a few things together that will be required by the particular test.
     Act: Perform the action that we want to test. Here, we call the update method with the appropriate arguments.
     Assert: Finally we assert that the outcome was as expected.
-
### Testing for exceptions
- id:: 63c66a26-a6b8-4e85-98cf-2023cca2b66d
   Method to test an exception #flashcard 
    The assertRaises method takes the expected exception as the first argument, the function to call as the second argument, and the parameters to the function are passed as in the remaining arguments
-
- id:: 63c66a26-da4a-49d5-97ea-1c17173c4721
  
  with self.assertRaises(ValueError):
     goog.update(datetime(2014, 2, 13), -1) #flashcard
-
### Exploring assert methods
- id:: 63c66a26-fadc-42c7-8848-62bb326a0f66
  
  self.assertAlmostEqual(8.4, goog.price, delta=0.0001) #flashcard
-
- id:: 63c66a26-10ce-47ec-a50a-da179ad459f7
  
  self.assertAlmostEqual(8.4, goog.price, places=4) #flashcard
-
- id:: 63c66a26-d041-49b0-bb8c-62d377303ddc
   AssertEqual VS assertIs #flashcard 
    assertEqual versus assertIs: These two sets of assertions are very similar. The critical difference is that the former checks for equality while the latter assertion is used to check for object identity
-
### Specific asserts versus generic asserts
- id:: 63c66a26-03fe-4e62-8dab-973f4b7e768c
   Specific asserts VS broader asserts #flashcard 
    one motivation for using a specific assert is that you get a better error message if the assertion fails. When comparing objects like lists and dicts, the error message will show exactly where the difference occurs, making it much easier to understand. Therefore, it is recommended to use the more specific asserts wherever possible.
-
### Setup and teardown
- id:: 63c66a26-f4a4-484f-8b28-d0374eaa49f5
   What’s the exact name of the function which prepares all? (Talking about tests cases) #flashcard 
    def setUp(self):
-
- id:: 63c66a26-f3bd-40b4-a7b5-fc580fdbb7dd
   When to use the setUpClass and setUpModule #flashcard 
    Class level and module level setups are only used when there is an expensive setup step, such as making a connection to a database or a remote server, and it is preferable to do this setup just once and share it between all the tests.
-
### Brittle tests
- id:: 63c66a26-0c80-459b-8065-b34d87296de3
  
  A test is brittle when a change in the implementation details requires a change in the test cases. Ideally, a test should be testing the interface and not the implementation directly. After all, it is the interface that other units will be using to interact with this unit. #flashcard
-
- id:: 63c66a26-64a9-4761-ad87-413b6a9589da
  
  Brittle tests can be worse than no tests, as the maintenance overhead of having to fix ten or twenty tests with every change in the implementation can turn developers away from TDD, increase the amount of frustration, and lead to teams disabling or skipping testing. #flashcard
-
- id:: 63c66a26-e61c-4442-9c0f-abc56a7aae24
  
  Here are some guidelines on how to think about test brittleness:
     If at all possible, avoid using implementation details in tests, and only use the publicly exposed interface. This includes using only the interface methods in setup code and assertions.
     If the test needs to check functionality that is internal to the unit being tested, and it is an important functionality, then it might make sense to check for specific implementation actions.
     If it is cumbersome to use the external interface to set up the exact state that we want, or there is no interface method that retrieves the specific value we want to assert, then we may need to peek into the implementation in our tests.
     If we are fairly confident that the implementation details are very unlikely to change in the future, then we might go ahead and use implementation-specific details in the test. #flashcard
-
### Refactoring the design
- id:: 63c66a26-d358-491c-bee6-d76ee4f6cb45
  
  When tests are passing, we can constantly run the tests to make sure we aren't breaking any functionality with our changes. When tests are failing, we do not have this safety net. It is inevitable that certain design changes, like the one we are making now, will temporarily make a number of tests fail until we finish the sequence of changes. We should try and minimize the time we spend making changes during failing tests, by making small changes at a time. This allows us to validate our changes as we go along. #flashcard
-
### Refactoring tests
- id:: 63c66a26-31d2-411c-9645-28c9fe772466
   About helper methods
   Lo que hacemos es usar una función auxiliar para encapsular la variable (en este caso list) que le pasamos al objeto en cuestión.
   En vez de crear una variable en la clase de test, se lo inyectamos el dato al objeto directamente (cada cual) que usas para el assert. A través de su interfaz (o contrato). #flashcard 
    Much better! Not only is the duplication removed, but the tests are a lot more readable. By default, the unittest module looks for methods that start with the word test and only executes those methods as tests, so there is no risk that our helper method will be mistaken for a test case.
-
### Exploring the Rule classes
- id:: 63c66a26-920e-41a2-9053-9499a5efc565
  
  The all function is a built-in function that takes a list and returns True only if every element of that list is True. #flashcard
-