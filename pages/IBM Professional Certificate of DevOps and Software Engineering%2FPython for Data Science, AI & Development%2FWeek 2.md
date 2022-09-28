title:: IBM Professional Certificate of DevOps and Software Engineering/Python for Data Science, AI & Development/Week 2
tags:: Coursera, DevOps, Python

- #tags #Coursera #DevOps #python
-
- ## Lists and Tuples
	- ### Tuples
		- Tuples are delimited by parenthesis
		- It's like an array, but immutable
			- New assigned variables reference the same tuple
		- If you do `my_tuple[1:4]` to `my_tuple = (0, 1, 2, 3, 4, 5)`, you get:
			- `(1, 2, 3)`
	- ### Flashcards
		- About tuples in Python #flashcard
			- Tuples are delimited by parenthesis
			- It's like an array, but immutable
				- New assigned variables reference the same tuple
			- If you do `my_tuple[1:4]` to `my_tuple = (0, 1, 2, 3, 4, 5)`, you get:
				- `(1, 2, 3)`
	- ### Lists
		- Lists are mutable. We can change them.
		- ```python
		  list_original = ["Wences", 3.14, 1987]
		  list_original.extend(["pop", 10])
		  
		  print(list_original) # ["Wences", 3.14, 1987, "pop", 10]
		  
		  list_original = ["Wences", 3.14, 1987]
		  list_original.append(["pop", 10])
		  
		  print(list_original) # ["Wences", 3.14, 1987, ["pop", 10]]
		  ```
		-
		- We can delete an element of a list with:
			- `del(my_list[i])`
		- We can split a string into an array with:
			- `"A B C D".split() # --> ["A", "B", "C", "D"]`
			- `"A,B,C,D".split(",") # --> ["A", "B", "C", "D"]`
		-
		- The list work like references.
			- If we change a variable wich was pointing to a previous list, that one will also change
			- The solution is clone the lists with:
				- `cloned_list = list_original[:]`
				-
		- ### Flashcards
			- How can you add elements (or entire lists) to an already existing list in Python? #flashcard
				- Lists are mutable. We can change them.
				- ```python
				  list_original = ["Wences", 3.14, 1987]
				  list_original.extend(["pop", 10])
				  
				  print(list_original) # ["Wences", 3.14, 1987, "pop", 10]
				  
				  list_original = ["Wences", 3.14, 1987]
				  list_original.append(["pop", 10])
				  
				  print(list_original) # ["Wences", 3.14, 1987, ["pop", 10]]
				  ```
			- How can you remove an element of a list in Python? #flashcard
				- We can delete an element of a list with:
					- `del(my_list[i])`
			- How can you divide a string into elements of an array? #flashcard
				- We can split a string into an array with:
					- `"A B C D".split() # --> ["A", "B", "C", "D"]`
					- `"A,B,C,D".split(",") # --> ["A", "B", "C", "D"]`
				-
			- How can you properly use a copy of a list variable in Python? #flashcard
				- The list work like references.
					- If we change a variable wich was pointing to a previous list, that one will also change
					- The solution is clone the lists with:
						- `cloned_list = list_original[:]`
						-
	-
	-
	-
		-