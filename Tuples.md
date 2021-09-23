# Tuples

### Definition

A tuple is an immutable data type in python that can store a sequence of characters belonging to different data types.

### Types of tuples

1. Empty tuples
2. Single element tuple
3. Long tuples
4. Nested tuple

### Creating tuples from sequences

##### Syntax:- 	

***t1 = tuple()***

```
t1=tuple('joe')
print(t1)
```

> OUTPUT:-  
> ('j','o','e')

## Indexing of tuples

Indexing in tuples is similar to that of lists.
For example, let tuple1 = ('a','b','c','d','e')

```
          0  1  2  3  4
          a  b  c  d  e  
         -5 -4 -3 -2 -1
```

len(tuple1)- returns the number of items in the tuple
tuple1[1]- returns 1st element
tuple1[2:7]-returns a tuple with objects from index 2 to index 7

<br>

## Mutable lists in tuples

Unlike tuples, lists are mutable data types.

```
t = ([6,8],[4,2,0])
```

This tuple has 2 lists. To change the items of the lists:

```
t(0)(1) = 9 #to change the second item of the first list in the tuple
print(t)
```

 output- 

> ([6,9],[4,2,0])

## Traversing a tuple

#### Syntax

```
for (item) in (tuple):
	print(tuple[item])
```


For example, if the tuple is ('c', 's' ,'c') then:

> OUTPUT:  
> c  
> s  
> c  

# Tuple operations

### Joining tuples

```
tpl1 = (1,3,5)
tpl2 = (6,7,8)
tpl = tpl1 + tpl2
print(tpl)
```

> OUTPUT (1,3,5,6,7,8)

*NOTE* -tuples cannot be added to items with other data types

# Slicing the tuples

Tuples slices are sub parts of a tuple extracted out.

### Syntax :

```
seq = tpl[start:stop]
```

The following syntax can be also used when we need to skip a few items:

```
seq = tpl[start:stop:step]
```

### Example for slicing tuples

```
tpl = (1, 2, 3, 4, 5)
seq = tpl[1:3]
print(seq)
```

> OUTPUT:  
> (2,3,4)

## Comparing tuples

For comparing two tuples we can use the comparing operators >,<,==,!= etc.
Python internally compares individual elements of two tuples.

### Example for comparing tuples

```
t1 = (6,9)
t2 = (2,3)
print(t1<t2)
```

Output:

> False

## Unpacking of tuples

##### Definition

Creating individual elements from tuples by assigning variables to the elements of a tuple.

### Example for unpacking of tuples

```
t = (1,2,3,4,5)
j, o, e, m, a = t
print(j)
print(m)
```

> OUTPUT:  
> 1  
> 4

## Tuple functions

<br>

| S.NO | FUNCTION                                  | DESCRIPTION                                                |
| :--- | :---------------------------------------- | :--------------------------------------------------------- |
| 1.   | len(tuple)                                | returns the length of the tuple                            |
| 2.   | max(tuple)                                | returns the element of the tuple having maximum value      |
| 3.   | min(tuple)                                | returns the element of the tuple having minimum value      |
| 4.   | sum(tuple)                                | returns the sum of the elements of tuple                   |
| 5.   | tuplename.index(item)                     | returns the index of the existing item of the tuple        |
| 6.   | sequence_name.count(object)               | returns the count of a member elements in a given sequence |
| 7.   | sorted(iterable_sequence,[reverse=False]) | returns a new sorted list with sorted elements in it       |
| 8.   | tuple(sequence)                           | used to create tuples from different types of values       |

### Example for count() function

```
t1 = (1,1,2,3,4,5)
t2 = t1.count(1)
print(t2)
```

> OUTPUT:  
> 2

### Example for sorted() function

tupl1 = (4,2,0,69)
tupl2 = sorted(tupl1, reverse=True)
print(tupl2)

> OUTPUT:  
> (69, 4, 2, 0)

## Indirectly modifying tuples

#### Using tuple unpacking

Tuples are immutable data types. Hence to modify it, we unpack it, change the values and repack it.

### Example for modifying using unpacking

```
tpl = (4, 2, 2, 6, 9)
a, b, c, d, e = tpl
c = 0
tpl = (a, b, c, d, e)
print(tpl)
```

> OUTPUT:  
> (4,2,0,6,9)

### Modification by converting to lists

1. Convert the tuple to list, which is mutable
2. Make changes in the desired elements of the list
3. Create a tuple from the modified list using tuple()

### Example for modification by converting to lists

```
tpl = ('ben', 4, 2, 0)
lst = list(tpl)
lst[0] = 'ben dover'
tpl = tuple(lst)
print(tpl)
```

> OUTPUT:  
> ('ben dover',4,2,0)

## Nested tuples

A tuple containing another tuple in it as an element is called a nested tuple
Example of a nested tuple is -

```
tpl=(1,2,3,(6,9))
print(len(tpl))
```

OUTPUT:

> 4

### Accessing individual elements of inner tuple

```
tpl = (1, 2, 3, (4,5,6))

# tuple name[index of inner tuple][index of element inside inner tuple]
tpl2 = tpl[3][1]

print(tpl2)
```

OUTPUT: 

> 4

## Functions for nested tuples

The functions such as len(), count(), index() work the same with nested tuples.
The max() and min() functions only work when all the elements of a nested tuple are tuple The sum() function won't work with nested tuples as tuples cannot be added with elements of the other data types.

## Example for functions of nested tuples

```
tpl1 = (12, 'mike', (1,2,3,4))

print(max(tpl1[2]))
print(min(tpl1[2]))
print(sum(tpl1[2]))
```

> OUTPUT:  
> 4  
> 1  
> 10