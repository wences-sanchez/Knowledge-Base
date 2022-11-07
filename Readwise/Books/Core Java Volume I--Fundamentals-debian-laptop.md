# Core Java Volume I--Fundamentals

deck:: [[O'Reilly-Learning::Core Java Volume I--Fundamentals]]\
author:: [[None]]\
full-title:: "Core Java Volume I--Fundamentals"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9780135167199_83c7f8df-08aa-4096-8796-af2f38bb7348_temp/)
## Highlights
### Chapter 2: The Java Programming Environment
- id:: 63639916-52dc-463b-b4b4-63aa8d900a0c
   About the shebang in Java 11 #flashcard 
    In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
-
### Chapter 3: Fundamental Programming Structures in Java
- id:: 63639916-c710-489a-a95a-230096fbd33e
   How do you define a long literal? #flashcard 
    Long integer numbers have a suffix L or l (for example, 4000000000L)
-
- id:: 63639916-7cc0-4b41-993f-69468af50554
   How do you define a float literal? #flashcard 
    Numbers of type float have a suffix F or f (for example, 3.14F)
-
- id:: 63639916-e8f9-46c1-84ed-cfe3d70f3ad5
   What is String::blank()? #flashcard 
    boolean blank() 11
     returns true if the string is empty or consists of whitespace.
-
- id:: 63639916-e9ee-4ffd-889c-c08303654c9c
   What does String::repeat do? #flashcard 
    String repeat(int count) 11
     returns a string that repeats this string count times.
-
- id:: 63639916-975c-428e-ab5d-d506d9123766
   Tip about your journey #flashcard 
    It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
-
- id:: 63639916-b37c-415e-8b63-424ca6571528
  
  case SMALL: // no need to use Size.SMALL #flashcard
-
### Chapter 1: An Introduction to Java
- id:: 63639916-5c24-4758-a088-af21960300aa
   Why the 'Java' name? #flashcard 
    Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java
-
- id:: 63639916-45cc-402d-8bc1-c7c1ff299506
   [CODE] Define una matriz que no sea fija #flashcard 
    int[][] odds = new int[NMAX + 1][];
-
- id:: 63639916-db66-4cf9-8c06-78ee7265d96e
   [CODE] Ordena un array #flashcard 
    Arrays.sort(a
-
- id:: 63639916-e65c-4665-a3de-6ec68369bc16
   [CODE] Clone an array #flashcard 
    int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
-
- id:: 63639916-266c-4530-8ed6-d078279f801b
   [CODE] Make a separate thousands, and two decimal float number #flashcard 
    System.out.printf("%,.2f", 10000.0 / 3.0);
-
- id:: 63639916-d7cf-4808-89cc-78f84b062ff8
   [CODE]
   Example of a printf() #flashcard 
    System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
-
- id:: 63639916-be26-4ac2-8235-a85a9e6ef50b
   [CODE]
   Declare and define a Scanner variable. #flashcard 
    Scanner in = new Scanner(System.in);
-
- id:: 63639916-8d33-4daa-9550-acc984c5d214
   [CODE]
   Print a StringBuffer 'builder' variable #flashcard 
    String completedString = builder.toString();
-
- id:: 63639916-e80e-4534-b8d1-84e1c409c7de
   [CODE]
   Append some content to a StringBuilder variable #flashcard 
    builder.append(str)
-
- id:: 63639916-4997-4c2d-947a-82469d085fd5
   [CODE]
   Create a StringBuilder object #flashcard 
    StringBuilder builder = new StringBuilder();
-
- id:: 63639916-ae5f-43ea-8beb-d61a68787dca
  
  (String str) #flashcard
-
- id:: 63639916-e70a-48db-b9ed-4f642f1a4769
  
  String trim() #flashcard
-
- id:: 63639916-ab3b-492a-8602-771c6f4d8f0f
   [CODE]
   Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard 
    Size s = Size.MEDIUM;
-
- id:: 63639916-35cb-4012-8197-b6bbbd93c54d
   [CODE]
   Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard 
    enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
-
- id:: 63639916-08c6-4871-b112-dd3601f4eb7a
   Where do you have to declare variables in Java? #flashcard 
    In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
-
### Chapter 4: Objects and Classes
- id:: 63639916-7e2a-4eef-b0bd-053454a87f5c
   Constructs an object that represents the given date. #flashcard 
    static LocalDate of(int year, int month, int day)
-
- id:: 63639916-8189-4ec0-ba5c-5b3585d62261
   Constructs an object that represents the current date. #flashcard 
    static LocalDate now()
-