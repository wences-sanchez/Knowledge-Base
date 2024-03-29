title:: Readwise/Core Java Volume I--Fundamentals (highlights)
deck:: [[O'Reilly-Learning::Core Java Volume I--Fundamentals]]
author:: [[]]
full-title:: "Core Java Volume I--Fundamentals"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- Chapter 2: The Java Programming Environment
		- -
			- About the shebang in Java 11 #flashcard
				- In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
		- -
	- Chapter 3: Fundamental Programming Structures in Java
		- -
			- How do you define a long literal? #flashcard
				- Long integer numbers have a suffix L or l (for example, 4000000000L)
		- -
		- -
			- How do you define a float literal? #flashcard
				- Numbers of type float have a suffix F or f (for example, 3.14F)
		- -
		- -
			- What is String::blank()? #flashcard
				- boolean blank() 11
				  returns true if the string is empty or consists of whitespace.
		- -
		- -
			- What does String::repeat do? #flashcard
				- String repeat(int count) 11
				  returns a string that repeats this string count times.
		- -
		- -
			- Tip about your journey #flashcard
				- It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
		- -
		- -
			- case SMALL: // no need to use Size.SMALL #flashcard
		- -
	- Chapter 1: An Introduction to Java
		- -
			- Why the 'Java' name? #flashcard
				- Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java
		- -
		- -
			- [CODE] Define una matriz que no sea fija #flashcard
				- int[][] odds = new int[NMAX + 1][];
		- -
		- -
			- [CODE] Ordena un array #flashcard
				- Arrays.sort(a
		- -
		- -
			- [CODE] Clone an array #flashcard
				- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
		- -
		- -
			- [CODE] Make a separate thousands, and two decimal float number #flashcard
				- System.out.printf("%,.2f", 10000.0 / 3.0);
		- -
		- -
			- [CODE]
			  Example of a printf() #flashcard
				- System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
		- -
		- -
			- [CODE]
			  Declare and define a Scanner variable. #flashcard
				- Scanner in = new Scanner(System.in);
		- -
		- -
			- [CODE]
			  Print a StringBuffer 'builder' variable #flashcard
				- String completedString = builder.toString();
		- -
		- -
			- [CODE]
			  Append some content to a StringBuilder variable #flashcard
				- builder.append(str)
		- -
		- -
			- [CODE]
			  Create a StringBuilder object #flashcard
				- StringBuilder builder = new StringBuilder();
		- -
		- -
			- (String str) #flashcard
		- -
		- -
			- String trim() #flashcard
		- -
		- -
			- [CODE]
			  Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard
				- Size s = Size.MEDIUM;
		- -
		- -
			- [CODE]
			  Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard
				- enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
		- -
		- -
			- Where do you have to declare variables in Java? #flashcard
				- In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
		- -
	- Chapter 4: Objects and Classes
		- -
			- Constructs an object that represents the given date. #flashcard
				- static LocalDate of(int year, int month, int day)
		- -
		- -
			- Constructs an object that represents the current date. #flashcard
				- static LocalDate now()
		- -