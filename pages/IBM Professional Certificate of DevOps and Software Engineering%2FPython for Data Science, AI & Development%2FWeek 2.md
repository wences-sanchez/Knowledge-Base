title:: IBM Professional Certificate of DevOps and Software Engineering/Python for Data Science, AI & Development/Week 2
tags:: Coursera, DevOps, Python
deck:: [[IBM-DevOps::Python for Data Science]]

-
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
		  id:: 634545b3-3025-41f5-a486-57c4645d97ef
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
			  id:: 634545b3-fdce-4aa4-960c-89e1f2de15c6
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
			  id:: 634545b3-fdc3-4283-abb8-c0c528d5808b
				- We can delete an element of a list with:
					- `del(my_list[i])`
			- How can you divide a string into elements of an array? #flashcard
			  id:: 634545b3-9a80-4785-a09e-b22303146f53
				- We can split a string into an array with:
					- `"A B C D".split() # --> ["A", "B", "C", "D"]`
					- `"A,B,C,D".split(",") # --> ["A", "B", "C", "D"]`
				-
			- How can you properly use a copy of a list variable in Python? #flashcard
			  id:: 634545b3-50ba-424c-9105-505dfe4e4082
				- The list work like references.
					- If we change a variable wich was pointing to a previous list, that one will also change
					- The solution is clone the lists with:
						- `cloned_list = list_original[:]`
			- How can you find an element inside a list (or tuple) in Python? #flashcard
			  id:: 634545b3-7145-4c2d-8a29-0be74f06b389
				- With: `my_list.index(element_to_search)`
-
-
- ## Dictionaries
	- A dictionary has keys and values instead of indexes and elements
	- We denote dictionaries with curly brackets (those keys have to be unique)
	- We can delete an element of a dictionary by putting the element instead its index
	-
	-
- ## Sets
	- We can turn a sequence into a set by casting it with `set()`
	- We use the method add() to insert an element to the set.
	- We can use the method my_set.remove(elem) to delete one.
	-
	- The intersection of two sets is denoted by `&`
	- The union of two sets is denoted by `set_1.union(set_2)`
	- We can check if a set is a subset of another by `set_1.issubset(set_2)`
	- We can check if a set is a superset of another by `set_1.issuperset(set_2)`
	- We difference of two sets is denoted by `set_1.difference(set_2)`
		- Those elements which are in set_1 and not in set_2
	-
	- ### Flashcards
		- About set operations in Python such as: build, insert, intersection, union, difference, subset, superset and inclusion. #flashcard
		  id:: 634545b3-a9c0-4f26-a4c0-1d804b4ae57a
			- We can turn a sequence into a set by casting it with `set()`
			- We use the method add() to insert an element to the set.
			- We can use the method my_set.remove(elem) to delete one.
			-
			- The intersection of two sets is denoted by `&`
			- The union of two sets is denoted by `set_1.union(set_2)`
			- We can check if a set is a subset of another by `set_1.issubset(set_2)`
			- We can check if a set is a superset of another by `set_1.issuperset(set_2)`
			- We difference of two sets is denoted by `set_1.difference(set_2)`
				- Those elements which are in set_1 and not in set_2
	-
	-
		-