title:: Introduction to Computation and Programming Using Python (highlights)
deck:: [[Other-Books::Introduction to Computation and Programming Using Python]]
author:: [[John V. Guttag]]
full-title:: "Introduction to Computation and Programming Using Python"
category:: #books

- ![](https://m.media-amazon.com/images/I/710JwUhWSVL._SY160.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- A computer does two things, and two things only: it performs calculations and it remembers the results of those calculations. #flashcard
		  id:: a79a03c5-6e67-48ee-bf68-8744504d199b
		- tags:: [[blue]]
		- ([Location 473](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=473))
	- -
	- -
		- Imperative knowledge is “how to” knowledge, or recipes for deducing information. #flashcard
		  id:: a125ffa2-0562-48c4-b58f-d9f9e13e518d
		- tags:: [[blue]]
		- ([Location 490](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=490))
	- -
	- -
		- an algorithm is a finite list of instructions describing a set of computations that when executed on a set of inputs will proceed through a sequence of well-defined states and eventually produce an output. #flashcard
		  id:: f0eb205e-f27c-43c1-ac5e-e16c44f83043
		- tags:: [[pink]]
		- ([Location 518](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=518))
	- -
	- -
		- The Church-Turing thesis states that if a function is computable, a Turing Machine can be programmed to compute it. #flashcard
		  id:: e8a9ab6a-add7-4620-8315-033dcb04f422
		- ([Location 559](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=559))
	- -
	- -
		- Explain the Halt-Problem. #flashcard
		  id:: fb881470-b7fb-4c28-8dc8-98de9e450501
			- The “if” in the Church-Turing thesis is important. Not all problems have computational solutions. Turing showed, for example, that it is impossible to write a program that takes an arbitrary program as input, and prints true if and only if the input program will run forever. This is known as the halting problem.
		- tags:: [[cs]] [[pink]]
		- ([Location 560](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=560))
	- -
	- -
		- Of course, some things may be easier to program in a particular language, but all languages are fundamentally equal with respect to computational power. #flashcard
		  id:: a4735783-6fcf-4b51-a8f7-73231ffa82b6
		- ([Location 566](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=566))
	- -
	- -
		- Exhaustive enumeration is a search technique that works only if the set of values being searched includes the answer. #flashcard
		  id:: 3438c0d6-9f59-40ea-8c35-c7fc078b939b
		- tags:: [[pink]]
		- ([Location 1597](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=1597))
	- -
	- -
		- Bisección #flashcard
		  id:: 8f699504-181f-46ef-83cb-67d74070bd88
			- notice that at each iteration of the loop, the size of the space to be searched is cut in half. For this reason, the algorithm is called bisection search. Bisection search is a huge improvement over our earlier algorithm, which reduced the search space by only a small amount at each iteration.
		- tags:: [[cs]] [[blue]]
		- ([Location 1666](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=1666))
	- -
	- -
		- lambda sequence of variable names : expression #flashcard
		  id:: 1baa9da0-88f3-4b5f-a131-eb64dab32599
		- tags:: [[orange]]
		- ([Location 2273](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2273))
	- -
	- -
		- Name Scalar and Structured types in Python. #flashcard
		  id:: 8c144eaf-66b7-4b16-b59d-a7ac8021d18a
			- The numeric types int and float are scalar types. That is to say, objects of these types have no accessible internal structure. In contrast, str can be thought of as a structured, or non-scalar, type. We can use indexing to extract individual characters from a string and slicing to extract substrings.
		- ([Location 2367](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2367))
	- -
	- -
		- Do the tuples and strings in Python...
		  id:: 13669010-ba3c-4338-bc7d-0abdd73ac2ce
		  * have the same elements type?
		  * have the same sequence behaviour? #flashcard
			- Like strings, tuples are immutable ordered sequences of elements. The difference is that the elements of a tuple need not be characters.
		- ([Location 2377](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2377))
	- -
	- -
		- However, if you keep repeating the mantra, “In Python a variable is merely a name, i.e., a label that can be attached to an object,” it will bring you clarity. #flashcard
		  id:: 82318c1f-a7c2-4255-a33f-641787504d4b
		- tags:: [[python]] [[pink]]
		- ([Location 2506](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2506))
	- -
	- -
		- [expr for elem in iterable if test] #flashcard
		  id:: d4a31155-c47d-4e3e-b466-c69fa6079f4a
		- tags:: [[orange]]
		- ([Location 2691](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2691))
	- -
	- -
		- The map function is often used with a for loop. When used in a for loop, map behaves like the range function in that it returns one value for each iteration of the loop. #flashcard
		  id:: c43112bf-4ac3-487a-ab5e-e233003a2b4a
		- tags:: [[pink]]
		- ([Location 2765](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2765))
	- -
	- -
		- Example of map() #flashcard
		  id:: 0038e87e-4b88-4ea2-bc60-5b40d8277792
			- For example, the code ﻿for i in map(lambda x: x**2, [2, 6, 4]):     print(i)  prints ﻿4 36 16
		- tags:: [[orange]]
		- ([Location 2769](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2769))
	- -
	- -
		- Can you access a set by index? #flashcard
		  id:: 306dedca-bdd7-4ca8-aa62-61ac1464faa2
			- Since the elements of a set are unordered, attempting to index into a set, e.g., evaluating baseball_teams[0], generates a runtime error.
		- tags:: [[python]] [[pink]]
		- ([Location 2833](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2833))
	- -
	- -
		- dict comprehension syntax #flashcard
		  id:: fa323eba-d93f-406b-a1a1-f028b557573f
			- {key: value for id1, id2 in iterable if test}
		- tags:: [[orange]]
		- ([Location 2980](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2980))
	- -
	- -
		- The key difference (other than the use of set braces rather than square braces) is that it uses two values to create each element of the dictionary, and allows (but does not require) the #flashcard
		  id:: 9c481c75-68a3-437f-9281-edf4b3ce5249
		- ([Location 2982](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=2982))
	- -
	- -
		- What is the difference between Testing and Debugging? #flashcard
		  id:: 82b15c66-331e-47f8-919e-95cfa756fd51
			- Testing is the process of running a program to try and ascertain whether it works as intended. Debugging is the process of trying to fix a program that you already know does not work as intended.
		- ([Location 3516](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3516))
	- -
	- -
		- Another positive feature of black-box testing is that it is robust with respect to implementation changes. Since the test data is generated without knowledge of the implementation, the tests need not be changed when the implementation is changed. #flashcard
		  id:: 23995182-4a7b-455e-bde0-f19734b1f274
		- ([Location 3563](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3563))
	- -
	- -
		- Tip for unit tests #flashcard
		  id:: 2c4267bb-91cc-4037-81dc-79467556cec6
			- It will work most of the time, but not when L1 and L2 refer to the same list. Any test suite that did not include a call of the form copy(L, L), would not reveal the bug.
		- ([Location 3595](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3595))
	- -
	- -
		- Steps for white-box tests #flashcard
		  id:: ec23a580-7be7-43bb-a50e-9e8f17e3f5fc
			- Despite the limitations of glass-box testing, a few rules of thumb are usually worth following: Exercise both branches of all if statements. Make sure that each except clause (see Chapter 9) is executed. For each for loop, have test cases in which ○ The loop is not entered (e.g., if the loop is iterating over the elements of a list, make sure that it is tested on the empty list). ○ The body of the loop is executed exactly once. ○ The body of the loop is executed more than once. For each while loop ○ Look at the same kinds of cases as when dealing with for loops. ○ Include test cases corresponding to all possible ways of exiting the loop. For example, for a loop starting with   while len(L) > 0 and not L[i] == e  find cases where the loop exits because len(L) is greater than zero and cases where it exits because L[i] == e. For recursive functions, include test cases that cause the function to return with no recursive calls, exactly one recursive call, and more than one recursive call.
		- ([Location 3630](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3630))
	- -
	- -
		- Usual cycle of tests in practice #flashcard
		  id:: 106459b9-b7b8-4ef5-8578-a103827721f1
			- Testing is often thought of as occurring in two phases. One should always start with unit testing. During this phase, testers construct and run tests designed to ascertain whether individual units of code (e.g., functions) work properly. This is followed by integration testing, which is designed to ascertain whether groups of units function properly when combined. Finally, functional testing is used to check if the program as a whole behaves as intended.
		- ([Location 3648](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3648))
	- -
	- -
		- Why is Functional Testing harder #flashcard
		  id:: b7c5566f-262b-4b93-bfaa-97923a99763a
			- Functional testing is almost always the most challenging phase. The intended behavior of an entire program is considerably harder to characterize than the intended behavior of each of its parts. For example, characterizing the intended behavior of a word processor is considerably more challenging than characterizing the behavior of the subsystem that counts the number of characters in a document.
		- ([Location 3653](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3653))
	- -
	- -
		- Soy un nuevo =) #flashcard
		  id:: 003c9693-749a-451d-b592-9b4d6d9d1fca
			- software quality assurance (SQA)
		- ([Location 3657](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3657))
	- -
	- -
		- Difference between 'overt' and 'covert' bugs #flashcard
		  id:: 5f95a380-6ec1-405b-9488-ed242293fefa
			- Overt → covert: An overt bug has an obvious manifestation, e.g., the program crashes or takes far longer (maybe forever) to run than it should. A covert bug has no obvious manifestation. The program may run to conclusion with no problem—other than providing an incorrect answer.
		- ([Location 3702](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3702))
	- -
	- -
		- Differences between 'Persistent' and 'Intermittent' Bugs #flashcard
		  id:: 2222a6d8-f272-4b3f-8f7d-db5793f86123
			- Persistent → intermittent: A persistent bug occurs every time the program is run with the same inputs. An intermittent bug occurs only some of the time, even when the program is run on the same inputs and seemingly under the same conditions.
		- ([Location 3705](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3705))
	- -
	- -
		- Steps for debugging #flashcard
		  id:: c88f4754-eb31-4b29-a580-cf8e7046df36
			- Start by studying the available data. This includes the test results and the program text. Study all of the test results. Examine not only the tests that revealed the presence of a problem, but also those tests that seemed to work perfectly. Trying to understand why one test worked and another did not is often illuminating. When looking at the program text, keep in mind that you don't completely understand it. If you did, there probably wouldn't be a bug. Next, form a hypothesis that you believe to be consistent with all the data. The hypothesis could be as narrow as “if I change line 403 from x < y to x <= y, the problem will go away” or as broad as “my program is not working because I forgot about the possibility of aliasing in multiple places.” Next, design and run a repeatable experiment with the potential to refute the hypothesis. For example, you might put a print statement before and after each loop. If these are always paired, then the hypothesis that a loop is causing nontermination has been refuted. Decide before running the experiment how you would interpret various possible results. All humans are subject to what psychologists call confirmation bias—we interpret information in a way that reinforces what we want to believe. If you wait until after you run the experiment to think about what the results should be, you are more likely to fall prey to wishful thinking. Finally, keep a record of what experiments you have tried. When you've spent many hours changing your code trying to track down an elusive bug, it's easy to forget what you have already tried. If you aren't careful, you can waste way too many hours trying the same experiment (or more likely an experiment that looks different but will give you the same information) over and over again.
		- ([Location 3738](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3738))
	- -
	- -
		- How to use the bisection search to better debugging #flashcard
		  id:: 431feb6a-76c3-475a-85b2-91e827f40c58
			- Often the best way to do this is to conduct a bisection search. Find some point about halfway through the code, and devise an experiment that will allow you to decide if there is a problem before that point that might be related to the symptom.
		- ([Location 3777](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3777))
	- -
	- -
		- Tip for a better approach in Testing #flashcard
		  id:: 8e054985-e341-4080-a9cb-8dd3b3751912
			- Stop asking yourself why the program isn't doing what you want it to. Instead, ask yourself why it is doing what it is. That should be an easier question to answer, and will probably be a good first step in figuring out how to fix the program.
		- tags:: [[pink]]
		- ([Location 3844](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3844))
	- -
	- -
		- Keep in mind that the bug is probably not where you think it is. #flashcard
		  id:: c307d944-f26b-428e-8c5a-692b4834f324
		- ([Location 3846](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3846))
	- -
	- -
		- Stop debugging and start writing documentation. This will help you approach the problem from a different perspective. #flashcard
		  id:: cb5d1a04-239b-4705-88a1-3f43550b375a
		- tags:: [[pink]]
		- ([Location 3853](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3853))
	- -
	- -
		- When you think you have found a bug in your code, the temptation to start coding and testing a fix is almost irresistible. It is often better, however, to pause. Remember that the goal is not to fix one bug, but to move rapidly and efficiently towards a bug-free program. #flashcard
		  id:: c041c9a9-0d06-4218-b927-1be28afd1d36
		- tags:: [[pink]]
		- ([Location 3859](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3859))
	- -
	- -
		- Always make sure that you can get back to where you are. Nothing is more frustrating than realizing that a long series of changes have left you farther from the goal than when you started, and having no way to get back to your starting point. #flashcard
		  id:: 435c002c-a9dc-4ed2-88b8-031a113916c5
		- tags:: [[pink]]
		- ([Location 3868](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=3868))
	- -
	- -
		- What is an abstract data type? #flashcard
		  id:: cabf8ebe-464f-42b8-8e84-40e2d89088b9
			- An abstract data type is a set of objects and the operations on those objects.
		- ([Location 4149](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=4149))
	- -
	- -
		- What is the purpose of an ADT? #flashcard
		  id:: 128c18d0-ab6c-4f36-81d7-05c0f0aebf0a
			- These are bound together so that programmers can pass an object from one part of a program to another, and in doing so provide access not only to the data attributes of the object but also to operations that make it easy to manipulate that data. The specifications of those operations define an interface between the abstract data type and the rest of the program. The interface defines the behavior of the operations—what they do, but not how they do it. The interface thus provides an abstraction barrier that isolates the rest of the program from the data structures, algorithms, and code involved in providing a realization of the type abstraction. Programming is about managing complexity in a way that facilitates change. Two powerful mechanisms are available for accomplishing this: decomposition and abstraction. Decomposition creates structure in a program, and abstraction suppresses detail. The key is to suppress the appropriate details. This is where data abstraction hits the mark. We can create domain-specific types that provide a convenient abstraction. Ideally, these types capture concepts that will be relevant over the lifetime of a program.
		- ([Location 4149](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=4149))
	- -
	- -
		- For simplicity, we will use a random access machine as our model of computation. In a random access machine, steps are executed sequentially, one at a time.66 A step is an operation that takes a fixed amount of time, such as binding a variable to an object, making a comparison, executing an arithmetic operation, or accessing an object in memory. #flashcard
		  id:: 4761aa01-c42b-4db2-9aea-e9265a444ace
		- tags:: [[cs]]
		- ([Location 4880](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=4880))
	- -
	- -
		- The worst-case provides an upper bound on the running time. #flashcard
		  id:: 3073c26b-7c9d-418b-9fba-ebf6fd2e343d
		- tags:: [[cs]]
		- ([Location 4909](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=4909))
	- -
	- -
		- Por esta razón hay que tener en cuenta el camino crítico #flashcard
		  id:: 3a5c2a5d-4679-4022-a5c7-722f5a84e01c
			- It should be immediately obvious that as n gets large, worrying about the difference between 5n and 5n+2 is kind of silly. For this reason, we typically ignore additive constants when reasoning about running time.
		- tags:: [[cs]]
		- ([Location 4924](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=4924))
	- -
	- -
		- About Big O #flashcard
		  id:: 5fadbfcf-cf0d-4a9f-86f8-8b8a73c74833
			- The most commonly used asymptotic notation is called “Big O” notation.67 Big O notation is used to give an upper bound on the asymptotic growth (often called the order of growth) of a function. For example, the formula f(x) ∈ O(x2) means that the function f grows no faster than the quadratic polynomial x2, in an asymptotic sense.
		- tags:: [[cs]]
		- ([Location 4989](https://readwise.io/to_kindle?action=open&asin=B08C6YH4XK&location=4989))
	- -