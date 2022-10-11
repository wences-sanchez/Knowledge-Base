title:: Core Java Volume I—Fundamentals (highlights)
author:: [[]]
full-title:: "Core Java Volume I—Fundamentals"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- Chapter 1: An Introduction to Java
		- -
		- Why the 'Java' name? #car
			- Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java.
		- -
	- Chapter 2: The Java Programming Environment
		- -
		- About the shebang in Java 11 #car
			- In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
		- -
	- Chapter 3: Fundamental Programming Structures in Java
		- -
		- How do you define a long literal? #car
		  id:: 63401501-d2a6-4391-b2ff-22ccf67d7529
			- Long integer numbers have a suffix L or l (for example, 4000000000L)
		- -
		- -
		- How do you define a float literal? #car
			- Numbers of type float have a suffix F or f (for example, 3.14F)
		- -
		- -
		- Where do you have to declare variables in Java? #car
		  id:: 63401501-2f42-4d4f-807a-0bcd7e5ddaf0
			- In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
		- -
		- -
		- [CODE]
		  id:: 63401501-1bbd-4803-909d-25836d0969c8
		  Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #car
			- enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
		- -
		- -
		- [CODE]
		  id:: 63401501-7ff4-49c8-8dd9-032b5c6ca072
		  Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #car
			- Size s = Size.MEDIUM;
		- -
		- -
		- What is String::blank()? #car
			- boolean blank() 11
			  returns true if the string is empty or consists of whitespace.
		- -
		- -
		- String trim() #ñspace
		- -
		- -
		- String strip() #ñspace
		- -
		- -
		- What does String::repeat do? #car
			- String repeat(int count) 11
			  returns a string that repeats this string count times.
		- -
		- -
		- Tip about your journey #car
		  id:: 63401501-6e3c-40fb-9c44-a8b752544155
			- It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
		- -
		- -
		- [CODE]
		  Create a StringBuilder object #car
			- StringBuilder builder = new StringBuilder();
		- -
		- -
		- [CODE]
		  Append some content to a StringBuilder variable #car
			- builder.append(str);
		- -
		- -
		- [CODE]
		  id:: 63401501-f914-4d22-ae78-3cec4a243b7a
		  Print a StringBuffer 'builder' variable #car
			- String completedString = builder.toString();
		- -
		- -
		- [CODE]
		  Declare and define a Scanner variable. #car
			- Scanner in = new Scanner(System.in);
		- -
		- -
		- [CODE]
		  Example of a printf() #car
			- System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
		- -
		- -
		- [CODE] Make a separate thousands, and two decimal float number #car
			- System.out.printf("%,.2f", 10000.0 / 3.0);
		- -
		- -
		- case SMALL: // no need to use Size.SMALL #ñspace
		- -
		- -
		- [CODE] Clone an array #car
			- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
		- -
		- -
		- [CODE] Ordena un array #car
		  id:: 63401501-7a8c-46a9-9993-58ad932e0a55
			- Arrays.sort(a)
		- -
		- -
		- [CODE] Define una matriz que no sea fija #car
			- int[][] odds = new int[NMAX + 1][];
		- -
	- Chapter 4: Objects and Classes
		- -
		- Constructs an object that represents the current date. #car
			- static LocalDate now()
		- -
		- -
		- Constructs an object that represents the given date. #car
			- static LocalDate of(int year, int month, int day)
		- -