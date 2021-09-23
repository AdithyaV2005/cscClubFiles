# Flow of Control

## Types of Statements in Python

1. Empty Statement
   - A null statement or a statement which does nothing.
   - In python, it is the `pass` statement.
2. Simple Statement
   - A single executable statement.
   - Single line statements.
   - eg. `print(name)`
3. Compound Statement
   - A group of statements executed as a unit.
   - Composes of:
     - A header line that begins with a keyword and ends with a colon.
     - A body that consists of simple or compound statements, **indented** inside the header line.

## Types of Statement flow of control

1. Sequence
   - Statements executed sequentially, that is, one after another in the way the program is written.
   - It is the **default** flow of control in a program and is the simplest one.
2. Selection
   - Statements executed based on a condition test.
   - If the condition is True, the first set of statements are executed and if the condition is False, the second set of statements are executed.
   - This type is also called **decision construct**.
3. Looping / Repetition Iteration
   - It is the repetition of a set of statements depending upon a condition test.
   - A set of statements are repeated until the condition turns from True to False.
   - This type is also called **looping construct**.
   - Each time the loop body is executed, it is called an **iteration**.
   - Conditions used in looping statements can be stored in variables. Eg. `equal_sides = a==b and b==c`

## The `if - elif - else` Statement

- It checks condition after condition, executes the block of code that first gives True and then exits the loop.

- There is **no limit** on the elif block.

- Syntax:

  ```
  if <conditional_expression> :  
    	[statements]  
  elif <conditional_expression> :  
    	[statements]  
  elif <conditional_expression> :  
    	[statements]  
  else <conditional_expression> :  
    	[statements]  
  ```

## Nested if

- It is an if - elif - else statement inside an if - elif - else statement.

- Eg. To check the sign of a number:

  ```
  num = 15  
  if num >= 0:  
    if num == 0:  
        print("Zero")  
    else:  
        print("Positive number")  
  else:  
    print("Negative number")  
  ```

  > Positive number

## `range()`

- range() generates a list of integers based on the arguments passed.
- Syntax: `range(<lower limit>, <upper limit>, <step value>)`
- The upper limit is **not included** in the list.

| Statement     | Values    |
| :------------ | :-------- |
| range(5)      | 0,1,2,3,4 |
| range(2,5)    | 2,3,4     |
| range(2,10,2) | 2,4,6,8   |
| range(7,1,-2) | 7,5,3     |

## `in` and `not in`

- `in` and `not in` are called **membership operators**
- These operators work with all sequences datatypes (strings, tuples, lists and dictionary)
- The `in` operator checks if a given value is present in a sequence or not and return True or False accordingly.
- The `not in` operator return the opposite of what `in` would return.
- Eg.

```
5 in [1,2,3,4]  
```

> False

```
5 not in [1,2,3,4]  
```

> True
>
> ## The `for` loop
>
> - Also known as counting loops since it repeats for a certain amount of times
>
> - The looping variable **does not** need to initialized for a for loop.
>
> - Syntax:
>
>   ```
>   for <variable> in <sequence>:  
>     	[statements]  
>   ```

## The `while` loop

- Also known as conditional loops since it repeats until the conditional turns false.

- The looping variable **does** need to initialized for a while loop.

- The looping variable must also be updated in the loop body.

- Syntax:

  ```
  while <test_condition>:  
    	loop_body  
    	update_expression  
  ```

## The `break` statement

- The break statement terminates the **loop it lies within**.  

![img](https://cdn.programiz.com/sites/tutorial2program/files/flowchart-break-statement.jpg)

## The `continue` statement

- The continue statement is used to skip the rest of the code inside a loop for the current iteration only.
- Loop **does not** terminate but continues on with the next iteration.  

![img](https://cdn.programiz.com/sites/tutorial2program/files/continue-statement-flowchart.jpg)

## Loop `else` statement

- The else statement executes when the loop terminates normally, i.e., when the condition becomes false for a while loop and once the last iteration has been completed for a for loop

- It **does not** execute when `break` terminates the loop.

- Syntax:

  ```
  for <variable> in <sequence>: / while <test_condition>:  
      [statements]  
  else:  
      [statements]  
  ```