# Java

deck:: [[Other-Books::Java]]\
author:: [[Herbert Schildt]]\
full-title:: "Java"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/51IpgznsrtL._SL200_.jpg)
## Highlights
- Although Java is otherwise completely object-oriented, the primitive types are not. They are analogous to the simple types found in most other non–object-oriented languages. The reason for this is efficiency. #flashcard  #pink #rosa 
  id:: 63cfbccf-f4ca-4e1e-8ac4-ba29a93ad4b3
  
  
    ([Location 2528](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2528))
-
- Java defines four integer types: byte, short, int, and long. All of these are signed, positive and negative values. #flashcard 
  id:: 63cfbccf-b4d9-43bc-836c-06e2760dafbe
  
  
    ([Location 2536](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2536))
-
- Java does not support unsigned, positive-only integers. #flashcard  #pink #rosa 
  id:: 63cfbccf-99ab-403a-a4c5-059fe100e32f
  
  
    ([Location 2537](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2537))
-
- The smallest integer type is byte. This is a signed 8-bit type that has a range from –128 to 127. #flashcard 
  id:: 63cfbccf-1f27-4cf1-9a5d-1e3cf79fb418
  
  
    ([Location 2546](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2546))
-
- id:: 63c66a0a-2bc4-4ddc-b8a0-6e498a610a2d
  
  The most commonly used integer type is int. It is a signed 32-bit type that has a range from –2,147,483,648 to 2,147,483,647. #flashcard 
  
  
    ([Location 2554](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2554))
-
- id:: 63c66a0a-9d1b-41d9-bc84-7e7021945dac
  
  Although you might think that using a byte or short would be more efficient than using an int in situations in which the larger range of an int is not needed, this may not be the case. The reason is that when byte and short values are used in an expression, they are promoted to int when the expression is evaluated. #flashcard 
  
  
    ([Location 2556](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2556))
-
- long is a signed 64-bit type and is useful for those occasions where an int type is not large enough #flashcard 
  id:: 63cfbccf-ddfb-447c-82a5-2921c2db0148
  
  
    ([Location 2561](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2561))
-
- Floating-point numbers, also known as real numbers, #flashcard 
  id:: 63cfbccf-c723-4b51-b786-e01feb42ee9b
  
  
    ([Location 2567](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2567))
-
- Variables of type float are useful when you need a fractional component, but don’t require a large degree of precision. For example, float can be useful when representing dollars and cents. #flashcard  #blue #azul 
  id:: 63cfbccf-83c3-47fb-88b6-c320a9b21c16
  
  
    ([Location 2575](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2575))
-
- However, to specify a long literal, you will need to explicitly tell the compiler that the literal value is of type long. You do this by appending an upper- or lowercase L to the literal. For example, 0x7ffffffffffffffL or 9223372036854775807L #flashcard 
  id:: 63cfbccf-ccaf-48fb-a391-052413b7c04e
  
  
    ([Location 2636](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2636))
-
- id:: 63c66a0a-b186-452b-a9ec-6085dfae299b
  
  in some other languages strings are implemented as arrays of characters. However, this is not the case in Java. Strings are actually object types. #flashcard  #pink #rosa 
  
  
    ([Location 2692](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2692))
-
- type identifier [ = value ][, identifier [= value ] …]; #flashcard  #orange #naranja 
  id:: 63cfbccf-f72a-427c-b6a0-1819c564fbb1
  
  
    ([Location 2698](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2698))
-
- It is not uncommon to think in terms of two general categories of scopes: global and local. However, these traditional scopes do not fit well with Java’s strict, object-oriented model. While it is possible to create what amounts to being a global scope, it is by far the exception, not the rule. In Java, the two major scopes are those defined by a class and those defined by a method. #flashcard  #blue #azul 
  id:: 63cfbccf-a52e-4403-9154-46e323c79b71
  
  
    ([Location 2719](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2719))
-
- id:: 63c66a0a-5b5f-456c-a901-d270b8140d1d
  
  the following fragment casts an int to a byte. If the integer’s value is larger than the range of a byte, it will be reduced modulo (the remainder of an integer division by the) byte’s range. #flashcard 
  
  
    ([Location 2778](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2778))
-
- Thus, when a floating-point value is assigned to an integer type, the fractional component is lost. For example, if the value 1.23 is assigned to an integer, the resulting value will simply be 1. The 0.23 will have been truncated. Of course, if the size of the whole number component is too large to fit into the target integer type, then that value will be reduced modulo the target type’s range. #flashcard 
  id:: 63cfbccf-8223-484c-bf3d-9f3ebb11595f
  
  
    ([Location 2782](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2782))
-
- Java defines several type promotion rules that apply to expressions. They are as follows: First, all byte, short, and char values are promoted to int, as just described. Then, if one operand is a long, the whole expression is promoted to long. If one operand is a float, the entire expression is promoted to float. If any of the operands are double, the result is double. #flashcard 
  id:: 63cfbccf-3b4c-4daa-887f-9576331a0787
  
  
    ([Location 2809](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2809))
-
- Recently, an exciting new feature called local variable type inference was added to the Java language. #flashcard 
  id:: 63cfbccf-2d05-45f9-b1c9-51c29932d3bc
  
  
    ([Location 2911](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2911))
-
- Beginning with JDK 10, it is now possible to let the compiler infer the type of a local variable based on the type of its initializer, thus avoiding the need to explicitly specify the type. #flashcard  #blue #azul 
  id:: 63cfbccf-7eca-4f16-8235-7d1f7057ff92
  
  
    ([Location 2917](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2917))
-
- In both cases, avg will be of type double. In the first case, its type is explicitly specified. In the second, its type is inferred as double because the initializer 10.0 is of type double. #flashcard  #blue #azul 
  id:: 63cfbccf-73d0-4536-a4f4-5f36f57ffc22
  
  
    ([Location 2929](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2929))
-
- id:: 63c66a0a-a4d8-4cf1-9d50-037be2d9e007
  
  int var = 1; // In this case, var is simply a user-defined identifier. #flashcard  #orange #naranja 
  
  
    ([Location 2934](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2934))
-
- id:: 63c66a0a-52fe-4ce9-8b1a-f925766cdfb4
  
  If you use the || and && forms, rather than the | and & forms of these operators, Java will not bother to evaluate the right-hand operand #flashcard 
  
  
    ([Location 3211](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3211))
-
- There is one important point to understand about the for-each style loop. Its iteration variable is “read-only” as it relates to the underlying array. An assignment to the iteration variable has no effect on the underlying array. In other words, you can’t change the contents of the array by assigning the iteration variable a new value. #flashcard  #blue #azul 
  id:: 63cfbccf-7219-4a7f-9adf-a2e348a67c66
  
  
    ([Location 3538](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3538))
-
- for(var v : nums) #flashcard  #orange #naranja 
  id:: 63cfbccf-e603-4506-93e9-1d6612357c85
  
  
    ([Location 3582](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3582))
-
- id:: 63c66a0a-7090-4a0c-933d-044e03aba453
  
  Because an object is an instance of a class, you will often see the two words object and instance used interchangeably. #flashcard 
  
  
    ([Location 3694](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3694))
-
- if no explicit constructor is specified, then Java will automatically supply a default constructor. #flashcard  #pink #rosa 
  id:: 63cfbccf-2c89-4f5e-b286-04479b76557b
  
  
    ([Location 3766](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3766))
-
- id:: 63c66a0a-7479-4994-af61-2457a4eb2d9a
  
  REMEMBER When you assign one object reference variable to another object reference variable, you are not creating a copy of the object, you are only making a copy of the reference. #flashcard  #blue #azul 
  
  
    ([Location 3796](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3796))
-
- A parameter is a variable defined by a method that receives a value when the method is called. For example, in square( ), i is a parameter. An argument is a value that is passed to a method when it is invoked. For example, square(100) passes 100 as an argument. Inside square( ), the parameter i receives that value. #flashcard 
  id:: 63cfbccf-e304-4399-9fb8-b1ea718bbdad
  
  
    ([Location 3870](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3870))
-
- garbage collection. It works like this: when no references to an object exist, that object is assumed to be no longer needed, and the memory occupied by the object can be reclaimed. There is no need to explicitly destroy objects. #flashcard  #blue #azul 
  id:: 63cfbccf-db20-499c-bb75-25ad3de96bf6
  
  
    ([Location 3951](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3951))
-
- Garbage collection only occurs sporadically (if at all) during the execution of your program. It will not occur simply because one or more objects exist that are no longer used. #flashcard  #blue #azul 
  id:: 63cfbccf-f385-4e78-8eb6-18ab22ebc9d5
  
  
    ([Location 3952](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3952))
-
- id:: 63c66a0a-9161-4902-a0bf-aef2ab77b71d
  
  REMEMBER When an object reference is passed to a method, the reference itself is passed by use of call-by-value. However, since the value being passed refers to an object, the copy of that value will still refer to the same object that its corresponding argument does. #flashcard  #pink #rosa 
  
  
    ([Location 4086](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4086))
-
- id:: 63c66a0a-a8a1-4bf7-a82f-4fd9627809c8
  
  When no access modifier is used, then by default the member of a class is public within its own package, but cannot be accessed outside of its package. #flashcard  #pink #rosa 
  
  
    ([Location 4151](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4151))
-
- If you need to do computation in order to initialize your static variables, you can declare a static block that gets executed exactly once, when the class is first loaded. The following example shows a class that has a static method, some static variables, and a static initialization block: #flashcard  #pink #rosa 
  id:: 63cfbccf-6193-4325-b6d1-280dc7941fd5
  
  
    ([Location 4193](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4193))
-
- id:: 63c66a0a-0b44-474e-b7c6-063fc0c67243
  
  In addition to fields, both method parameters and local variables can be declared final. Declaring a parameter final prevents it from being changed within the method. Declaring a local variable final prevents it from being assigned a value more than once. #flashcard  #blue #azul 
  
  
    ([Location 4220](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4220))
-
- id:: 63c66a0a-da46-4984-9474-0d717b87af8a
  
  System.out.println("This is a String, too"); the string "This is a String, too" is a String object. #flashcard  #orange #naranja 
  
  
    ([Location 4279](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4279))
-
- boolean equals(secondStr) int length( ) char charAt(index) #flashcard  #orange #naranja 
  id:: 63cfbccf-dad7-438e-8bd1-01e11467f9ec
  
  
    ([Location 4300](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4300))
-
- static void vaTest(int ... v) { #flashcard  #orange #naranja 
  id:: 63cfbccf-5483-48d9-8aa8-be7237ebf7e5
  
  
    ([Location 4340](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4340))
-
- super(arg-list); #flashcard  #orange #naranja 
  id:: 63cfbccf-49aa-4c99-8a4e-04dadf77b6cc
  
  
    ([Location 4492](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4492))
-
- super.member #flashcard  #orange #naranja 
  id:: 63cfbccf-0a80-4e90-8446-f114534929a7
  
  
    ([Location 4520](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4520))
-
- constructors complete their execution in order of derivation, from superclass to subclass. #flashcard  #pink #rosa 
  id:: 63cfbccf-9361-49ac-aef4-f5f65a5a1dab
  
  
    ([Location 4555](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4555))
-
- id:: 63c66a0a-6897-4e95-8613-6dfae15760e0
  
  Dynamic, run-time polymorphism is one of the most powerful mechanisms that object-oriented design brings to bear on code reuse and robustness. The ability of existing code libraries to call methods on instances of new classes without recompiling while maintaining a clean abstract interface is a profoundly powerful tool. #flashcard 
  
  
    ([Location 4618](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4618))
-
- Consider the class Triangle. It has no meaning if area( ) is not defined. In this case, you want some way to ensure that a subclass does, indeed, override all necessary methods. Java’s solution to this problem is the abstract method. #flashcard  #blue #azul 
  id:: 63cfbccf-635a-4529-927d-26b463c8c325
  
  
    ([Location 4642](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4642))
-
- abstract type name(parameter-list); #flashcard  #orange #naranja 
  id:: 63cfbccf-ecb3-4279-9605-777cc7b04aeb
  
  
    ([Location 4647](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4647))
-
- Any class that contains one or more abstract methods must also be declared abstract. #flashcard  #pink #rosa 
  id:: 63cfbccf-9354-41cd-8936-39e38a3e1a54
  
  
    ([Location 4648](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4648))
-
- To disallow a method from being overridden, specify final as a modifier at the start of its declaration. Methods declared as final cannot be overridden. #flashcard  #blue #azul 
  id:: 63cfbccf-83b3-4675-9ffc-b06724022ed8
  
  
    ([Location 4675](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4675))
-
- Sometimes you will want to prevent a class from being inherited. To do this, precede the class declaration with final. #flashcard  #blue #azul 
  id:: 63cfbccf-e795-4356-b435-d4dbae912830
  
  
    ([Location 4685](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4685))
-
- id:: 63c66a0a-4a04-431b-8c53-15b6172cd30d
  
  java mypack.AccountBalance #flashcard  #orange #naranja 
  
  
    ([Location 4782](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4782))
-
- id:: 63c66a0a-149c-4d91-8b9c-3329ad76aafc
  
  AccountBalance must be qualified with its package name. #flashcard  #blue #azul 
  
  
    ([Location 4786](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4786))
-
- When a member does not have an explicit access specification, it is visible to subclasses as well as to other classes in the same package. This is the default access. #flashcard  #pink #rosa 
  id:: 63cfbccf-9b3f-4e86-a15f-d725f7001076
  
  
    ([Location 4803](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4803))
-
- REMEMBER When you implement an interface method, it must be declared as public. #flashcard  #blue #azul 
  id:: 63cfbccf-ed52-4568-827c-4f333ee7d4b4
  
  
    ([Location 4917](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4917))
-
- id:: 63c66a0a-259a-4e58-a5d5-27021818a00d
  
  If a class includes an interface but does not fully implement the methods required by that interface, then that class must be declared as abstract. #flashcard  #blue #azul 
  
  
    ([Location 4942](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4942))
-
- id:: 63c66a0a-39df-48cf-8d60-180769b79727
  
  Variables in Interfaces #flashcard 
  
  
    ([Location 4982](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4982))
-
- id:: 63c66a0a-150c-4f55-a79a-44c97fd85f1c
  
  Here is the output of a sample run of this program. Note that the results are different each time it is run. #flashcard 
  
  
    ([Location 4994](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4994))
-
- id:: 63c66a0a-19f7-48a2-bc2e-6e3c40c17867
  
  A key point to understand about generic types is that a reference of one specific version of a generic type is not type compatible with another version of the same generic type. #flashcard  #blue #azul 
  
  
    ([Location 6984](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=6984))
-
- id:: 63c66a0a-f32d-4176-8f76-ed10f6fd3c21
  
  You can remove all elements except those of a specified group by calling retainAll( ). #flashcard  #blue #azul 
  
  
    ([Location 9445](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9445))
-
- id:: 63c66a0a-9f2f-4fa6-9841-218ba3fda874
  
  To remove an element only if it statisfies some condition, you can use removeIf( ). #flashcard  #blue #azul 
  
  
    ([Location 9446](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9446))
-
- id:: 63c66a0a-b687-4779-a35b-ce8cd9fe479b
  
  The toArray( ) methods return an array that contains the elements stored in the collection. The first returns an array of Object. The second returns an array of elements that have the same type as the array specified as a parameter. #flashcard 
  
  
    ([Location 9450](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9450))
-
- id:: 63c66a0a-1bc6-4c45-abc7-278660943f2c
  
  You can obtain a sublist of a list by calling subList( ), #flashcard  #blue #azul 
  
  
    ([Location 9480](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9480))
-
- id:: 63c66a0a-6f66-43e3-ad72-0ec56370be85
  
  One way to sort a list is with the sort( ) method defined by List. #flashcard  #blue #azul 
  
  
    ([Location 9481](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9481))
-
- Each version returns an unmodifiable, value-based collection that is comprised of the arguments that it is passed. #flashcard  #blue #azul 
  id:: 63cfbccf-3a55-4aff-8f10-40c94e280bd9
  
  
    ([Location 9483](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9483))
-
- static <E> List<E> of( ) #flashcard  #orange #naranja 
  id:: 63cfbccf-431a-4ae0-8113-407e8fc45a9c
  
  
    ([Location 9485](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9485))
-
- static <E> List<E> of(E ... objs) #flashcard  #orange #naranja 
  id:: 63cfbccf-a65a-4a45-9da1-a615969b84fb
  
  
    ([Location 9489](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9489))
-
- Beginning with JDK 10, Set includes the static copyOf( ) method shown here: static <E> Set<E> copyOf(Collection <? extends E> from) It returns a set that contains the same elements as from. Null values are not allowed. The returned set is unmodifiable. #flashcard  #blue #azul 
  id:: 63cfbccf-e1e6-42f2-8726-28df49c527dc
  
  
    ([Location 9505](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9505))
-
- The SortedSet interface extends Set and declares the behavior of a set sorted in ascending order. #flashcard  #blue #azul 
  id:: 63cfbccf-48eb-4040-8207-ba43e08a7e15
  
  
    ([Location 9509](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9509))
-
- id:: 63c66a0a-697a-45a4-aeb0-4453aba75418
  
  The NavigableSet interface extends SortedSet and declares the behavior of a collection that supports the retrieval of elements based on the closest match to a given value or values. #flashcard  #blue #azul 
  
  
    ([Location 9522](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9522))
-
- there are two methods that obtain and remove elements: poll( ) and remove( ). The difference between them is that poll( ) returns null if the queue is empty, but remove( ) throws an exception. #flashcard  #blue #azul 
  id:: 63cfbccf-9298-44df-89ed-e5d551f41e63
  
  
    ([Location 9542](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9542))
-
- id:: 63c66a0a-7cca-4a09-b564-49f0b9356607
  
  there are two methods, element( ) and peek( ), that obtain but don’t remove the element at the head of the queue. They differ only in that element( ) throws an exception if the queue is empty, but peek( ) returns null. #flashcard  #blue #azul 
  
  
    ([Location 9544](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9544))
-
- notice that offer( ) only attempts to add an element to a queue. #flashcard  #blue #azul 
  id:: 63cfbccf-15eb-442a-bfa6-8aac9e1c26a5
  
  
    ([Location 9546](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9546))
-
- Double-ended queues can function as standard, first-in, first-out queues or as last-in, first-out stacks. Deque is a generic interface that has this declaration: interface Deque<E> #flashcard 
  id:: 63cfbccf-cb2e-447f-80fb-0be0a6819853
  
  
    ([Location 9549](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9549))
-
- id:: 63c66a0a-eb3a-4b4b-8b69-4814c203c28d
  
  Notice that Deque includes the methods push( ) and pop( ). These methods enable a Deque to function as a stack. #flashcard  #blue #azul 
  
  
    ([Location 9559](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9559))
-
- id:: 63c66a0a-d5b8-4dab-adcd-111db701f290
  
  <T> T[ ] toArray(T array[ ]) #flashcard  #orange #naranja 
  
  
    ([Location 9618](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9618))
-
- id:: 63c66a0a-3d2b-4d97-a4c5-1516168700e5
  
  TreeSet extends AbstractSet and implements the NavigableSet interface. It creates a collection that uses a tree for storage. Objects are stored in sorted, ascending order. Access and retrieval times are quite fast, which makes TreeSet an excellent choice when storing large amounts of sorted information that must be found quickly. #flashcard 
  
  
    ([Location 9683](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9683))
-