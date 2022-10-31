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
			  id:: 12a99c12-ddd9-41fd-ba6c-1d8c84819265
				- In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
		- -
	- Chapter 3: Fundamental Programming Structures in Java
		- -
			- How do you define a long literal? #flashcard
			  id:: 246a108e-6d32-4889-af51-f210bbef990b
				- Long integer numbers have a suffix L or l (for example, 4000000000L)
		- -
		- -
			- How do you define a float literal? #flashcard
			  id:: 02009c9e-0cd0-460a-b7c4-308f059fe74f
				- Numbers of type float have a suffix F or f (for example, 3.14F)
		- -
		- -
			- Where do you have to declare variables in Java? #flashcard
			  id:: 3aea2dc6-7b0a-4719-b864-4ae7990b91cb
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
			  id:: 654e9d77-1a44-4f83-bf21-a3ffbdd837a1
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
			  id:: 9bbb16b6-2107-45e1-8a55-5888938a3c32
		- -
		- -
			- What does String::repeat do? #flashcard
			  id:: 40e94b3f-f466-4168-bf17-797846c577e1
				- String repeat(int count) 11
				  returns a string that repeats this string count times.
		- -
		- -
			- Tip about your journey #flashcard
			  id:: aee191ac-4e59-4e9c-912c-41e1a1eb5b1a
				- It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
		- -
		- -
			- [CODE]
			  id:: b2d00de2-349a-4fe0-a725-bb1155b67601
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
			  id:: 855633dd-edb8-4a2a-9d8f-a243d1f18987
			  Print a StringBuffer 'builder' variable #flashcard
				- String completedString = builder.toString();
		- -
		- -
			- [CODE]
			  id:: 374835ac-88a5-42a9-9490-1a9f9acb3084
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
			  id:: 1ba20701-dbc8-4bf0-bf00-e555b48f8c9e
		- -
		- -
			- [CODE] Clone an array #flashcard
			  id:: f1e3c9ce-1152-4656-835c-8d42926571a5
				- int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
		- -
		- -
			- [CODE] Ordena un array #flashcard
			  id:: 4cdd449e-99ea-40ee-a2f1-0aad38825549
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
			  id:: 7703c55b-24dc-4924-affa-ee6ba8a7121b
				- static LocalDate now()
		- -
		- -
			- Constructs an object that represents the given date. #flashcard
			  id:: 117ac45b-8f4a-478a-93fd-3cb223b289f1
				- static LocalDate of(int year, int month, int day)
		- -