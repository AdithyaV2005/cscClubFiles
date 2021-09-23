# Understanding Sorting

Sorting in a computer means arranging elements in a specific order or manner. This can be anything, normally, such as ascending, descending, or anything specific such as all- even, all-odd elements, etc. Sorting is done for the purpose of organization, or better understanding in a user interface.

example of elements: [1,2,3,4,5,6], etc.

### Types of Sorting

There are 2 main types of sorting methods:

- Bubble Sort
- Insertion Sort

### Bubble Sort

During a bubble sort, two adjoining values in an element are compared together, and are exchanged if they are not in proper order of requirements.

Here's a program example for the bubble sort:

```
alist=[15,6,13,22,3,52,2]
print("original list is:", alist)
n=len(alist)
#traverse through all list elements:
for i in range(n):
    #last i elements are already in place.
    for j in range(0,n-i-1):
        # traverse the list from 0 to n-i-1
        # swap if the element is found greater than the next element.
    
        if alist[j]>alist[j+1]:

            alist[j], alist[j+1]= alist[j+1], alist[j]
print("list after sorting is:",alist)

Output:
original list is: [15, 6, 13, 22, 3, 52, 2]
list after sorting is: [2, 3, 6, 13, 15, 22, 52]
```

#### Possibilities

The number of swapping will vary depending on the elements of the sequence. Here,

##### Best case:  

When all elements of the sequence are already sorted, in which case there are **N^2 comparisons** and **0 swaps**. Total operations = **N^2**

##### Worst case: 

When all the elements are in exact opposite order, in which case there will be approx. **N^2 comparisons** and **N^2 swaps**. Total operations = **2N^2**

### Insertion Sort

Insertion sort is a method of sorting that builds a sorted list of one element at at time from the unsorted list, by inserting he element at its correct position in the sorted list.

Here's is a program example of the insertion sort:

```
alist=[15,6,13,22,3,52,2]
print("Original list is:",alist)
for i in range (1,len(alist)):
    key= alist[i]
    j=i-1
    while j>=0 and key < alist[j]:
        alist[j+1] = alist[j]# shift elements to right to make room for key 
        j=j-1
    else:
        alist[j+1]=key
print("List after sorting:", alist) 

Output:
Original list is: [15, 6, 13, 22, 3, 52, 2]
List after sorting: [2, 3, 6, 13, 15, 22, 52]
```

### Possibilities

Here,

##### Best case: 

When the sequence is already in desired order, there will be at most **n-1** number of comparison and exchanges.

##### Worst case: 

In the worst case, there will be maximum possible number of comparisons and exchanges, whose value is less than **N^2**.

### Number of Operations

The number of operations is a very important aspect to know as the amount of CPU time is defined by the total number of operations performed to sort , and this depends upon how the elements initially exist before sorting.

1. ***Operations consist of 3 functions: the assignment, the comparison and the swap. All of these can be considered as 1 operation, for better understanding.***

2. ***The more efficient the program is, the faster the sorting can take place.***

3. ***The number of operations computed is determined by how efficient and logically written the program is, and by the best and worst cases possibly occurring for elements, for each type of sort. They are mentioned above.***

### That's it guys! Hope y'all find this a bit useful!