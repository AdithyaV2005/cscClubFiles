# LIST MANIPULATION

## Creating Lists

In [2]:

```
l=[]
l=[2,3]
```

This construct is known as list display construct

You have 3 kinds of lists

- Empty list
- Long list
- Nested list



## Creating lists from existing sequences<\h2>

In [3]:

```
l1 = list('hello')
print(l1)

Output:
['h', 'e', 'l', 'l', 'o']
```

In [4]:

```
l1 = list(input("Enter list elements:"))
print(l1)

Output:
['h', 'e', 'l', 'l', 'o']
```

eval method. Most commonly used for integers

In [5]:

```
l1 = eval(input("Enter list to be added: "))
print(l1)

Output:
Enter list to be added: 10, 20, 21
(10, 20, 21)
```

**NOTE**:  *eval* may not work always in python shell

## Accessing Lists



### Length

len() function gives number of elements in the string





### Indexing and Slicing

L[i] returns the item at index i( indexing begins at 0)

L[i:j] returns a new list containing objects at indexes between i and j(excluding j)





### Membership operators

in- tells whether element is present in list

not in - confirms that element is not in list





### Concatenation and Replication Operators (+ and *)



- Plus (+) : combines elements present in 2 lists end to end
- Asterisk (*) : repeats a list twice (for example [1,2,3,1,2,3])



## Accessing Individual elements

You can access elements in a list through normal indexing  

Here is where lists are different from strings, you can replace elements of a list



In [6]:

```
vowels=list('aeiou')
print(vowels)
vowels[0]='A'
print(vowels)
# Notice the replacement of the first element

Output:
['a', 'e', 'i', 'o', 'u']
['A', 'e', 'i', 'o', 'u']
```



## Traversing a list

Traversing means processing each element of a list. 

For example, going through each element in a list and printing it. 

The for loop makes our job easier:



In [7]:

```
L = list("python")
for a in L:
    print(a)
    
Output:
p
y
t
h
o
n
```

You can traverse using indexes too

In [8]:

```
L=list("python")
for index in range(len(L)):
    print(L[index])
    
Output:
p
y
t
h
o
n
```

## Comparing Lists

For two lists to be equal,we have 3 conditions

1. Each corresponding element must be equal
2. No of elements must be equal
3. The Lists must be of the same type

### Non-Equality comparisons

The Individual elements are compared in ordered format
1st element of (list 1) is compared to 1st element of (list 2)
if they are not equal, it prints true or false
if they are equal, it moves on to comparing the second elements
**Refer to table on page 376**

## List operations

### Joining lists

The following programs show how lists can be joined and how they cannot. If you see a try except block, just know that it is there to get a concise version of the error in the statement.

In [10]:

```
[1, 2, 3] + [4, 5, 6]
```

Out[10]:

```
[1, 2, 3, 4, 5, 6]
```

In [29]:

```
try:
    l1 = [1, 2, 3, 4] + 5
except Exception as e:
    print(type(e), ':', e)
    
Output:
<class 'TypeError'> : can only concatenate list (not "int") to list
```

**Note: += and -= work for adding iterables (like strings) to lists, but can't add... say, integers**

In [32]:

```
l = [1, 2, 3]
l += "abc"
print(l)

Output:
[1, 2, 3, 'a', 'b', 'c']
```

In [30]:

```
l = [1, 2, 3]
try:
    l += 5
except Exception as e:
    print(type(e), ':', e)
    
Output:
<class 'TypeError'> : 'int' object is not iterable
```

### Replicating lists

In [34]:

```
l = [1, 2, 3]
print(l * 3)

Output:
[1, 2, 3, 1, 2, 3, 1, 2, 3]
```

### Slicing lists

- Use 0, 1, 2, 3 to index from the left
- Use -1, -2, -3 to index from the right
- Use : to separate the start index, end index and step
- Unlike indexing, slicing doesn't give Index Errors if index is out of range

In [38]:

```
digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]

try:
    print(digits[100])
except Exception as e:
    print(type(e), ':', e)
    
try:
    print(digits[0 : 101])
except Exception as e:
    print(type(e), ':', e)
    
Output:
<class 'IndexError'> : list index out of range
[1, 2, 3, 4, 5, 6, 7, 8, 9, 0]
```

You can also leave the *start*, *stop* and *step* arguments empty if you want to.

In [41]:

```
digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]

odd_digits = digits[::2] # Same as digits[0: -1: 2], it assumes the extreame indexes
print(odd_digits)

Output:
[1, 3, 5, 7, 9]
```

Slices can be used to modify lists

In [43]:

```
planets = ["Earth", "Mars", "Jupiter", "Saturn"]
planets[2:] = ["Supiter", "Jaturn"]
print(planets)

Output:
['Earth', 'Mars', 'Supiter', 'Jaturn']
```

## Making a true copy of a list

If you set list2 = list1, then both variables point to the same list. So, if you change list1, list2 also changes.

In [46]:

```
list1 = ["Jupiter", "Saturn"]
list2 = list1
list1[:] = ["Supiter", "Jaturn"]
print(list2)

Output:
['Supiter', 'Jaturn']
```

To make an independent copy of list1, you can use the list function:

In [47]:

```
list1 = ["Jupiter", "Saturn"]
list2 = list(list1)
list1[:] = ["Supiter", "Jaturn"]
print(list2)

Output:
['Jupiter', 'Saturn']
```

The copy function:

In [48]:

```
list1 = ["Jupiter", "Saturn"]
list2 = list1.copy()
list1[:] = ["Supiter", "Jaturn"]
print(list2)

Output:
['Jupiter', 'Saturn']
```

Or the just set list2 as a complete slice of list1:

In [49]:

```
list1 = ["Jupiter", "Saturn"]
list2 = list1[:]
list1[:] = ["Supiter", "Jaturn"]
print(list2)

Output:
['Jupiter', 'Saturn']
```

## List functions

I think the functions are self explanatory.

In [53]:

```
odd_digits_dictionary = {1: "one", 3: "three", 5: "five", 7: "seven", 9: "nine"}

# 1. list()
odd_digits = list(odd_digits_dictionary)
print(odd_digits)

# 2. len()
print(len(odd_digits))

# 3. index()
print(odd_digits.index(9))

# 4. append() and extend()
planets = ["Mercury"]
planets.append("Venus") # Append adds an element to the end
planets.extend(["Mars", "Jupiter"]) # Extend adds the elements of a list to the end
print(planets)
# Both do not return any value, they just modify the list

# 5. insert()
planets.insert(2, "Earth") # Adds "Earth" at index 2 (3rd planet)
print(planets)

# 6. pop() and remove()

planets.pop(0) # Removes planet with index 0 (Mercury)
planets.pop() # Removes last planet in the list (Jupiter)
# Returns IndexError if index is out of range

planets.remove("Venus") # Removes Venus
# Returns ValueError if list does not contain the value
print(planets)

# 7. clear()
planets.clear() # Annihilates the solar system
print(planets)

# 8. count()
print(planets.count("Earth")) # Returns the number of Earths among the planets (currently zero)

# 9. reverse()
odd_digits.reverse() # Reverses the elements in the list, but doesnt return anything
print(odd_digits)

# 10. sort() and sorted() - Both have optional parameter reverse which is set to False by default

odd_digits = sorted(odd_digits) # Sorted creates a new list
print(odd_digits)

odd_digits.sort(reverse=True) # Sort simply sorts the list, and doesn't return a new list
print(odd_digits)

# The final trio: min(), max() and sum()
print(min(odd_digits), max(odd_digits), sum(odd_digits))

Output:
[1, 3, 5, 7, 9]
5
4
['Mercury', 'Venus', 'Mars', 'Jupiter']
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter']
['Earth', 'Mars']
[]
0
[9, 7, 5, 3, 1]
[1, 3, 5, 7, 9]
[9, 7, 5, 3, 1]
1 9 25
```

## Nested lists

A list which has lists inside it is called a nested list

In [57]:

```
l = [1, [2, 3], [[4, 5], [6, 7]], [8, [9]]]
print(l[0])
print(l[1][0])
print(l[2][1][0])

Output:
1
2
6
```

A 2D list is a list of list, but that's as far as they go.
The lists inside the 2D list do not have any more lists.

2D lists are of two types:

- **Ragged list**: The lists in it have different shapes (lengths)
- **Regular list**: The lists in it have the same shape. It can be thought of as a matrix. The length of a regular list gives the number of rows in it and the length of each row gives the number of columns

In [60]:

```
# Creating a 2d list of coordinates:
list_of_coordinates = []
nP = int(input("Number of points: "))
nD = int(input("Number of dimensions: "))
for iP in range(nP):
    print("\nPoint", iP + 1)
    coordinates = []
    for iD in range(nD):
        if iD == 0:
            msg = "x: "
        elif iD == 1:
            msg = "y: "
        elif iD == 2:
            msg = "z: "
        else:
            msg = "Dimension " + str(iD + 1) + ": "
        coordinates.append(int(input(msg)))
    list_of_coordinates.append(coordinates)
    
print(list_of_coordinates)


Output:
Number of points:  2
Number of dimensions:  2

Point 1
x:  12
y:  -4

Point 2
x:  22
y:  7
[[12, -4], [22, 7]]
```

In [70]:

```
def distance(p1, p2):
    '''
    Calculates distance between two points using the Distance Formula
    '''
    return ((p1[0] - p2[0]) ** 2 + (p1[1] - p2[1]) ** 2) ** 0.5

# Traversing through a list of coordinates
def perimeter(vertices):
    '''
    Given the vertices of a polygon, returns the perimeter
    '''
    l = len(vertices)
    if l == 0:
        return 0
    
    vertices.append(vertices[0])
    d = 0
    
    for i in range(1, l):
        d += distance(vertices[i - 1], vertices[i])
    return d

print(perimeter([[1, 1], [2, 2], [1, 2]]))

Output:
2.414213562373095
```

In [75]:

```
# Accessing/changing individual elements
# Let us learn how to make kid friendly comments

swear_words = ['shit', 'damn', 'crap']
comment = '''HOLY CRAP THAT WAS CRAAZYY!!!
Didn't see that shit coming.
That was damn smart, wasn't it?
'''

def split_text(text):
    lines = []
    for line in text.split('\n'):
        words = []
        for word in line.split():
            words.append(word)
        lines.append(words)
    return lines

def reconstruct_text(text_list):
    text = ""
    for line in text_list:
        for word in line:
            text += word + " "
        text += "\n"
    return text

def kid_friendly(text):
    l = split_text(text)
    for i1 in range(len(l)):
        for i2 in range(len(l[i1])):
            if l[i1][i2].lower() in swear_words:
                l[i1][i2] = '####'
    return reconstruct_text(l)
    
print(kid_friendly(comment))

Output:
HOLY #### THAT WAS CRAAZYY!!! 
Didn't see that #### coming. 
That was #### smart, wasn't it? 
```

## Working with lists

To work with lists, all you have to do is to use the right list function at the right time. So, you might want to review the list functions once more.
Also, you can delete a sublist from a list using the del function:

In [77]:

```
terrestrial_planets = ["Mercury", "Venus", "Earth", "Mars"]
del terrestrial_planets[:2] # Sun becomes red giant
print(terrestrial_planets)

Output:
['Earth', 'Mars']
```