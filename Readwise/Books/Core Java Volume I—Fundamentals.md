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
- Why the 'Java' name? #flashcard 
    Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java.
-
### Chapter 2: The Java Programming Environment
- About the shebang in Java 11 #flashcard 
    In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
-
### Chapter 3: Fundamental Programming Structures in Java
- How do you define a long literal? #flashcard 
    Long integer numbers have a suffix L or l (for example, 4000000000L)
-
- id:: 63c669f2-790f-4944-9328-f43429b524ae
   How do you define a float literal? #flashcard 
    Numbers of type float have a suffix F or f (for example, 3.14F)
-
- id:: 63c669f2-11da-4c34-bc4d-84bed75fc219
   Where do you have to declare variables in Java? #flashcard 
    In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
-
- [CODE]
   Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard 
    enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
-
- id:: 63c669f2-d820-4a89-8b4f-b3584738911f
   [CODE]
   Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard 
    Size s = Size.MEDIUM;
-
- id:: 63c669f2-4ab5-47e9-b18d-a7cb1f46075d
   What is String::blank()? #flashcard 
    boolean blank() 11
     returns true if the string is empty or consists of whitespace.
-
- String trim() #flashcard
-
- String strip() #flashcard
-
- What does String::repeat do? #flashcard 
    String repeat(int count) 11
     returns a string that repeats this string count times.
-
- id:: 63c669f1-0c69-43c3-84bf-022dddd1456c
   Tip about your journey #flashcard 
    It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
-
- [CODE]
   Create a StringBuilder object #flashcard 
    StringBuilder builder = new StringBuilder();
-
- id:: 63c669f1-16be-44ea-baa7-0194ccb6585e
   [CODE]
   Append some content to a StringBuilder variable #flashcard 
    builder.append(str);
-
- [CODE]
   Print a StringBuffer 'builder' variable #flashcard 
    String completedString = builder.toString();
-
- [CODE]
   Declare and define a Scanner variable. #flashcard 
    Scanner in = new Scanner(System.in);
-
- id:: 63c669f1-49d2-4e13-873f-25e023103c65
   [CODE]
   Example of a printf() #flashcard 
    System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
-
- [CODE] Make a separate thousands, and two decimal float number #flashcard 
    System.out.printf("%,.2f", 10000.0 / 3.0);
-
- case SMALL: // no need to use Size.SMALL #flashcard
-
- id:: 63c669f1-5f06-442e-b94c-14c9e9f7c18b
   [CODE] Clone an array #flashcard 
    int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
-
- id:: 63c669f1-0a19-47b9-95c1-7e9dc2237ee3
   [CODE] Ordena un array #flashcard 
    Arrays.sort(a)
-
- id:: 63c669f1-0fee-45a7-8a14-1c90c81fa8fb
   [CODE] Define una matriz que no sea fija #flashcard 
    int[][] odds = new int[NMAX + 1][];
-
### Chapter 4: Objects and Classes
- id:: 63c669f1-507c-44fd-b1fd-88301fd8224d
   Constructs an object that represents the current date. #flashcard 
    static LocalDate now()
-
- Constructs an object that represents the given date. #flashcard 
    static LocalDate of(int year, int month, int day)
-