title:: Real-World Software Development (highlights)
deck:: [[O'Reilly-Learning::Real-World Software Development]]
author:: [[]]
full-title:: "Real-World Software Development"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 2. The Bank Statements Analyzer
		- -
			- Describe the SRP Principle #flashcard
				- The Single Responsibility Principle (SRP) is a general software development guideline to follow that contributes to writing code that is easier to manage and maintain.
				  
				  You can think about SRP in two complementary ways:
				  
				  
				  
				  A class has responsibility over a single functionality
				  
				  
				  There is only one single reason for a class to change1
				  
				  
				  
				  The SRP is usually applied to classes and methods. SRP is concerned with one particular behavior, concept, or category.
				  It leads to code that is more robust because there is one specific reason why it should change rather than multiple concerns.
				  The reason why multiple concerns is problematic is, as you saw earlier, it complicates code maintainability by potentially introducing bugs in several places. It can also make the code harder to understand and change.
		- -
		- -
			- Talk about the Principle of Least Surprise #flashcard
			  id:: 2d8111a6-08c6-4dc3-9a36-d4d71b3859d2
				- It is a good habit to follow the principle of least surprise when you implement methods. It will help ensure that it is obvious what is happening when looking at the code. This means:
				  
				  
				  
				  Use self-documenting method names so it is immediately obvious what they do (e.g., calculateTotalAmount())
				  
				  
				  Do not change the state of parameters as other parts of code may depend on it
				  
				  
				  
				  The principle of least surprise can be a subjective concept, though. When in doubt, speak to your colleagues and team members to ensure everyone is aligned.
		- -
		- -
			- An old bad practice of mine… #flashcard
				- Ultimately your goal is to manage the complexity of the application you are building. However, if you keep on copy pasting the same code as new requirements come in, you will end up with the following issues, which are called anti-patterns because they are common ineffective solutions:
				  
				  Hard to understand code because you have one giant “God Class”
				  
				  Code that is brittle and easily broken by changes because of code duplication
		- -
		- -
			- Don’t overuse KISS #flashcard
				- it is good to keep things simple when possible, but do not abuse the KISS principle. Instead, you need to reflect on the design of your whole application and have an understanding of how to break down the problem into separate sub-problems that are easier to manage individually. The result is that you will have code that is easier to understand, maintain, and adapt to new requirements.
		- -
		- -
			- Suggested structure of tests #flashcard
			  id:: da717da6-bc7a-468a-a254-54afa5fe5f5d
				- There are three parts:
				  
				  You set up the context for your test. In this case a line to parse.
				  
				  You carry out an action. In this case, you parse the input line.
				  
				  You specify assertions of the expected output. Here, you check that the date, amount, and description were parsed correctly.
				  
				  This three-stage pattern for setting up a unit test is often referred to as the Given-When-Then formula. It is a good idea to follow the pattern and split up the different parts because it helps to clearly understand what the test is actually doing.
		- -
		- -
			- Takeaways
			  God Classes and code duplication lead to code that is hard to reason about and maintain.
			  
			  The Single Responsibility Principle helps you write code that is easier to manage and maintain.
			  
			  Cohesion is concerned with how how strongly related the responsibilities of a class or method are.
			  
			  Coupling is concerned with how dependent a class is on other parts of your code.
			  
			  High cohesion and low coupling are characteristics of maintainable code.
			  
			  A suite of automated tests increases confidence that your software is correct, makes it more robust for changes, and helps program comprehension.
			  
			  JUnit is a Java testing framework that lets you specify unit tests that verify the behavior of your methods and classes.
			  
			  Given-When-Then is a pattern for setting up a test into three parts to help understand the tests you implement. #flashcard
		- -
		- -
			- Will this break my tuning? #flashcard
			  id:: 8cf0edee-985f-43a2-94c7-eda7afb9d42c
				- Code Coverage
		- -
	- 3. Extending the Bank Statements Analyzer
		- -
			- __Open/Closed Principle #flashcard
				- This is where the Open/Closed principle comes in. It promotes the idea of being able to change the behavior of a method or class without having to modify the code. In our example, it would mean the ability to extend the behavior of a findTransactions() method without having to duplicate the code or change it to introduce a new parameter. How is this possible? As discussed earlier, the concepts of iterating and the business logic are coupled together. In the previous chapter, you learned about interfaces as a useful tool to decouple concepts from one another. In this case, you will introduce a BankTransactionFilter interface that will be responsible for the selection logic, as shown in Example 3-4. It contains a single method test() that returns a boolean and takes the complete BankTransaction object as an argument. This way the method test() has access to all the properties of a BankTransaction to specify any appropriate selection criteria.
		- -
		- -
			- A functional interface code's example in Java #flashcard
			  id:: 9af3ae86-cee5-4d95-abaf-7681fc17ac4d
				- @FunctionalInterface
				  public interface BankTransactionFilter {
				    boolean test(BankTransaction bankTransaction);
				  }
		- -
		- -
			- OCP applied to a solution #flashcard
				- This refactoring is very important because you now have introduced a way to decouple the iteration logic from the business logic through this interface. Your method no longer depends on one specific implementation of a filter. You can introduce new implementations by passing them as an argument without modifying the body of this method. Hence, it is now open for extension and closed for modification. This reduces the scope for introducing new bugs because it minimizes cascading changes required to parts of code that have already been implemented and tested. In other words, old code still works and is untouched.
		- -
		- -
			- Example of class implementing an interface for OCP in Java #flashcard
				- class BankTransactionIsInFebruaryAndExpensive implements BankTransactionFilter {
				  
				    @Override
				    public boolean test(final BankTransaction bankTransaction) {
				        return bankTransaction.getDate().getMonth() == Month.FEBRUARY
				               &amp;&amp; bankTransaction.getAmount() &gt;= 1_000);
				    }
				  }
				  Example 3-7. Calling findTransactions() with a specific implementation of BankTransactionFilter
				  final List transactions
				    = bankStatementProcessor.findTransactions(new BankTransactionIsInFebruaryAndExpensive());
		- -
		- -
			- Same code but using Lambda. Much better than the previous!!! #flashcard
				- Example 3-8. Implementing BankTransactionFilter using a lambda expression
				  final List transactions
				    = bankStatementProcessor.findTransactions(bankTransaction -&gt;
				                bankTransaction.getDate().getMonth() == Month.FEBRUARY
				                &amp;&amp; bankTransaction.getAmount() &gt;= 1_000);
		- -
		- -
			- Benefits of OCP #flashcard
			  id:: 44eef8cb-d568-44c3-953d-63be75b80ba3
				- To summarize, the Open/Closed Principle is a useful principle to follow because it:
				  
				  Reduces fragility of code by not changing existing code
				  
				  Promotes reusability of existing code and as a result avoids code duplication
				  
				  Promotes decoupling, which leads to better code maintenance
		- -
		- -
			- All these reasons are why it is generally recommended to define smaller interfaces. The idea is to minimize dependency to multiple operations or internals of a domain object. #flashcard
		- -
		- -
			- In fact, there are two sides of the coin to consider. On one side a method like findTransactionsGreaterThanEqual() is self-explanatory and easy to use. You should not be worried about adding descriptive method names to help readability and comprehension of your API. However, this method is restricted to a particular case and you can easily have an explosion of new methods to cater for various multiple requirements. On the other side, a method like findTransactions() is initially more difficult to use and it needs to be well-documented. However, it provides a unified API for all cases where you need to look up transactions. There isn’t a rule of what is best; it depends on what kind of queries you expect. If findTransactionsGreaterThanEqual() is a very common operation, it makes sense to extract it into an explicit API to make it easier for users to understand and use. #flashcard
			  id:: 7ad1f111-3c0f-4121-af62-4088f835f537
		- -
		- -
			- Domain Class or Primitive Value?
			  While we kept the interface definition of BankTransactionSummarizer simple, it is often preferable to not return a primitive value like a double if you are looking at returning a result from an aggregation. This is because it doesn’t give you the flexibility to later return multiple results. For example, the method summarizeTransaction() returns a double. If you were to change the signature of the result to include more results, you would need to change every single implementation of the BankTransactionProcessor.
			  
			  A solution to this problem is to introduce a new domain class such as Summary that wraps the double value. This means that in the future you can add other fields and results to this class. This technique helps further decouple the various concepts in your domain and also helps minimize cascading changes when requirements change. #flashcard
		- -
		- -
			- About code ready for test #flashcard
				- Returning void makes it very hard to test the result with assertions. What is the actual result to compare with the expected result? Unfortunately, you can’t get a result with void.
		- -
		- -
			- About illegal values VS exceptions #flashcard
			  id:: 632ba075-d295-4dee-854a-8f60eb6d920a
				- Back in the frightening days of the C programming language, you would add a lot of if-condition checks that would return a cryptic error code. This approach had several drawbacks. First, it relied on global shared mutable state to look up the most recent error. This made it harder to understand individual parts of your code in isolation. As a result, your code became harder to maintain. Second, this approach was error prone as you needed to distinguish between real values and errors encoded as values. The type system in this case was weak and could be more helpful to the programmer. Finally, the control flow was mixed with the business logic, which contributed to making the code harder to maintain and test in isolation.
		- -
		- -
			- ou may be familiar with the fact that Java distinguishes between two kinds of exceptions:
			  
			  Checked exceptions
			  These are errors that you are expected to be able to recover from. In Java, you have to declare a method with a list of checked exceptions it can throw. If not, you have to provide a suitable try/catch block for that particular exception.
			  
			  Unchecked exceptions
			  These are errors that can be thrown at any time during the program execution. Methods don’t have to explicitly declare these exceptions in their signature and the caller doesn’t have to handle them explicitly, as it would with a checked exception. #flashcard
		- -
		- -
			- In a nutshell, the recommendation is to use unchecked exceptions and only use checked exceptions sparingly to avoid significant clutter in the code. #flashcard
		- -
		- -
			- we recommend creating a dedicated Validator class for several reasons:
			  
			  You don’t have to duplicate the validation logic when you need to reuse it.
			  
			  You get confidence that different parts of your system validate the same way.
			  
			  You can easily unit test this logic separately.
			  
			  It follows the SRP, which leads to simpler maintenance and program comprehension. #flashcard
		- -
		- -
			- Notification Pattern
			  The Notification pattern aims to provide a solution for the situation in which you are using too many unchecked exceptions. The solution is to introduce a domain class to collect errors.1
			  
			  The first thing you need is a Notification class whose responsibility is to collect errors. The code in Example&nbsp;3-20 shows its declaration.
			  
			  Example 3-20. Introducing the domain class Notification to collect errors
			  public class Notification {
			    private final List errors = new ArrayList&lt;&gt;();
			  
			    public void addError(final String message) {
			        errors.add(message);
			    }
			  
			    public boolean hasErrors() {
			        return !errors.isEmpty();
			    }
			  
			    public String errorMessage() {
			        return errors.toString();
			    }
			  
			    public List getErrors() {
			        return this.errors;
			    }
			  
			  } #flashcard
		- -
		- -
			- Example 3-21. Notification pattern
			  id:: 2a5a2338-af34-4f64-b06f-71bac868f02f
			  public Notification validate() {
			  
			    final Notification notification = new Notification();
			    if(this.description.length() > 100) {
			        notification.addError("The description is too long");
			    }
			  
			    final LocalDate parsedDate;
			    try {
			        parsedDate = LocalDate.parse(this.date);
			        if (parsedDate.isAfter(LocalDate.now())) {
			            notification.addError("date cannot be in the future");
			        }
			    }
			    catch (DateTimeParseException e) {
			        notification.addError("Invalid format for date");
			    }
			  
			    final double amount;
			    try {
			        amount = Double.parseDouble(this.amount);
			    }
			    catch (NumberFormatException e) {
			        notification.addError("Invalid format for amount");
			    }
			    return notification;
			  } #flashcard
		- -
		- -
			- A build tool has many benefits:
			  
			  It provides you with a common structure to think about a project so your colleagues feel immediately at home with the project.
			  
			  It sets you up with a repeatable and standardized process to build and run an application.
			  
			  You spend more time on development, and less time on low-level configurations and setup.
			  
			  You are reducing the scope for introducing errors due to bad configurations or missing steps in the build.
			  
			  You save time by reusing common build tasks instead of reimplementing them. #flashcard
		- -
		- -
			- Takeaways
			  id:: 9b06733d-b447-4986-a4a2-85af9a53cc36
			  The Open/Closed Principle promotes the idea of being able to change the behavior of a method or class without having to modify the code.
			  
			  The Open/Closed Principle reduces fragility of code by not changing existing code, promotes reusability of existing code, and promotes decoupling, which leads to better code maintenance.
			  
			  God interfaces with many specific methods introduce complexity and coupling.
			  
			  An interface that is too granular with single methods can introduce the opposite of cohesion.
			  
			  You should not be worried about adding descriptive method names to help readability and comprehension of your API .
			  
			  Returning void as a result of an operation makes it difficult to test its behavior.
			  
			  Exceptions in Java contribute to documentation, type safety, and separation of concerns.
			  
			  Use checked exceptions sparingly rather than the default as they can cause significant clutter.
			  
			  Overly specific exceptions can make software development unproductive.
			  
			  The Notification Pattern introduces a domain class to collect errors.
			  
			  Do not ignore an exception or catch the generic Exception as you will lose the benefits of diagnosing the root of the problem.
			  
			  A build tool automates the repetitive tasks in the software development life cycle including building, testing, and deploying your application.
			  
			  Maven and Gradle are two popular build tools used in the Java community. #flashcard
		- -
	- 4. The Document Management System
		- -
			- __switch #flashcard
			  id:: f71d8ce6-1ff8-464a-aefe-cde9b67271bc
				- This approach would have solved the problem in question but would be hard to extend. Every time you want to add another type of file that gets processed you would need to implement another entry in the switch statement. Over time this method would become intractably long and hard to read.
		- -
		- -
			- About public constructors #flashcard
				- One final thing to note about Document is that it has a package-scoped constructor. Often Java classes make their constructor public, but this can be a bad choice as it allows code anywhere in your project to create objects of that type. Only code in the Document Management System should be able to create Documents, so we keep the constructor package scoped and restrict access to only the package that the Document Management System lives in.
		- -
		- -
			- Example 4-5. How to define a constant in Java
			  id:: 84aad341-1183-4b36-9fab-e63d70065184
			  public static final String PATH = "path"; #flashcard
		- -
		- -
			- But really there’s a broader principle at stake here, one that allows us to generalize these examples into an approach that you can use in any piece of software. This is called the Liskov Substitution Principle (LSP) and it helps us understand how to subclass and implement interfaces correctly. LSP forms the L of the SOLID principles that we’ve been referring to throughout this book.
			  
			  The Liskov Substitution Principle is often stated in these very formal terms, but is actually a very simple concept. Let’s demystify some of this terminology. If you hear type in this context, just think of a class or an interface. The term subtype means establish a parent-to-child relationship between types; in other words, extend a class or implement an interface. So informally you can think of this as meaning that child classes should maintain the behavior they inherit from their parents. We know, we know—it sounds like an obvious statement, but we can be more specific and split out LSP into four distinct parts: #flashcard
		- -
		- -
			- Formal definition of LSP #flashcard
				- LSP
				  Let q(x) be a property provable about objects x of type T. Then q(y) should be true for objects y of type S where S is a subtype of T.
		- -
		- -
			- Preconditions cannot be strengthened in a subtype #flashcard
				- LSP means that you can’t require any more restrictive preconditions than your parent required. So, for example, you can’t require your document to be smaller than 100KB in size if your parent should be able to import any size of document.
		- -
		- -
			- Postconditions cannot be weakened in a subtype #flashcard
			  id:: 51c0262d-c27a-488b-9932-7bf56ac8f7ea
				- This might sound a bit confusing because it reads a lot like the first rule. Postconditions are things that have to be true after some code has run. For example, after importFile() has run, if the file in question is valid it must be in the list of documents returned by contents(). So if the parent has some kind of side effect or returns some value, then the child must do so as well.
		- -
		- -
			- The History Rule
			  This is the hardest aspect of LSP to understand. In essence, the child class shouldn’t allow state changes that your parent disallowed. So, in our example program we have an immutable Document class. In other words, once it has been instantiated you can’t remove, add, or alter any of the attributes. You shouldn’t subclass this Document class and create a mutable Document class. This is because any user of the parent class would expect certain behavior in response to calling methods on the Document class. If the child were mutable, it could violate callers’ expectations about what calling those methods does. #flashcard
		- -
		- -
			- About test function names #flashcard
			  id:: a4193c43-d2e9-46ed-acac-85287169da5e
				- The key driving principles when it comes to test naming are readability, maintainability, and acting as executable documentation. When you see a report of a test class being run, the names should act as statements that document what functionality works and what does not.
		- -
		- -
			- Don't overuse the white-box tests!!!
			  Specification, NOT Behaviour!!! #flashcard
				- Our tests should only invoke these public API methods and not try to inspect the internal state of the objects or the design. This is one of the key mistakes made by developers that leads to hard-to-maintain tests. Relying on specific implementation details results in brittle tests because if you change the implementation detail in question, the test can start to fail even if the behavior is still working.
		- -
		- -
			- DRY in unit tests #flashcard
			  id:: e31b8569-5720-4b1b-a684-5dac7330f80a
				- Example 4-20. Implementing a new assertion
				    private void assertAttributeEquals(
				        final Document document,
				        final String attributeName,
				        final String expectedValue)
				    {
				        assertEquals(
				            "Document has the wrong value for " + attributeName,
				            expectedValue,
				            document.getAttribute(attributeName));
				    }
		- -
		- -
			- Do a little research about hamcrest #flashcard
			  id:: ac127fd1-d650-4235-9110-c8c33378f71f
				- These matchers come from the Hamcrest library, which is a very commonly used Java library that enables cleaner testing.
		- -
		- -
			- Example of Test expecting an Exception #flashcard
				- @Test(expected = UnknownFileTypeException.class)
				    public void shouldNotImportUnknownFile() throws Exception
				    {
				        system.importFile(RESOURCES + "unknown.txt");
				    }
		- -
	- 5. The Business Rules Engine
		- -
			- Why should you take this approach? There are several benefits:
			  
			  Writing a test at a time will help you focus and refine the requirements by correctly implementing one thing at a time.
			  
			  It’s a way to ensure a relevant organization for your code. For example, by writing a test first, you need to think hard about the public interfaces for your code.
			  
			  You are building a comprehensive test suite as you iterate through the requirements, which increases confidence that you are matching the requirements and also reduces the scope of bugs.
			  
			  You don’t write code that you don’t need (over-engineer) because you’re just writing code that passes the tests. #flashcard
		- -
		- -
			- You’ll be using Mockito, which is a popular mocking library for Java. At its simplest you can do two things:
			  
			  Create a mock.
			  
			  Verify that a method is called.
			  
			  So how do you get started? You will need to import the library first:
			  
			  import static org.mockito.Mockito.*;
			  This import allows you to use the methods mock() and verify(). The static method mock() allows you to create a mock object which you can then verify that certain behaviors happen. The method verify() allows you to set up assertions that a particular method is invoked. #flashcard
		- -
		- -
			- Example 5-5. Mocking and verifying interaction with an Action object
			  @Test
			  void shouldExecuteOneAction() {
			        final BusinessRuleEngine businessRuleEngine = new BusinessRuleEngine();
			        final Action mockAction = mock(Action.class);
			  
			        businessRuleEngine.addAction(mockAction);
			        businessRuleEngine.run();
			  
			        verify(mockAction).perform();
			  } #flashcard
		- -
		- -
			- Example 5-20. Switch expression with no fall-through behavior
			  id:: ef302031-279e-46c6-abab-aecf34555c01
			  var forecastedAmount = amount * switch (dealStage) {
			    case LEAD -> 0.2;
			    case EVALUATING -> 0.5;
			    case INTERESTED -> 0.8;
			    case CLOSED -> 1;
			  } #flashcard
		- -
		- -
			- ISP (Cohesion between Interfaces and clients) #flashcard
				- Interface Segregation Principle. It makes the case that no class should be forced to depend on methods it does not use because this introduces unnecessary coupling. In Chapter 2, you learned about another principle, the Single Responsibility Principle (SRP), which promotes high cohesion. The SRP is a general design guideline that a class has responsibility over a single functionality and there should be only one reason for it to change. Although the ISP may sound like the same idea, it takes a different view. The ISP focuses on the user of an interface rather than its design. In other words, if an interface ends up very large, it may be that the user of that interface sees some behaviors it doesn’t care for, which causes unnecessary coupling.
		- -
	- 7. Extending Twootr
		- -
			- What does the Dependency Inversion principle mean? #flashcard
				- It states that:
				  
				  High-level modules should not depend upon low-level modules. Both should depend upon abstractions.
				  
				  Abstractions should not depend upon details. Details should depend upon abstractions.
				  
				  The principle is called an inversion because in traditional imperative, structured programming it is often the case that high-level modules compose down to produce low-level modules. It’s often a side effect of the top-down design that we talked about in this chapter. You split up a big problem into different subproblems, write a module to solve each of those subproblems, and then the main problem (the high-level module) depends on the subproblems (the low-level modules).
		- -