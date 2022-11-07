title:: Java (highlights)
deck:: [[Other-Books::Java]]
author:: [[Herbert Schildt]]
full-title:: "Java"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/51IpgznsrtL._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Although Java is otherwise completely object-oriented, the primitive types are not. They are analogous to the simple types found in most other non–object-oriented languages. The reason for this is efficiency. #flashcard
		  id:: ee81edeb-1563-4dce-913e-79696fece93f
		- tags:: [[pink]] [[rosa]]
		- ([Location 2528](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2528))
	- -
	- -
		- Java defines four integer types: byte, short, int, and long. All of these are signed, positive and negative values. #flashcard
		  id:: 0872b918-3ed6-4478-ab03-6fd6979fd4bf
		- ([Location 2536](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2536))
	- -
	- -
		- Java does not support unsigned, positive-only integers. #flashcard
		  id:: 0a0bdf2e-3e70-4566-abe4-6e60f9b5196a
		- tags:: [[pink]] [[rosa]]
		- ([Location 2537](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2537))
	- -
	- -
		- The smallest integer type is byte. This is a signed 8-bit type that has a range from –128 to 127. #flashcard
		  id:: bd106e24-4dc2-4963-b69b-661860957771
		- ([Location 2546](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2546))
	- -
	- -
		- The most commonly used integer type is int. It is a signed 32-bit type that has a range from –2,147,483,648 to 2,147,483,647. #flashcard
		  id:: a8209fde-0d75-440e-80aa-257562b4be25
		- ([Location 2554](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2554))
	- -
	- -
		- Although you might think that using a byte or short would be more efficient than using an int in situations in which the larger range of an int is not needed, this may not be the case. The reason is that when byte and short values are used in an expression, they are promoted to int when the expression is evaluated. #flashcard
		  id:: 3442ffcb-ad40-4081-a693-0eb88e0f44fa
		- ([Location 2556](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2556))
	- -
	- -
		- long is a signed 64-bit type and is useful for those occasions where an int type is not large enough #flashcard
		  id:: 48631051-9ce4-4ae4-a510-571df040a024
		- ([Location 2561](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2561))
	- -
	- -
		- Floating-point numbers, also known as real numbers, #flashcard
		  id:: 675d74ca-e1e1-422e-bd44-1e7f5b676df2
		- ([Location 2567](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2567))
	- -
	- -
		- Variables of type float are useful when you need a fractional component, but don’t require a large degree of precision. For example, float can be useful when representing dollars and cents. #flashcard
		  id:: beb06f43-556c-4aa5-b0b8-7b05455ef752
		- tags:: [[blue]] [[azul]]
		- ([Location 2575](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2575))
	- -
	- -
		- However, to specify a long literal, you will need to explicitly tell the compiler that the literal value is of type long. You do this by appending an upper- or lowercase L to the literal. For example, 0x7ffffffffffffffL or 9223372036854775807L #flashcard
		  id:: 96238d42-2228-4b44-a3cb-f2bbb7a77029
		- ([Location 2636](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2636))
	- -
	- -
		- in some other languages strings are implemented as arrays of characters. However, this is not the case in Java. Strings are actually object types. #flashcard
		  id:: 9875b051-57d2-40c8-a84f-f814dfc31b28
		- tags:: [[pink]] [[rosa]]
		- ([Location 2692](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2692))
	- -
	- -
		- type identifier [ = value ][, identifier [= value ] …]; #flashcard
		  id:: ab38e23c-285a-42ac-8ca5-ba9734595b68
		- tags:: [[orange]] [[naranja]]
		- ([Location 2698](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2698))
	- -
	- -
		- It is not uncommon to think in terms of two general categories of scopes: global and local. However, these traditional scopes do not fit well with Java’s strict, object-oriented model. While it is possible to create what amounts to being a global scope, it is by far the exception, not the rule. In Java, the two major scopes are those defined by a class and those defined by a method. #flashcard
		  id:: 930aba04-136a-45c1-8dc1-1ae7ce4f50b9
		- tags:: [[blue]] [[azul]]
		- ([Location 2719](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2719))
	- -
	- -
		- the following fragment casts an int to a byte. If the integer’s value is larger than the range of a byte, it will be reduced modulo (the remainder of an integer division by the) byte’s range. #flashcard
		  id:: a4cdc3da-7649-4826-8145-413fb4d5745b
		- ([Location 2778](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2778))
	- -
	- -
		- Thus, when a floating-point value is assigned to an integer type, the fractional component is lost. For example, if the value 1.23 is assigned to an integer, the resulting value will simply be 1. The 0.23 will have been truncated. Of course, if the size of the whole number component is too large to fit into the target integer type, then that value will be reduced modulo the target type’s range. #flashcard
		  id:: 6f4d0203-2206-4705-93fc-1e8d0a0a7ac7
		- ([Location 2782](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2782))
	- -
	- -
		- Java defines several type promotion rules that apply to expressions. They are as follows: First, all byte, short, and char values are promoted to int, as just described. Then, if one operand is a long, the whole expression is promoted to long. If one operand is a float, the entire expression is promoted to float. If any of the operands are double, the result is double. #flashcard
		  id:: b6238bb6-95ce-4cb4-9b9f-857cc61c3e0d
		- ([Location 2809](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2809))
	- -
	- -
		- Recently, an exciting new feature called local variable type inference was added to the Java language. #flashcard
		  id:: 189e86e6-8b2d-4342-a65c-4f52dce87da1
		- ([Location 2911](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2911))
	- -
	- -
		- Beginning with JDK 10, it is now possible to let the compiler infer the type of a local variable based on the type of its initializer, thus avoiding the need to explicitly specify the type. #flashcard
		  id:: 19bf9697-8b94-4340-b9d5-d73633b19eed
		- tags:: [[blue]] [[azul]]
		- ([Location 2917](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2917))
	- -
	- -
		- In both cases, avg will be of type double. In the first case, its type is explicitly specified. In the second, its type is inferred as double because the initializer 10.0 is of type double. #flashcard
		  id:: ff84553c-4d63-48c4-a36d-8df941bb0f14
		- tags:: [[blue]] [[azul]]
		- ([Location 2929](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2929))
	- -
	- -
		- int var = 1; // In this case, var is simply a user-defined identifier. #flashcard
		  id:: 6faf639f-a85f-481d-b912-97c65346822b
		- tags:: [[orange]] [[naranja]]
		- ([Location 2934](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=2934))
	- -
	- -
		- If you use the || and && forms, rather than the | and & forms of these operators, Java will not bother to evaluate the right-hand operand #flashcard
		  id:: 7095d5ab-ea89-47dc-9190-416bc9d7c03b
		- ([Location 3211](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3211))
	- -
	- -
		- There is one important point to understand about the for-each style loop. Its iteration variable is “read-only” as it relates to the underlying array. An assignment to the iteration variable has no effect on the underlying array. In other words, you can’t change the contents of the array by assigning the iteration variable a new value. #flashcard
		  id:: 6b8b2ae2-7926-44d4-ba84-1c73223b184e
		- tags:: [[blue]] [[azul]]
		- ([Location 3538](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3538))
	- -
	- -
		- for(var v : nums) #flashcard
		  id:: 8b7deea1-fcdb-4532-8cd7-c38e3fb6c790
		- tags:: [[orange]] [[naranja]]
		- ([Location 3582](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3582))
	- -
	- -
		- Because an object is an instance of a class, you will often see the two words object and instance used interchangeably. #flashcard
		  id:: 575abdf0-8c91-4f29-815a-5375a4dff803
		- ([Location 3694](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3694))
	- -
	- -
		- if no explicit constructor is specified, then Java will automatically supply a default constructor. #flashcard
		  id:: 5b603ecd-01dc-4c42-9aa0-969b5edd14e0
		- tags:: [[pink]] [[rosa]]
		- ([Location 3766](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3766))
	- -
	- -
		- REMEMBER When you assign one object reference variable to another object reference variable, you are not creating a copy of the object, you are only making a copy of the reference. #flashcard
		  id:: 79a50a88-dda6-4d8c-bd16-3f0dac225900
		- tags:: [[blue]] [[azul]]
		- ([Location 3796](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3796))
	- -
	- -
		- A parameter is a variable defined by a method that receives a value when the method is called. For example, in square( ), i is a parameter. An argument is a value that is passed to a method when it is invoked. For example, square(100) passes 100 as an argument. Inside square( ), the parameter i receives that value. #flashcard
		  id:: 0eb029f6-7dca-463b-8020-6c9553442fcd
		- ([Location 3870](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3870))
	- -
	- -
		- garbage collection. It works like this: when no references to an object exist, that object is assumed to be no longer needed, and the memory occupied by the object can be reclaimed. There is no need to explicitly destroy objects. #flashcard
		  id:: 1ea3ea17-87ca-465a-af74-3cf7ed46cfd6
		- tags:: [[blue]] [[azul]]
		- ([Location 3951](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3951))
	- -
	- -
		- Garbage collection only occurs sporadically (if at all) during the execution of your program. It will not occur simply because one or more objects exist that are no longer used. #flashcard
		  id:: 4b505e58-6622-46bf-a5d5-99aa3a4ed294
		- tags:: [[blue]] [[azul]]
		- ([Location 3952](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=3952))
	- -
	- -
		- REMEMBER When an object reference is passed to a method, the reference itself is passed by use of call-by-value. However, since the value being passed refers to an object, the copy of that value will still refer to the same object that its corresponding argument does. #flashcard
		  id:: 17c3618e-7d46-47d9-9363-645c6cf6a9ad
		- tags:: [[pink]] [[rosa]]
		- ([Location 4086](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4086))
	- -
	- -
		- When no access modifier is used, then by default the member of a class is public within its own package, but cannot be accessed outside of its package. #flashcard
		  id:: 6a84af94-1656-4a1e-9fa9-0f2596f5badc
		- tags:: [[pink]] [[rosa]]
		- ([Location 4151](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4151))
	- -
	- -
		- If you need to do computation in order to initialize your static variables, you can declare a static block that gets executed exactly once, when the class is first loaded. The following example shows a class that has a static method, some static variables, and a static initialization block: #flashcard
		  id:: 484aad1d-2600-496f-b870-d3c32a314feb
		- tags:: [[pink]] [[rosa]]
		- ([Location 4193](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4193))
	- -
	- -
		- In addition to fields, both method parameters and local variables can be declared final. Declaring a parameter final prevents it from being changed within the method. Declaring a local variable final prevents it from being assigned a value more than once. #flashcard
		  id:: 5c3ffb29-3887-48aa-9097-ada442681c30
		- tags:: [[blue]] [[azul]]
		- ([Location 4220](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4220))
	- -
	- -
		- System.out.println("This is a String, too"); the string "This is a String, too" is a String object. #flashcard
		  id:: 16f4a604-a143-4e38-ab19-397ce34dfe1c
		- tags:: [[orange]] [[naranja]]
		- ([Location 4279](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4279))
	- -
	- -
		- boolean equals(secondStr) int length( ) char charAt(index) #flashcard
		  id:: b82fd5cd-020a-4fa4-916a-9f070f2db586
		- tags:: [[orange]] [[naranja]]
		- ([Location 4300](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4300))
	- -
	- -
		- static void vaTest(int ... v) { #flashcard
		  id:: 7c3321e0-bdcc-4b00-9a12-d86db4d542fa
		- tags:: [[orange]] [[naranja]]
		- ([Location 4340](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4340))
	- -
	- -
		- super(arg-list); #flashcard
		  id:: 072f540c-a262-439a-9b6a-712ac233b819
		- tags:: [[orange]] [[naranja]]
		- ([Location 4492](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4492))
	- -
	- -
		- super.member #flashcard
		  id:: 101af93c-4e5e-4d1c-8a36-efd0f394d643
		- tags:: [[orange]] [[naranja]]
		- ([Location 4520](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4520))
	- -
	- -
		- constructors complete their execution in order of derivation, from superclass to subclass. #flashcard
		  id:: 4949bf31-e0f9-4167-848e-2b1313f978fd
		- tags:: [[pink]] [[rosa]]
		- ([Location 4555](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4555))
	- -
	- -
		- Dynamic, run-time polymorphism is one of the most powerful mechanisms that object-oriented design brings to bear on code reuse and robustness. The ability of existing code libraries to call methods on instances of new classes without recompiling while maintaining a clean abstract interface is a profoundly powerful tool. #flashcard
		  id:: 18ddfc01-6a00-401c-97ec-20d898e9c651
		- ([Location 4618](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4618))
	- -
	- -
		- Consider the class Triangle. It has no meaning if area( ) is not defined. In this case, you want some way to ensure that a subclass does, indeed, override all necessary methods. Java’s solution to this problem is the abstract method. #flashcard
		  id:: 5e599a21-5e3f-478c-bae2-88f0699520b3
		- tags:: [[blue]] [[azul]]
		- ([Location 4642](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4642))
	- -
	- -
		- abstract type name(parameter-list); #flashcard
		  id:: 90875f3c-60f8-4998-a417-b4b83118adc4
		- tags:: [[orange]] [[naranja]]
		- ([Location 4647](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4647))
	- -
	- -
		- Any class that contains one or more abstract methods must also be declared abstract. #flashcard
		  id:: aaeb5a4b-98be-4ba2-8430-c13e9caa9bcf
		- tags:: [[pink]] [[rosa]]
		- ([Location 4648](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4648))
	- -
	- -
		- To disallow a method from being overridden, specify final as a modifier at the start of its declaration. Methods declared as final cannot be overridden. #flashcard
		  id:: 04e0b645-3698-43e6-8dbf-06bb302d0e54
		- tags:: [[blue]] [[azul]]
		- ([Location 4675](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4675))
	- -
	- -
		- Sometimes you will want to prevent a class from being inherited. To do this, precede the class declaration with final. #flashcard
		  id:: 24376daf-8282-4094-8d31-7fd8719e9bc9
		- tags:: [[blue]] [[azul]]
		- ([Location 4685](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4685))
	- -
	- -
		- java mypack.AccountBalance #flashcard
		  id:: aa2ef3c6-fcb5-4408-a134-8990b1a7acc0
		- tags:: [[orange]] [[naranja]]
		- ([Location 4782](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4782))
	- -
	- -
		- AccountBalance must be qualified with its package name. #flashcard
		  id:: 9cfd0ef6-e780-4d5d-8844-36e5df34fe05
		- tags:: [[blue]] [[azul]]
		- ([Location 4786](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4786))
	- -
	- -
		- When a member does not have an explicit access specification, it is visible to subclasses as well as to other classes in the same package. This is the default access. #flashcard
		  id:: d1115f2f-2c91-4e5c-a479-46915c087717
		- tags:: [[pink]] [[rosa]]
		- ([Location 4803](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4803))
	- -
	- -
		- REMEMBER When you implement an interface method, it must be declared as public. #flashcard
		  id:: 8cae10f5-3046-491f-82b7-74942565c560
		- tags:: [[blue]] [[azul]]
		- ([Location 4917](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4917))
	- -
	- -
		- If a class includes an interface but does not fully implement the methods required by that interface, then that class must be declared as abstract. #flashcard
		  id:: 98a09b89-e092-45ea-91a3-7f571eceb428
		- tags:: [[blue]] [[azul]]
		- ([Location 4942](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4942))
	- -
	- -
		- Variables in Interfaces #flashcard
		  id:: a628d416-cc83-428b-a778-1d2815f09a8a
		- ([Location 4982](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4982))
	- -
	- -
		- Here is the output of a sample run of this program. Note that the results are different each time it is run. #flashcard
		  id:: f24f636b-8f98-4e6e-b808-0adda709fd65
		- ([Location 4994](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=4994))
	- -
	- -
		- A key point to understand about generic types is that a reference of one specific version of a generic type is not type compatible with another version of the same generic type. #flashcard
		  id:: 98d7d99b-1c16-4cfe-87a7-bc0c4383fda7
		- tags:: [[blue]] [[azul]]
		- ([Location 6984](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=6984))
	- -
	- -
		- You can remove all elements except those of a specified group by calling retainAll( ). #flashcard
		  id:: 5f49f12d-f2db-4fae-bb51-efe0c5de6f4d
		- tags:: [[blue]] [[azul]]
		- ([Location 9445](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9445))
	- -
	- -
		- To remove an element only if it statisfies some condition, you can use removeIf( ). #flashcard
		  id:: 56641ef0-e094-45a1-8f57-82a9279945be
		- tags:: [[blue]] [[azul]]
		- ([Location 9446](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9446))
	- -
	- -
		- The toArray( ) methods return an array that contains the elements stored in the collection. The first returns an array of Object. The second returns an array of elements that have the same type as the array specified as a parameter. #flashcard
		  id:: d49537d9-580f-43ef-823a-fc31c266e22b
		- ([Location 9450](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9450))
	- -
	- -
		- You can obtain a sublist of a list by calling subList( ), #flashcard
		  id:: cb257f2d-8a1e-420f-9aed-22c0c0079cb5
		- tags:: [[blue]] [[azul]]
		- ([Location 9480](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9480))
	- -
	- -
		- One way to sort a list is with the sort( ) method defined by List. #flashcard
		  id:: 3fc5a3fd-13ec-4481-a297-132924ee5b86
		- tags:: [[blue]] [[azul]]
		- ([Location 9481](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9481))
	- -
	- -
		- Each version returns an unmodifiable, value-based collection that is comprised of the arguments that it is passed. #flashcard
		  id:: 1a41b3a8-0dbd-4b15-9855-b468b54d38c5
		- tags:: [[blue]] [[azul]]
		- ([Location 9483](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9483))
	- -
	- -
		- static <E> List<E> of( ) #flashcard
		  id:: 0f21624b-2584-44f2-85af-947ab0c0e384
		- tags:: [[orange]] [[naranja]]
		- ([Location 9485](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9485))
	- -
	- -
		- static <E> List<E> of(E ... objs) #flashcard
		  id:: e664cc6d-0696-4e1b-9009-de00aad351e3
		- tags:: [[orange]] [[naranja]]
		- ([Location 9489](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9489))
	- -
	- -
		- Beginning with JDK 10, Set includes the static copyOf( ) method shown here: static <E> Set<E> copyOf(Collection <? extends E> from) It returns a set that contains the same elements as from. Null values are not allowed. The returned set is unmodifiable. #flashcard
		  id:: b6ee24bf-b758-4e85-af32-53f18a6f8198
		- tags:: [[blue]] [[azul]]
		- ([Location 9505](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9505))
	- -
	- -
		- The SortedSet interface extends Set and declares the behavior of a set sorted in ascending order. #flashcard
		  id:: 7d1aa88c-c893-49c1-a71d-58127ca6840c
		- tags:: [[blue]] [[azul]]
		- ([Location 9509](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9509))
	- -
	- -
		- The NavigableSet interface extends SortedSet and declares the behavior of a collection that supports the retrieval of elements based on the closest match to a given value or values. #flashcard
		  id:: 6e1f5e2b-7a48-4762-8d79-195088021d57
		- tags:: [[blue]] [[azul]]
		- ([Location 9522](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9522))
	- -
	- -
		- there are two methods that obtain and remove elements: poll( ) and remove( ). The difference between them is that poll( ) returns null if the queue is empty, but remove( ) throws an exception. #flashcard
		  id:: 97d13bc3-b1b2-4d59-8dde-e0d76ffdc966
		- tags:: [[blue]] [[azul]]
		- ([Location 9542](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9542))
	- -
	- -
		- there are two methods, element( ) and peek( ), that obtain but don’t remove the element at the head of the queue. They differ only in that element( ) throws an exception if the queue is empty, but peek( ) returns null. #flashcard
		  id:: c1666c55-d167-49b1-b994-9f23dc03ea99
		- tags:: [[blue]] [[azul]]
		- ([Location 9544](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9544))
	- -
	- -
		- notice that offer( ) only attempts to add an element to a queue. #flashcard
		  id:: 1d9f4ceb-74bf-4e99-9bee-b211c462dd27
		- tags:: [[blue]] [[azul]]
		- ([Location 9546](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9546))
	- -
	- -
		- Double-ended queues can function as standard, first-in, first-out queues or as last-in, first-out stacks. Deque is a generic interface that has this declaration: interface Deque<E> #flashcard
		  id:: f88668d2-7c82-47aa-835c-f306ea3cd5ed
		- ([Location 9549](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9549))
	- -
	- -
		- Notice that Deque includes the methods push( ) and pop( ). These methods enable a Deque to function as a stack. #flashcard
		  id:: e9629d46-c9a1-4d97-9e11-8e7ffa62e4d2
		- tags:: [[blue]] [[azul]]
		- ([Location 9559](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9559))
	- -
	- -
		- <T> T[ ] toArray(T array[ ]) #flashcard
		  id:: bdb25f0e-1f1d-4e42-b0d5-c3c5163e5e2b
		- tags:: [[orange]] [[naranja]]
		- ([Location 9618](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9618))
	- -
	- -
		- TreeSet extends AbstractSet and implements the NavigableSet interface. It creates a collection that uses a tree for storage. Objects are stored in sorted, ascending order. Access and retrieval times are quite fast, which makes TreeSet an excellent choice when storing large amounts of sorted information that must be found quickly. #flashcard
		  id:: b7e2760a-c186-4081-acfe-3fedbbee4b25
		- ([Location 9683](https://readwise.io/to_kindle?action=open&asin=B07KSQ9RKF&location=9683))
	- -