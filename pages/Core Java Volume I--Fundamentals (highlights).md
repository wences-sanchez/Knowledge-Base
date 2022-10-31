title:: Core Java Volume I--Fundamentals (highlights)
deck:: [[O'Reilly-Learning::Core Java Volume I--Fundamentals]]
author:: [[]]
full-title:: "Core Java Volume I--Fundamentals"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Chapter 2: The Java Programming Environment
		- -
		- In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java. #flashcard
			- About the shebang in Java 11
		- -
	- Chapter 3: Fundamental Programming Structures in Java
		- -
		- Long integer numbers have a suffix L or l (for example, 4000000000L) #flashcard
			- How do you define a long literal?
		- -
		- -
		- Numbers of type float have a suffix F or f (for example, 3.14F) #flashcard
			- How do you define a float literal?
		- -
		- -
		- boolean blank() 11
		  returns true if the string is empty or consists of whitespace. #flashcard
			- What is String::blank()?
		- -
		- -
		- String repeat(int count) 11
		  returns a string that repeats this string count times. #flashcard
			- What does String::repeat do?
		- -
		- -
		- It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library. #flashcard
			- Tip about your journey
		- -
		- -
		- case SMALL: // no need to use Size.SMALL #flashcard
		- -
	- Chapter 1: An Introduction to Java
		- -
		- Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java #flashcard
			- Why the 'Java' name?
		- -
		- -
		- int[][] odds = new int[NMAX + 1][]; #flashcard
			- [CODE] Define una matriz que no sea fija
		- -
		- -
		- Arrays.sort(a #flashcard
			- [CODE] Ordena un array
		- -
		- -
		- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length); #flashcard
			- [CODE] Clone an array
		- -
		- -
		- System.out.printf("%,.2f", 10000.0 / 3.0); #flashcard
			- [CODE] Make a separate thousands, and two decimal float number
		- -
		- -
		- System.out.printf("Hello, %s. Next year, you'll be %d", name, age); #flashcard
			- [CODE]
			  Example of a printf()
		- -
		- -
		- Scanner in = new Scanner(System.in); #flashcard
			- [CODE]
			  Declare and define a Scanner variable.
		- -
		- -
		- String completedString = builder.toString(); #flashcard
			- [CODE]
			  Print a StringBuffer 'builder' variable
		- -
		- -
		- builder.append(str) #flashcard
			- [CODE]
			  Append some content to a StringBuilder variable
		- -
		- -
		- StringBuilder builder = new StringBuilder(); #flashcard
			- [CODE]
			  Create a StringBuilder object
		- -
		- -
		- (String str) #flashcard
		- -
		- -
		- String trim() #flashcard
		- -
		- -
		- Size s = Size.MEDIUM; #flashcard
			- [CODE]
			  Declare a variable s of type Size[enum] and initialize it with the field MEDIUM.
		- -
		- -
		- enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE }; #flashcard
			- [CODE]
			  Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE
		- -
		- -
		- In Java, it is considered good style to declare variables as closely as possible to the point where they are first used. #flashcard
			- Where do you have to declare variables in Java?
		- -
	- Chapter 4: Objects and Classes
		- -
		- static LocalDate of(int year, int month, int day) #flashcard
			- Constructs an object that represents the given date.
		- -
		- -
		- static LocalDate now() #flashcard
			- Constructs an object that represents the current date.
		- -