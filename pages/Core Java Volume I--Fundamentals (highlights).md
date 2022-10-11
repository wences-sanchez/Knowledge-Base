title:: Core Java Volume I--Fundamentals (highlights)
author:: [[]]
full-title:: "Core Java Volume I--Fundamentals"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- Chapter 2: The Java Programming Environment
		- -
		- About the shebang in Java 11 #car
			- In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
		- -
	- Chapter 3: Fundamental Programming Structures in Java
		- -
		- How do you define a long literal? #car
			- Long integer numbers have a suffix L or l (for example, 4000000000L)
		- -
		- -
		- How do you define a float literal? #car
		  id:: 63401501-d8c6-4b81-8a5b-c8f7b6ae669d
			- Numbers of type float have a suffix F or f (for example, 3.14F)
		- -
		- -
		- What is String::blank()? #car
		  id:: 63401501-cf25-4e8c-ad9b-269cc4780d25
			- boolean blank() 11
			  returns true if the string is empty or consists of whitespace.
		- -
		- -
		- What does String::repeat do? #car
			- String repeat(int count) 11
			  returns a string that repeats this string count times.
		- -
		- -
		- Tip about your journey #car
			- It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
		- -
		- -
		- case SMALL: // no need to use Size.SMALL #ñspace
		- -
	- Chapter 1: An Introduction to Java
		- -
		- Why the 'Java' name? #car
			- Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java
		- -
		- -
		- [CODE] Define una matriz que no sea fija #car
		  id:: 63401501-4a31-40cb-a9f8-12892b69685e
			- int[][] odds = new int[NMAX + 1][];
		- -
		- -
		- [CODE] Ordena un array #car
		  id:: 63401501-5b09-45e5-a79e-9b79b94f9e99
			- Arrays.sort(a
		- -
		- -
		- [CODE] Clone an array #car
			- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
		- -
		- -
		- [CODE] Make a separate thousands, and two decimal float number #car
		  id:: 63401501-2a38-40c4-9379-ddf0efde0f59
			- System.out.printf("%,.2f", 10000.0 / 3.0);
		- -
		- -
		- [CODE]
		  Example of a printf() #car
			- System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
		- -
		- -
		- [CODE]
		  id:: 63401501-b6cd-48b3-bd3a-a6271bdb65eb
		  Declare and define a Scanner variable. #car
			- Scanner in = new Scanner(System.in);
		- -
		- -
		- [CODE]
		  Print a StringBuffer 'builder' variable #car
			- String completedString = builder.toString();
		- -
		- -
		- [CODE]
		  Append some content to a StringBuilder variable #car
			- builder.append(str)
		- -
		- -
		- [CODE]
		  id:: 63401501-28ee-416a-9fa0-dbc36520ad4e
		  Create a StringBuilder object #car
			- StringBuilder builder = new StringBuilder();
		- -
		- -
		- (String str) #ñspace
		- -
		- -
		- String trim() #ñspace
		- -
		- -
		- [CODE]
		  Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #car
			- Size s = Size.MEDIUM;
		- -
		- -
		- [CODE]
		  id:: 63401501-3365-4b37-885f-389aba1c707f
		  Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #car
			- enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
		- -
		- -
		- Where do you have to declare variables in Java? #car
			- In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
		- -
	- Chapter 4: Objects and Classes
		- -
		- Constructs an object that represents the given date. #car
		  id:: 63401501-ef9d-47b4-be77-593b4bb25e96
			- static LocalDate of(int year, int month, int day)
		- -
		- -
		- Constructs an object that represents the current date. #car
		  id:: 63401501-9ca6-4e32-b32a-c8b3aae1c413
			- static LocalDate now()
		- -