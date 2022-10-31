title:: OCP Oracle Certified Professional Java SE 11 Programmer I Exam Fundamentals 1z0-815 (highlights)
deck:: [[Other-Books::OCP Oracle Certified Professional Java SE 11 Programmer I Exam Fundamentals 1z0-815]]
author:: [[Hanumant Deshmukh]]
full-title:: "OCP Oracle Certified Professional Java SE 11 Programmer I Exam Fundamentals 1z0-815"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/51hydbMukbL._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- I will recommend you to buy the exam simulator created by this team from our website Enthuware.com. It is priced quite reasonably (only 9.99 USD) and has stood the test of time. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 266](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=266))
	- -
	- -
		- Instead of presenting MCQs or quizzes at the end of a topic or chapter, I ask you to write code that uses the concepts taught in that topic or chapter. #flashcard
		- ([Location 297](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=297))
	- -
	- -
		- I strongly suggest you use Enthuware's exam simulator to get familiar with this style. It closely mimics the user interface of the real exam. #flashcard
		- ([Location 306](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=306))
	- -
	- -
		- API stands for Application Programming Interface #flashcard
		- ([Location 447](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=447))
	- -
	- -
		- The key point about an interface is that you cannot have an instance of an interface #flashcard
		- ([Location 488](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=488))
	- -
	- -
		- For example, you cannot really have just a Movable. #flashcard
		- ([Location 489](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=489))
	- -
	- -
		- In that sense, an interface is always abstract. It cannot exist on its own. You need a class to implement the behavior described by an interface. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 490](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=490))
	- -
	- -
		- An abstract class lies somewhere in between a class and an interface. Just like a class, it defines behavior as well as implementation but the implementation that it provides is not complete enough for you to create instances of it. Therefore, just like an interface, it cannot exist on its own. #flashcard
		  id:: 68160e67-4ff2-45c3-a534-1d335f7ef1f0
		- tags:: [[blue]] [[azul]]
		- ([Location 492](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=492))
	- -
	- -
		- C++ has pointer arithmetic, global functions, operator overloading, extern declarations, preprocessor directives, unsigned data types, and so many other "features" that Java simply does not have. These are some really powerful tools in the hands of a C++ programmer. So, why doesn't Java have them? Java has actually gone in reverse with respect to features. Java does not have a lot of features that are found in languages that came before Java. The reason is simple. Java follows the philosophy of making life simpler for the programmer. Having more and more features is not necessarily a good thing. #flashcard
		  id:: 8faf8d52-6ca4-4836-80f6-ca2e62819d65
		- ([Location 522](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=522))
	- -
	- -
		- since Java 8, interfaces contain method declarations as well as definitions. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 588](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=588))
	- -
	- -
		- String str = 0; //will not compile int n = null; //will not compile. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 655](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=655))
	- -
	- -
		- It should now be clear that a program needs two kinds of memory spaces to keep the stuff. One for temporary stuff that can be cleaned up as soon as a method call ends and one for permanent stuff that remains in use for longer than a single method call. The space for storing the temporary stuff is called Stack space and the space for storing all other stuff is called Heap space #flashcard
		  id:: 45d7366b-2f40-4b7f-a74d-b2646fecbe65
		- tags:: [[blue]] [[azul]]
		- ([Location 706](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=706))
	- -
	- -
		- When a thread dies, its stack space is reverted back to the JVM. Since this space behaves like a stack, it is called stack space #flashcard
		  id:: f74fb96f-5733-43a7-8e53-a8bc8aec2708
		- tags:: [[blue]] [[azul]]
		- ([Location 732](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=732))
	- -
	- -
		- Local variables are always kept on the stack. Objects are always stored in the heap. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 750](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=750))
	- -
	- -
		- JVM may have several threads. Each thread is given a fixed amount of stack space that is dedicated completely and exclusively to that thread. No one but that thread can access its stack space. This is called "stack semantics".  A thread accesses its stack space by creating and using variables. There is no other special way of accessing the stack space. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 752](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=752))
	- -
	- -
		- Heap space is shared among all threads. Any thread can use space on a heap by creating objects. Since heap space is shared, it is possible for one thread to access objects created by another if it has a reference to that object. This is called "heap semantics". #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 755](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=755))
	- -
	- -
		- Stack space is limited for a program. So, if you have a huge chain of method calls where each method creates a lot of temporary variables (recursion is a good example), it is possible to run out of stack space. In Java, the default stack space size is 64KB but it can be changed at the time of executing the program using command line option -Xss. Heap space is unlimited from the program's perspective. It is limited only by the amount of space available on your machine. #flashcard
		  id:: 90b1a8a9-8c02-4411-adcf-3f88f87698ac
		- tags:: [[pink]] [[rosa]]
		- ([Location 756](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=756))
	- -
	- -
		- Only temporary variables, i.e., variables created in a method (also known as local variables and automatic variables) are created on the stack space. Everything else is created on the heap space. If you have any doubt, ask yourself this question - is this a temporary variable created in a method? #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 760](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=760))
	- -
	- -
		- When a method is invoked by a thread, it uses the thread's stack space to keep its temporary variables. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 763](https://readwise.io/to_kindle?action=open&asin=B07VWMD2LB&location=763))
	- -