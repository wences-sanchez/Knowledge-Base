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
- id:: 63c669f1-1ab6-4851-8aee-4e0956ea694f
   About the shebang in Java 11 #flashcard 
    In JDK 11, the javac command is not required with a single source file. This feature is intended to support shell scripts starting with a “shebang” line #!/path/to/java.
-
### Chapter 3: Fundamental Programming Structures in Java
- id:: 63c669f1-2db6-4af6-933c-927a53fa851d
   How do you define a long literal? #flashcard 
    Long integer numbers have a suffix L or l (for example, 4000000000L)
-
- id:: 63c669f1-646e-4029-99c4-d33c7252729c
   How do you define a float literal? #flashcard 
    Numbers of type float have a suffix F or f (for example, 3.14F)
-
- id:: 63c669f1-7f04-44b2-9963-8c715f892cad
   What is String::blank()? #flashcard 
    boolean blank() 11
     returns true if the string is empty or consists of whitespace.
-
- id:: 63c669f1-bcad-4f36-b369-33a7f5d1f605
   What does String::repeat do? #flashcard 
    String repeat(int count) 11
     returns a string that repeats this string count times.
-
- id:: 63c669f1-19fc-4ab8-9871-210191336cca
   Tip about your journey #flashcard 
    It is plainly impossible to remember all useful classes and methods. Therefore, it is essential that you become familiar with the online API documentation that lets you look up all classes and methods in the standard library.
-
- id:: 63c669f1-e1bd-4bd0-81c1-28bc2db2fb49
  
  case SMALL: // no need to use Size.SMALL #flashcard
-
### Chapter 1: An Introduction to Java
- id:: 63c669f1-6e21-42da-bfb6-7b1c39df9d52
   Why the 'Java' name? #flashcard 
    Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java
-
- id:: 63c669f1-ba3b-4f25-b550-2fa7fca39e86
   [CODE] Define una matriz que no sea fija #flashcard 
    int[][] odds = new int[NMAX + 1][];
-
- id:: 63c669f1-860d-42d9-a9c5-2d35bd29149a
   [CODE] Ordena un array #flashcard 
    Arrays.sort(a
-
- id:: 63c669f1-4fc2-4e1a-994e-671893b905d5
   [CODE] Clone an array #flashcard 
    int[] copiedLuckyNumbers = Arrays.copyOf(luckyNumbers, luckyNumbers.length);
-
- id:: 63c669f1-eee3-452a-b8b0-829fab372ff3
   [CODE] Make a separate thousands, and two decimal float number #flashcard 
    System.out.printf("%,.2f", 10000.0 / 3.0);
-
- id:: 63c669f1-a515-4209-90e9-6951b387fcf1
   [CODE]
   Example of a printf() #flashcard 
    System.out.printf("Hello, %s. Next year, you'll be %d", name, age);
-
- id:: 63c669f1-ee88-4fe4-ae2c-8170a059a729
   [CODE]
   Declare and define a Scanner variable. #flashcard 
    Scanner in = new Scanner(System.in);
-
- id:: 63c669f1-427b-4360-bc61-ec0c934301e9
   [CODE]
   Print a StringBuffer 'builder' variable #flashcard 
    String completedString = builder.toString();
-
- id:: 63c669f1-302d-412d-a17e-152988c36934
   [CODE]
   Append some content to a StringBuilder variable #flashcard 
    builder.append(str)
-
- id:: 63c669f1-e3e5-40fd-a006-794bac203190
   [CODE]
   Create a StringBuilder object #flashcard 
    StringBuilder builder = new StringBuilder();
-
- id:: 63c669f1-5f58-4203-8c4c-7732a0fe0f61
  
  (String str) #flashcard
-
- id:: 63c669f1-e344-4f68-acc2-42cda8b4ccda
  
  String trim() #flashcard
-
- id:: 63c669f1-17bd-4afb-b0c3-2e17c8b0db03
   [CODE]
   Declare a variable s of type Size[enum] and initialize it with the field MEDIUM. #flashcard 
    Size s = Size.MEDIUM;
-
- id:: 63c669f1-0c78-41cf-a0c9-7bcf0f43390b
   [CODE]
   Create a enum type with name Size and fields: SMALL, MEDIUM, LARGE and EXTRA_LARGE #flashcard 
    enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
-
- id:: 63c669f1-1d34-41e7-97ad-ad51bafe3949
   Where do you have to declare variables in Java? #flashcard 
    In Java, it is considered good style to declare variables as closely as possible to the point where they are first used.
-
### Chapter 4: Objects and Classes
- id:: 63c669f1-3eeb-4806-9533-08699396c5da
   Constructs an object that represents the given date. #flashcard 
    static LocalDate of(int year, int month, int day)
-
- id:: 63c669f1-6a84-48cb-a727-5f7e97da7040
   Constructs an object that represents the current date. #flashcard 
    static LocalDate now()
-