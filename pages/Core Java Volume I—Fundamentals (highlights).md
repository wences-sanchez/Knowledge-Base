title:: Core Java Volume I—Fundamentals (highlights)
deck:: [[O'Reilly-Learning::Core Java Volume I—Fundamentals]]
author:: [[]]
full-title:: "Core Java Volume I—Fundamentals"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Chapter 1: An Introduction to Java
		- -
			- Why the 'Java' name? #flashcard
			  id:: d061fc3f-a5fc-4e0a-a813-76a6879c9d80
				- Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java.
		- -
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
			- Where do you have to declare variables in Java? #flashcard
				- In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
		- -
		- -
			- [CODE]
			  id:: 3d88a545-494c-44da-abc6-0fa418c31a77
			  Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard
				- enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
		- -
		- -
			- [CODE]
			  Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard
				- Size s = Size.MEDIUM;
		- -
		- -
			- What is String::blank()? #flashcard
			  id:: 7cb357cc-6bf8-4056-8784-950afc6f836e
				- boolean blank() 11
				  returns true if the string is empty or consists of whitespace.
		- -
		- -
			- String trim() #flashcard
			  id:: 5f4026c5-2f3b-4463-a723-e082f7bd7825
		- -
		- -
			- String strip() #flashcard
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
			- [CODE]
			  Create a StringBuilder object #flashcard
				- StringBuilder builder = new StringBuilder();
		- -
		- -
			- [CODE]
			  id:: a869c730-7c5c-40d2-b336-b768f8b761dd
			  Append some content to a StringBuilder variable #flashcard
				- builder.append(str);
		- -
		- -
			- [CODE]
			  Print a StringBuffer 'builder' variable #flashcard
				- String completedString = builder.toString();
		- -
		- -
			- [CODE]
			  Declare and define a Scanner variable. #flashcard
				- Scanner in = new Scanner(System.in);
		- -
		- -
			- [CODE]
			  id:: e3524128-f328-4391-8a8c-83f3522ccfe6
			  Example of a printf() #flashcard
				- System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
		- -
		- -
			- [CODE] Make a separate thousands, and two decimal float number #flashcard
			  id:: 42912f4a-d161-4745-8541-ebd34e91c5f9
				- System.out.printf("%,.2f", 10000.0 / 3.0);
		- -
		- -
			- case SMALL: // no need to use Size.SMALL #flashcard
		- -
		- -
			- [CODE] Clone an array #flashcard
				- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
		- -
		- -
			- [CODE] Ordena un array #flashcard
				- Arrays.sort(a)
		- -
		- -
			- [CODE] Define una matriz que no sea fija #flashcard
			  id:: 68c623e5-ed67-4fe5-a6e4-72d229bca2af
				- int[][] odds = new int[NMAX + 1][];
		- -
	- Chapter 4: Objects and Classes
		- -
			- Constructs an object that represents the current date. #flashcard
				- static LocalDate now()
		- -
		- -
			- Constructs an object that represents the given date. #flashcard
				- static LocalDate of(int year, int month, int day)
		- -