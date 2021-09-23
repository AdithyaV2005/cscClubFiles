# Python

------

In [1]:

    print("Hello, world!")  

## Character set

1. Letters
2. Digits
3. Special characters
4. Whitespace characters
5. Other characters

## Tokens

1. Keywords
2. Identifiers
3. Literals
4. Operators
5. Punctuators

### Literals

1. String
2. Numeric
3. Boolean
4. Special
5. Literal collections

#### Escape sequences

1. Tab
2. Newline
3. Vertical tab
4. Carriage return
5. Formfeed
6. ASCII Bell
7. ASCII backspace
8. Apostrophe
9. Quotation
10. Backslash
11. Octal character
12. Hex character
13. Unicode 16 bit
14. Unicode 32 bit
15. Unicode named

In [2]:

    normal_multiline = "Hello\  
    world"  
    triple_quoted = '''Hello  
    world'''  

    print(len(normal_multiline), len(triple_quoted))   

#### Numeric literals

1. Integers
   - Decimal
   - Octal
   - Hexadecimal
2. Floating
   - Fractional
   - Exponential
3. Complex

In [3]:

    print(10, 0o10, 0x10, 3.14, 314E-2, 3 + 14j)   

**` is the bitwise complement operator**

**&, ^, | - Bitwise and, XOR and OR**

**<< and >> --> Shift left and right**

## Barebones of a python program

------

1. Expressions
2. Statement
3. Comments
4. Functions
5. Blocks and indentations

In [5]:

    # Program with all barebones included  

    def area_of_circle(radius):  
        return 3.14 * radius ** 2  

    radius = 10  
    print("Area =", area_of_circle(radius))   

In [9]:

    # Variables are not containers in python. They are named labels which point to values in front loaded dataspace.  

    x = 10  
    print(id(x))  

    x = 20  
    print(id(x))  

    # This is not true for all types of variables.   

In [11]:

    # Multiple assignments  

    x = y = 1  
    a, b = x + 1, y - 1  

    print(a, b)  

In [13]:

    # Type function  
    a = 1  
    print(type(a))  
    print(type(type(a)))   

## Input

In [14]:

    name = input("Name: ")  
    print(name)   

In [17]:

    # Program to square an integer  

    def get_int(prompt):  
        try:  
            return int(input(prompt))  
        except ValueError:  
            return get_int(prompt)  

    x = get_int("x: ")  
    print(x ** 2)   

In [18]:

    # Program to square a number  

    def get_float(prompt):  
        try:  
            return float(input(prompt))  
        except ValueError:  
            return get_float(prompt)  

    x = get_float("x: ")  
    print(x ** 2)  

## Print

In [22]:

    print("Never gonna give you up!\n", end="Never gonna ")  
    print("let", "you", "down\n", end="Never gonna ")  
    print("tell", "a", "lie\n", sep="-", end="Never gonna ")  
    print("And desert you!")  

## Sample programs

Just try them out! I have defined a custom function for getting number input to avoid ValueErrors. Also, each codeblock works as a standalone program :)

In [23]:

    msg = input("Greet message: ")  
    print(msg)  

In [27]:

    def number(prompt="Enter a number: "):  
        try:  
            return int(input(prompt))  
        except ValueError:  
            return number(prompt)  

    print(number() + number() + number())  

In [26]:

    def number(prompt="Enter a number: "):  
        try:  
            return int(input(prompt))  
        except ValueError:  
            return number(prompt)  

    print(number("Length: ") * number("Breadth: "))  

In [29]:

    def number(prompt="Enter a number: "):  
        try:  
            return float(input(prompt))  
        except ValueError:  
            return number(prompt)  

    print("BMI = ", number("Mass: ") / number("Height: ") ** 2)  

In [30]:

    def number(prompt="Enter a number: "):  
        try:  
            return float(input(prompt))  
        except ValueError:  
            return number(prompt)  

    print(number() ** 3)  

In [32]:

    def number(prompt="Enter a number: "):  
        try:  
            return float(input(prompt))  
        except ValueError:  
            return number(prompt)  

    print(number("Km: ") * 0.621371, "miles")  

In [33]:

    def number(prompt="Enter a number: "):  
        try:  
            return float(input(prompt))  
        except ValueError:  
            return number(prompt)  

    tonnes = number("Tonnes: ")  
    print(tonnes * 10, "quintals or", tonnes * 1000, "Kg")  

In [34]:

    print(input("Poem: "))  

In [35]:

    def number(prompt="Enter a number: "):  
        try:  
            return float(input(prompt))  
        except ValueError:  
            return number(prompt)  

    x, y = number("x: "), number("y: ")  
    print("Before swapping, x =", x, "and y =", y)  

    x, y = y, x  
    print("After swapping, x =", x, "and y =", y)  
