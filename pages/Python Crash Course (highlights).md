title:: Python Crash Course (highlights)
deck:: [[O'Reilly-Learning::Python Crash Course]]
author:: [[Eric Matthes]]
full-title:: "Python Crash Course"
category:: #books

tags:: O'Reilly-Learning Python

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 2 VARIABLES AND SIMPLE DATA TYPES
	- 3 INTRODUCING LISTS
	- 4 WORKING WITH LISTS
	- 11 TESTING YOUR CODE
		- -
			- Variable names can contain only letters, numbers, and underscores. They can start with a letter or an underscore, but not with a number. For instance, you can call a variable message_1 but not 1_message. #flashcard
			  id:: 635faa3b-b218-4925-855c-15bacf4c509b
		- -
		- -
			- Show the last item of the list bicycles. #flashcard
			  id:: 635faa3b-63a7-4856-a1cd-775e568a83c8
				- print(bicycles[-1])
		- -
		- -
			- Remove the last item of the list motorcycles, 
			  id:: 635faa3b-b90c-44bc-a53d-9ee73ac24d86
			  then show the resultant list, 
			  then show the removed object
			  [call it removed_item] #flashcard
				- popped_motorcycle = motorcycles.pop()
				  ➌ print(motorcycles)
				  ➍ print(popped_motorcycle)
		- -
		- -
			- Save in a variable named first_owned the (just removed) element with index 0 of the list motorcycles #flashcard
			  id:: 3277b60f-d1a3-4f0b-8c3b-b6ffd7009932
				- first_owned = motorcycles.pop(0)
		- -
		- -
			- Steps to create tests in Python #flashcard
			  id:: 635faa3b-a392-4c89-a4d8-087342c3be62
				- To write a test case for a function, import the unittest module and the function you want to test. Then create a class that inherits from unittest.TestCase, and write a series of methods to test
		- -
		- -
			- universe_age = 14_000_000_000 #flashcard
			  id:: 635faa3b-d371-4712-b5fe-f18d7d88d816
		- -
		- -
			- Sometimes you won’t know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the remove() method. #flashcard
			  id:: c78a7324-6be6-4377-abc0-bed301eae79b
		- -
		- -
			- The Python variables you’re using at this point should be lowercase. You won’t get errors if you use uppercase letters, but uppercase letters in variable names have special meanings that we’ll discuss in later chapters. #flashcard
			  id:: 690d7903-9ad0-4f78-b682-38e7f03b2b8a
		- -
	- 9 CLASSES
		- -
			- How do we call a testing function? #flashcard
			  id:: e3e6d419-95c4-47c1-b7ab-9d8a7a257188
				- Any method that starts with test_ will be run automatically when we run test_name_function.py.
		- -
		- -
			- Show a variable named status inside a string (in Python 3) #flashcard
			  id:: 1e08f40f-82de-43e5-8cfd-22d913be477a
				- message = f"My first bicycle was a {bicycles[0].title()}."
		- -
		- -
			- 'Steal' the element with value 'ducati' from the motorcycles list #flashcard
			  id:: 635faa3b-9fa2-4389-ba44-87aa9b1f9243
				- motorcycles.remove('ducati')
		- -
		- -
			- It’s much better to think of variables as labels that you can assign to values. You can also say that a variable references a certain value. #flashcard
			  id:: 4d3ac1d3-25df-4949-bf8c-6fa855e2cd0f
		- -
		- -
			- Add 'ducati' at the end of the list motorcycles #flashcard
			  id:: 635faa3b-4a82-46b1-96ef-a776fd4fd69f
				- motorcycles.append('ducati')
		- -
		- -
			- 'Steal' the element with content 'ducati' from the motorcycles list.
			  id:: 635faa3b-9ec7-4bdc-8468-9ae57b2c0551
			  [Use the already defined variable named my_brand for this task] #flashcard
				- motorcycles.remove(too_expensive)
		- -
		- -
			- Function to get the size of the list cars #flashcard
			  id:: f772dfc0-0898-4bf6-b829-7e185eecfeca
				- len(cars)
		- -
		- -
			- How would you define a constructor of a child class in Python? #flashcard
			  id:: 635faa3b-5f58-4fef-a0c3-60007d7c2b97
				- def __init__(self, make, model, year):
				           """Initialize attributes of the parent class."""
				  ➍         super().__init__(make, model, year)
		- -
		- -
			- A method is an action that Python can perform on a piece of data. #flashcard
			  id:: 4d1f3baa-a1ab-40a8-987a-9dfa80f8ef1d
		- -
		- -
			- Construct a list named bicycles which contains the items:
			  id:: eda28f35-e086-42ef-80d1-d05982129b93
			  * 'trek'
			  * 'cannondale'
			  * 'redline'
			  * 'specialized' #flashcard
				- bicycles = ['trek', 'cannondale', 'redline', 'specialized']
		- -
		- -
			- Show the first element of the list bicycles. #flashcard
			  id:: 08ebf3b5-10ea-41a9-8333-cee4712f1ddd
				- print(bicycles[0])
		- -
		- -
			- Insert 'ducati' at the beginning of the list motorcycles without using square brackets: #flashcard
			  id:: cf043330-a252-4ec8-934f-d615b1db18c8
				- motorcycles.insert(0, 'ducati')
		- -
		- -
			- Order alphabetically a list named cars. Make this change permanent. #flashcard
			  id:: 635faa3b-27b1-4c86-8713-cb6854139411
				- cars.sort()
		- -
		- -
			- hese strings are called f-strings. The f is for format, because Python formats the string by replacing the name of any variable in braces with its value. #flashcard
			  id:: ce6b74f2-a739-411a-b991-2ca039845f5b
		- -
		- -
			- Remove the first element of the list motorcycles #flashcard
			  id:: 27905e46-a8ee-4136-89ed-20b3ce83044e
				- del motorcycles[0]
		- -
		- -
			- Order alphabetically inversed a list named cars. Make this change permanent. #flashcard
			  id:: 635faa3b-9b0d-44fe-b95f-3f7f404aec8a
				- cars.sort(reverse=True)
		- -
		- -
			- To maintain the original order of a list but present it in a sorted order, you can use the #flashcard
			  id:: 635faa3b-b4e4-4354-bdff-b76768efc865
		- -
		- -
			- F-strings were first introduced in Python 3.6 #flashcard
			  id:: 635faa3b-d7a1-4e1d-aca3-c51751b6105c
		- -
		- -
			- Show an alphabetically ordered list named cars. Make this change temporal. #flashcard
			  id:: b81e8927-2ca3-4aa6-adcf-e65fd9346322
				- print(sorted(cars))
		- -
		- -
			- Sometimes you won't know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the #flashcard
			  id:: 635faa3b-8a19-4965-983e-e2f5cf6fdcb8
		- -
		- -
			- Python programmers use all capital letters to indicate a variable should be treated as a constant and never be changed #flashcard
			  id:: 635faa3b-42a0-4c2a-9cb1-25d8e49ea818
		- -
		- -
			- Make the order of the list cars inverse. #flashcard
			  id:: 635faa3b-e3f1-421e-90e2-0c4512879fb3
				- cars.reverse()
		- -
		- -
			- Is it possible to reassign a tuple's content? #flashcard
			  id:: 635faa3b-28c9-4ad0-80c4-29352be13d16
				- Although you can't modify a tuple, you can assign a new value to a variable that represents a tuple.
		- -
		- -
			- Python considers the first item in a list to be at position 0, not position 1 #flashcard
			  id:: f22e4552-d4e4-4798-ab01-288c5e79b5fd
		- -
		- -
			- Show the numbers: [1, 4] #flashcard
			  id:: e2c33370-bcc1-4fab-b6f7-58bafd2e5557
				- for value in range(1, 5):
				    print(value)
		- -
		- -
			- A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item's index, just as you would for a list. #flashcard
			  id:: 635faa3b-6e29-48ef-97c7-514bc6b6c3ef
		- -
		- -
			- Python has a special syntax for accessing the last element in a list. By asking for the item at index -1, Python always returns the last item in the list: #flashcard
			  id:: e0942b34-8969-4b89-94f8-65c87adb17b4
		- -
		- -
			- Show in a slice the first three items of the list players. #flashcard
			  id:: 635faa3b-27e1-43f0-ac11-b5c6aa0e86c5
				- print(players[0:3])
		- -
		- -
			- Copy the list my_foods to the list friend_foods without affectations. #flashcard
			  id:: 635faa3b-d337-4fa2-b7aa-7a67b2bf3b96
				- friend_foods = my_foods[:]
		- -
		- -
			- Remember that each time you use pop(), the item you work with is no longer stored in the list. #flashcard
			  id:: e32e6d17-8b0a-45d2-af51-4103c6ae8501
		- -
		- -
			- [List Comprehension]
			  id:: 5c4849f3-a9c3-4759-89ab-bcfae656593b
			  Begin with a descriptive name for the list, such as squares. Next, open a set of square brackets and define the expression for the values you want to store in the new list. In this example the expression is value**2, which raises the value to the second power. Then, write a for loop to generate the numbers you want to feed into the expression, and close the square brackets. The for loop in this example is for value in range [1, 10] #flashcard
				- squares = [value**2 for value in range(1, 11)]
		- -
		- -
			- Show in a slice the second, third and fourth items of the list players #flashcard
			  id:: 635faa3b-3cd1-4925-95eb-4d2f02cbb133
				- print(players[1:4])
		- -
		- -
			- alphabetically #flashcard
			  id:: 687b4d01-a23b-4845-a5d4-a47a27760278
		- -
		- -
			- Construct a list with the numbers: [1, 5] #flashcard
			  id:: 76915ba3-0245-465c-a71d-9dae0a44a880
				- numbers = list(range(1, 6))
		- -
		- -
			- Notice that reverse() doesn’t sort backward alphabetically; it simply reverses the order of the list: #flashcard
			  id:: 1372fdf1-a359-4d0e-a82c-25be2c52f113
		- -
		- -
			- Another way of access to an element in a dict instead of indexes in square brackets #flashcard
			  id:: 635faa3b-7e7b-4370-b8be-01af78f104a5
				- For dictionaries, specifically, you can use the get() method to set a default value that will be returned if the requested key doesn’t exist.
		- -
		- -
			- The PEP 8 guidelines for line length are not set in stone, and some teams prefer a 99-character limit. #flashcard
			  id:: 63eb1a16-bdf8-4150-aa3d-b30c33f98ff3
		- -
		- -
			- keep in mind when writing your own for loops that you can choose any name you want for the temporary variable that will be associated with each value in the list. However, it’s helpful to choose a meaningful name that represents a single item from the list. #flashcard
			  id:: 635faa3b-3bd7-4074-af65-cd4f262a50fe
		- -
		- -
			- How can you split a string in multiple lines? #flashcard
			  id:: d67673f0-5bdb-4b13-82ed-6c1ee582cef3
				- print(f"You ordered a {pizza['crust']}-crust pizza "
				       "with the following toppings:")
		- -
		- -
			- Tuples are technically defined by the presence of a comma; the parentheses make them look neater and more readable. If you want to define a tuple with one element, you need to include a trailing comma: #flashcard
			  id:: a262aa36-3795-4a88-b4fa-56f94acffeeb
		- -
		- -
			- Using singular and plural names can help you identify whether a section of code is working with a single element from the list or the entire list. #flashcard
			  id:: 635faa3b-1eb0-4f2e-86a6-3ba952abccbb
		- -
		- -
			- If you omit the first index in a slice, Python automatically starts your slice at the beginning of the list: #flashcard
			  id:: 8c96f8e7-49e3-4ee4-acc4-719045e2162d
		- -
		- -
			- You can avoid unexpected indentation errors by indenting only when you have a specific reason to do so. #flashcard
			  id:: 635faa3b-9db0-4a07-8528-789826e35350
		- -
	- 6 DICTIONARIES
		- -
			- The colon at the end of a for statement tells Python to interpret the next line as the start of a loop. #flashcard
			  id:: 89b12ec8-b503-47b4-ab84-1306aa8c74ec
		- -
		- -
			- Build a dict named alien_0 with:
			  id:: 190928e9-0663-44c3-9ee2-269afc32ad8f
			  color ---> green
			  points ---> 50 #flashcard
				- alien_0 = {'color': 'green', 'points': 5}
		- -
		- -
			- If you want to make a list of numbers, you can convert the results of range() directly into a list using the list() function. When you wrap list() around a call to the range() function, the output will be a list of numbers. #flashcard
			  id:: 525a8aa3-c9b2-4af9-85e5-7e2191c77f06
		- -
	- 8 FUNCTIONS
		- -
			- A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item’s index, just as you would for a list. #flashcard
			  id:: 635faa3b-3ace-4e8c-948a-2cd008ca216d
		- -
		- -
			- How should I use the import's in Python? #flashcard
			  id:: e5018d01-1b7a-4700-b463-58d9f2df5171
				- The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that's easy to read and understand.
		- -
	- 10 FILES AND EXCEPTIONS
		- -
			- To do any work with a file, even just printing its contents, you first need to open the file to access it. The open() function needs one argument: the name of the file you want to open. Python looks for this file in the directory where the program that’s currently being executed is stored. #flashcard
			  id:: cf0c5409-4f2c-40bb-b938-e6279e26f939
		- -
		- -
			- The keyword with closes the file once access to it is no longer needed. #flashcard
			  id:: 635faa3b-dcf4-4d9b-802a-b3d97e00d37c
		- -
		- -
			- u'll often want to run through all entries in a list, performing the same task with each item. For example, in a game you might want to move every element on the screen by the same amount, or in a list of numbers you might want to perform the same statistic #flashcard
			  id:: 22b005fb-ab2b-451c-9b9c-649f4ee9e127
		- -
		- -
			- Is it possible to reassign a tuple's content? #flashcard
			  id:: e8a6cf46-3ffc-4243-b2f0-6ddfd15bb78c
				- Although you can’t modify a tuple, you can assign a new value to a variable that represents a tuple.
		- -
		- -
			- How do you call a base class' constructor? #flashcard
			  id:: e2a5de9f-311a-4243-84e2-41fa92659a0b
				- super().__init__(make, model, year)
		- -
		- -
			- How should I use the import's in Python? #flashcard
			  id:: 635faa3b-8245-4bca-980f-034dc9b9390f
				- The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that’s easy to read and understand.
		- -
		- -
			- Build a dict named alien_0 with:
			  id:: 635faa3b-66f5-446c-bf8a-da5c34a11999
			  color ---> green
			  points ---> 50 #flashcard
				- alien_0 = {'color': 'green', 'points': 5}
		- -
		- -
			- Add a new key-value entry to an existing dict in Python.
			  id:: 635faa3b-fdfd-41f2-b111-527c12af5282
			  Values x-0, y-25.
			  
			  BEFORE:
			  my_dict = {'color': 'green', 'points': 5} #flashcard
				- ➊ alien_0['x_position'] = 0
				  ➋ alien_0['y_position'] = 25
		- -
		- -
			- Remove the entry with key ‘points’ from the dict alien. #flashcard
			  id:: 2582d457-4350-4623-b144-cdfd54938f17
				- del alien_0['points']
		- -
		- -
			- Access to a dict but printing a message in case of error.
			  id:: 635faa3b-80fe-4e16-a0f5-d9da9bb746b3
			  dict: my_map
			  key: ‘point’
			  Message: ‘unassigned’
			  Variable: point_value #flashcard
				- point_value = alien_0.get('points', 'No point value assigned.')
		- -
		- -
			- Loop over dict user_0 with its separate parts #flashcard
			  id:: 635faa3b-ee6e-46e7-8fc0-39f3679ea7ce
				- for key, value in user_0.items():
		- -
		- -
			- Iterate over the keys of a dict fav_langs {name:value} #flashcard
			  id:: cca7740d-91b7-4bd2-ab2a-ad96793551cf
				- for name in favorite_languages.keys():
				       print(name.title())
		- -
		- -
			- Tell another use of keys() in Python aside looping #flashcard
			  id:: 635faa3b-f141-4e37-9c5d-8440720f2136
				- The keys() method isn’t just for looping: it actually returns a list of all the keys, and the line at ➊ simply checks if 'erin' is in this list.
		- -
		- -
			- Iterate over the content of a dict fav_langs on a loop {key: content} #flashcard
			  id:: 635faa3b-8825-4f35-b71d-bb64f8b61ee0
				- for language in favorite_languages.values():
		- -
		- -
			- Iterate over the content of a dict without repeating.
			  id:: 5f895da7-9ca4-4517-98ff-8173eee83f64
			  Dict: fav_langs #flashcard
				- for language in set(favorite_languages.values()):
		- -
		- -
			- Repeat a message ‘me’ 30 times in Python. #flashcard
			  id:: 635faa3b-fbcc-42a6-a556-10dbd494e06b
				- for alien_number in range(30):
		- -
		- -
			- What are the differences between:
			  id:: 635faa3b-8650-4767-9be3-a53f20fafa47
			  
			  describe_pet(animal_type='hamster', pet_name='harry')
			  
			  describe_pet(‘hamster', ‘harry') #flashcard
				- The function describe_pet() hasn’t changed. But when we call the function, we explicitly tell Python which parameter each argument should be matched with. When Python reads the function call, it knows to assign the argument 'hamster' to the parameter animal_type and the argument 'harry' to pet_name. The output correctly shows that we have a hamster named Harry.
				  
				  The order of keyword arguments doesn’t matter because Python knows where each value should go.
		- -
		- -
			- Print via a function in Python a list without being able to modify it. #flashcard
			  id:: 6a55ebbc-8577-4064-b0fd-c87a439a0623
				- print_models(unprinted_designs[:], completed_models)
		- -
		- -
			- Design a function which contains unlimited arguments. #flashcard
			  id:: 7000edb5-e560-4642-88e7-fe544bae54dc
				- def make_pizza(*toppings):
				    """Print the list of toppings that have been requested."""
				    print(toppings)
		- -
		- -
			- Explain how unlimited function parameters works in Python #flashcard
			  id:: 25b06acc-0bac-4e6b-bf9b-c62b5ff91699
				- The asterisk in the parameter name *toppings tells Python to make an empty tuple called toppings and pack whatever values it receives into this tuple. The print() call in the function body produces output showing that Python can handle a function call with one value and a call with three values. It treats the different calls similarly. Note that Python packs the arguments into a tuple, even if the function receives only one value
		- -
		- -
			- Can you pass infinite key-value entries to a function in Python? #flashcard
			  id:: 635faa3b-256a-438c-9e27-6e4c8a487a73
				- def build_profile(first, last, **user_info):
				       """Build a dictionary containing everything we know about a user."""
				  ➊     user_info['first_name'] = first
				       user_info['last_name'] = last
				       return user_info
		- -
		- -
			- Bring the module ‘pizza’ into your scope to use pizza.make_pizza() #flashcard
			  id:: 635faa3b-0230-4665-b5ff-66d4a873a0cb
				- import pizza
		- -
		- -
			- Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza().
			  id:: 635faa3b-d7cd-4c46-bd61-349b92fa7f8d
			  
			  Use it. #flashcard
				- from pizza import make_pizza
		- -
		- -
			- Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza(). Use an alias.
			  id:: b43cf3a2-e92a-43db-90bc-d4579ed1b528
			  
			  Use it. #flashcard
				- from pizza import make_pizza as mp
		- -
		- -
			- Bring a module ‘pizza’ to your scope but using an abbreviation.
			  id:: 3dad54ef-b370-4174-9a18-3f101ab53d81
			  
			  Use it. #flashcard
				- import pizza as p
		- -
		- -
			- Build a constructor in Python #flashcard
			  id:: 90c50e84-84fc-454f-bb4d-985aee440fa3
				- def __init__(self, name, age):
				           """Initialize name and age attributes."""
				  ➍         self.name = name
				           self.age = age
		- -
		- -
			- Define a method in Python #flashcard
			  id:: 635faa3b-dab2-4637-8b02-c0945cf94129
				- def sit(self):
				           """Simulate a dog sitting in response to a command."""
				           print(f"{self.name} is now sitting.")
		- -
		- -
			- Construct an object my_dog by calling the constructor Dog with the arguments:
				- my_dog = Dog('Willie', 6)
		- -
		- -
			- How do you call a base class' constructor from the subclass? #flashcard
			  id:: 635faa3b-dcf7-4dfc-91f8-cd046843ace3
				- def __init__(self, make, model, year):
				           """Initialize attributes of the parent class."""
				  ➍         super().__init__(make, model, year)
		- -
		- -
			- How do you read a text file? #flashcard
			  id:: 635faa3b-b76b-4610-abb2-65be56cc7b16
				- with open('pi_digits.txt') as file_object:
				    contents = file_object.read()
				  print(contents)
		- -
		- -
			- Should I close a file in Python or not? #flashcard
			  id:: 635faa3b-553d-4e6b-8e6c-6145d6ca9f1a
				- Notice how we call open() in this program but not close(). You could open and close the file by calling open() and close(), but if a bug in your program prevents the close() method from being executed, the file may never close. This may seem trivial, but improperly closed files can cause data to be lost or corrupted. And if you call close() too early in your program, you’ll find yourself trying to work with a closed file (a file you can’t access), which leads to more errors. It’s not always easy to know exactly when you should close a file, but with the structure shown here, Python will figure that out for you. All you have to do is open the file and work with it as desired, trusting that Python will close it automatically when the with block finishes execution.
		- -
		- -
			- Forward slashes OR backslashes in Python? #flashcard
			  id:: 635faa3b-997f-4195-bb39-fa1caaf4da8a
				- Windows systems use a backslash (\) instead of a forward slash (/) when displaying file paths, but you can still use forward slashes in your code.
		- -
		- -
			- Example to read a file line by line #flashcard
			  id:: 635faa3b-f24d-4303-bbc5-cfb999bf92d7
				- filename = 'pi_digits.txt'
				  
				  ➋ with open(filename) as file_object:
				  ➌     for line in file_object:
				          print(line)
		- -
		- -
			- Write some text in a file in Python. #flashcard
			  id:: 635faa3b-815f-4596-9f63-0843810c5c69
				- filename = 'programming.txt'
				  
				  ➊ with open(filename, 'w') as file_object:
				  ➋     file_object.write("I love programming.")
		- -
		- -
			- Different file modes in Python. #flashcard
			  id:: 635faa3b-5549-4623-88df-8d0e14d5fb0f
				- You can open a file in read mode ('r'), write mode ('w'), append mode ('a'), or a mode that allows you to read and write to the file ('r+'). If you omit the mode argument, Python opens the file in read-only mode by default.
		- -
		- -
			- What does ‘else’ mean in a Exception? #flashcard
			  id:: 635faa3b-14c8-4fcd-9f8d-91c00c646047
				- Any code that depends on the try block succeeding is added to the else block. In this case if the division operation is successful, we use the else block to print the result
		- -
		- -
			- Example of exception in Python #flashcard
			  id:: 635faa3b-3056-4c2d-8d28-4ad9a3d3d61e
				- try:
				           answer = int(first_number) / int(second_number)
				  ➋     except ZeroDivisionError:
				           print("You can't divide by 0!")
				  ➌     else:
				           print(answer)
		- -