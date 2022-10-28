# Implement – What's Up on the Field? – Tic-Tac-Toe – JetBrains Academy

deck:: [[Across-the-Net]]\
author:: [[hyperskill.org]]\
full-title:: "Implement – What's Up on the Field? – Tic-Tac-Toe – JetBrains Academy"\
category:: #articles\
url:: https://hyperskill.org/learn/step/6224\

![](https://readwise-assets.s3.amazonaws.com/static/images/article3.5c705a01b476.png)

## Highlights
- 
 About Dynamic typing in .python #flashcard 
    Dynamic vs. Static typingPython is a dynamically and strongly typed language. Dynamic typing means that only runtime objects (values) have a type, but not the variables that store them. You are able to store several values of different types in a single variable during your code execution and no errors will occur.
     The following code is totally valid:
     v = 10  # variable v stores an integer valuev = 'hello'  # v now stores a string
     On the other side, in statically typed languages each variable has a type that cannot be changed during the runtime, so the code above would fail. The examples of statically typed languages are C++, Java and Go.

    
-
- 
 About Strong typing in .python #flashcard 
    Strong vs. Weak typingStrong typing means that implicit type conversions don't happen. For example, even though "125" consists only of digits it's a string. To use it in arithmetic operations you need to change its type to an integer or another numerical type. Trying to use it as is leads to a TypeError.
     >>> "125" + 10...TypeError: can only concatenate str (not "int") to str
     If Python had a weak type system, such value could be interpreted as an integer to successfully perform the operation. Such behavior, when one of the operands is implicitly converted to the type of another operand, is called type coercion.
     Since there is no type of coercion in Python, the same operand may give different results depending on the types of provided arguments. For example, you can add two strings to get a concatenation. It is also possible to multiply a string by an integer:
     print(125 + 125)  #  "250"print("125" + "125")  # "125125"print(125 * 4)  # "500"print("125" * 4)  # "125125125125"print("This is a number:", 125)  # "This is a number: 125"
     The example also shows that you can print values of different types if you separate them with commas in the parentheses. The print() function will print all the arguments delimited by a space.

    
-
- 
 About Type Casting in .python #flashcard 
    Explicit type castingThe process of converting a value to another type is also called type casting. Though implicit type casting isn't allowed in Python you will often find yourself in need to define an explicit type conversion within your code. This happens a lot when you work with the user's input.
     Imagine, you asked a user to provide an age that you will later use in some calculations. To convert a string to integer type you can use the built-in int function.
     raw_age = "22"print(type(raw_age))  # <class 'str'>age = int(raw_age)print(type(age))  # <class 'int'>
     The type function is used to find out the type of the value provided.

    
-
