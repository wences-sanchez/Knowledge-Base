title:: Core Java Volume I--Fundamentals (highlights)
deck:: [[O'Reilly-Learning::Core Java Volume I--Fundamentals]]
author:: [[]]
full-title:: "Core Java Volume I--Fundamentals"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Chapter 2: The Java Programming Environment
		- -
			- About the shebang in Java 11 #flashcard
			  id:: 96eb1260-6cad-408f-a3c9-8832e86c1a3f
				- In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
		- -
	- Chapter 3: Fundamental Programming Structures in Java
		- -
			- How do you define a long literal? #flashcard
			  id:: 48e40b71-40e8-46f1-9d90-b51853dd74b6
				- Long integer numbers have a suffix L or l (for example, 4000000000L)
		- -
		- -
			- How do you define a float literal? #flashcard
			  id:: a86e6207-aae6-49a7-aa2d-8706757f9b29
				- Numbers of type float have a suffix F or f (for example, 3.14F)
		- -
		- -
			- What is String::blank()? #flashcard
			  id:: 7101fab4-754b-4f72-8970-4b9b26829fea
				- boolean blank() 11
				  returns true if the string is empty or consists of whitespace.
		- -
		- -
			- What does String::repeat do? #flashcard
			  id:: d311bb3d-a1bd-461a-a404-e13e1e881c7f
				- String repeat(int count) 11
				  returns a string that repeats this string count times.
		- -
		- -
			- Tip about your journey #flashcard
			  id:: 7c939222-820c-4a7c-842a-5022ed864c55
				- It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
		- -
		- -
			- case SMALL: // no need to use Size.SMALL #flashcard
			  id:: caa93f6f-e0ee-4888-99b5-5d393bef757c
		- -
	- Chapter 1: An Introduction to Java
		- -
			- Why the 'Java' name? #flashcard
			  id:: 51151867-40f2-4be6-8a51-c3b35a0f971d
				- Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java
		- -
		- -
			- [CODE] Define una matriz que no sea fija #flashcard
			  id:: 05e93df2-2db5-4b21-90cf-0e87d9566089
				- int[][] odds = new int[NMAX + 1][];
		- -
		- -
			- [CODE] Ordena un array #flashcard
			  id:: 2017b7f4-69fb-48a2-90ac-fda40e5a36f7
				- Arrays.sort(a
		- -
		- -
			- [CODE] Clone an array #flashcard
			  id:: 73a003dd-12a9-47ef-8ffa-80c755b3779e
				- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
		- -
		- -
			- [CODE] Make a separate thousands, and two decimal float number #flashcard
			  id:: af3e9583-4925-46ed-8cf6-c5112b763b0f
				- System.out.printf("%,.2f", 10000.0 / 3.0);
		- -
		- -
			- [CODE]
			  id:: 661345eb-4e21-4706-b417-76fa7496a7da
			  Example of a printf() #flashcard
				- System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
		- -
		- -
			- [CODE]
			  id:: 6b6dca15-483c-4c7b-a0cd-5570f6f3860b
			  Declare and define a Scanner variable. #flashcard
				- Scanner in = new Scanner(System.in);
		- -
		- -
			- [CODE]
			  id:: 20bb4db5-4da0-448e-a00f-1e81e9392e05
			  Print a StringBuffer 'builder' variable #flashcard
				- String completedString = builder.toString();
		- -
		- -
			- [CODE]
			  id:: 1da6e60f-383b-4f31-83b5-3fe4d9052a0d
			  Append some content to a StringBuilder variable #flashcard
				- builder.append(str)
		- -
		- -
			- [CODE]
			  id:: cc5faaa2-3775-4810-89ea-5d3661d6acbb
			  Create a StringBuilder object #flashcard
				- StringBuilder builder = new StringBuilder();
		- -
		- -
			- (String str) #flashcard
			  id:: 4e1c5e2b-4c03-471c-8075-1631f320ab47
		- -
		- -
			- String trim() #flashcard
			  id:: af18119d-4680-4934-a4c7-78893a9ed687
		- -
		- -
			- [CODE]
			  id:: 1f952a3a-eede-4b00-a5d8-84063306e9ed
			  Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard
				- Size s = Size.MEDIUM;
		- -
		- -
			- [CODE]
			  id:: 5593d1ed-a1fc-43c7-844d-493ddef4febb
			  Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard
				- enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
		- -
		- -
			- Where do you have to declare variables in Java? #flashcard
			  id:: 21ca54bf-84a6-469a-95c9-ac087ea5fc3c
				- In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
		- -
	- Chapter 4: Objects and Classes
		- -
			- Constructs an object that represents the given date. #flashcard
			  id:: 9e7f2d0a-cccd-437f-bced-bc326e533b74
				- static LocalDate of(int year, int month, int day)
		- -
		- -
			- Constructs an object that represents the current date. #flashcard
			  id:: 50cb9920-b745-474a-a181-1f529dfbd07c
				- static LocalDate now()
		- -