# Python Crash Course

deck:: [[O'Reilly-Learning::Python Crash Course]]\
author:: [[Eric Matthes]]\
full-title:: "Python Crash Course"\
category:: #books\
\
tags:: O'Reilly-Learning Python  

![](https://learning.oreilly.com/library/view/python-crash-course/9781492071266/ibis_generated_cover_thumbnail.jpg)
## Highlights
### 2 VARIABLES AND SIMPLE DATA TYPES
### 3 INTRODUCING LISTS
### 4 WORKING WITH LISTS
### 11 TESTING YOUR CODE
- Variable names can contain only letters, numbers, and underscores. They can start with a letter or an underscore, but not with a number. For instance, you can call a variable message_1 but not 1_message. #flashcard
  id:: 63cfbcdc-cd4b-4c8d-9ff2-5301a98cd2da
-
- Show the last item of the list bicycles. #flashcard 
  id:: 63cfbcdc-ae72-4973-bcda-a7c15dd71d50
    print(bicycles[-1])
-
- Remove the last item of the list motorcycles, 
  id:: 63cfbcdc-be24-48a2-bd0d-92f096f78c7c
   then show the resultant list, 
   then show the removed object
   [call it removed_item] #flashcard 
    popped_motorcycle = motorcycles.pop()
     ➌ print(motorcycles)
     ➍ print(popped_motorcycle)
-
- Save in a variable named first_owned the (just removed) element with index 0 of the list motorcycles #flashcard 
  id:: 63cfbcdc-2f03-4a2f-81df-24e5b1c56196
    first_owned = motorcycles.pop(0)
-
- Steps to create tests in Python #flashcard 
  id:: 63cfbcdc-bdab-4be4-9233-7b755709bec7
    To write a test case for a function, import the unittest module and the function you want to test. Then create a class that inherits from unittest.TestCase, and write a series of methods to test
-
- universe_age = 14_000_000_000 #flashcard
  id:: 63cfbcdc-06f8-446e-81b9-c3e3a3a24d7f
-
- id:: 63c66a1d-fd00-4624-ae1c-b40aa07bef4b
  
  Sometimes you won’t know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the remove() method. #flashcard
-
- id:: 63c66a1d-d672-4764-abf3-0334b1e68445
  
  The Python variables you’re using at this point should be lowercase. You won’t get errors if you use uppercase letters, but uppercase letters in variable names have special meanings that we’ll discuss in later chapters. #flashcard
-
### 9 CLASSES
- How do we call a testing function? #flashcard 
  id:: 63cfbcdc-1eb2-47e2-bbdd-f733e94d029a
    Any method that starts with test_ will be run automatically when we run test_name_function.py.
-
- id:: 63c66a1d-f120-477b-b574-7748b8943a21
   Show a variable named status inside a string (in Python 3) #flashcard 
    message = f"My first bicycle was a {bicycles[0].title()}."
-
- id:: 63c66a1d-0d92-4674-8570-e2f5b30a1130
   'Steal' the element with value 'ducati' from the motorcycles list #flashcard 
    motorcycles.remove('ducati')
-
- id:: 63c66a1d-c582-4bef-a68f-9761116c52b0
  
  It’s much better to think of variables as labels that you can assign to values. You can also say that a variable references a certain value. #flashcard
-
- id:: 63c66a1d-8acb-4e2d-abef-b8c445388129
   Add 'ducati' at the end of the list motorcycles #flashcard 
    motorcycles.append('ducati')
-
- 'Steal' the element with content 'ducati' from the motorcycles list.
  id:: 63cfbcdc-a9c0-4713-a217-0d57c9d6ddfb
   [Use the already defined variable named my_brand for this task] #flashcard 
    motorcycles.remove(too_expensive)
-
- Function to get the size of the list cars #flashcard 
  id:: 63cfbcdc-3c4c-46ce-8eca-b24de8b2ed00
    len(cars)
-
- How would you define a constructor of a child class in Python? #flashcard 
  id:: 63cfbcdc-e528-46bd-9ab6-b54e7333b7da
    def __init__(self, make, model, year):
     """Initialize attributes of the parent class."""
     ➍ super().__init__(make, model, year)
-
- A method is an action that Python can perform on a piece of data. #flashcard
  id:: 63cfbcdc-366e-4a75-909c-d30662ca990b
-
- id:: 63c66a1d-547e-4597-80f7-f80aa2f65bcb
   Construct a list named bicycles which contains the items:
   * 'trek'
   * 'cannondale'
   * 'redline'
   * 'specialized' #flashcard 
    bicycles = ['trek', 'cannondale', 'redline', 'specialized']
-
- id:: 63c66a1d-c9a8-4843-a061-6a5cc92585e1
   Show the first element of the list bicycles. #flashcard 
    print(bicycles[0])
-
- Insert 'ducati' at the beginning of the list motorcycles without using square brackets: #flashcard 
  id:: 63cfbcdc-3037-4f44-84a1-cd0aab11b311
    motorcycles.insert(0, 'ducati')
-
- id:: 63c66a1d-b7ae-46f8-9f3a-f3176d6f3759
   Order alphabetically a list named cars. Make this change permanent. #flashcard 
    cars.sort()
-
- id:: 63c66a1d-5aac-41e4-8f07-7501a9c35a43
  
  hese strings are called f-strings. The f is for format, because Python formats the string by replacing the name of any variable in braces with its value. #flashcard
-
- Remove the first element of the list motorcycles #flashcard 
  id:: 63cfbcdc-d623-46b0-a18e-89d7222225a1
    del motorcycles[0]
-
- Order alphabetically inversed a list named cars. Make this change permanent. #flashcard 
  id:: 63cfbcdc-b9c6-457d-88a8-bb724cf5a38f
    cars.sort(reverse=True)
-
- To maintain the original order of a list but present it in a sorted order, you can use the #flashcard
  id:: 63cfbcdc-1e9e-47bf-9346-41d0fd05cdd5
-
- F-strings were first introduced in Python 3.6 #flashcard
  id:: 63cfbcdc-48b2-4a56-b68f-4db3138a0663
-
- Show an alphabetically ordered list named cars. Make this change temporal. #flashcard 
  id:: 63cfbcdc-b3f2-40fa-9d8b-9796756a1bd8
    print(sorted(cars))
-
- id:: 63c66a1d-92da-48f2-a8ba-2aba746b1a11
  
  Sometimes you won't know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the #flashcard
-
- Python programmers use all capital letters to indicate a variable should be treated as a constant and never be changed #flashcard
  id:: 63cfbcdc-2df8-4e82-a67e-e39a7c9aa22f
-
- Make the order of the list cars inverse. #flashcard 
  id:: 63cfbcdc-7e38-4872-b6a8-75432c374706
    cars.reverse()
-
- id:: 63c66a1d-2b14-4a17-b7fe-0955d17857d2
   Is it possible to reassign a tuple's content? #flashcard 
    Although you can't modify a tuple, you can assign a new value to a variable that represents a tuple.
-
- id:: 63c66a1d-4740-43c4-9fd1-2d0fc39009cc
  
  Python considers the first item in a list to be at position 0, not position 1 #flashcard
-
- id:: 63c66a1d-a8dd-47c3-bf57-1cffdeffc357
   Show the numbers: [1, 4] #flashcard 
    for value in range(1, 5):
     print(value)
-
- A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item's index, just as you would for a list. #flashcard
  id:: 63cfbcdc-5e6a-4994-94e7-604a79ec16c1
-
- id:: 63c66a1d-41a1-4d3f-872e-e75c1cbe1b8b
  
  Python has a special syntax for accessing the last element in a list. By asking for the item at index -1, Python always returns the last item in the list: #flashcard
-
- id:: 63c66a1d-1036-4cc9-aecb-258a28adcfe0
   Show in a slice the first three items of the list players. #flashcard 
    print(players[0:3])
-
- id:: 63c66a1d-d73a-453a-8f64-7ed5ddc3b00a
   Copy the list my_foods to the list friend_foods without affectations. #flashcard 
    friend_foods = my_foods[:]
-
- Remember that each time you use pop(), the item you work with is no longer stored in the list. #flashcard
  id:: 63cfbcdc-174c-4cb7-8b39-198648dcf705
-
- [List Comprehension]
   Begin with a descriptive name for the list, such as squares. Next, open a set of square brackets and define the expression for the values you want to store in the new list. In this example the expression is value**2, which raises the value to the second power. Then, write a for loop to generate the numbers you want to feed into the expression, and close the square brackets. The for loop in this example is for value in range [1, 10] #flashcard 
    squares = [value**2 for value in range(1, 11)]
-
- id:: 63c66a1d-3c50-4b19-80dd-d1631d99d285
   Show in a slice the second, third and fourth items of the list players #flashcard 
    print(players[1:4])
-
- id:: 63c66a1d-cce4-4cd8-9437-d0ccb5c18522
  
  alphabetically #flashcard
-
- id:: 63c66a1d-455a-4e30-8f7a-4432db9a092d
   Construct a list with the numbers: [1, 5] #flashcard 
    numbers = list(range(1, 6))
-
- Notice that reverse() doesn’t sort backward alphabetically; it simply reverses the order of the list: #flashcard
  id:: 63cfbcdc-9299-4e1e-9348-aac894645e21
-
- id:: 63c66a1d-1980-473f-ab67-fadb24cd46be
   Another way of access to an element in a dict instead of indexes in square brackets #flashcard 
    For dictionaries, specifically, you can use the get() method to set a default value that will be returned if the requested key doesn’t exist.
-
- id:: 63c66a1d-619e-412a-b7c3-766811be799b
  
  The PEP 8 guidelines for line length are not set in stone, and some teams prefer a 99-character limit. #flashcard
-
- keep in mind when writing your own for loops that you can choose any name you want for the temporary variable that will be associated with each value in the list. However, it’s helpful to choose a meaningful name that represents a single item from the list. #flashcard
  id:: 63cfbcdc-e3ff-4c77-be96-3c17c57a7499
-
- id:: 63c66a1d-9cba-4051-b1fb-0f6d2c8b2e1a
   How can you split a string in multiple lines? #flashcard 
    print(f"You ordered a {pizza['crust']}-crust pizza "
     "with the following toppings:")
-
- Tuples are technically defined by the presence of a comma; the parentheses make them look neater and more readable. If you want to define a tuple with one element, you need to include a trailing comma: #flashcard
  id:: 63cfbcdc-dc1b-405b-a34e-4dd3f1825958
-
- id:: 63c66a1d-4bc3-4437-8204-924f0fe48efc
  
  Using singular and plural names can help you identify whether a section of code is working with a single element from the list or the entire list. #flashcard
-
- id:: 63c66a1d-071a-4d1a-97af-1abc92284e8f
  
  If you omit the first index in a slice, Python automatically starts your slice at the beginning of the list: #flashcard
-
- id:: 63c66a1d-8b42-49da-b75a-8c305de8dfd5
  
  You can avoid unexpected indentation errors by indenting only when you have a specific reason to do so. #flashcard
-
### 6 DICTIONARIES
- The colon at the end of a for statement tells Python to interpret the next line as the start of a loop. #flashcard
  id:: 63cfbcdc-a294-4800-bab8-f48af057341a
-
- Build a dict named alien_0 with:
  id:: 63cfbcdc-dcb2-4301-8955-24defeb0f2b7
   color ---> green
   points ---> 50 #flashcard 
    alien_0 = {'color': 'green', 'points': 5}
-
- If you want to make a list of numbers, you can convert the results of range() directly into a list using the list() function. When you wrap list() around a call to the range() function, the output will be a list of numbers. #flashcard
  id:: 63cfbcdc-7fe8-40fa-a1a8-aeb7f94324aa
-
### 8 FUNCTIONS
- id:: 63c66a1d-4810-497a-bce2-49f7ed97e1fd
  
  A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item’s index, just as you would for a list. #flashcard
-
- id:: 63c66a1d-ecfe-446c-a536-391101d58029
   How should I use the import's in Python? #flashcard 
    The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that's easy to read and understand.
-
### 10 FILES AND EXCEPTIONS
- id:: 63c66a1d-7a0d-46fa-afc9-877243bd0b15
  
  To do any work with a file, even just printing its contents, you first need to open the file to access it. The open() function needs one argument: the name of the file you want to open. Python looks for this file in the directory where the program that’s currently being executed is stored. #flashcard
-
- The keyword with closes the file once access to it is no longer needed. #flashcard
  id:: 63cfbcdc-d5c6-4eac-8d66-9303532b59f0
-
- u'll often want to run through all entries in a list, performing the same task with each item. For example, in a game you might want to move every element on the screen by the same amount, or in a list of numbers you might want to perform the same statistic #flashcard
  id:: 63cfbcdc-80fc-414f-9470-c845b60274c4
-
- Is it possible to reassign a tuple's content? #flashcard 
  id:: 63cfbcdc-a63e-4f5b-8ca3-861138f26760
    Although you can’t modify a tuple, you can assign a new value to a variable that represents a tuple.
-
- How do you call a base class' constructor? #flashcard 
  id:: 63cfbcdc-4cce-4578-b825-28dd847b17c9
    super().__init__(make, model, year)
-
- How should I use the import's in Python? #flashcard 
  id:: 63cfbcdc-6f5b-4b78-9f18-4dfeda0b26b0
    The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that’s easy to read and understand.
-
- id:: 63c66a1d-8a31-47b2-97ed-d7f647c5da1e
   Build a dict named alien_0 with:
   color ---> green
   points ---> 50 #flashcard 
    alien_0 = {'color': 'green', 'points': 5}
-
- Add a new key-value entry to an existing dict in Python.
  id:: 63cfbcdc-a67b-452a-ad3b-2d5165e7259b
   Values x-0, y-25.
   BEFORE:
   my_dict = {'color': 'green', 'points': 5} #flashcard 
    ➊ alien_0['x_position'] = 0
     ➋ alien_0['y_position'] = 25
-
- Remove the entry with key ‘points’ from the dict alien. #flashcard 
  id:: 63cfbcdc-7d13-4f7e-a067-e6897d43f0c7
    del alien_0['points']
-
- Access to a dict but printing a message in case of error.
  id:: 63cfbcdc-f4f1-41d0-932d-4c8cee904486
   dict: my_map
   key: ‘point’
   Message: ‘unassigned’
   Variable: point_value #flashcard 
    point_value = alien_0.get('points', 'No point value assigned.')
-
- Loop over dict user_0 with its separate parts #flashcard 
  id:: 63cfbcdc-c471-4dad-aadc-73d2735cdcbe
    for key, value in user_0.items():
-
- id:: 63c66a1d-9f8a-4328-8927-f89c42d5765a
   Iterate over the keys of a dict fav_langs {name:value} #flashcard 
    for name in favorite_languages.keys():
     print(name.title())
-
- id:: 63c66a1d-3fed-4e96-9305-a50597ac60c5
   Tell another use of keys() in Python aside looping #flashcard 
    The keys() method isn’t just for looping: it actually returns a list of all the keys, and the line at ➊ simply checks if 'erin' is in this list.
-
- Iterate over the content of a dict fav_langs on a loop {key: content} #flashcard 
  id:: 63cfbcdc-1751-4712-aaec-63618dcb0158
    for language in favorite_languages.values():
-
- Iterate over the content of a dict without repeating.
  id:: 63cfbcdc-5c23-4464-9a5c-46b8df30716d
   Dict: fav_langs #flashcard 
    for language in set(favorite_languages.values()):
-
- Repeat a message ‘me’ 30 times in Python. #flashcard 
  id:: 63cfbcdc-4fe6-485f-80e1-5666919cc359
    for alien_number in range(30):
-
- What are the differences between:
  id:: 63cfbcdc-ce4c-4251-8b4d-fcd2a8c77ba1
   describe_pet(animal_type='hamster', pet_name='harry')
   describe_pet(‘hamster', ‘harry') #flashcard 
    The function describe_pet() hasn’t changed. But when we call the function, we explicitly tell Python which parameter each argument should be matched with. When Python reads the function call, it knows to assign the argument 'hamster' to the parameter animal_type and the argument 'harry' to pet_name. The output correctly shows that we have a hamster named Harry.
     The order of keyword arguments doesn’t matter because Python knows where each value should go.
-
- id:: 63c66a1d-76da-44b6-b1b9-9c3b01a9a3ee
   Print via a function in Python a list without being able to modify it. #flashcard 
    print_models(unprinted_designs[:], completed_models)
-
- id:: 63c66a1d-6207-427e-99c0-a7f07f74f5ed
   Design a function which contains unlimited arguments. #flashcard 
    def make_pizza(*toppings):
     """Print the list of toppings that have been requested."""
     print(toppings)
-
- Explain how unlimited function parameters works in Python #flashcard 
  id:: 63cfbcdc-da6f-4960-bb2b-f95fa60ce9bf
    The asterisk in the parameter name *toppings tells Python to make an empty tuple called toppings and pack whatever values it receives into this tuple. The print() call in the function body produces output showing that Python can handle a function call with one value and a call with three values. It treats the different calls similarly. Note that Python packs the arguments into a tuple, even if the function receives only one value
-
- id:: 63c66a1d-4c05-4553-931e-f3ccb7622c65
   Can you pass infinite key-value entries to a function in Python? #flashcard 
    def build_profile(first, last, **user_info):
     """Build a dictionary containing everything we know about a user."""
     ➊     user_info['first_name'] = first
     user_info['last_name'] = last
     return user_info
-
- Bring the module ‘pizza’ into your scope to use pizza.make_pizza() #flashcard 
  id:: 63cfbcdc-dabc-412b-8d4b-fe2d9e47d1db
    import pizza
-
- id:: 63c66a1d-49b3-4c61-b7c3-a15a489234f6
   Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza().
   Use it. #flashcard 
    from pizza import make_pizza
-
- Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza(). Use an alias.
  id:: 63cfbcdc-8ade-4ff1-bde4-cff79fcb1b1d
   Use it. #flashcard 
    from pizza import make_pizza as mp
-
- id:: 63c66a1d-fd05-4405-bbc1-758f168c724a
   Bring a module ‘pizza’ to your scope but using an abbreviation.
   Use it. #flashcard 
    import pizza as p
-
- id:: 63c66a1d-533b-4cf0-af8b-df5cf81548a1
   Build a constructor in Python #flashcard 
    def __init__(self, name, age):
     """Initialize name and age attributes."""
     ➍         self.name = name
     self.age = age
-
- id:: 63c66a1d-1acf-4149-8d7c-13e759a46694
   Define a method in Python #flashcard 
    def sit(self):
     """Simulate a dog sitting in response to a command."""
     print(f"{self.name} is now sitting.")
-
- Construct an object my_dog by calling the constructor Dog with the arguments:
	- 'Willie'
	- 6 #flashcard 
	  id:: 63cfbcdc-ae90-491b-81d1-4430db605d11
	      my_dog = Dog('Willie', 6)
-
- How do you call a base class' constructor from the subclass? #flashcard 
  id:: 63cfbcdc-335a-45b2-8053-0c5aa9d4252e
    def __init__(self, make, model, year):
     """Initialize attributes of the parent class."""
     ➍         super().__init__(make, model, year)
-
- How do you read a text file? #flashcard 
  id:: 63cfbcdc-8601-4991-8c23-b245aa316328
    with open('pi_digits.txt') as file_object:
     contents = file_object.read()
     print(contents)
-
- id:: 63c66a1d-93cd-4126-adb1-2bf1444c0d4b
   Should I close a file in Python or not? #flashcard 
    Notice how we call open() in this program but not close(). You could open and close the file by calling open() and close(), but if a bug in your program prevents the close() method from being executed, the file may never close. This may seem trivial, but improperly closed files can cause data to be lost or corrupted. And if you call close() too early in your program, you’ll find yourself trying to work with a closed file (a file you can’t access), which leads to more errors. It’s not always easy to know exactly when you should close a file, but with the structure shown here, Python will figure that out for you. All you have to do is open the file and work with it as desired, trusting that Python will close it automatically when the with block finishes execution.
-
- id:: 63c66a1d-ea33-4eff-b610-37b5890745dc
   Forward slashes OR backslashes in Python? #flashcard 
    Windows systems use a backslash (\) instead of a forward slash (/) when displaying file paths, but you can still use forward slashes in your code.
-
- id:: 63c66a1d-0bcc-4578-8ed0-68bb2b2d4af7
   Example to read a file line by line #flashcard 
    filename = 'pi_digits.txt'
     ➋ with open(filename) as file_object:
     ➌     for line in file_object:
     print(line)
-
- Write some text in a file in Python. #flashcard 
  id:: 63cfbcdc-1261-4955-80b2-c7762f8f3c8f
    filename = 'programming.txt'
     ➊ with open(filename, 'w') as file_object:
     ➋     file_object.write("I love programming.")
-
- id:: 63c66a1d-16e0-4d8b-b207-5ef5096af2b9
   Different file modes in Python. #flashcard 
    You can open a file in read mode ('r'), write mode ('w'), append mode ('a'), or a mode that allows you to read and write to the file ('r+'). If you omit the mode argument, Python opens the file in read-only mode by default.
-
- id:: 63c66a1d-ee70-44e1-affd-239a36a59fab
   What does ‘else’ mean in a Exception? #flashcard 
    Any code that depends on the try block succeeding is added to the else block. In this case if the division operation is successful, we use the else block to print the result
-
- id:: 63c66a1d-06ab-497e-85c4-b9e82feef194
   Example of exception in Python #flashcard 
    try:
     answer = int(first_number) / int(second_number)
     ➋     except ZeroDivisionError:
     print("You can't divide by 0!")
     ➌     else:
     print(answer)
-