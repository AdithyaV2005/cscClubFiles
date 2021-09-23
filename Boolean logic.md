# **BOOLEAN LOGIC**

## **Chapter Contents :**

- Development of Boolean Logic and Its Integration with Computers
- Logical or Binary valued Variables
- Logical Operations And Operators
- Logic Gates
- Basic Postulates
- Principle Of Duality
- Theorems Of Boolean Logic
- DeMorgan's Theorem
- Logic Circuits

## **Development of Boolean Logic and Its Integration with Computers :**

- Firstly developed by Aristotle, who created a complete system of formal logic and wrote 6 famous books on logic
- Many mathematicians tried to solve logic problems through conventional methods of algebra, but George Boole could manipulate the symbols to arrive at a successful solution through his own system of logic
- His revolutionary paper, "An Investigation of the Laws of Thought", published in 1854, led to development of new system, the "Algebra of Logic","Boolean Algebra" or "Boolean Logic"
- Claude. E. Shannon, in his paper "Symbol Analysis of Relay Switching Circuits" published 1938, applied Boolean Logic to solve relay logic problems, as Boolean logic effectively deals with binary-based logic problems

## **Binary Valued Quantities :**

- The decision which results into either TRUE or FALSE is called a Binary Decision
- The values TRUE or FALSE are called Truth values
- The Truth Values are depicted by binary digits 0 and 1, where 0 is for False and 1 is for True
- The variables which can store these Truth Values are called Logical Variables or Binary Valued Variables

=> **TRUTH TABLES**:

- A truth table is a table which represents all the possible values of logical variables/statements along with all the possible results of the given combination of values.

Example of a truth table:

A two variable truth table:

|  X   |  Y   |
| :--: | :--: |
|  0   |  0   |
|  1   |  1   |

<br>A three variable truth table:

|  X   |  Y   |  Z   |
| :--: | :--: | :--: |
|  0   |  1   |  1   |
|  1   |  0   |  0   |

<br>=> **TAUTOLOGY AND FALLACY**:

- **TAUTOLOGY**: If the result of any logical statement or expression is **ALWAYS TRUE** or **1** for all input combinations, it is called tautology
- **FALLACY**: If the result of any logical statement or expression is **ALWAYS FALSE** or **0** for all input combinations, it is called fallacy

## **Logical Operations And Operators :**

### **Logical Operators:**

**NOT** :

- It operates on single variable
- Operation performed is called as **COMPLEMENTATION**
- Symbol Used: - on top of the variable, like:

![image](https://user-images.githubusercontent.com/86146695/134514876-57d45605-8a42-41d9-b216-364d62760b1a.png)

- Other symbols used are ~ and '

TRUTH TABLE FOR NOT OPERATOR:

|  X   | NOT X |
| :--: | :---: |
|  0   |   1   |
|  1   |   0   |

<br>**OR**:

- It denotes logical addition
- Symbol used: +
- X + Y is read as **X OR Y**
- Rules for OR operator:

TRUTH TABLE FOR OR OPERATOR:

|  X   |  Y   | X+Y  |
| :--: | :--: | :--: |
|  0   |  0   |  0   |
|  0   |  1   |  1   |
|  1   |  0   |  1   |
|  1   |  1   |  1   |

<br>**AND**:

- It performs logical addition
- Symbol used: .
- X . Y is read as **X AND Y**

TRUTH TABLE FOR AND OPERATOR:

|  X   |  Y   | X.Y  |
| :--: | :--: | :--: |
|  0   |  0   |  0   |
|  0   |  1   |  0   |
|  1   |  0   |  0   |
|  1   |  1   |  1   |

### <br>Logical Operations:

Logical variables are combined by the logical operators to form a Boolean expression

Example: X + [~(YZ)] + (~Z)

To study a Boolean expression, it is useful to construct a table of values for the variables and then evaluate the expression for each possible combination in turn

Ex: X + [~(YZ)]

Step 1: Write all the possible values:

| X    | Y    | Z    |
| :--- | :--- | :--- |
| 0    | 0    | 0    |
| 0    | 0    | 1    |
| 0    | 1    | 0    |
| 0    | 1    | 1    |
| 1    | 0    | 0    |
| 1    | 0    | 1    |
| 1    | 1    | 0    |
| 1    | 1    | 1    |

<br>Step 2: Evaluate the expressions: (The Order Of Evaluation: NOT>AND>OR)

|  X   |  Y   |  Z   | Y.Z  |
| :--: | :--: | :--: | :--: |
|  0   |  0   |  0   |  0   |
|  0   |  0   |  1   |  0   |
|  0   |  1   |  0   |  0   |
|  0   |  1   |  1   |  1   |
|  1   |  0   |  0   |  0   |
|  1   |  0   |  1   |  0   |
|  1   |  1   |  0   |  0   |
|  1   |  1   |  1   |  1   |

<br>Y.Z is evaluated first

|  X   |  Y   |  Z   | Y.Z  | ~(Y>Z) |
| :--: | :--: | :--: | :--: | :----: |
|  0   |  0   |  0   |  0   |   1    |
|  0   |  0   |  1   |  0   |   1    |
|  0   |  1   |  0   |  0   |   1    |
|  0   |  1   |  1   |  1   |   0    |
|  1   |  0   |  0   |  0   |   1    |
|  1   |  0   |  1   |  0   |   1    |
|  1   |  1   |  0   |  0   |   1    |
|  1   |  1   |  1   |  1   |   0    |

<br>NOT(Y.Z) is evaluated

|  X   |  Y   |  Z   | Y.Z  | ~(Y.Z) | X+[~(Y.Z)] |
| :--: | :--: | :--: | :--: | :----: | :--------: |
|  0   |  0   |  0   |  0   |   1    |     1      |
|  0   |  0   |  1   |  0   |   1    |     1      |
|  0   |  1   |  0   |  0   |   1    |     1      |
|  0   |  1   |  1   |  1   |   0    |     0      |
|  1   |  0   |  0   |  0   |   1    |     1      |
|  1   |  0   |  1   |  0   |   1    |     1      |
|  1   |  1   |  0   |  0   |   1    |     1      |
|  1   |  1   |  1   |  1   |   0    |     1      |

<br>X+[~(Y.Z)] is evaluated

## **Logic Gates**:

### What is a Logic Gate ?

A Gate is a basic electronic circuits which operates on one or more signals to produce an output signal. They are digital(2-state) circuits because the input and output signals are either **Low Voltage(0)** and **High Voltage(1)**. They are often called *logic circuits* as they can be analyzed with Boolean logic. The different types of gates are:

> Inverter (NOT) Gate: It is a gate with only one input signal and only one output signal. The Output state is always opposite to that of the input state.
>
> ![image](https://user-images.githubusercontent.com/86146695/134515029-90108b1b-b0c4-41ba-89eb-9e417418162a.png)
>
> Truth Table for NOT gate:
>
> | X    | NOT X |
> | :--- | :---- |
> | 0    | 1     |
> | 1    | 0     |
>
> <br>OR Gate: It has two or more input signals but only one output signal. If any input signal is 1, the output is 1. If all the inputs are 0, then output is also zero. It can have as many inputs as desired. No matter how many inputs are given, action of OR gate is same: one or more 1 inputs produce 1 as a result
>
> ![image](https://user-images.githubusercontent.com/86146695/134515211-700a2827-1d26-4aab-b594-4710a902a8e8.png)
>
> Truth Table for OR gate: 2 inputs:
>
> |  X   |  Y   |  F   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  0   |  1   |  1   |
> |  1   |  0   |  1   |
> |  1   |  1   |  1   |
>
> <br>3 inputs:
>
> |  X   |  Y   |  Z   |  F   |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  0   |
> |  0   |  0   |  1   |  1   |
> |  0   |  1   |  0   |  1   |
> |  0   |  1   |  1   |  1   |
> |  1   |  0   |  0   |  1   |
> |  1   |  0   |  1   |  1   |
> |  1   |  1   |  0   |  1   |
> |  1   |  1   |  1   |  1   |
>
> <br>AND Gate: It can have 2 or more inputs and produce an output. It produces 1 as an output only if all the input values are 1. Else it produces 0. If any of the input is 0, then the input is 0. It can have as many inputs as desired.
>
> ![image](https://user-images.githubusercontent.com/86146695/134515327-341fb11a-1842-41cc-88ec-de8be6861a6c.png)
>
> Truth Table for AND gate: 2 inputs:
>
> |  X   |  Y   |  F   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  0   |  1   |  0   |
> |  1   |  0   |  0   |
> |  1   |  1   |  1   |
>
> <br>3 inputs:
>
> |  X   |  Y   |  Z   |  F   |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  0   |
> |  0   |  0   |  1   |  0   |
> |  0   |  1   |  0   |  0   |
> |  0   |  1   |  1   |  0   |
> |  1   |  0   |  0   |  0   |
> |  1   |  0   |  1   |  0   |
> |  1   |  1   |  0   |  0   |
> |  1   |  1   |  1   |  1   |
>
> <br>NOR Gate: It is nothing but an inverted OR gate. It can have 2 or more inputs but only 1 output. If all the inputs are 0, then output is 1. If either of the 2 inputs is 1, then output will be zero. No matter how many inputs are given, action of NOR gate is same: one or more 0 inputs produce 1 as a result
>
> ![image](https://user-images.githubusercontent.com/86146695/134515456-c860b78b-e5a7-4319-8e20-0b01b3f1cbfd.png)
>
> Truth Table for OR gate: 2 inputs:
>
> |  X   |  Y   |  F   |
> | :--: | :--: | :--: |
> |  0   |  0   |  1   |
> |  0   |  1   |  0   |
> |  1   |  0   |  0   |
> |  1   |  1   |  0   |
>
> <br>3 inputs:
>
> |  X   |  Y   |  Z   |  F   |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  1   |
> |  0   |  0   |  1   |  0   |
> |  0   |  1   |  0   |  0   |
> |  0   |  1   |  1   |  0   |
> |  1   |  0   |  0   |  0   |
> |  1   |  0   |  1   |  0   |
> |  1   |  1   |  0   |  0   |
> |  1   |  1   |  1   |  0   |
>
> <br>NAND Gate: It is nothing but an inverted AND gate. It can have 2 or more inputs but only 1 output. If all the inputs are 1, then output is 0. For any other input combination, output is 1.
>
> ![image](https://user-images.githubusercontent.com/86146695/134515514-b8a4f8b5-2923-4006-ac9a-103fc0e2ef52.png)
>
> Truth Table for NAND gate: 2 inputs:
>
> |  X   |  Y   |  F   |
> | :--: | :--: | :--: |
> |  0   |  0   |  1   |
> |  0   |  1   |  1   |
> |  1   |  0   |  1   |
> |  1   |  1   |  0   |
>
> <br>3 inputs:
>
> |  X   |  Y   |  Z   |  F   |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  1   |
> |  0   |  0   |  1   |  1   |
> |  0   |  1   |  0   |  1   |
> |  0   |  1   |  1   |  1   |
> |  1   |  0   |  0   |  1   |
> |  1   |  0   |  1   |  1   |
> |  1   |  1   |  0   |  1   |
> |  1   |  1   |  1   |  0   |
>
> <br>XOR (Exclusive OR) Gate: The XOR gate can also have 2 or more inputs but produces only 1 output. The XOR gate is different from OR gate. While the OR gate produces output as 1 if any input is 1, the XOR gate produces output as 1 only if there are an odd number of 1's as an input. In Boolean algebra, ⊕ stands for the XOR operations.
>
> ![image](https://user-images.githubusercontent.com/86146695/134515590-47fd23c7-cbee-4d44-b4b0-aec944df1e78.png)
>
> Truth Table for XOR gate: 2 inputs:
>
> |  X   |  Y   |  F   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  0   |  1   |  1   |
> |  1   |  0   |  1   |
> |  1   |  1   |  0   |
>
> <br>3 inputs:
>
> |  X   |  Y   |  Z   |  F   |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  0   |
> |  0   |  0   |  1   |  1   |
> |  0   |  1   |  0   |  1   |
> |  0   |  1   |  1   |  0   |
> |  1   |  0   |  0   |  1   |
> |  1   |  0   |  1   |  0   |
> |  1   |  1   |  0   |  0   |
> |  1   |  1   |  1   |  1   |
>
> <br>To summarize, **0⊕0=0 0⊕1=1 1⊕0=1 1⊕1=0**
>
> XNOR (Exclusive NOR) Gate: It is logically equal to an inverted XOR gate. This, it produces 1 when input has an even number of 1's
>
> ![image](https://user-images.githubusercontent.com/86146695/134515672-0518adfe-c4fb-4678-b3af-8161a01d600c.png)
>
> Truth Table for XNOR gate: 2 inputs:
>
> |  X   |  Y   |  F   |
> | :--: | :--: | :--: |
> |  0   |  0   |  1   |
> |  0   |  1   |  0   |
> |  1   |  0   |  0   |
> |  1   |  1   |  1   |
>
> <br>3 inputs:
>
> |  X   |  Y   |  Z   |  F   |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  1   |
> |  0   |  0   |  1   |  0   |
> |  0   |  1   |  0   |  0   |
> |  0   |  1   |  1   |  1   |
> |  1   |  0   |  0   |  0   |
> |  1   |  0   |  1   |  1   |
> |  1   |  1   |  0   |  1   |
> |  1   |  1   |  1   |  0   |

## <br>**Basic Postulates :**

Boolean logic algebra, being a system of mathematics, consists of fundamental laws that are used to build a workable, cohesive framework upon which are based the theorems of boolean algebra. These postulates state basic relations in boolean algebra, that follow

- If X ≠ 0 then X=1, and if X ≠ 1 then X=0
- 0+0=0; 0+1=1; 1+0=1; 1+1=1
- 0.0=0; 0.1=0; 1.0=0; 1.1=1
- Complement of 0 = 1; Complement of 1 = 0

## **Principle Of Duality** :

This states that with a boolean relation, another boolean relation can be obtained by:

1. Changing OR sign to AND sign
2. Changing AND sign to OR sign
3. Replacing 0 by 1 and 1 by 0

The relation obtained is called the **DUAL** of the original expression.

In Boolean Algebra, if an **expression is true then its dual is also true** and vice versa.

## **Basic Theorems of Boolean Algebra** :

> #### **Properties of 0 and 1** :
>
> a) **0 + X = X**
>
> |  0   |  X   |  R   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  0   |  1   |  1   |
>
> <br>b) **0 . X = 0**
>
> |  0   |  X   |  R   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  0   |  1   |  0   |
>
> It is a **FALLACY**
>
> <br>c) **1 + X = 1**
>
> |  1   |  X   |  R   |
> | :--: | :--: | :--: |
> |  1   |  0   |  1   |
> |  1   |  1   |  1   |
>
> It is a **TAUTOLOGY**
>
> <br>d) **1 . X = X**
>
> |  1   |  X   |  R   |
> | :--: | :--: | :--: |
> |  1   |  0   |  0   |
> |  1   |  1   |  1   |
>
> #### **Idempotence Law** :
>
> <br>a) **X + X = X**
>
> |  X   |  X   |  R   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  1   |  1   |  1   |
>
> <br>b) **X . X = X**
>
> |  X   |  X   |  X   |
> | :--: | :--: | :--: |
> |  0   |  0   |  0   |
> |  1   |  1   |  1   |
>
> <br>**(a) and (b) are duals of each other**
>
> #### **Involution** :
>
> **!(!(X)) = X**
>
> |  X   |  !X  | !(!(X)) |
> | :--: | :--: | :-----: |
> |  0   |  1   |    0    |
> |  1   |  0   |    1    |
>
> <br>This law is also called *DOUBLE-INVERSION RULE*
>
> #### **Complementarity Law** :
>
> a) **X + !X = 1**
>
> |  X   |  !X  | X + !X |
> | :--: | :--: | :----: |
> |  0   |  1   |   1    |
> |  1   |  0   |   1    |
>
> <br>It is a **TAUTOLOGY**
>
> b) **X . !X = 0**
>
> |  X   |  !X  | X . !X |
> | :--: | :--: | :----: |
> |  1   |  0   |   0    |
> |  0   |  1   |   0    |
>
> <br>It is a **FALLACY**
>
> (a) and (b) are **DUALS** of each other
>
> #### **Commutative Law** :
>
> a) **X + Y = Y + X**
>
> |  X   |  Y   | X+Y  | Y+X  |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  0   |
> |  0   |  1   |  1   |  1   |
> |  1   |  0   |  1   |  1   |
> |  1   |  1   |  1   |  1   |
>
> <br>b) **X . Y = Y . X**
>
> |  X   |  Y   | X.Y  | Y.X  |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  0   |
> |  0   |  1   |  0   |  0   |
> |  1   |  0   |  0   |  0   |
> |  1   |  1   |  1   |  1   |
>
> #### <br>**Associative Law** :
>
> a) **X + (Y + Z) = (X + Y) + Z**
>
> |  X   |  Y   |  Z   | Y+Z  | X+Y  | X+(Y+Z) | (X+Y)+Z |
> | :--: | :--: | :--: | :--: | :--: | :-----: | :-----: |
> |  0   |  0   |  0   |  0   |  0   |    0    |    0    |
> |  0   |  0   |  1   |  1   |  0   |    1    |    1    |
> |  0   |  1   |  0   |  1   |  1   |    1    |    1    |
> |  0   |  1   |  1   |  1   |  1   |    1    |    1    |
> |  1   |  0   |  0   |  0   |  1   |    1    |    1    |
> |  1   |  0   |  1   |  1   |  1   |    1    |    1    |
> |  1   |  1   |  0   |  1   |  1   |    1    |    1    |
> |  1   |  1   |  1   |  1   |  1   |    1    |    1    |
>
> <br>b) **X(YZ) = (XY)Z**
>
> |  X   |  Y   |  Z   |  YZ  |  XY  | X(YZ) | (XY)Z |
> | :--: | :--: | :--: | :--: | :--: | :---: | :---: |
> |  0   |  0   |  0   |  0   |  0   |   0   |   0   |
> |  0   |  0   |  1   |  0   |  0   |   0   |   0   |
> |  0   |  1   |  0   |  0   |  0   |   0   |   0   |
> |  0   |  1   |  1   |  1   |  0   |   0   |   0   |
> |  1   |  0   |  0   |  0   |  0   |   0   |   0   |
> |  1   |  0   |  1   |  0   |  0   |   0   |   0   |
> |  1   |  1   |  0   |  0   |  1   |   0   |   0   |
> |  1   |  1   |  1   |  1   |  1   |   1   |   1   |
>
> <br>(a) and (b) are the **DUALS** of each other
>
> #### **Distributive Law** :
>
> a) **X(Y+Z) = XY + YZ**
>
> |  X   |  Y   |  Z   | Y+Z  |  XY  |  XZ  | X(Y+Z) | XY+XZ |
> | :--: | :--: | :--: | :--: | :--: | :--: | :----: | :---: |
> |  0   |  0   |  0   |  0   |  0   |  0   |   0    |   0   |
> |  0   |  0   |  1   |  1   |  0   |  0   |   0    |   0   |
> |  0   |  1   |  0   |  1   |  0   |  0   |   0    |   0   |
> |  0   |  1   |  1   |  1   |  0   |  0   |   0    |   0   |
> |  1   |  0   |  0   |  0   |  0   |  0   |   0    |   0   |
> |  1   |  0   |  1   |  1   |  0   |  1   |   1    |   1   |
> |  1   |  1   |  0   |  1   |  1   |  0   |   1    |   1   |
> |  1   |  1   |  1   |  1   |  1   |  1   |   1    |   1   |
>
> <br>b) **X + YZ = (X+Y)(Y+Z)**
>
> It is the dual of (a), hence it is also true. Algebraic Proof of this law is:
>
> RHS = (X+Y)(Y+Z) = XX + XZ + XY + YZ = X + XZ + XY + YZ (XX = X) = X + XY + XZ + YZ = X(1+Y) + XZ + YZ = X.1 + XZ + YZ (1+Y=1) = X + XZ + YZ (X.1=X) = X(1+Z) + YZ (1+Z=1) = X + YZ (X.1=X)
>
> #### **Absorption Law** :
>
> a) **X + XY = X**
>
> |  X   |  Y   |  XY  | X+XY |
> | :--: | :--: | :--: | :--: |
> |  0   |  0   |  0   |  0   |
> |  0   |  1   |  0   |  0   |
> |  1   |  0   |  0   |  1   |
> |  1   |  1   |  1   |  1   |
>
> <br>Also, X + XY = X(1 + Y) = X . 1 = X
>
> b) **X (X + Y) = X**
>
> It is the dual of (a), hence it is also true. Algebraic Proof of this law is:
>
> LHS = X(X+Y) = X.X + XY = X + XY = X (1 + Y) = X . 1 = X
>
> #### **Third Distributive Law** :
>
> **X + (!X)Y = X + Y**
>
> Algebraic Proof of this law is:
>
> LHS = X + (!X)Y = X.1 + (!X)Y = X(1+Y) + (!X)Y = X + XY + (!X)Y = X + Y(X + (!X)) = X + Y.1 = X + Y

## **De Morgan's Theorems** :

Given by Augustus De Morgan, it is one of the most powerful identities used in Boolean logic. He paved the way to Boolean logic by giving these 2 important theorems.

> ### De Morgan's First Theorem:
>
> **!(X+Y) = !X . !Y**
>
> Proof: We need to recall the complementarity laws to prove this theorem, which states that X + !X = 1 and X . !X = 0
>
> If !(X+Y) = !X . !Y, then, **(X+Y) + !(XY) = 1** ① and **(X+Y) . !(XY) = 0** ②
>
> Proving the first part, i.e., (X+Y) + !(XY) = 1
>
> (X+Y) + !(XY) = ((X + Y) + !X).((X + Y) + !Y) = (X + !X + Y ) . (X + Y + !Y) = 1 + Y . X + 1 = 1.1 = 1
>
> Proving the second part, i.e., (X+Y) . !(XY) = 0
>
> (X+Y) . !(XY) = !(XY) . (X+Y) = !X . !Y . X + !X . !Y . Y = 0. !Y + !X . 0 = 0 + 0 = 0
>
> Since both the parts are proved, thus **!(X+Y) = !X . !Y**
>
> ### De Morgan's Second Theorem:
>
> **!(X.Y) = !X + !Y**
>
> Proof: We need to recall the complementarity laws to prove this theorem, which states that X + !X = 1 and X . !X = 0
>
> If !(X.Y) = !X + !Y, then **XY + (!X + !Y) = 1** ① and **XY . (!X + !Y) = 0** ②
>
> Proving the first part, i.e., XY + (!X + !Y) = 1
>
> XY + (!X + !Y) = (!X + !Y) + XY = (!X + !Y + X) . (!X + !Y + Y) = (1 + !Y) . (!X + 1) = 1 . 1 = 1
>
> Proving the second part, i.e., XY . (!X + !Y) = 0
>
> XY . (!X + !Y) = XY(!X) + XY(!Y) = 0 . Y + X . 0 = 0 + 0 = 0
>
> Since both the parts are proved, thus **!(X.Y) = !X + !Y**

Although the above identities represent De Morgan's theorem, the transformation is more easily performed by following steps:

1. Complement entire function
2. Change ORs to ANDs and ANDs to ORs
3. Complement each of the individual variables

This process is called as **DEMORGANIZATION**. To demorganize a Boolean expression, "Break the line, Change the sign"

## **Logic Circuits** :

A logic circuit is a circuit that carries out a set of logic actions based on an expression. To execute a Boolean expression, a logic circuit and the input values for the variables are required. A boolean expression can be represented by using a combination of logic gates so that the output of the expression can be determined by the various combination of input values. Logic circuit diagrams are used to represent Boolean expressions through combination of logic gates.

Rules to create a logic circuit are:

1. Break the Boolean expression into smaller sub-expressions
2. For each sub-expression, determine the logic gates that can implement them.
3. Implement the sub-expressions using the gates determined in the previous steps
4. Determine the logic gate for the symbol joining the sub-expressions
5. Using the logic gate for the joining symbol (from step 4), connect the sub-expressions' gate implementation
