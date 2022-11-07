# Java

deck:: [[Other-Books::Java]]\
author:: [[Herbert Schildt]]\
full-title:: "Java"\
category:: #books\
\

![](https://images-na.ssl-images-amazon.com/images/I/51IpgznsrtL._SL200_.jpg)
## Highlights
- id:: 6363991f-36a1-4240-95cb-b49d6aa7097e
  
  Although Java is otherwise completely object-oriented, the primitive types are not. They are analogous to the simple types found in most other non–object-oriented languages. The reason for this is efficiency. #flashcard  #pink #rosa 
  
  
    ([Location 2528](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2528))
-
- id:: 6363991f-7376-4b03-883c-ac23f5fc4c69
  
  Java defines four integer types: byte, short, int, and long. All of these are signed, positive and negative values. #flashcard 
  
  
    ([Location 2536](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2536))
-
- id:: 6363991f-1419-4dd2-849c-35da30145071
  
  Java does not support unsigned, positive-only integers. #flashcard  #pink #rosa 
  
  
    ([Location 2537](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2537))
-
- id:: 6363991f-348b-47f4-a1f3-9f3c7f7071d2
  
  The smallest integer type is byte. This is a signed 8-bit type that has a range from –128 to 127. #flashcard 
  
  
    ([Location 2546](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2546))
-
- id:: 6363991f-89da-4b30-9bab-db856174f575
  
  The most commonly used integer type is int. It is a signed 32-bit type that has a range from –2,147,483,648 to 2,147,483,647. #flashcard 
  
  
    ([Location 2554](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2554))
-
- id:: 6363991f-1cb5-4803-aff8-91cf3742cfcd
  
  Although you might think that using a byte or short would be more efficient than using an int in situations in which the larger range of an int is not needed, this may not be the case. The reason is that when byte and short values are used in an expression, they are promoted to int when the expression is evaluated. #flashcard 
  
  
    ([Location 2556](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2556))
-
- id:: 6363991f-528d-4aae-a22e-24c56d1f213f
  
  long is a signed 64-bit type and is useful for those occasions where an int type is not large enough #flashcard 
  
  
    ([Location 2561](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2561))
-
- id:: 6363991e-4bd6-4e7f-a1b1-6cf4db19192c
  
  Floating-point numbers, also known as real numbers, #flashcard 
  
  
    ([Location 2567](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2567))
-
- id:: 6363991e-dd99-429b-8cde-a1b9ea09e5fd
  
  Variables of type float are useful when you need a fractional component, but don’t require a large degree of precision. For example, float can be useful when representing dollars and cents. #flashcard  #blue #azul 
  
  
    ([Location 2575](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2575))
-
- id:: 6363991e-28ce-4fd7-b885-b1b03ecbe4fe
  
  However, to specify a long literal, you will need to explicitly tell the compiler that the literal value is of type long. You do this by appending an upper- or lowercase L to the literal. For example, 0x7ffffffffffffffL or 9223372036854775807L #flashcard 
  
  
    ([Location 2636](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2636))
-
- id:: 6363991e-a482-40fa-acdf-c94b69241878
  
  in some other languages strings are implemented as arrays of characters. However, this is not the case in Java. Strings are actually object types. #flashcard  #pink #rosa 
  
  
    ([Location 2692](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2692))
-
- id:: 6363991e-9939-443e-84e2-9996edf1a42a
  
  type identifier [ = value ][, identifier [= value ] …]; #flashcard  #orange #naranja 
  
  
    ([Location 2698](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2698))
-
- id:: 6363991e-8cc6-4052-bcb9-3670a91c9812
  
  It is not uncommon to think in terms of two general categories of scopes: global and local. However, these traditional scopes do not fit well with Java’s strict, object-oriented model. While it is possible to create what amounts to being a global scope, it is by far the exception, not the rule. In Java, the two major scopes are those defined by a class and those defined by a method. #flashcard  #blue #azul 
  
  
    ([Location 2719](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2719))
-
- id:: 6363991e-ffe3-4ddb-8c8e-843003081622
  
  the following fragment casts an int to a byte. If the integer’s value is larger than the range of a byte, it will be reduced modulo (the remainder of an integer division by the) byte’s range. #flashcard 
  
  
    ([Location 2778](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2778))
-
- id:: 6363991e-0321-41c3-a3a3-4154e7bc2442
  
  Thus, when a floating-point value is assigned to an integer type, the fractional component is lost. For example, if the value 1.23 is assigned to an integer, the resulting value will simply be 1. The 0.23 will have been truncated. Of course, if the size of the whole number component is too large to fit into the target integer type, then that value will be reduced modulo the target type’s range. #flashcard 
  
  
    ([Location 2782](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2782))
-
- id:: 6363991e-0763-43fb-95ca-b6b30cb91f16
  
  Java defines several type promotion rules that apply to expressions. They are as follows: First, all byte, short, and char values are promoted to int, as just described. Then, if one operand is a long, the whole expression is promoted to long. If one operand is a float, the entire expression is promoted to float. If any of the operands are double, the result is double. #flashcard 
  
  
    ([Location 2809](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2809))
-
- id:: 6363991e-01f4-4ca3-bbf8-fe679a77ba7e
  
  Recently, an exciting new feature called local variable type inference was added to the Java language. #flashcard 
  
  
    ([Location 2911](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2911))
-
- id:: 6363991e-7380-429b-a6ef-0b87f22e9cf6
  
  Beginning with JDK 10, it is now possible to let the compiler infer the type of a local variable based on the type of its initializer, thus avoiding the need to explicitly specify the type. #flashcard  #blue #azul 
  
  
    ([Location 2917](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2917))
-
- id:: 6363991e-1c80-4aa7-bc6c-3ca8de6f4115
  
  In both cases, avg will be of type double. In the first case, its type is explicitly specified. In the second, its type is inferred as double because the initializer 10.0 is of type double. #flashcard  #blue #azul 
  
  
    ([Location 2929](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2929))
-
- id:: 6363991e-1e38-4375-acc4-22728ef58702
  
  int var = 1; // In this case, var is simply a user-defined identifier. #flashcard  #orange #naranja 
  
  
    ([Location 2934](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2934))
-
- id:: 6363991e-4548-4949-aba1-8c7df7affd6c
  
  If you use the || and && forms, rather than the | and & forms of these operators, Java will not bother to evaluate the right-hand operand #flashcard 
  
  
    ([Location 3211](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3211))
-
- id:: 6363991e-a098-4167-a6d5-9f99719a9869
  
  There is one important point to understand about the for-each style loop. Its iteration variable is “read-only” as it relates to the underlying array. An assignment to the iteration variable has no effect on the underlying array. In other words, you can’t change the contents of the array by assigning the iteration variable a new value. #flashcard  #blue #azul 
  
  
    ([Location 3538](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3538))
-
- id:: 6363991e-29ad-4045-8cf0-2ff67dda69cf
  
  for(var v : nums) #flashcard  #orange #naranja 
  
  
    ([Location 3582](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3582))
-
- id:: 6363991e-9b1a-401d-8b2d-a06fe256ecbb
  
  Because an object is an instance of a class, you will often see the two words object and instance used interchangeably. #flashcard 
  
  
    ([Location 3694](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3694))
-
- id:: 6363991e-4fd9-4ec6-aa82-0327d9574c83
  
  if no explicit constructor is specified, then Java will automatically supply a default constructor. #flashcard  #pink #rosa 
  
  
    ([Location 3766](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3766))
-
- id:: 6363991e-4c6a-440b-b349-5f97bf9eb39d
  
  REMEMBER When you assign one object reference variable to another object reference variable, you are not creating a copy of the object, you are only making a copy of the reference. #flashcard  #blue #azul 
  
  
    ([Location 3796](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3796))
-
- id:: 6363991e-99f2-49c6-8626-bf1f980c836e
  
  A parameter is a variable defined by a method that receives a value when the method is called. For example, in square( ), i is a parameter. An argument is a value that is passed to a method when it is invoked. For example, square(100) passes 100 as an argument. Inside square( ), the parameter i receives that value. #flashcard 
  
  
    ([Location 3870](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3870))
-
- id:: 6363991e-d6d9-4271-a332-9a129cf79675
  
  garbage collection. It works like this: when no references to an object exist, that object is assumed to be no longer needed, and the memory occupied by the object can be reclaimed. There is no need to explicitly destroy objects. #flashcard  #blue #azul 
  
  
    ([Location 3951](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3951))
-
- id:: 6363991e-12e7-4618-b65a-42c8bce0edbb
  
  Garbage collection only occurs sporadically (if at all) during the execution of your program. It will not occur simply because one or more objects exist that are no longer used. #flashcard  #blue #azul 
  
  
    ([Location 3952](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3952))
-
- id:: 6363991e-6dd2-4005-8849-f7556b380622
  
  REMEMBER When an object reference is passed to a method, the reference itself is passed by use of call-by-value. However, since the value being passed refers to an object, the copy of that value will still refer to the same object that its corresponding argument does. #flashcard  #pink #rosa 
  
  
    ([Location 4086](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4086))
-
- id:: 6363991e-0f0e-4d0c-b946-c77bdb516a87
  
  When no access modifier is used, then by default the member of a class is public within its own package, but cannot be accessed outside of its package. #flashcard  #pink #rosa 
  
  
    ([Location 4151](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4151))
-
- id:: 6363991e-4c49-4bfa-bc58-8af49a7ae356
  
  If you need to do computation in order to initialize your static variables, you can declare a static block that gets executed exactly once, when the class is first loaded. The following example shows a class that has a static method, some static variables, and a static initialization block: #flashcard  #pink #rosa 
  
  
    ([Location 4193](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4193))
-
- id:: 6363991e-2893-4a87-9307-50df7504e56b
  
  In addition to fields, both method parameters and local variables can be declared final. Declaring a parameter final prevents it from being changed within the method. Declaring a local variable final prevents it from being assigned a value more than once. #flashcard  #blue #azul 
  
  
    ([Location 4220](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4220))
-
- id:: 6363991e-fdb5-4f36-8911-fffed5fc27a8
  
  System.out.println("This is a String, too"); the string "This is a String, too" is a String object. #flashcard  #orange #naranja 
  
  
    ([Location 4279](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4279))
-
- id:: 6363991e-b581-4e26-a46a-0e66eeb4b728
  
  boolean equals(secondStr) int length( ) char charAt(index) #flashcard  #orange #naranja 
  
  
    ([Location 4300](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4300))
-
- id:: 6363991e-ef6e-47b6-b97a-6fbe9e7e08f7
  
  static void vaTest(int ... v) { #flashcard  #orange #naranja 
  
  
    ([Location 4340](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4340))
-
- id:: 6363991e-0017-42ac-bf0f-8f5fd1aab276
  
  super(arg-list); #flashcard  #orange #naranja 
  
  
    ([Location 4492](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4492))
-
- id:: 6363991e-fb7a-4d86-bbc5-90e7163e0070
  
  super.member #flashcard  #orange #naranja 
  
  
    ([Location 4520](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4520))
-
- id:: 6363991e-00b3-4117-81ff-d68770002756
  
  constructors complete their execution in order of derivation, from superclass to subclass. #flashcard  #pink #rosa 
  
  
    ([Location 4555](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4555))
-
- id:: 6363991e-a709-41c8-94e8-75b78796596c
  
  Dynamic, run-time polymorphism is one of the most powerful mechanisms that object-oriented design brings to bear on code reuse and robustness. The ability of existing code libraries to call methods on instances of new classes without recompiling while maintaining a clean abstract interface is a profoundly powerful tool. #flashcard 
  
  
    ([Location 4618](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4618))
-
- id:: 6363991e-faab-4da1-bcec-2ec124a4d19a
  
  Consider the class Triangle. It has no meaning if area( ) is not defined. In this case, you want some way to ensure that a subclass does, indeed, override all necessary methods. Java’s solution to this problem is the abstract method. #flashcard  #blue #azul 
  
  
    ([Location 4642](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4642))
-
- id:: 6363991e-d1fe-489e-a166-884dfceba8dc
  
  abstract type name(parameter-list); #flashcard  #orange #naranja 
  
  
    ([Location 4647](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4647))
-
- id:: 6363991e-c1e8-4aeb-874a-111ed37be5ff
  
  Any class that contains one or more abstract methods must also be declared abstract. #flashcard  #pink #rosa 
  
  
    ([Location 4648](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4648))
-
- id:: 6363991e-1ff6-4c2e-a91b-27f9432b0265
  
  To disallow a method from being overridden, specify final as a modifier at the start of its declaration. Methods declared as final cannot be overridden. #flashcard  #blue #azul 
  
  
    ([Location 4675](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4675))
-
- id:: 6363991e-bdcd-4d33-9e0d-60abd8e22114
  
  Sometimes you will want to prevent a class from being inherited. To do this, precede the class declaration with final. #flashcard  #blue #azul 
  
  
    ([Location 4685](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4685))
-
- id:: 6363991e-aa59-4230-b0b8-87490122b5a6
  
  java mypack.AccountBalance #flashcard  #orange #naranja 
  
  
    ([Location 4782](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4782))
-
- id:: 6363991e-30d1-4866-a383-cd9268ec72f5
  
  AccountBalance must be qualified with its package name. #flashcard  #blue #azul 
  
  
    ([Location 4786](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4786))
-
- id:: 6363991e-9c3d-4539-a093-c91a3cb73e08
  
  When a member does not have an explicit access specification, it is visible to subclasses as well as to other classes in the same package. This is the default access. #flashcard  #pink #rosa 
  
  
    ([Location 4803](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4803))
-
- id:: 6363991e-ac3e-493b-959c-3802b94f96a2
  
  REMEMBER When you implement an interface method, it must be declared as public. #flashcard  #blue #azul 
  
  
    ([Location 4917](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4917))
-
- id:: 6363991e-3e8e-4685-a0a3-c8fe2f77009d
  
  If a class includes an interface but does not fully implement the methods required by that interface, then that class must be declared as abstract. #flashcard  #blue #azul 
  
  
    ([Location 4942](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4942))
-
- id:: 6363991e-9f8c-4b20-95de-ea74d01f4065
  
  Variables in Interfaces #flashcard 
  
  
    ([Location 4982](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4982))
-
- id:: 6363991e-2e50-44af-b696-0a286afdd03e
  
  Here is the output of a sample run of this program. Note that the results are different each time it is run. #flashcard 
  
  
    ([Location 4994](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4994))
-
- id:: 6363991e-9a8a-4590-ba1c-21b36fb9658f
  
  A key point to understand about generic types is that a reference of one specific version of a generic type is not type compatible with another version of the same generic type. #flashcard  #blue #azul 
  
  
    ([Location 6984](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=6984))
-
- id:: 6363991e-5fd1-4bfb-95ba-4652e8497a50
  
  You can remove all elements except those of a specified group by calling retainAll( ). #flashcard  #blue #azul 
  
  
    ([Location 9445](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9445))
-
- id:: 6363991e-2839-4d05-ac46-902a9c9da951
  
  To remove an element only if it statisfies some condition, you can use removeIf( ). #flashcard  #blue #azul 
  
  
    ([Location 9446](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9446))
-
- id:: 6363991e-0157-443e-bcc2-c0d7021d105b
  
  The toArray( ) methods return an array that contains the elements stored in the collection. The first returns an array of Object. The second returns an array of elements that have the same type as the array specified as a parameter. #flashcard 
  
  
    ([Location 9450](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9450))
-
- id:: 6363991e-6274-4673-bf5b-d7c9c0f5bf8e
  
  You can obtain a sublist of a list by calling subList( ), #flashcard  #blue #azul 
  
  
    ([Location 9480](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9480))
-
- id:: 6363991e-7e2e-4e1b-9a5f-f63b2336fa72
  
  One way to sort a list is with the sort( ) method defined by List. #flashcard  #blue #azul 
  
  
    ([Location 9481](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9481))
-
- id:: 6363991e-e0de-4541-a630-3cf62ba6d11b
  
  Each version returns an unmodifiable, value-based collection that is comprised of the arguments that it is passed. #flashcard  #blue #azul 
  
  
    ([Location 9483](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9483))
-
- id:: 6363991e-a2e1-4352-9205-2fa820ddf8f5
  
  static <E> List<E> of( ) #flashcard  #orange #naranja 
  
  
    ([Location 9485](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9485))
-
- id:: 6363991e-db6e-4645-b845-c3fcd93bb9f6
  
  static <E> List<E> of(E ... objs) #flashcard  #orange #naranja 
  
  
    ([Location 9489](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9489))
-
- id:: 6363991e-a87c-4566-bf31-bb39df00699d
  
  Beginning with JDK 10, Set includes the static copyOf( ) method shown here: static <E> Set<E> copyOf(Collection <? extends E> from) It returns a set that contains the same elements as from. Null values are not allowed. The returned set is unmodifiable. #flashcard  #blue #azul 
  
  
    ([Location 9505](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9505))
-
- id:: 6363991e-15d2-4828-b1df-ed13cb51ab27
  
  The SortedSet interface extends Set and declares the behavior of a set sorted in ascending order. #flashcard  #blue #azul 
  
  
    ([Location 9509](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9509))
-
- id:: 6363991e-2e0b-4be5-80f5-23e15abcc229
  
  The NavigableSet interface extends SortedSet and declares the behavior of a collection that supports the retrieval of elements based on the closest match to a given value or values. #flashcard  #blue #azul 
  
  
    ([Location 9522](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9522))
-
- id:: 6363991e-2635-4ce5-88fd-62ce05cb8053
  
  there are two methods that obtain and remove elements: poll( ) and remove( ). The difference between them is that poll( ) returns null if the queue is empty, but remove( ) throws an exception. #flashcard  #blue #azul 
  
  
    ([Location 9542](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9542))
-
- id:: 6363991e-4b86-45d6-8d31-317fadcf8f80
  
  there are two methods, element( ) and peek( ), that obtain but don’t remove the element at the head of the queue. They differ only in that element( ) throws an exception if the queue is empty, but peek( ) returns null. #flashcard  #blue #azul 
  
  
    ([Location 9544](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9544))
-
- id:: 6363991e-edf3-4d24-8631-dd857708e6f0
  
  notice that offer( ) only attempts to add an element to a queue. #flashcard  #blue #azul 
  
  
    ([Location 9546](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9546))
-
- id:: 6363991e-9a13-4924-8e31-045cdaec16dc
  
  Double-ended queues can function as standard, first-in, first-out queues or as last-in, first-out stacks. Deque is a generic interface that has this declaration: interface Deque<E> #flashcard 
  
  
    ([Location 9549](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9549))
-
- id:: 6363991e-9cb5-4054-9ecf-58db58326525
  
  Notice that Deque includes the methods push( ) and pop( ). These methods enable a Deque to function as a stack. #flashcard  #blue #azul 
  
  
    ([Location 9559](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9559))
-
- id:: 6363991e-a0d2-483d-85a0-cfff404c8215
  
  <T> T[ ] toArray(T array[ ]) #flashcard  #orange #naranja 
  
  
    ([Location 9618](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9618))
-
- id:: 6363991e-cad7-46e1-8fc2-e7b66258b43f
  
  TreeSet extends AbstractSet and implements the NavigableSet interface. It creates a collection that uses a tree for storage. Objects are stored in sorted, ascending order. Access and retrieval times are quite fast, which makes TreeSet an excellent choice when storing large amounts of sorted information that must be found quickly. #flashcard 
  
  
    ([Location 9683](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9683))
-