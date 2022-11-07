# Core Java Volume I—Fundamentals

deck:: [[O'Reilly-Learning::Core Java Volume I—Fundamentals]]\
author:: [[None]]\
full-title:: "Core Java Volume I—Fundamentals"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/core-java-volume/9780135167199/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Chapter 1: An Introduction to Java
- id:: 63639916-bd1d-4bb5-bd79-3adeb89000ce
   Why the 'Java' name? #flashcard 
    Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java.
-
### Chapter 2: The Java Programming Environment
- id:: 63639916-be57-4f65-8fbf-a824f8f691dd
   About the shebang in Java 11 #flashcard 
    In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
-
### Chapter 3: Fundamental Programming Structures in Java
- id:: 63639916-6802-48c7-b02b-e48f0b901612
   How do you define a long literal? #flashcard 
    Long integer numbers have a suffix L or l (for example, 4000000000L)
-
- id:: 63639916-5cea-409f-b37e-6695ae6eba6a
   How do you define a float literal? #flashcard 
    Numbers of type float have a suffix F or f (for example, 3.14F)
-
- id:: 63639916-c319-4c6a-a711-d5acd8261e60
   Where do you have to declare variables in Java? #flashcard 
    In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
-
- id:: 63639916-dc2f-4f20-9784-f9d3d53f0c45
   [CODE]
   Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard 
    enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
-
- id:: 63639916-0e08-476e-8214-511384f2ad66
   [CODE]
   Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard 
    Size s = Size.MEDIUM;
-
- id:: 63639916-7e44-4aab-853e-7ca7a8bc17e5
   What is String::blank()? #flashcard 
    boolean blank() 11
     returns true if the string is empty or consists of whitespace.
-
- id:: 63639916-6513-4c18-bbcc-65911d08cafd
  
  String trim() #flashcard
-
- id:: 63639916-86a4-4dd0-8cb6-76eebe743e03
  
  String strip() #flashcard
-
- id:: 63639916-fefa-4db7-ba5a-d8aeded57a21
   What does String::repeat do? #flashcard 
    String repeat(int count) 11
     returns a string that repeats this string count times.
-
- id:: 63639916-c272-4947-80ac-a9343e9a81e1
   Tip about your journey #flashcard 
    It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
-
- id:: 63639916-e61c-4eed-97c9-52ba4d819c05
   [CODE]
   Create a StringBuilder object #flashcard 
    StringBuilder builder = new StringBuilder();
-
- id:: 63639916-5129-4dcf-82bf-5a60a8b2d8bc
   [CODE]
   Append some content to a StringBuilder variable #flashcard 
    builder.append(str);
-
- id:: 63639916-5818-4bb9-b11d-d874045785f8
   [CODE]
   Print a StringBuffer 'builder' variable #flashcard 
    String completedString = builder.toString();
-
- id:: 63639916-e699-47a0-80a2-3393f75d04f2
   [CODE]
   Declare and define a Scanner variable. #flashcard 
    Scanner in = new Scanner(System.in);
-
- id:: 63639916-22a1-4c56-9798-f58c0eab034e
   [CODE]
   Example of a printf() #flashcard 
    System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
-
- id:: 63639916-8ed5-4b01-b308-da21b6cd27b6
   [CODE] Make a separate thousands, and two decimal float number #flashcard 
    System.out.printf("%,.2f", 10000.0 / 3.0);
-
- id:: 63639916-b2c3-42ba-b3cc-6819d0e42f2e
  
  case SMALL: // no need to use Size.SMALL #flashcard
-
- id:: 63639916-15df-474d-a3ee-14d19d6cf29c
   [CODE] Clone an array #flashcard 
    int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
-
- id:: 63639916-752c-4a27-873e-fe959a4fa558
   [CODE] Ordena un array #flashcard 
    Arrays.sort(a)
-
- id:: 63639916-1c8f-4aca-ab24-60e315e72164
   [CODE] Define una matriz que no sea fija #flashcard 
    int[][] odds = new int[NMAX + 1][];
-
### Chapter 4: Objects and Classes
- id:: 63639916-7204-499d-aeaf-2721e2e8f979
   Constructs an object that represents the current date. #flashcard 
    static LocalDate now()
-
- id:: 63639916-c524-425a-802b-33262431dc9e
   Constructs an object that represents the given date. #flashcard 
    static LocalDate of(int year, int month, int day)
-