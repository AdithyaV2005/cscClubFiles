# Chapter 5: Introduction to Problem Solving

## PROBLEM SOLVING CYCLE

In order to create efficient and effective programs, you must follow a cycle- ***a problem solving cycle***.



### STEPS FOR SOLVING A PROBLEM

#### Four main steps of problem solving:



1. **Identify** and **analyse** the problem

2. **Find its solution** and **Development algorithm** of the solution.

3. **Code the solution** in a programming language

4. **Test** and **Debug** the coded solution

   and finally, **implement** and **maintain** it.
   
   

#### Sub-steps of problem solving:



##### ANALYSE THE PROGRAM:

1. Understand the problem well.

2. While analyzing, 

   - Identify the processing components

   - Identify the relationship along processing components

     

##### DEVELOPING THE ALGORITHM:

1. Think of possible solutions and zero on most appropriate one.
2. Follow Modular approach while designing most appropriate solution
   - Modular approach is dividing a big problem into smaller and manageable and understandable modules
   - Decide step by step solution
   - Break down solution into simple steps
3. Identify operations for solution
   - Identify minimum number of inputs required.
   - Identify arithmetic and logical operations required
   - Identify simple and efficient data structures.



##### CODING:

1. Code program using appropriate control structures
   - Coding is to translate the algorithm into a programming language.
   - Use appropriate control structures such as conditional and looping control structures.
   - Think programs efficiency in terms of speed, performance and effectiveness.



##### TESTING AND DEBUGGING:

1. Test and debug your program
   - Testing is the process of finding errors in a program.
   - Debugging is the process of correcting errors found in a program.
2. Complete your documentation
   - It is to allow another programmer at a later date to understand the program.
   - It might also consist of a detailed description



##### IMPLEMENT AND MAINTAIN:

1. Implement your code for real users to use your program.
2. Maintain your program
   - Modify- to remove undetected errors
   - Enhance- with different features and functions
   - Keep the program up-to-date as government regulations or company policy.



### PROBLEM SOLVING USING DECOMPOSITION

The process of breaking down a big/complex problem into a set of smaller sub-processes in order to understand the problem better is called as decomposition. It is important because, large problems are disproportionately harder to solve than smaller ones.

It involves,

- Dividing a task into sequence of subtasks.
- Identifying elements or parts of a complex system.



## DESIGNING ALGORITHMS

The set of rules that define how a problem can be solved in a finite number of steps is called as algorithm. It is composed of finite steps, each of which may gave one/more operations.

Constraints on the type of operations as algorithm:

- Each operation must be **definite**.
- Each operation must be **effective**
- Each operation must be **finite**.



##### **Characteristics of a good Algorithm:**

1. **Precision**

   ​     Steps must be precisely defined.

2. **Uniqueness**

   ​     Every step must uniquely contribute to the algorithm.

3. **Finiteness**

   ​     An algorithm must stop after a finite number of instructions. It shouldn't repeat the steps.

4. **Input**

   ​     An algorithm requires a specific type of input to work upon.

5. **Output**

   ​     An algorithm produces as per the stated objectives and the input it has received.



##### Components of an Algorithm:

1. **Input**

   ​      The inputs and the type of inputs required by the algorithm. It can be provided by a user or can be self-obtained.

2. **Processing**

   ​      What and how the processing would use inputs to produce the desired output.

3. **Output**

   ​      The output expected from the algorithm; the objective of the algorithm.
   
   

------

A program is the expression of an algorithm. The success of a program depends upon the algorithm. Therefore the logic of the problem must be clearly expressed in algorithm. 

The most preferred method is **graphical method of representing the problem's solution** (*Flowchart*).

Another useful method is **pseudo-code**.



### FLOWCHARTS

A flowchart is pictorial representation of step by step solution of a problem. It is also used as an aid in developing algorithm.



##### FLOW CHART SYMBOLS       

<img src="https://www.codesansar.com/storage/app/media/computer-basics/flowchart-symbol.png" alt="f" style="zoom: 80%;" />

### WRITING ALGORITHM

1. **Identifiers:** 

   Identifiers are names used to identify a variable, function, or other entities in a program.

   

2. **Assignment**:

   An assignment statement evaluates the expression list and assigns the single resulting object to each of the target lists, from left to right.

   ​          Format:                       

   ```python
   variable ← <expression>
   ```

   ​           Example:

   ```python
   A ← 10
   ```

   

3. **Sequence**:

   Sequence is the generic term for an ordered set. The steps must be listed in the correct order.

   

4. **Selection/Conditional Statements**:

   There may be one or more if-then else statements embedded in another if-then-else statement.

   ```python
   if condition:                                    if condition:
    statement #block 1                 OR              statement         #block 1
                                                       else
                                                         S2               #block 2                                             
   ```

   

   

5. **Repetition - Lopping statement:**

   A looping statement lets you repeat a set of statements depending upon a condition. For this, the ***for loop*** and ***while loop*** are used.

   

   - FOR LOOPING STATEMENT        

     ```python
     for item in sequence:
          : St             #block of statements
     :
     ```

     St - Set of statements to be repeated.

     For loop stops when statement block gets executed.

     

     

   - WHILE LOOPING STATEMENT
   
     ```python
     while condition :
         :   St       #block of statements
     :
     ```

     St - Set of statements to be repeated.

     The *while* statement tests the condition before entering into loop.

     Thus, if condition is false, the loop will never get executed.

   

   

   

   ## PSEUDOCODE

   Pseudocode is an informal way of describing the steps of program's solution.

   → it doesn't use any strict programming language syntax.

   → it is a "text-based" detail design tool.

   → instructions are written in uppercase.

   → variables are written in lowercase.

   → messages are written in sentence case.
   
   
   
   ##### ADVANTAGES OF PSEUDOCODE
   
   - It's similar to everyday English, thus easy to understand.
   - It highlights the sequence of instructions
   - The structure of an algorithm is clearly visible, e.g., selection and repetition blocks.
   - It can be easily modified.
   
   
   
   ##### DISADVANTAGES OF PSUEDOCODE
   
   - It isn't a visual look like flowcharts
   - Since there is no accepted standard, it varies from programmer to programmer.
   - It can only be tested on paper, there's no program to test it.
   - It is an informal representation.

   

   ### VERIFYING ON ALGORITHM
   
   Verification of an algorithm is to ensure that the algorithm is working as intended.

   To verify algorithms:

   - Test it with a sample input for which we know the output.
   - If the expected output matched with the output received.
   - Then the algorithm is verified.

   But for larger algorithms, we may want to verify the intermediate results too.

   For this, a useful mechanism of verifying algorithm called Dry-Run is used.

   

   #### DRY RUN
   
   It is the process of a programmer manually working through their code to trace the value of variables. There's no software involved in this process.

   ##### Characteristics of Dry Run:

   - It's carried out during design, implementation, testing or maintenance.
   - It's used to identify the logic errors
   - It can't find the execution errors in a code.

   

   #### TRACE TABLES

   Dry running an algorithm is carried out using trace tables where the impact of each line is seen on the values of variables. As per the line of code, the processing that takes place is applied on the variable' values.

   

   ### COMPARING ALGORITHM

    In order to decide which algorithm to choose over another, their efficiency will be the deciding factor.

   

   #### **Two deciding factors for an algorithm are:**

   - **Space-wise efficiency**

     The amount of memory the algorithm uses before terminating.

   - **Time-wise efficiency**

     Time taken to complete. It's dependent on RAM available, programming language chosen, hardware platforms etc.

     When the hardware platform is fixed with a specific RAM size, then space efficiency becomes the deciding factor.

   

   

   ------

   

   

   
   
   
   
   
   
   
