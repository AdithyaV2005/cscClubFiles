# String Manipulation

## Introduction:

1) Python strings are nothing but characters enclosed wihin quotations of any type:
   * Single quotations (' ')
   * Double quotations (" ")
   * And triple quotations (''' ''')

2) Python strings are thus sequences of characters enclosed within quotes of any type, where each character has an unique position id or index.

3) Note: "ABC" is a different string from "BCA", as even though all the characters are the same, the position of each and every character isn't the same.

4) Indexes of a string begin from 0 to (length-1) in forward direction and -1,-2,-3,....,-length in backward direction.

## Traversing a String:

1) Traversing of a string refers to iterating through the elements of a string one character at a time. (A string is traversed through by writing out its characters individually. For this purpose a "for loop" is used to print out all the characters of a string).

2) Example program and output for it:

Example Program:

```
name = "superb"
for ch in name :
	print (ch,'-', end = '')

Output:
s-u-p-e-r-b-
```

## String Operators:

1) String operators are used to manipulate strings in multiple ways. 
2) For example,'+' operator is used to perform concatenation (Creating a new string by joining two strings. The strings here are the operand and concatenation is the operation)

### Basic operators

- String concatenation operator (+)

  
   -  The (+) operator creates a new string by joining two operand strings. For example: "tea" + "pot" will result into the string "teapot".
   
   -  You cannot concatenate numbers and strings together by means of the (+) operator. The (+) operator can either be used to add two numbers, (Here the operator performs the addition function), or used to concatenate two strings, (Here the operator performs the concatenation function).


- String replication operator-(*):
  - To use a (*) operator with strings, you need two types of operands - a string and a number, i.e., as number* string or string * number.
  - The string operand tells the string to replicated and number operand tells the number of times it is to repeated. Python will create a new string that is the same of number of repetitions as the number specified.
  - For example, 3 * "go!" will return 'go!go!go!'.
  - The (*) operator works with a string and a number for replication but never with two strings.

- Membership Operators:
  - There are two types of membership operators, and they are 'in', and 'not in', membership operators respectively.
  
  - The 'in' membership operator returns true if the characters of a string are present in another given string, otherwise false. Eg: "jap" in "heya" will give false as all of the characters of the first string aren't present in the second string.
  
  - The 'not in' operator returns true if the characters of a string don't exist in another given string, otherwise false. Eg: "jap" not in "Japan" will give false as all of the characters of the first string aren't present in the second.
    - Both operands used must be of string type.
    - Both the in and not in operators can also work with string variables. Consider this :
    
    ```
    >>> sub = "help"
    >>> string = 'helping hand'
    >>> sub2 = 'HELP'
    >>> sub in string
    True
    >>> sub not in string
    False
    ```

    *(Note that the above process is carried out in interactive mode).*
    
  - Example program to input an integer and check if it has zero in it:
  
         n = int(input("Enter a number:"))
         s = str(n)      # convert n to string
         if '0' in s:
             print("There's a 0 in",n)
         else:
             print("No 0 in",n)


- Comparison Operators:

  * Python's standard comparison operators i.e., all relational operators (<, <=, >, >=, ==, !=) apply to strings also.

  * The comparisons using these operators are based on the standard character-by-character comparison rules for Unicode (i.e., dictionary order).

  * Two strings are equal if all their characters (including the position of each character) exactly match. For characters that are letters, the cases of the letters must also match for two strings to be equal.

  * Python compares two strings through relational operators by comparing the Unicode values of the corresponding characters of the two strings. Eg: 'a'<'A' comparison will give false because the Unicode values of lower case letters are greater than that of upper case letters. Hence 'a' is greater than 'A', not lesser.
  * 2.4.5) Common characters and their Unicode (ordinal values):

| Characters | Unicode Values |
| ---------- | -------------- |
| '0' to '9' | 48 to 57       |
| 'A' to 'Z' | 65 to 90       |
| 'a' to 'z' | 97 to 122      |

## String Slices:

1) The term 'string slice' refers to a part of a string, where strings are sliced using a range of indices.

2) For any string s, if we give s[n : m], where n and m are integers and legal indices, Python will return a slice of the string returning the characters falling between the indices n and m (starting at n, n+1, n+2,... till m-1).

3) The characters of a string are given the positions 0,1,2,...,k-1, for the first,second,.... until the kth character of the string. In the 2nd point, n represents the position of the nth character, n+1 represents the position of the (n+1)th character, and so on.

4) Example: Taking the string 'amazing',which is stored within the string namely word:

   word[0:3] will give 'ama' (Letters from index 0 going up to 3-1 i.e., 2

5) If the first index of the string isn't specified, 0 will considered as the first index by default, and if the last index of the string isn't specified, the last index will then be the length of the string.

6) Example: Taking the same string;

   word(:5) will give 'amazi' (initial index is taken to be 0 by default).

7) You can also give a third (optional) index (say n) in string slice too. With that every nth element will be taken as a part of a slice e.g., for word = 'amazing', look at the following examples.

   word(1:6:2)

   (It will take every 2nd character starting from index = 1 till index<6.) Result will be 'mzn'.

8) Index out of bounds causes error with strings but slicing a string outside the bounds doesn't cause any error.

   Eg: 

```
s = 'Hello' 
print(s[5])
```

This will cause an error because 5 is invalid index out of bounds, for the string "Hello".

Instead if you give

```
s = 'Hello' 
print(s[4:8])
```

the above will not give any error and print output as: o (i.e, letter o followed by empty string in next line.)

1) Example program: Program to input a string and check if it is a palindrome string using a string slice.

```
s=input("Enter a string:")
if s==s[::-1]: 
	print(s,"is a palindrome.") 
else: 
	print(s, " is not a palindrome)
```

Output:

Enter a string : Mira  

Mira is not a palindrome.

## String Functions and Methods:

The various string manipulation methods and functions can be applied to a string as per the following syntax: 

```
<string Object>.<method name>()
```

Python's various built in string manipulation methods and functions are given below:

### The len() function:

 - It returns the length of its argument string, i.e.,it returns the count of characters in the passed string. It is also a standard library function.


 - Syntax: len(string)

   ```
   >>> len("hello")
   6
   
   >>> name = "Maria"
   >>> len(name)
   5
   ```

### The capitalize() method:

 - It returns a copy of the string with its first character capitalized.

 - Syntax: string.capitalize()

   ```
   >>> 'true'.capitalize()
   True
   
   >>> 'i love my India'.capitalize()
   I love my India
   ```

### The count () method:

  - It returns the number of occurrences of the substring sub in a string for a certain range of characters of the string.

  - The range of characters is specified in the syntax for a particular Count statement.

  - Syntax: string.count(sub[,start[,end]])

```
>>> 'abracadabra'.count('ab')   
2    

>>> 'abracadabra'.count('ab',4,8)
0
```




### The find() method

  - It gives the lowest index in the string where the substring sub is found within the slice range of start and end.

  - Returns -1 if  sub isn't found.


  - Syntax: string.find(sub[,start[,end]])

```
>>> string = 'it goes as - ringa ringa roses'
>>> sub = 'ringa'
>>> string.find(sub,15,22)
-1

>>> string.find(sub,15,25)
19
```



### The index method:

  - It returns the lowest index where the specified substring is found.


  - If the substring isn't found than an exception, ValueError, is raised.


  - Syntax: string.index(sub[,start[,end]])

```
>>> 'abracadabra'.index('ab')
0

>>> 'abracadabra'.index('ab',6)
7
```

### The isalnum() method

  - It returns true if the characters in the string are (alphabets or numbers) and there is at least one character. False otherwise

  - Syntax: string.isalnum()

```
>>> string = "abc123"
>>> string.isalnum()
True

>>> string1 = " "  
>>> string1.isalnum()
False
```

### The isalpha() method:

 - It returns true if all the characters in the string are alphabetic, false otherwise.


 - Syntax: string.isalpha()

```
>>> string = "abc123"
>>> string.isalpha()
False

>>> string1 = "hello"
>>> string1.isalpha()
True
```

### The isdigit() method

 - It returns true if all the characters in the string are digits, otherwise false.

 - Syntax: string.isdigit()

 - Examples: Considering the strings in the previous cases - for the first one false and the second one also false.

### The islower() method:

 - True if all cased characters in the string are lowercase (at least one cased character). It returns false otherwise.


 - Syntax: string.islower()

```
>>> string = "hello"
>>> string.islower()
True

>>> string2 = "There"
>>> string2.islower()
False
```

### The isspace() method

- It returns true if there are only whitespace characters in the string, otherwise false.

- Syntax: string.isspace()

```
>>> string = "   "
>>> string2 = ""

>>> string.isspace()
True

>>> string2.isspace()
False
```

### The isupper() method:

* It tests whether all cased characters in the string are uppercase and requires that there be at least one cased character. Returns true is so, otherwise false.

* Syntax: string.isupper()

```
>>> string = "Hello"
>>> string2 = "There"

>>> string.isupper()
True

>>> string2.isupper()
False
```

### The lower() method:

* It returns a copy of the string converted to lowercase.

* Syntax: string.lower()

* Examples: Considering the same string values in the previous example: The results are 'hello' and 'there'.

### The upper() method:

* It returns a copy of the string converted to uppercase.

* Syntax: string.upper()

* Examples: Considering the same string values used in the previous example: The corresponding results are "HELLO" and "THERE"

### The lstrip(), rstrip(), and strip() methods:

#### The lstrip method:

* Returns a copy of the string with the whitespaces form the left-most end removed.

* Syntax: string.lstrip()

  ```
  >>> " Sipo ".lstrip()
  'Sipo '
  ```

#### The rstrip method:

* Returns a copy of the string with whitespaces from the rightmost end removed.

* Syntax: string.rstrip()   

  ```
  >>> " Sipo ".rstrip()
  ' Sipo'
  ```

#### The strip() method:

* Returns a copy of the string with whitespaces from the right and left most end removed.

* Syntax: string.strip()

  ```
  >>> "Sipo".strip()
  'Sipo'
  ```

  

### The startswith(), endswith() method:

#### The startswith() method:

* Returns true if the string starts with the substring sub, otherwise returns false.
* Syntax: string.startswith(sub)

```
>>> "abcd".startswith("cd")
False
```

#### The endswith() method:

   - Returns true if the string ends with the substring sub, otherwise returns false.


   - Syntax: string.endswith(sub)

```
>>> "abcd".endswith("cd")
True
```



### The title() method:

- It returns a version of the string where all words in the string start with uppercase letters and all the remaining letters of each word are in lowercase.

- Syntax: string.title()

```
>>> "the sipo app".title()
'The Sipo App'
```

### The istitle() method:

- It returns true if the first letter of each word is in uppercase, while the rest of the letters are in lowercase., otherwise false.

- Syntax: string.istitle()

```
>>> 'Computer Science'.istitle()
True
```

### The replace() method:

- It returns a copy of the string with all occurences of substring old replaced by new string.

- Syntax: string.replace(old,new)

```
>>> 'abracadabra'.replace('ab','sp')
'spracadspra'
```

### The join() method:

- It joins a string or character (i.e.,) after each member of the string iterator i.e, a string based sequence.

- Syntax: string.join(string iterable)

- If the iterator is a string:

  ```
  >>> "*".join("Hello")
  'H*e*l*l*o'
  ```

- If the iterator is a list or a tuple of strings:

  ```
  >>> "$$".join(["trial","hello"])
  'trial$$hello'
  ```

  

### The split() method:

- It splits a string() based on the given string or character(i.e.,<string/char>) and returns a list containing the split strings as members.

- Syntax: .split(<string/char>)
- The default separator is whitespace.

```
>>> "I love Python".split()
['I','Love','Python']

>>> "I love Python".split("o")
['I', 'Love', 'Python']
```

### The partition() method:

- The partition() method splits the strings at the first occurrence of the separator, and returns a tuple containing three items
  -  The part before the separator.
  - The separator itself.
  - The part after the separator.
- Syntax: string.partition(separator)

```
>>> txt = "I enjoy working in Python"
>>> x = txt.partition("working")
>>> print(x)
('I enjoy', 'working', 'in Python')
```

## Sample programs:

1.

```
# Example Code for traversing through a string
name = "superb"
for ch in name :
	print (ch,'-', end = '')
      
Output:
s -u -p -e -r -b -
```

2.

```
#  Program to input a string and check whether it is a palindrome
#  using string slice.
s = input("Enter a string: ")
if  (s == s[::-1]) :
	print(s,"is a palindrome.")
else:
	print(s," is not a palindrome)

Output:
Enter a string: malayalam
malayalam is a palindrome.
```

3.

```
# Program that reads a line and prints its statistics like:

# Number of uppercase letters :
# Number of lowercase letters :
# Number of alphabets : 
# Number of digits :
# Number of symbols

line = input("Enter a line:")
lowercount = uppercount = 0
digitcount = alphacount = symcount = 0
for a in line :
     if a.islower() :
            lowercount += 1
     elif a.isupper()  :
        uppercount += 1
     if a.isdigit() :
        digitcount += 1
     if a.isalpha() :
        alphacount += 1
     elif a.isalnum() != True and a != ' ' :
        symcount += 1
        
print("Number of uppercase letters:",uppercount)
print("Number of lowercase letters:",lowercount)
print("Number of alphabets:",alphacount)
print("Number of digits:",digitcount)
print("Number of symbols:",symcount)
    
Output:
Enter a line: Hello, world!
Number of uppercase letters: 1
Number of lowercase letters: 9
Number of alphabets: 10
Number of digits: 0
Number of symbols: 2
```

4.

```
# Program that inputs a string that contains a decimal number and 
# prints out the decimal part of the number
s = input("Enter a string (a decimal number):")
t = s.partition('.')
print("Given string:",s)
print("part after decimal",t[2])

Output:
Enter a string (a decimal number):12.980
Given string: 12.980
part after decimal 980
```