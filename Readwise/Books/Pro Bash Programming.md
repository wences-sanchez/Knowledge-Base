# Pro Bash Programming

deck:: [[O'Reilly-Learning::Pro Bash Programming]]\
author:: [[Chris F. A. Johnson, Jayant Varma]]\
full-title:: "Pro Bash Programming"\
category:: #books\
\
tags:: Bash O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9781484201213/)
## Highlights
### Chapter 2: Input, Output, and Throughput
- id:: 63c66a19-57fe-4bab-9aac-f58d19182fa2
  
  If you limit the use of echo to situations where there cannot be a conflict, that is, where you are sure the arguments do not begin with -n and do not contain escape sequences, you will be fairly safe. For everything else (or if you’re not sure), use printf. #flashcard
-
- id:: 63c66a19-3a41-4f7b-a226-3a9ab3be8b0d
  
  When a command reads a character or a line, it reads from the standard input stream, which is the keyboard. When it prints information, it is sent to the standard output, your monitor. The third stream, standard error, is also connected to your monitor; as the name implies, it is used for error messages. These streams are referred to by numbers, called file descriptors (FDs). These are 0, 1, and 2, respectively. The stream names are also often contracted to stdin, stdout, and stderr. #flashcard
-
- id:: 63c66a19-bec9-4401-8734-680a2f53b7b4
   How could you send the error output to an unused file? #flashcard 
    printf '%s\n%v\n' OK? Oops! 2>/dev/null
-
- id:: 63c66a19-5f5e-4ec8-ab19-541418f31cc5
   How could you send the standard output to FILE and the standard error to that same file? #flashcard 
    printf '%s\n%v\n' OK? Oops! > FILE 2>&1
-
- id:: 63c66a19-f6ab-41d3-9bb3-653d16c6f5bd
   What nonstandard syntax has Bash for redirecting both standard output and standard error to the same place? #flashcard 
    &> FILE
-
- id:: 63c66a19-6ee8-4a15-8adc-ebe5b076c662
   How can you parse a content into your program? #flashcard 
    The read commandis a builtin command that reads from the standard input. By default, it reads until a newline is received. The input is stored in one or more variables given as arguments:
     read var
     If more than one variable is given, the first word (the input up to the first space or tab) is assigned to the first variable, the second word is assigned to the second variable, and so on, with any leftover words assigned to the last one:
     $ read a b c d
     January February March April May June July August
     $ echo $a
     January
     $ echo $b
     February
     $ echo $c
     March
     $ echo $d
     April May June July August
-
- id:: 63c66a19-b70d-4e40-a3c2-80c9384bdfb2
   How can you mix two file descriptors in one token in Bash (bit more complex way)? #flashcard 
    Instead of sending output to a file, it can be redirected to another I/O stream by using >&N where N is the number of the file descriptor. This command sends both standard output and standard error to FILE:
     printf '%s\n%v\n' OK? Oops! > FILE 2>&1
     Here, the order is important. The standard output is sent to FILE, and then standard error is redirected to where standard output is going. If the order is reversed, the effect is different.
-
- id:: 63c66a19-562e-4861-94b2-6e825c7d4ba4
   How can you use *command substitution* in Bash? #flashcard 
    Command Substitution
     The output of a command can be stored in a variable using command substitution. There are two forms for doing this. The first, which originated in the Bourne shell, uses backticks:
     date=`date`
     The newer (and recommended) syntax is as follows:
     date=$( date )
-
### Chapter 3: Looping and Branching
- id:: 63c66a19-8fd2-4531-ad96-043183ed9633
   About evaluating an arithmetic expression inside Bash (i.e. in a loop) #flashcard 
    8.
     (( … )): Evaluate an Arithmetic Expression
     A nonstandard feature, (( arithmetic expression )) returns false if the arithmetic expression evaluates to zero and returns true otherwise. The portable equivalent uses test and the POSIX syntax for shell arithmetic:
     test $(( a - 2 )) -ne 0
     [ $a != 0 ]
-
- id:: 63c66a19-5531-45d3-8482-d9b00bf6eae3
   About evaluating an arithmetic expression inside Bash (i.e. in a loop) #flashcard 
    8.
     (( … )): Evaluate an Arithmetic Expression
     A nonstandard feature, (( arithmetic expression )) returns false if the arithmetic expression evaluates to zero and returns true otherwise. The portable equivalent uses test and the POSIX syntax for shell arithmetic:
     test $(( a - 2 )) -ne 0
     [ $a != 0 ]
-
- id:: 63c66a19-6b88-4ed1-81ee-079650b5b0f5
   How could you manage a one-line error inside a Bash script? #flashcard 
    To change directory and exit with an error if cd fails, use this:
     cd "$HOME/bin" || exit 1
-
- id:: 63c66a19-4af8-4dd3-a11e-8d071599efe5
   Syntax of case statement in Bash #flashcard 
    A case statement compares a word (usually a variable) against one or more patterns and executes the commands associated with that pattern. The patterns are pathname expansion patterns using wildcards (* and ?) and character lists and ranges ([...]). The syntax is as follows:
     case WORD in
     PATTERN) COMMANDS ;;
     PATTERN) COMMANDS ;; ## optional
     esac
-
### Chapter 6: Shell Functions
- id:: 63c66a19-6be9-472c-8902-111caa5924ea
   Syntax of function prototypes in Bash #flashcard 
    When the Bourne shell added functions in 1984, the syntax (which was later included in ksh and adopted by the POSIX standard) was as follows:
     name() <compound command>
     bash allows either syntax as well as the hybrid:
     function name() <compound command>
-