# Dictionaries

### What is a Python Dictionary?

A python dictionary is a collection of elements where each element is a Key-Value pair. Each value is associated with a unique key. All the Key-Value pairs are enclosed in Curly braces. In other words we can say:

***”Dictionaries are mutable, unordered collection of elements in the form of Key-Value Pairs which are enclosed in curly braces“***

* Internally, dictionaries are **indexed** on the basis of **keys**
* Dictionaries are also called **associative arrays** or **mappings** or **hashes**
* Different Key-Value pairs are separated by commas (,)

### Examples of Dictionaries:

```
numbers = {1 : "One", 2 : "Two", 3 : "Three"}
alphabet = {"A" : "Apple", "B" : "Ball", "C" : "Cat"}
```

### Characteristics of Python Dictionary:

* A dictionary is an **unordered** set of Key-Value pairs.
* Unlike strings, lists and tuples; a dictionary is **not a sequence** (since the elements are not ordered).
* Values in a dictionary are **indexed using keys**, not numbers.
* Keys are **unique** for each Value.
* Dictionaries are **mutable**, but the keys of a dictionary must be of **immutable** type. If you try to assign a key with a mutable type, you will get a TypeError.
* Dictionaries are internally stored as **mappings**. The keys and values are associated using a **hash function**.

```
d = {[1, 3, 5, 7, 9]: "odd", [2, 4, 6, 8, 0]: "even"}

Output:
TypeError: unhashable type: 'list'
```

### Accessing elements

A dictionary operation that takes a key and finds its value is called a **lookup**.

To get the keys and values in a dictionary, you can use the .keys() and .values() functions

```
houses = {"Harry": "Gryffindor", "Luna": "Ravenclaw"}
print(list(houses.keys()))
print(list(houses.values()))
print(houses["Luna"])
print(houses["Dudley"])

['Harry', 'Luna']
['Gryffindor', 'Ravenclaw']
Ravenclaw
Traceback (most recent call last):
  File "<string>", line 5, in <module>
KeyError: 'Dudley'
```

### Using the dict() method to create a dictionary:

Avoid using this methods unless necessary as they take **longer time** compared to just using {}.

```
# Empty dictionary
empty = dict()

# Key value pairs as arguments
alphabet = dict(A="Apple", B="Ball", C="Cat") 

# Comma separated Key Value pairs
numbers = dict({1 : "One", 2 : "Two", 3 : "Three"}) 

# Using zip function to specify keys and values separately
details = dict(zip(("Name", "Salary", "Age"), ("Carol", 10000, 37))) 

# Key value pairs in the form of sequences
scores = dict([["Ada", 7], ["Bob", 5]])

print(empty, alphabet, numbers, details, scores, sep="\n")

Output:
{}
{'A': 'Apple', 'B': 'Ball', 'C': 'Cat'}
{1: 'One', 2: 'Two', 3: 'Three'}
{'Name': 'Carol', 'Salary': 10000, 'Age': 37}
{'Ada': 7, 'Bob': 5}
```

###  Traversing a Python Dictionary:

It means to access each element of dictionary by using a loop. 
For example:

```
A = {1 : "One", 2 : "Two", 3 : "Three"} 
for k in A:   
	print(k, "--->", A[k])
	
Output:
1 ---> One
2 ---> Two
3 ---> Three
```

Here is an example where a dictionary is created using a for loop:

```
d = {}
for i in range(3):
	r=int(input("Enter a number: "))
	name=input("Enter a name: ")
	d[r] = name
print(d)

Output:
Enter a number: 1
Enter a name: Ada
Enter a number: 2
Enter a name: Carl
Enter a number: 3
Enter a name: Ned
{1: 'Ada', 2: 'Carl', 3: 'Ned'}
```

Here is another example:

```
d = {}
for i in range(2):   
	b_id = int(input("Enter book id : "))
	b_name = input("Enter book name : ")
	b_price = int(input("Enter price of book : "))
	
	temp=[b_name,b_price]
	dict[b_id] = temp
	
	print()
print(dict)

Output:
Enter book id : 113
Enter book name : Frankenstein
Enter price of book : 155

Enter book id : 114
Enter book name : La La Land
Enter price of book : 150

{113: ['Frankenstein', 155], 114: ['La La Land', 150]}
```

### Adding new elements to a dictionary:

We have already seen how to add values in the example programs above.

```
A = {1 : "One", 2 : "Two", 3 : "Three"} 
A[4] = "Four"
print(A)

Output:
{1: 'One', 2: 'Two', 3: 'Three', 4: 'Four'}
```

### Update values in a Python Dictionary :

We can not change the key of an element, but can change the value of a respective key as follows

```
B = {1: 'Amit', 2: 'Sunil', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
B[2] = 'Ram'
print(B)

Output:
{1: 'Amit', 2: 'Ram', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
```

### Removing an element from a Dictionary:

There are two ways by which we can delete the elements of dictionary:

1. **By using del statement :**
   Syntax of using del statement is: del dictionary[key]

   ```
   B = {1: 'Amit', 2: 'Sunil', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
   del B[2] # It will remove the element of key 2
   print(B)
   
   Output:
   {1: 'Amit', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
   ```

2. **By Using pop() function**: 

   This function not only deletes the element of required key but also return the deleted value. For example:

   ```
   B = {1: 'Amit', 2: 'Sunil', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
   a=B.pop(2) #It returns the element of Key - 2
   print(a)
   print(B)
   
   Output:
   Sunil
   {1: 'Amit', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
   ```

   Here is another one:

   ```
   B = {1: 'Amit', 2: 'Sunil', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
   a=B.pop(9, "Not here") # If there is no key 9, returns "Not here"
   print(a)
   print(B)
   
   Output:
   Not here
   {1: 'Amit', 2: 'Sunil', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
   ```


### Checking for the existence of a key

The **in** and **not in** operators check the existence of keys in dictionaries.

```
>>> numbers = {"One": 1, "Two": 2}
>>> "One" in numbers
True
>>> 1 in numbers
False
```

### Pretty printing a dictionary

Use **json.dumps()** to pretty print dictionaries.

```
import json
numbers = {"One": 1, "Two": 2}
print(numbers)
print(json.dumps(numbers, indent=2))

Output:
{'One': 1, 'Two': 2}
{
  "One": 1,
  "Two": 2
}
```

### Counting the frequency of elements in a list using a dictionary

```
def word_counts(text):
    d = {}
    words = text.split()
    for word in words:
        d[word] = words.count(word)
    return d

print(word_counts("Hello? Hello? Who is there? Who is this?"))

Output:
{'Hello?': 2, 'Who': 2, 'is': 2, 'there?': 1, 'this?': 1}
```

### Extend or update Dictionary with new key value pairs

We can also join two dictionaries into one by using update() method. It merges the keys and values of one dictionary into other and overwrites the values of the same key.

```
A = {1 : "One", 2 : "Two", 3 : "Three"}
B = {1: 'Amit', 2: 'Sunil', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
A.update(B)
print(A)

Output:
{1: 'Amit', 2: 'Sunil', 3: 'Three', 5: 'Lata', 6: 'Suman', 7: 'Ravi'}
```

### Dictionary functions:

It would be tedious to memorize each and every function separately, so here is a program which uses them all. 

I recommend copying the program in IDLE, running it, and comparing it with the output.

```
planets = {1: "Mercury", 2: "Venus", 3: "Earth", 4: "Mars"}
terrestrials = planets.copy() # Shallow copy
print(terrestrials)

print(len(planets))
print(planets.items())
print(planets.keys())
print(planets.values())
print()

for i in range(1, 9):
    planets.setdefault(i, "Unknown") # If value exists, returns the existing value
print(planets)

gas_giants = {5: 'Jupiter', 6: 'Saturn', 7: 'Uranus', 8: 'Neptune', 9: 'Pluto'}
planets.update(gas_giants)
print(planets.popitem()) # Removes lastly added pair
print(planets.pop(9, "Not here")) # If there is a ninth planet, deletes it. Otherwise returns "Not here"
print(planets)
print()

planets.clear() # Annihilates all planets

digits = dict.fromkeys([1, 5, 3, 9, 7], "odd")
print(sorted(digits), max(digits), min(digits), sum(digits))

Output:
{1: 'Mercury', 2: 'Venus', 3: 'Earth', 4: 'Mars'}
4
dict_items([(1, 'Mercury'), (2, 'Venus'), (3, 'Earth'), (4, 'Mars')])
dict_keys([1, 2, 3, 4])
dict_values(['Mercury', 'Venus', 'Earth', 'Mars'])

{1: 'Mercury', 2: 'Venus', 3: 'Earth', 4: 'Mars', 5: 'Unknown', 6: 'Unknown', 7: 'Unknown', 8: 'Unknown'}(9, 'Pluto')
Not here
{1: 'Mercury', 2: 'Venus', 3: 'Earth', 4: 'Mars', 5: 'Jupiter', 6: 'Saturn', 7: 'Uranus', 8: 'Neptune'}

[1, 3, 5, 7, 9] 9 1 25
```

Note that the copy() function above creates only a shallow copy, whereby only a copy of the keys is created and the values are not copied (only referenced). Here is a short article which explains the difference between shallow and deep copy. Note that deep copy is not in our syllabus, but I encourage you to read it if you are interested.

[Different ways to copy a dictionary](https://www.programiz.com/python-programming/shallow-deep-copy)