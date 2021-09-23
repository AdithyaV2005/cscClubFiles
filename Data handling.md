# Data handling
***

## Core data types

1. Number
   - Integers
     - Signed
     - Boolean
   - Floating point
     - Fractional form
     - Exponent form
   - Complex
2. String
3. List
4. Tuple
5. Dictionary

In [1]:

    # Complex data type  
    z = 3 + 4j  
    print(z.real)  
    print(z.imag)   

In [4]:

    # Program representing indexing of strings  
    string = "python"  
    for i in range(len(string)):  
        print(string[i], string[-(i + 1)])  

In [6]:

    # lists are mutable  
    
    planets = [  
        'Mercury',  
        'Venus',  
        'Earth',  
        'Mars',  
        'Jupyter',  
        'Saturn',  
        'Uranus',  
        'Neptune',  
        'Pluto'  
    ]  
    print(planets, planets[-1])  
    
    planets.remove('Pluto')  
    print(planets, planets[-1])  
    ['Mercury', 'Venus', 'Earth', 'Mars', 'Jupyter', 'Saturn', 'Uranus', 'Neptune', 'Pluto'] Pluto  
    ['Mercury', 'Venus', 'Earth', 'Mars', 'Jupyter', 'Saturn', 'Uranus', 'Neptune'] Neptune  

In [7]:

    # tuples are immutable  
    digits = (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)  
    print(digits)  
    digits.remove(9)  

This will cause an attribute error:  
AttributeError: 'tuple' object has no attribute 'remove'  

In [8]:

    # Sets can't have duplicates  
    digits = set()  
    
    for i in range(10):  
        digits.add(i)  
    
    print(digits)  
    
    digits.add(3)  
    
    print(digits)  
    {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}  
    {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}  

In [9]:

    # Sets cant have mutable items  
    primary_colors = {(255, 0, 0), (0, 0, 255), (255, 255, 0)}  
    print(primary_colors)  
    
    primary_colors = {[255, 0, 0], [0, 0, 255], [255, 255, 0]}  
    print(primarry_colors)  

This will cause a type error:  
TypeError: unhashable type: 'list'  

In [11]:

    # Sets are unordered
    odd_digits = {1, 3, 5, 7, 9}
    print(odd_digits[0])

This will cause a type error:  
TypeError: 'set' object is not subscriptable

In [14]:

    # Note: No two keys can be the same
    digits = {  
        '0' : 'zero',  
        '1' : 'one',  
        '2' : 'two',  
        '3' : 'three',  
        '4' : 'four',  
        '5' : 'five',  
        '6' : 'six',  
        '7' : 'seven',  
        '8' : 'eight',  
        '9' : 'nine'  
    }  
    
    phone_number = input('Enter phone number: ')  
    for digit in phone_number:  
        try:  
            print(digits[digit], end=' ')  
        except:  
            print(digit, end='')  

**Integers are not mutable as their values do not change "in place". When an variable is given a different integer value, it simply refers/points to that immutable value's location.**

In [17]:

    x = 1  
    y = x  
    print(id(x) == id(y))  
    
    a = 1  
    i1 = id(a)  
    a = 2  
    i2 = id(a)  
    print(i1 == i2)  

## Mutable types

1. Lists
2. Dictionaries
3. Sets

In [19]:

    # Mutable data types are like storage containers  
    mars_moons = ['Phobos']  
    print(mars_moons, id(mars_moons))  
    mars_moons.append('Deimos')  
    print(mars_moons, id(mars_moons))  

## Variable internals

1. Type
2. Value
3. Id

## Operators

1. Arithmetic
   - Unary
   - Binary
   - Augmented assignment
2. Relational
3. Logical
4. Identity
5. Bitwise
6. Membership

### Guess the answer before running

In [20]:

	5 // -3

In [21]:

	-5 // 3

In [22]:

	-7 / 4

In [23]:

	-7 % 4

In [24]:

	7 % -4


In [25]:

	7 // -4

In [50]:

    # strings are compared lexicographically  
    decimal2ascii = {i: chr(i) for i in range(128)}  
    ascii2decimal = {chr(i): i for i in range(128)}  
    
    print(decimal2ascii.get(100))  
    print(ascii2decimal.get('d'))  
    
    print('Hell' < 'Hello')  
    print(' Hello' == 'Hello')  

In [56]:

    # Floating point limitations  
    print(0.1 + 0.1 + 0.1 == 0.3)  
    print(round(0.1 + 0.1 + 0.1, 1) == 0.3)  

In [57]:

    # Equality vs is  
    a = 10  
    b = 5  
    print(a is b)  
    print(a is not b)  
    
    b += 5  
    print(a is b)  
    print(a == b)  
    print(a is not b)  
    
    s1 = 'abc'  
    s2 = input('s2: ')  
    s3 = 'abc'  
    print(s1 is s2, s2 is s3, s3 is s1)  
    
    pi = 3.14  
    pi2 = 3.14  
    print(pi is pi2)  
    
    i1 = 9876543210  
    i2 = 9876543210  
    print(i1 is i2)  

**Two different objects are created for same value when:**

1. Console input
2. Float / complex numeric literals
3. Very large integers

<table>
    <thead>
        <tr>
            <th style="text-align:left">Logical operator</th>
            <th style="text-align:left">Relational operands</th>
            <th style="text-align:left">Literal operands</th>
            <th style="text-align:left">Return value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align:left">and</td>
            <td style="text-align:left">Checks for both True</td>
            <td style="text-align:left">Checks for first False</td>
            <td style="text-align:left">Boolean or Literal</td>
        </tr>
        <tr>
            <td style="text-align:left">or</td>
            <td style="text-align:left">Checks for one True</td>
            <td style="text-align:left">Checks for first True</td>
            <td style="text-align:left">Boolean or Literal</td>
        </tr>
        <tr>
            <td style="text-align:left">not</td>
            <td style="text-align:left">Checks for False</td>
            <td style="text-align:left">Checks for False</td>
            <td style="text-align:left">Boolean only</td>
        </tr>
    </tbody>
</table>


## BITWISE OPERATORS

------

### Complement

E.g.: ~12  
12 --> 00001100  
~12-->11110011  

If 11110011 is the two's complement of x, then x is the bitwise complement of 12.  
Turns out x is -13  

13 --> 00001101  
1's complement: 11110010  
2's complement: 11110011  

2's complement of -13 = Complement of 12 = 11110011 So -13 is the bitwise complement of 12  

#### Shortcut

Take the mirror reflection of the number by considering it as a list index  

E.g: For 15 it is -16  
E.g: For 0 it is -1  
E.g: For -5 it is 4  

------

### &

Convert the numbers to binary and compare each bit with the 'and' condition.

E.g: 25 & 30

25 --> 11001  
30 --> 11110  
Result:11000 --> 24  

------

### |

Convert the numbers to binary and compare each bit with the 'or' condition.  

E.g: 25 & 30  

25 --> 11001  
30 --> 11110  
Result:11111 --> 31  

------

### ^

Convert the numbers to binary and compare each bit with the 'xor' condition.  

E.g: 25 & 30  

25 --> 11001  
30 --> 11110  
Result:00111 --> 7  

------

In [60]:

    # use the bin function to get numbers in binary form  
    bin(13)  

## Operator precedence

- Brackets
- Exponent
- Complement
- Positive, negative
- Multiplication, division, floor division, modulus
- Addition, subtraction
- &
- ^
- |
- Comparisons, identity operators
- not
- and
- or

**Everything except exponents has left associativity.**

## Expressions

1. Arithmetic
2. Relational
3. Logical
4. String

**+ and \* are string operators**

------

### Arithmetic evaluation:

- Order of precedence
- For each sub-expression
  1. Evaluates operands
  2. Coercions
  3. Computes result
  4. Replaces sub-expression with result
  5. Repeat till final result obtained

**In coercion, complex is promoted over float, which is promoted over int**
**Exception: In division, result will be float even if both operands are integers**

------

### Relational evaluation

- Left associativity
- Combined rel. expression split into logical expression

------

### Logical evaluation

- Arithmetic sub-expressions
- not > and > or
- Reduction of internal work
  - In or, second argument evaluated only if first is false
  - In and, second argument evaluated only if first is true

In [61]:

    f = 3.14  
    print(int(f))  
    print(float(int(f))) # float to int causes loss of precision, i.e., loss of fractional part  
    print(str(f))  
    print(complex(f))  
    print(bool(f))  

In [62]:

    import math  
    dir(math)  

## Math module

1. **Functions**
   - ceil, floor, fabs
   - exp, sqrt, pow
   - log, log10
   - sin, cos, tan
   - degrees, radians
2. **Constants**
   - pi
   - e

In [63]:

    # Radius is 7.5, calculate area and volume.  
    import math  
    
    r = 7.5  
    a = 4 * math.pi * pow(r, 2)  
    v = 4 / 3 * math.pi * pow(r, 3)  
    
    print("Radius =", r)  
    print("Area =", round(a, 2))  
    print("Volume =", round(v, 2))  
    Radius = 7.5  
    Area = 706.86  
    Volume = 1767.15  

## Random module

- **random**
- **randint(a, b)**
- **randrange(start, stop, step)**

In [68]:

    from random import random, randint, randrange  
    help(random)  
    help(randint)  
    help(randrange)  

## Statistics module

- **mean**
- **median(a, b)**
- **mode**

In [69]:

    from statistics import mean, median, mode
    help(mean)
    help(median)
    help(mode)

## Errors

1. Compile-time errors
   - Syntax errors
   - Semantics errors
2. Logical errors
3. Run-time errors

## Exceptions

- EOFError, IOError, OverflowError
- NameError, TypeError, ValueError, ZeroDivisionError
- IndexError, KeyError, ImportError