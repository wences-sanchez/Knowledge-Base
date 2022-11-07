# Python Crash Course

deck:: [[O'Reilly-Learning::Python Crash Course]]\
author:: [[Eric Matthes]]\
full-title:: "Python Crash Course"\
category:: #books\
\
tags:: Python O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/python-crash-course/9781492071266/ibis_generated_cover_thumbnail.jpg)
## Highlights
### 2 VARIABLES AND SIMPLE DATA TYPES
### 3 INTRODUCING LISTS
### 4 WORKING WITH LISTS
### 11 TESTING YOUR CODE
- id:: 6363992d-f8ff-4c5f-954a-0cc55c2ae089
  
  Variable names can contain only letters, numbers, and underscores. They can start with a letter or an underscore, but not with a number. For instance, you can call a variable message_1 but not 1_message. #flashcard
-
- id:: 6363992d-5be5-40c5-bb9b-6b7190e21875
   Show the last item of the list bicycles. #flashcard 
    print(bicycles[-1])
-
- id:: 6363992d-1f59-4d06-84e3-b291fc5ca2e9
   Remove the last item of the list motorcycles, 
   then show the resultant list, 
   then show the removed object
   [call it removed_item] #flashcard 
    popped_motorcycle = motorcycles.pop()
     ➌ print(motorcycles)
     ➍ print(popped_motorcycle)
-
- id:: 6363992d-b651-40e3-96a9-1d7d177e3abb
   Save in a variable named first_owned the (just removed) element with index 0 of the list motorcycles #flashcard 
    first_owned = motorcycles.pop(0)
-
- id:: 6363992d-ea86-4c23-92ba-31df7bd360aa
   Steps to create tests in Python #flashcard 
    To write a test case for a function, import the unittest module and the function you want to test. Then create a class that inherits from unittest.TestCase, and write a series of methods to test
-
- id:: 6363992d-a8ae-41a1-93fe-ffa96cc08530
  
  universe_age = 14_000_000_000 #flashcard
-
- id:: 6363992d-1994-4303-acc1-609ecfe1ce45
  
  Sometimes you won’t know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the remove() method. #flashcard
-
- id:: 6363992d-28b3-447a-a568-ead42a191f96
  
  The Python variables you’re using at this point should be lowercase. You won’t get errors if you use uppercase letters, but uppercase letters in variable names have special meanings that we’ll discuss in later chapters. #flashcard
-
### 9 CLASSES
- id:: 6363992d-268d-4477-ad2e-92b51c63d628
   How do we call a testing function? #flashcard 
    Any method that starts with test_ will be run automatically when we run test_name_function.py.
-
- id:: 6363992d-547c-4777-b84d-929a269808e7
   Show a variable named status inside a string (in Python 3) #flashcard 
    message = f"My first bicycle was a {bicycles[0].title()}."
-
- id:: 6363992d-5682-40a6-82b0-2e0f9d75eab1
   'Steal' the element with value 'ducati' from the motorcycles list #flashcard 
    motorcycles.remove('ducati')
-
- id:: 6363992d-9239-49a4-ad7f-a00bded7562a
  
  It’s much better to think of variables as labels that you can assign to values. You can also say that a variable references a certain value. #flashcard
-
- id:: 6363992d-bdc6-4bd8-8890-e7c5ab078d81
   Add 'ducati' at the end of the list motorcycles #flashcard 
    motorcycles.append('ducati')
-
- id:: 6363992d-34c0-4c58-97f5-5e73aef236d2
   'Steal' the element with content 'ducati' from the motorcycles list.
   [Use the already defined variable named my_brand for this task] #flashcard 
    motorcycles.remove(too_expensive)
-
- id:: 6363992d-c030-4388-88cf-196d1fa0ca97
   Function to get the size of the list cars #flashcard 
    len(cars)
-
- id:: 6363992d-21e7-43a4-9a09-bbb8137acabc
   How would you define a constructor of a child class in Python? #flashcard 
    def __init__(self, make, model, year):
     """Initialize attributes of the parent class."""
     ➍ super().__init__(make, model, year)
-
- id:: 6363992d-d144-4f24-bc94-faaefba239f7
  
  A method is an action that Python can perform on a piece of data. #flashcard
-
- id:: 6363992d-f902-4c10-9b95-509d1f10fbeb
   Construct a list named bicycles which contains the items:
   * 'trek'
   * 'cannondale'
   * 'redline'
   * 'specialized' #flashcard 
    bicycles = ['trek', 'cannondale', 'redline', 'specialized']
-
- id:: 6363992d-130d-4eca-bd8f-e00aa0d41b1f
   Show the first element of the list bicycles. #flashcard 
    print(bicycles[0])
-
- id:: 6363992d-c349-4d69-9563-7bfb4c137c19
   Insert 'ducati' at the beginning of the list motorcycles without using square brackets: #flashcard 
    motorcycles.insert(0, 'ducati')
-
- id:: 6363992d-f89e-44c8-b829-a2ed18874460
   Order alphabetically a list named cars. Make this change permanent. #flashcard 
    cars.sort()
-
- id:: 6363992d-f2c0-4fca-9a09-761d2156f4a6
  
  hese strings are called f-strings. The f is for format, because Python formats the string by replacing the name of any variable in braces with its value. #flashcard
-
- id:: 6363992d-9e4f-43ab-a4b8-24937bbb59e9
   Remove the first element of the list motorcycles #flashcard 
    del motorcycles[0]
-
- id:: 6363992d-a7a1-4dce-b4d0-87fece1ab91f
   Order alphabetically inversed a list named cars. Make this change permanent. #flashcard 
    cars.sort(reverse=True)
-
- id:: 6363992d-4aba-4e75-9a57-3f394a106244
  
  To maintain the original order of a list but present it in a sorted order, you can use the #flashcard
-
- id:: 6363992d-fc2b-4023-b947-27ad0541e903
  
  F-strings were first introduced in Python 3.6 #flashcard
-
- id:: 6363992d-67eb-4fdc-889d-234391f8979c
   Show an alphabetically ordered list named cars. Make this change temporal. #flashcard 
    print(sorted(cars))
-
- id:: 6363992d-7039-415a-abf4-41c23c38dffb
  
  Sometimes you won't know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the #flashcard
-
- id:: 6363992d-fafd-48ee-8aeb-78c9d00afdc1
  
  Python programmers use all capital letters to indicate a variable should be treated as a constant and never be changed #flashcard
-
- id:: 6363992d-a32b-4935-9de1-d22f44dffa2b
   Make the order of the list cars inverse. #flashcard 
    cars.reverse()
-
- id:: 6363992d-a389-4f81-bcf3-5b85bcf7c56e
   Is it possible to reassign a tuple's content? #flashcard 
    Although you can't modify a tuple, you can assign a new value to a variable that represents a tuple.
-
- id:: 6363992d-936d-40e4-899f-a5fa50bad7ff
  
  Python considers the first item in a list to be at position 0, not position 1 #flashcard
-
- id:: 6363992d-fb90-4962-8c2d-5038fc17a861
   Show the numbers: [1, 4] #flashcard 
    for value in range(1, 5):
     print(value)
-
- id:: 6363992d-bfec-4662-ab13-9725517b2814
  
  A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item's index, just as you would for a list. #flashcard
-
- id:: 6363992d-164e-4f31-b413-eb0437097d23
  
  Python has a special syntax for accessing the last element in a list. By asking for the item at index -1, Python always returns the last item in the list: #flashcard
-
- id:: 6363992d-fa14-4036-85d2-0ee3e65e4922
   Show in a slice the first three items of the list players. #flashcard 
    print(players[0:3])
-
- id:: 6363992d-a099-40b4-9c3c-1ed0469d6455
   Copy the list my_foods to the list friend_foods without affectations. #flashcard 
    friend_foods = my_foods[:]
-
- id:: 6363992d-ce57-4c1b-805f-4c26982592fa
  
  Remember that each time you use pop(), the item you work with is no longer stored in the list. #flashcard
-
- [List Comprehension]
   Begin with a descriptive name for the list, such as squares. Next, open a set of square brackets and define the expression for the values you want to store in the new list. In this example the expression is value**2, which raises the value to the second power. Then, write a for loop to generate the numbers you want to feed into the expression, and close the square brackets. The for loop in this example is for value in range [1, 10] #flashcard 
    squares = [value**2 for value in range(1, 11)]
-
- id:: 6363992d-a745-45e4-b72a-ad4df170f11f
   Show in a slice the second, third and fourth items of the list players #flashcard 
    print(players[1:4])
-
- id:: 6363992d-8196-47af-b236-f18bb9e8d7d9
  
  alphabetically #flashcard
-
- id:: 6363992d-1a2a-4b61-a8fe-d8b548675bc9
   Construct a list with the numbers: [1, 5] #flashcard 
    numbers = list(range(1, 6))
-
- id:: 6363992d-d799-4086-b06b-6a4ca27f4354
  
  Notice that reverse() doesn’t sort backward alphabetically; it simply reverses the order of the list: #flashcard
-
- id:: 6363992d-c2fb-4223-8e07-1f017580f1c1
   Another way of access to an element in a dict instead of indexes in square brackets #flashcard 
    For dictionaries, specifically, you can use the get() method to set a default value that will be returned if the requested key doesn’t exist.
-
- id:: 6363992d-dc46-4d88-bd16-c25cf9b384ae
  
  The PEP 8 guidelines for line length are not set in stone, and some teams prefer a 99-character limit. #flashcard
-
- id:: 6363992d-bfb3-40c7-a04d-85ff8ce6ab1e
  
  keep in mind when writing your own for loops that you can choose any name you want for the temporary variable that will be associated with each value in the list. However, it’s helpful to choose a meaningful name that represents a single item from the list. #flashcard
-
- id:: 6363992d-9e11-4feb-9b5e-991ca64d954d
   How can you split a string in multiple lines? #flashcard 
    print(f"You ordered a {pizza['crust']}-crust pizza "
     "with the following toppings:")
-
- id:: 6363992d-d2e6-41f8-89a3-dbe0757c6a8e
  
  Tuples are technically defined by the presence of a comma; the parentheses make them look neater and more readable. If you want to define a tuple with one element, you need to include a trailing comma: #flashcard
-
- id:: 6363992d-fec1-4056-8e63-04c976fe54cc
  
  Using singular and plural names can help you identify whether a section of code is working with a single element from the list or the entire list. #flashcard
-
- id:: 6363992d-521c-48dc-b3b7-52c968864b05
  
  If you omit the first index in a slice, Python automatically starts your slice at the beginning of the list: #flashcard
-
- id:: 6363992d-4607-4b71-b922-0e26493bc075
  
  You can avoid unexpected indentation errors by indenting only when you have a specific reason to do so. #flashcard
-
### 6 DICTIONARIES
- id:: 6363992d-ec02-41b5-a57f-78d692c23f47
  
  The colon at the end of a for statement tells Python to interpret the next line as the start of a loop. #flashcard
-
- id:: 6363992d-e7ac-43ef-baa4-b7dafe0b6395
   Build a dict named alien_0 with:
   color ---> green
   points ---> 50 #flashcard 
    alien_0 = {'color': 'green', 'points': 5}
-
- id:: 6363992d-81d4-40bf-b19c-596531845e51
  
  If you want to make a list of numbers, you can convert the results of range() directly into a list using the list() function. When you wrap list() around a call to the range() function, the output will be a list of numbers. #flashcard
-
### 8 FUNCTIONS
- id:: 6363992d-b7a8-4900-b8aa-eb067dec3b12
  
  A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item’s index, just as you would for a list. #flashcard
-
- id:: 6363992d-130e-4924-97de-202fc07b13b9
   How should I use the import's in Python? #flashcard 
    The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that's easy to read and understand.
-
### 10 FILES AND EXCEPTIONS
- id:: 6363992d-beab-4111-a379-f82f16a1e409
  
  To do any work with a file, even just printing its contents, you first need to open the file to access it. The open() function needs one argument: the name of the file you want to open. Python looks for this file in the directory where the program that’s currently being executed is stored. #flashcard
-
- id:: 6363992d-1fff-428d-9887-d96f9bff0fc3
  
  The keyword with closes the file once access to it is no longer needed. #flashcard
-
- id:: 6363992d-a39e-4a9f-a81f-4458c1db3be9
  
  u'll often want to run through all entries in a list, performing the same task with each item. For example, in a game you might want to move every element on the screen by the same amount, or in a list of numbers you might want to perform the same statistic #flashcard
-
- id:: 6363992d-233f-4748-91ce-915876989a01
   Is it possible to reassign a tuple's content? #flashcard 
    Although you can’t modify a tuple, you can assign a new value to a variable that represents a tuple.
-
- id:: 6363992d-b46a-4231-8a8e-fc49858042e8
   How do you call a base class' constructor? #flashcard 
    super().__init__(make, model, year)
-
- id:: 6363992d-bd89-4264-91b2-e9ce46fbb2a3
   How should I use the import's in Python? #flashcard 
    The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that’s easy to read and understand.
-
- id:: 6363992d-fe0a-46b1-a86b-c1793052d29d
   Build a dict named alien_0 with:
   color ---> green
   points ---> 50 #flashcard 
    alien_0 = {'color': 'green', 'points': 5}
-
- id:: 6363992d-3081-490d-82f8-57a29ea2f153
   Add a new key-value entry to an existing dict in Python.
   Values x-0, y-25.
   BEFORE:
   my_dict = {'color': 'green', 'points': 5} #flashcard 
    ➊ alien_0['x_position'] = 0
     ➋ alien_0['y_position'] = 25
-
- id:: 6363992d-5b90-4c54-b37d-63cc1077e810
   Remove the entry with key ‘points’ from the dict alien. #flashcard 
    del alien_0['points']
-
- id:: 6363992d-0ff8-4435-b3ea-2ec8c09d6db5
   Access to a dict but printing a message in case of error.
   dict: my_map
   key: ‘point’
   Message: ‘unassigned’
   Variable: point_value #flashcard 
    point_value = alien_0.get('points', 'No point value assigned.')
-
- id:: 6363992d-6c6b-4362-befe-58982f176403
   Loop over dict user_0 with its separate parts #flashcard 
    for key, value in user_0.items():
-
- id:: 6363992d-80cc-42dc-969d-b89f4ad44324
   Iterate over the keys of a dict fav_langs {name:value} #flashcard 
    for name in favorite_languages.keys():
     print(name.title())
-
- id:: 6363992d-b4bc-4d31-9077-af9429f42ee1
   Tell another use of keys() in Python aside looping #flashcard 
    The keys() method isn’t just for looping: it actually returns a list of all the keys, and the line at ➊ simply checks if 'erin' is in this list.
-
- id:: 6363992d-fca3-4038-90f9-9243adeff878
   Iterate over the content of a dict fav_langs on a loop {key: content} #flashcard 
    for language in favorite_languages.values():
-
- id:: 6363992d-0dab-4988-a35e-cac671187bb5
   Iterate over the content of a dict without repeating.
   Dict: fav_langs #flashcard 
    for language in set(favorite_languages.values()):
-
- id:: 6363992d-1da3-4e17-a268-e3cc9e26cef1
   Repeat a message ‘me’ 30 times in Python. #flashcard 
    for alien_number in range(30):
-
- id:: 6363992d-4537-413a-a1b4-cb38e4bfc17f
   What are the differences between:
   describe_pet(animal_type='hamster', pet_name='harry')
   describe_pet(‘hamster', ‘harry') #flashcard 
    The function describe_pet() hasn’t changed. But when we call the function, we explicitly tell Python which parameter each argument should be matched with. When Python reads the function call, it knows to assign the argument 'hamster' to the parameter animal_type and the argument 'harry' to pet_name. The output correctly shows that we have a hamster named Harry.
     The order of keyword arguments doesn’t matter because Python knows where each value should go.
-
- id:: 6363992d-4a79-4947-ac2e-cbfae0aa37f4
   Print via a function in Python a list without being able to modify it. #flashcard 
    print_models(unprinted_designs[:], completed_models)
-
- id:: 6363992d-8ac2-4f97-a512-ce0ce18b37c2
   Design a function which contains unlimited arguments. #flashcard 
    def make_pizza(*toppings):
     """Print the list of toppings that have been requested."""
     print(toppings)
-
- id:: 6363992d-a9c2-4405-9c81-7490d2d15c78
   Explain how unlimited function parameters works in Python #flashcard 
    The asterisk in the parameter name *toppings tells Python to make an empty tuple called toppings and pack whatever values it receives into this tuple. The print() call in the function body produces output showing that Python can handle a function call with one value and a call with three values. It treats the different calls similarly. Note that Python packs the arguments into a tuple, even if the function receives only one value
-
- id:: 6363992d-eb0c-4a38-8c4c-f9be5a3a3c99
   Can you pass infinite key-value entries to a function in Python? #flashcard 
    def build_profile(first, last, **user_info):
     """Build a dictionary containing everything we know about a user."""
     ➊     user_info['first_name'] = first
     user_info['last_name'] = last
     return user_info
-
- id:: 6363992d-e34d-46d8-bd09-20fe6ed9d5e6
   Bring the module ‘pizza’ into your scope to use pizza.make_pizza() #flashcard 
    import pizza
-
- id:: 6363992d-71b2-4504-a4df-7a56f64f11e7
   Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza().
   Use it. #flashcard 
    from pizza import make_pizza
-
- id:: 6363992d-23e4-475e-b220-db2d65c01dd9
   Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza(). Use an alias.
   Use it. #flashcard 
    from pizza import make_pizza as mp
-
- id:: 6363992d-fa3b-4cd8-9e3a-f885a0bcfc0c
   Bring a module ‘pizza’ to your scope but using an abbreviation.
   Use it. #flashcard 
    import pizza as p
-
- id:: 6363992d-e523-4f46-836d-fd2c8ae7b02b
   Build a constructor in Python #flashcard 
    def __init__(self, name, age):
     """Initialize name and age attributes."""
     ➍         self.name = name
     self.age = age
-
- id:: 6363992d-fab3-45c4-832c-6743d0d8b27e
   Define a method in Python #flashcard 
    def sit(self):
     """Simulate a dog sitting in response to a command."""
     print(f"{self.name} is now sitting.")
-
- Construct an object my_dog by calling the constructor Dog with the arguments:
	- 'Willie'
	- 6 #flashcard 
	  id:: 6363992d-ee32-45cf-ad05-1ef5f7737f88
	      my_dog = Dog('Willie', 6)
-
- id:: 6363992d-8660-47a9-a8a1-0e5de4103a84
   How do you call a base class' constructor from the subclass? #flashcard 
    def __init__(self, make, model, year):
     """Initialize attributes of the parent class."""
     ➍         super().__init__(make, model, year)
-
- id:: 6363992d-4ee3-4540-a06a-c138e6019c8d
   How do you read a text file? #flashcard 
    with open('pi_digits.txt') as file_object:
     contents = file_object.read()
     print(contents)
-
- id:: 6363992d-8ace-44db-9d1f-9419288b72ac
   Should I close a file in Python or not? #flashcard 
    Notice how we call open() in this program but not close(). You could open and close the file by calling open() and close(), but if a bug in your program prevents the close() method from being executed, the file may never close. This may seem trivial, but improperly closed files can cause data to be lost or corrupted. And if you call close() too early in your program, you’ll find yourself trying to work with a closed file (a file you can’t access), which leads to more errors. It’s not always easy to know exactly when you should close a file, but with the structure shown here, Python will figure that out for you. All you have to do is open the file and work with it as desired, trusting that Python will close it automatically when the with block finishes execution.
-
- id:: 6363992d-a70c-4013-bfee-ac7ddccd3d04
   Forward slashes OR backslashes in Python? #flashcard 
    Windows systems use a backslash (\) instead of a forward slash (/) when displaying file paths, but you can still use forward slashes in your code.
-
- id:: 6363992d-349b-4b6f-947a-afa052b3d9e6
   Example to read a file line by line #flashcard 
    filename = 'pi_digits.txt'
     ➋ with open(filename) as file_object:
     ➌     for line in file_object:
     print(line)
-
- id:: 6363992d-b64c-476a-87b1-c87c2580a449
   Write some text in a file in Python. #flashcard 
    filename = 'programming.txt'
     ➊ with open(filename, 'w') as file_object:
     ➋     file_object.write("I love programming.")
-
- id:: 6363992d-88e5-4ef8-9f25-f816298d414f
   Different file modes in Python. #flashcard 
    You can open a file in read mode ('r'), write mode ('w'), append mode ('a'), or a mode that allows you to read and write to the file ('r+'). If you omit the mode argument, Python opens the file in read-only mode by default.
-
- id:: 6363992d-fa2f-4f4d-ada9-073f9a63ed2d
   What does ‘else’ mean in a Exception? #flashcard 
    Any code that depends on the try block succeeding is added to the else block. In this case if the division operation is successful, we use the else block to print the result
-
- id:: 6363992d-d0f4-47b7-b3f8-dc0aa64d0257
   Example of exception in Python #flashcard 
    try:
     answer = int(first_number) / int(second_number)
     ➋     except ZeroDivisionError:
     print("You can't divide by 0!")
     ➌     else:
     print(answer)
-