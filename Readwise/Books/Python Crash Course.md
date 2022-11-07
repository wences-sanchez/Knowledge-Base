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
- 

Variable names can contain only letters, numbers, and underscores. They can start with a letter or an underscore, but not with a number. For instance, you can call a variable message_1 but not 1_message. #flashcard 


    
-
- 
 Show the last item of the list bicycles. #flashcard 
    print(bicycles[-1])

    
-
- 
 Remove the last item of the list motorcycles, 
   then show the resultant list, 
   then show the removed object
   [call it removed_item] #flashcard 
    popped_motorcycle = motorcycles.pop()
     ➌ print(motorcycles)
     ➍ print(popped_motorcycle)

    
-
- 
 Save in a variable named first_owned the (just removed) element with index 0 of the list motorcycles #flashcard 
    first_owned = motorcycles.pop(0)

    
-
- 
 Steps to create tests in Python #flashcard 
    To write a test case for a function, import the unittest module and the function you want to test. Then create a class that inherits from unittest.TestCase, and write a series of methods to test

    
-
- 

universe_age = 14_000_000_000 #flashcard 


    
-
- 

Sometimes you won’t know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the remove() method. #flashcard 


    
-
- 

The Python variables you’re using at this point should be lowercase. You won’t get errors if you use uppercase letters, but uppercase letters in variable names have special meanings that we’ll discuss in later chapters. #flashcard 


    
-
### 9 CLASSES
- 
 How do we call a testing function? #flashcard 
    Any method that starts with test_ will be run automatically when we run test_name_function.py.

    
-
- 
 Show a variable named status inside a string (in Python 3) #flashcard 
    message = f"My first bicycle was a {bicycles[0].title()}."

    
-
- 
 'Steal' the element with value 'ducati' from the motorcycles list #flashcard 
    motorcycles.remove('ducati')

    
-
- 

It’s much better to think of variables as labels that you can assign to values. You can also say that a variable references a certain value. #flashcard 


    
-
- 
 Add 'ducati' at the end of the list motorcycles #flashcard 
    motorcycles.append('ducati')

    
-
- 
 'Steal' the element with content 'ducati' from the motorcycles list.
   [Use the already defined variable named my_brand for this task] #flashcard 
    motorcycles.remove(too_expensive)

    
-
- 
 Function to get the size of the list cars #flashcard 
    len(cars)

    
-
- 
 How would you define a constructor of a child class in Python? #flashcard 
    def __init__(self, make, model, year):
     """Initialize attributes of the parent class."""
     ➍ super().__init__(make, model, year)

    
-
- 

A method is an action that Python can perform on a piece of data. #flashcard 


    
-
- 
 Construct a list named bicycles which contains the items:
   * 'trek'
   * 'cannondale'
   * 'redline'
   * 'specialized' #flashcard 
    bicycles = ['trek', 'cannondale', 'redline', 'specialized']

    
-
- 
 Show the first element of the list bicycles. #flashcard 
    print(bicycles[0])

    
-
- 
 Insert 'ducati' at the beginning of the list motorcycles without using square brackets: #flashcard 
    motorcycles.insert(0, 'ducati')

    
-
- 
 Order alphabetically a list named cars. Make this change permanent. #flashcard 
    cars.sort()

    
-
- 

hese strings are called f-strings. The f is for format, because Python formats the string by replacing the name of any variable in braces with its value. #flashcard 


    
-
- 
 Remove the first element of the list motorcycles #flashcard 
    del motorcycles[0]

    
-
- 
 Order alphabetically inversed a list named cars. Make this change permanent. #flashcard 
    cars.sort(reverse=True)

    
-
- 

To maintain the original order of a list but present it in a sorted order, you can use the #flashcard 


    
-
- 

F-strings were first introduced in Python 3.6 #flashcard 


    
-
- 
 Show an alphabetically ordered list named cars. Make this change temporal. #flashcard 
    print(sorted(cars))

    
-
- 

Sometimes you won't know the position of the value you want to remove from a list. If you only know the value of the item you want to remove, you can use the #flashcard 


    
-
- 

Python programmers use all capital letters to indicate a variable should be treated as a constant and never be changed #flashcard 


    
-
- 
 Make the order of the list cars inverse. #flashcard 
    cars.reverse()

    
-
- 
 Is it possible to reassign a tuple's content? #flashcard 
    Although you can't modify a tuple, you can assign a new value to a variable that represents a tuple.

    
-
- 

Python considers the first item in a list to be at position 0, not position 1 #flashcard 


    
-
- 
 Show the numbers: [1, 4] #flashcard 
    for value in range(1, 5):
     print(value)

    
-
- 

A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item's index, just as you would for a list. #flashcard 


    
-
- 

Python has a special syntax for accessing the last element in a list. By asking for the item at index -1, Python always returns the last item in the list: #flashcard 


    
-
- 
 Show in a slice the first three items of the list players. #flashcard 
    print(players[0:3])

    
-
- 
 Copy the list my_foods to the list friend_foods without affectations. #flashcard 
    friend_foods = my_foods[:]

    
-
- 

Remember that each time you use pop(), the item you work with is no longer stored in the list. #flashcard 


    
-
- 
 [List Comprehension]
   Begin with a descriptive name for the list, such as squares. Next, open a set of square brackets and define the expression for the values you want to store in the new list. In this example the expression is value**2, which raises the value to the second power. Then, write a for loop to generate the numbers you want to feed into the expression, and close the square brackets. The for loop in this example is for value in range [1, 10] #flashcard 
    squares = [value**2 for value in range(1, 11)]

    
-
- 
 Show in a slice the second, third and fourth items of the list players #flashcard 
    print(players[1:4])

    
-
- 

alphabetically #flashcard 


    
-
- 
 Construct a list with the numbers: [1, 5] #flashcard 
    numbers = list(range(1, 6))

    
-
- 

Notice that reverse() doesn’t sort backward alphabetically; it simply reverses the order of the list: #flashcard 


    
-
- 
 Another way of access to an element in a dict instead of indexes in square brackets #flashcard 
    For dictionaries, specifically, you can use the get() method to set a default value that will be returned if the requested key doesn’t exist.

    
-
- 

The PEP 8 guidelines for line length are not set in stone, and some teams prefer a 99-character limit. #flashcard 


    
-
- 

keep in mind when writing your own for loops that you can choose any name you want for the temporary variable that will be associated with each value in the list. However, it’s helpful to choose a meaningful name that represents a single item from the list. #flashcard 


    
-
- 
 How can you split a string in multiple lines? #flashcard 
    print(f"You ordered a {pizza['crust']}-crust pizza "
     "with the following toppings:")

    
-
- 

Tuples are technically defined by the presence of a comma; the parentheses make them look neater and more readable. If you want to define a tuple with one element, you need to include a trailing comma: #flashcard 


    
-
- 

Using singular and plural names can help you identify whether a section of code is working with a single element from the list or the entire list. #flashcard 


    
-
- 

If you omit the first index in a slice, Python automatically starts your slice at the beginning of the list: #flashcard 


    
-
- 

You can avoid unexpected indentation errors by indenting only when you have a specific reason to do so. #flashcard 


    
-
### 6 DICTIONARIES
- 

The colon at the end of a for statement tells Python to interpret the next line as the start of a loop. #flashcard 


    
-
- 
 Build a dict named alien_0 with:
   color ---> green
   points ---> 50 #flashcard 
    alien_0 = {'color': 'green', 'points': 5}

    
-
- 

If you want to make a list of numbers, you can convert the results of range() directly into a list using the list() function. When you wrap list() around a call to the range() function, the output will be a list of numbers. #flashcard 


    
-
### 8 FUNCTIONS
- 

A tuple looks just like a list except you use parentheses instead of square brackets. Once you define a tuple, you can access individual elements by using each item’s index, just as you would for a list. #flashcard 


    
-
- 
 How should I use the import's in Python? #flashcard 
    The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that's easy to read and understand.

    
-
### 10 FILES AND EXCEPTIONS
- 

To do any work with a file, even just printing its contents, you first need to open the file to access it. The open() function needs one argument: the name of the file you want to open. Python looks for this file in the directory where the program that’s currently being executed is stored. #flashcard 


    
-
- 

The keyword with closes the file once access to it is no longer needed. #flashcard 


    
-
- 

u'll often want to run through all entries in a list, performing the same task with each item. For example, in a game you might want to move every element on the screen by the same amount, or in a list of numbers you might want to perform the same statistic #flashcard 


    
-
- 
 Is it possible to reassign a tuple's content? #flashcard 
    Although you can’t modify a tuple, you can assign a new value to a variable that represents a tuple.

    
-
- 
 How do you call a base class' constructor? #flashcard 
    super().__init__(make, model, year)

    
-
- 
 How should I use the import's in Python? #flashcard 
    The best approach is to import the function or functions you want, or import the entire module and use the dot notation. This leads to clear code that’s easy to read and understand.

    
-
- 
 Build a dict named alien_0 with:
   color ---> green
   points ---> 50 #flashcard 
    alien_0 = {'color': 'green', 'points': 5}

    
-
- 
 Add a new key-value entry to an existing dict in Python.
   Values x-0, y-25.
   BEFORE:
   my_dict = {'color': 'green', 'points': 5} #flashcard 
    ➊ alien_0['x_position'] = 0
     ➋ alien_0['y_position'] = 25

    
-
- 
 Remove the entry with key ‘points’ from the dict alien. #flashcard 
    del alien_0['points']

    
-
- 
 Access to a dict but printing a message in case of error.
   dict: my_map
   key: ‘point’
   Message: ‘unassigned’
   Variable: point_value #flashcard 
    point_value = alien_0.get('points', 'No point value assigned.')

    
-
- 
 Loop over dict user_0 with its separate parts #flashcard 
    for key, value in user_0.items():

    
-
- 
 Iterate over the keys of a dict fav_langs {name:value} #flashcard 
    for name in favorite_languages.keys():
     print(name.title())

    
-
- 
 Tell another use of keys() in Python aside looping #flashcard 
    The keys() method isn’t just for looping: it actually returns a list of all the keys, and the line at ➊ simply checks if 'erin' is in this list.

    
-
- 
 Iterate over the content of a dict fav_langs on a loop {key: content} #flashcard 
    for language in favorite_languages.values():

    
-
- 
 Iterate over the content of a dict without repeating.
   Dict: fav_langs #flashcard 
    for language in set(favorite_languages.values()):

    
-
- 
 Repeat a message ‘me’ 30 times in Python. #flashcard 
    for alien_number in range(30):

    
-
- 
 What are the differences between:
   describe_pet(animal_type='hamster', pet_name='harry')
   describe_pet(‘hamster', ‘harry') #flashcard 
    The function describe_pet() hasn’t changed. But when we call the function, we explicitly tell Python which parameter each argument should be matched with. When Python reads the function call, it knows to assign the argument 'hamster' to the parameter animal_type and the argument 'harry' to pet_name. The output correctly shows that we have a hamster named Harry.
     The order of keyword arguments doesn’t matter because Python knows where each value should go.

    
-
- 
 Print via a function in Python a list without being able to modify it. #flashcard 
    print_models(unprinted_designs[:], completed_models)

    
-
- 
 Design a function which contains unlimited arguments. #flashcard 
    def make_pizza(*toppings):
     """Print the list of toppings that have been requested."""
     print(toppings)

    
-
- 
 Explain how unlimited function parameters works in Python #flashcard 
    The asterisk in the parameter name *toppings tells Python to make an empty tuple called toppings and pack whatever values it receives into this tuple. The print() call in the function body produces output showing that Python can handle a function call with one value and a call with three values. It treats the different calls similarly. Note that Python packs the arguments into a tuple, even if the function receives only one value

    
-
- 
 Can you pass infinite key-value entries to a function in Python? #flashcard 
    def build_profile(first, last, **user_info):
     """Build a dictionary containing everything we know about a user."""
     ➊     user_info['first_name'] = first
     user_info['last_name'] = last
     return user_info

    
-
- 
 Bring the module ‘pizza’ into your scope to use pizza.make_pizza() #flashcard 
    import pizza

    
-
- 
 Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza().
   Use it. #flashcard 
    from pizza import make_pizza

    
-
- 
 Bring the module ‘pizza’ into your scope to use ONLY pizza.make_pizza(). Use an alias.
   Use it. #flashcard 
    from pizza import make_pizza as mp

    
-
- 
 Bring a module ‘pizza’ to your scope but using an abbreviation.
   Use it. #flashcard 
    import pizza as p

    
-
- 
 Build a constructor in Python #flashcard 
    def __init__(self, name, age):
     """Initialize name and age attributes."""
     ➍         self.name = name
     self.age = age

    
-
- 
 Define a method in Python #flashcard 
    def sit(self):
     """Simulate a dog sitting in response to a command."""
     print(f"{self.name} is now sitting.")

    
-
- 
 Construct an object my_dog by calling the constructor Dog with the arguments:
   - 'Willie'
   - 6 #flashcard 
    my_dog = Dog('Willie', 6)

    
-
- 
 How do you call a base class' constructor from the subclass? #flashcard 
    def __init__(self, make, model, year):
     """Initialize attributes of the parent class."""
     ➍         super().__init__(make, model, year)

    
-
- 
 How do you read a text file? #flashcard 
    with open('pi_digits.txt') as file_object:
     contents = file_object.read()
     print(contents)

    
-
- 
 Should I close a file in Python or not? #flashcard 
    Notice how we call open() in this program but not close(). You could open and close the file by calling open() and close(), but if a bug in your program prevents the close() method from being executed, the file may never close. This may seem trivial, but improperly closed files can cause data to be lost or corrupted. And if you call close() too early in your program, you’ll find yourself trying to work with a closed file (a file you can’t access), which leads to more errors. It’s not always easy to know exactly when you should close a file, but with the structure shown here, Python will figure that out for you. All you have to do is open the file and work with it as desired, trusting that Python will close it automatically when the with block finishes execution.

    
-
- 
 Forward slashes OR backslashes in Python? #flashcard 
    Windows systems use a backslash (\) instead of a forward slash (/) when displaying file paths, but you can still use forward slashes in your code.

    
-
- 
 Example to read a file line by line #flashcard 
    filename = 'pi_digits.txt'
     ➋ with open(filename) as file_object:
     ➌     for line in file_object:
     print(line)

    
-
- 
 Write some text in a file in Python. #flashcard 
    filename = 'programming.txt'
     ➊ with open(filename, 'w') as file_object:
     ➋     file_object.write("I love programming.")

    
-
- 
 Different file modes in Python. #flashcard 
    You can open a file in read mode ('r'), write mode ('w'), append mode ('a'), or a mode that allows you to read and write to the file ('r+'). If you omit the mode argument, Python opens the file in read-only mode by default.

    
-
- 
 What does ‘else’ mean in a Exception? #flashcard 
    Any code that depends on the try block succeeding is added to the else block. In this case if the division operation is successful, we use the else block to print the result

    
-
- 
 Example of exception in Python #flashcard 
    try:
     answer = int(first_number) / int(second_number)
     ➋     except ZeroDivisionError:
     print("You can't divide by 0!")
     ➌     else:
     print(answer)

    
-
