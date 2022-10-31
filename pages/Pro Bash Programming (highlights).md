title:: Pro Bash Programming (highlights)
deck:: [[O'Reilly-Learning::Pro Bash Programming]]
author:: [[Chris F. A. Johnson, Jayant Varma]]
full-title:: "Pro Bash Programming"
category:: #books

tags:: Bash O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Chapter 2: Input, Output, and Throughput
		- -
		- If you limit the use of echo to situations where there cannot be a conflict, that is, where you are sure the arguments do not begin with -n and do not contain escape sequences, you will be fairly safe. For everything else (or if you’re not sure), use printf. #flashcard
		- -
		- -
		- When a command reads a character or a line, it reads from the standard input stream, which is the keyboard. When it prints information, it is sent to the standard output, your monitor. The third stream, standard error, is also connected to your monitor; as the name implies, it is used for error messages. These streams are referred to by numbers, called file descriptors (FDs). These are 0, 1, and 2, respectively. The stream names are also often contracted to stdin, stdout, and stderr. #flashcard
		- -
		- -
		- printf '%s\n%v\n' OK? Oops! 2>/dev/null #flashcard
			- How could you send the error output to an unused file?
		- -
		- -
		- printf '%s\n%v\n' OK? Oops! > FILE 2>&1 #flashcard
			- How could you send the standard output to FILE and the standard error to that same file?
		- -
		- -
		- &> FILE #flashcard
			- What nonstandard syntax has Bash for redirecting both standard output and standard error to the same place?
		- -
		- -
		- The read commandis a builtin command that reads from the standard input. By default, it reads until a newline is received. The input is stored in one or more variables given as arguments:
		  
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
		  April May June July August #flashcard
			- How can you parse a content into your program?
		- -
		- -
		- Instead of sending output to a file, it can be redirected to another I/O stream by using >&N where N is the number of the file descriptor. This command sends both standard output and standard error to FILE:
		  
		  printf '%s\n%v\n' OK? Oops! > FILE 2>&1
		  Here, the order is important. The standard output is sent to FILE, and then standard error is redirected to where standard output is going. If the order is reversed, the effect is different. #flashcard
			- How can you mix two file descriptors in one token in Bash (bit more complex way)?
		- -
		- -
		- Command Substitution
		  
		  The output of a command can be stored in a variable using command substitution. There are two forms for doing this. The first, which originated in the Bourne shell, uses backticks:
		  
		  date=`date`
		  The newer (and recommended) syntax is as follows:
		  
		  date=$( date ) #flashcard
			- How can you use *command substitution* in Bash?
		- -
	- Chapter 3: Looping and Branching
		- -
		- 8.
		  
		  (( … )): Evaluate an Arithmetic Expression
		  
		  A nonstandard feature, (( arithmetic expression )) returns false if the arithmetic expression evaluates to zero and returns true otherwise. The portable equivalent uses test and the POSIX syntax for shell arithmetic:
		  
		  test $(( a - 2 )) -ne 0
		  [ $a != 0 ] #flashcard
			- About evaluating an arithmetic expression inside Bash (i.e. in a loop)
		- -
		- -
		- 8.
		  
		  (( … )): Evaluate an Arithmetic Expression
		  
		  A nonstandard feature, (( arithmetic expression )) returns false if the arithmetic expression evaluates to zero and returns true otherwise. The portable equivalent uses test and the POSIX syntax for shell arithmetic:
		  
		  test $(( a - 2 )) -ne 0
		  [ $a != 0 ] #flashcard
			- About evaluating an arithmetic expression inside Bash (i.e. in a loop)
		- -
		- -
		- To change directory and exit with an error if cd fails, use this:
		  
		  cd "$HOME/bin" || exit 1 #flashcard
			- How could you manage a one-line error inside a Bash script?
		- -
		- -
		- A case statement compares a word (usually a variable) against one or more patterns and executes the commands associated with that pattern. The patterns are pathname expansion patterns using wildcards (* and ?) and character lists and ranges ([...]). The syntax is as follows:
		  
		  case WORD in
		  PATTERN) COMMANDS ;;
		  PATTERN) COMMANDS ;; ## optional
		  esac #flashcard
			- Syntax of case statement in Bash
		- -
	- Chapter 6: Shell Functions
		- -
		- When the Bourne shell added functions in 1984, the syntax (which was later included in ksh and adopted by the POSIX standard) was as follows:
		  
		  name() <compound command>
		  bash allows either syntax as well as the hybrid:
		  
		  function name() <compound command> #flashcard
			- Syntax of function prototypes in Bash
		- -