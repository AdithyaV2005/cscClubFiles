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

![A.png](data:image/png;base64,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)

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
> ![Not 2.png](data:image/png;base64,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)
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
> ![or.png](data:image/png;base64,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)
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
> ![AND 2.png](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAbYAAAC5CAYAAABEKBoRAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAEnQAABJ0Ad5mH3gAAATcSURBVHhe7d3hbqJgEIbRuvd/z11JNMsSQGpBmHfOSTbb/+D3OCO1t++7LwAI8efxPwBEEDYAoggbAFGEDYAowgZAFGEDIIqwARBF2ACIImwARBE2AKIIGwBRhA2AKMIGQBRhAyCKsAEQRdgAiCJsAEQRNgCiCBsAUYQNgCi377vHzwS43W6Pn+AYjgyuTtjCCBtncZRwFcIWRti4CkcLZxG2MOOwubQc4d03T+5HPkXYwggbZ/lJ8NybHEnYwggbV7EldO5RjuBxf+AQQ7Se/5YM8fvJpAdbCBtwuFeREzj2JGzAR61FTuDYg7ABpxE4jiBswOkEjj0JG3AZa4GDrYQNuBzTG78hbMAlmd54l7ABlzYXONMba4QNKMH0xlbCBpQhbmwhbEApS6tJeBI2oCRxY4mwAWWJG3OEDShN3JgSNqC86eduQ9wEri9hA2KY3hgIGxBF3BA2II649SZsQCRx6+t2v/j/X/0RN0J9K5cXWpieY14T+UxsQDQh60fYgFZsovKtriKpZ/yidWnhHyvJPkxsQAtC1oewAW2M42YlmUvYgLbELZOwAa1YSeYTNqA1U1seYQPaMbVlEzagJQ+S5BI2AKIIG9CWqS2TsAEQRdiA1kxteYQNgCjCBrRnassibABEETaACVNbbcIGcOfbSHIIGwBRhA1ghnVkXcIG8GAdmUHYAIgibABEETaAEb+sXZ+wARBF2ACIImwAK6wj6xE2gAmP/dcmbABEETYAoggbAFGEDYAowgZAFGEDmOEbSOoSNgCiCBsAUYQNgCjCBkAUYQMgyu3bl6JFGT+95dLC73ga8rrWzjcTGwBRhA2AKFaRYawiYT9eTzWZ2ACIImwARBE2AKIIGwBRhA2AKMIGMMMTkXUJGwBRhA2AKMIGQBRhAyCKsAEQRdgAJvy5mtqEDWCFR/3rETYAoggbAFGEDWDE52v1CRvAAp+v1SRsAEQRNoAHa8gMwgYwwxqyLmEDIIqwAdxZQ+YQNoAJa8jahA2AKMIGtDdeQ5rW6hM2AKIIG9CaaS2PsAEQRdiAtjzin0nYAO6sIXMIG9CSaS2XsAHtTKNmWssibEBropZH2IBWrCDzCRvQlmktk7ABbZjWehA2oAUPjPQhbEA8UetF2IBWRC2fsAHRfK7Wz+3+7mXx7YsbojbvTOnOCrInExsQSdT6EjYgjqj1trqKpJ7xC9qlpSNRw8QGxBA1BsIGRBA1noQNKG8aNXoTNqC0uUnNtNabsAElDUEbR03QeBI2oJRp0AaCxpiwAWVMgzYQNaaEDShB1NhK2IBLW1o9ihpLhA24pLmgDQSNV4QNuJy5oA1EjS2EDbiMtSlN1NhK2IDTCRp7EjbgNEtBGwga7xI24KOeMVsLmqjxG/4eW5jxYeHSchVLEXtyr7InExtwiFeT2WAImqixNxNbGBMbZ3k1lY25NzmSsIURNo72k4CNuR/5FGELI2zs4d14TbkHOYOwhdnrQIJ3OE64AmELI2wczZHB1QlbGGFjD44FKhM2AKL4PTYAoggbAFGEDYAowgZAFGEDIIqwARBF2ACIImwARBE2AKIIGwBRhA2AKMIGQBRhAyCKsAEQRdgAiCJsAEQRNgCiCBsAUYQNgCjCBkAUYQMgirABEEXYAIgibABEETYAgnx9/QWM9LQZK4qAkQAAAABJRU5ErkJggg==)
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
> ![NOR gate.png](data:image/png;base64,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)
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
> ![NAND @.png](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAb0AAAC3CAYAAACGwoCWAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAEnQAABJ0Ad5mH3gAAAVOSURBVHhe7d3tbqJQFIbROvd/zx1JNHOGAAKKHPa7VmLatD/5eNxbbW+/dz8AEODP4ysAlCd6AMQQPQBiiB4AMUQPgBiiB0AM0QMghugBEEP0AIghegDEED0AYogeADFED4AYogdADNEDIIboARBD9ACIIXoAxBA9AGKIHgAxRA+AGKIHQIzb793jewq53W6P7+AYbh1ckegVJXqcxS2FnoleUaJHL9xi6InoFdVGzyHmCHufWDkfOZPoFSV6nGVLDJ2bfJvoFSV69GJNBJ2jfIuPLACHGoL2fMwZwrhlQoS9RA/4mlcBFD+OJnrAKZYCKH4cRfSA04kf3yJ6QDfEj6OJHtCdpfjBO0QP6Japj08TPaBrpj4+SfSAS5iKn6mPrUQPuBRTH+8QPeByhI+9RA+4pLl1JywRPeDShI8tRA+4POFjLdEDShA+1hA9oIzx63xD+MSPlugB5Zj6mCN6QEnCxxTRA8oSPsZEDyhN+Gjd7ifE/2fEBCfJ9a04zFDa+D7mmshk0gMiiBwD0QMi2WBlWrXe5HraC9ohhn+sObOZ9IAoIpdN9IA4bfisObOIHhBP+HKIHhDJmjOT6AHcmfYyiB4Qy7SXR/SAaN7UkkX0AIghekA8014O0QMghugB3Jn2MogeADFED+DBtFef6AEQQ/QAZpj26hE9gIa/0lKb6AEQQ/QAFlhx1iJ6ACNWnHWJHgAxRA+AGKIHMMEH1WsSPQBiiB4AMUQPYAUrzhpED2CGjy7UI3oAxBA9AGKIHgAxRA/gTcObXMYP+iR6ADstBU78+iR6AAum/jLLlqCJX19ED2CDqYANYRw/xoSvD6IH8IapwA3mfs65RA9gp1dhG099pr3ziR7ADia5axI9gI22Bs+014/b/WB4ulJQe2E5xPCecaj2XFNid7w1x8WkB0AM0QMghvVmUdab8DmfXm+6Js9j0gPYaOvrc4LXD9ED2GFr+OiD6AEcSBz7InoAOw1Bm4va1O+sNs8negAbTIXrGbj2MSZ4fRA9gAVtwJ7hGr5uiZjg9UP0AHZait/zd4LXF9EDeFMbOKHrm+gBEEP0AIghegDEED2AGVMfPeDaRA9gBW9OqUH0AIghegDEED2ACV7Pq0n0AF7wel4dogdADNEDGLHarEv0ABZYbdYiegDEED2AhtVmbaIHMMNqsx7RAyCG6AE8tKtNU15NogdADNEDuDPlZRA9AGKIHhDPxxRyiB5Aw2qzNtEDopnysogeEGscPFNefaIHcCd4GUQPiGStmUn0gHimvByiB8Qx5eUSPSCKN69kEz0ghuAhekAkwcskekAEr+MxuN2f7bx8uuNkuTbPaElnrcmTSQ8oTfBoiR5QluAxtmq9yfW0F7tDTCLBY4pJDyhH8JgjekApgscS0QPKGAcPxkQPKGFqwjPlMSZ6wKUNsWuDJ3YsET3gksaxG4gdr4gecDnj2A0EjzVED7gUweMdogdcwtw6U/DYQvSArk3FbiB27CF6QLemYjcQPPYSPaA7S9Od4PEO0QO6IXYcTfSA083FbiB2fJLoAad4hm4pdoLHp/l/ekW1NxKHmF7MBe7JucrRTHrAoV5NdIMhdoLHN5j0ijLpcZZX01zLucm3iV5RosfRtsSt5XzkTKJXlOjxCXvDNuYcpBeiV9Snblawh9sKvRK9okSPo7l1cEWiV5To8QluD1QjegDE8Dk9AGKIHgAxRA+AGKIHQAzRAyCG6AEQQ/QAiCF6AMQQPQBiiB4AMUQPgBiiB0AM0QMghugBEEP0AIghegDEED0AYogeADFED4AYogdADNEDIMTPz1+nTxQkbEr8PgAAAABJRU5ErkJggg==)
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
> ![XOR 2.png](data:image/png;base64,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)
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
> ![XNOR gate.png](data:image/png;base64,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)
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