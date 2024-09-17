# Arithmetic Expression Evaluation

Expressions are usually represented in what is known as Infix notation, in which each operator is written between two operands (i.e., A + B). With this notation, we must distinguish between ( A + B )*C and A + ( B * C ) by using either parentheses or some operator-precedence convention. Thus, the order of operators and operands in an arithmetic expression does not uniquely determine the order in which the operations are to be performed. 

```
1.Polish notation (prefix notation) – 
It refers to the notation in which the operator is placed before its two operands.
Here no parentheses are required, i.e., 
+AB
```

```
2. Reverse Polish notation(postfix notation) – 
It refers to the analogous notation in which the operator is placed after its two operands.
 Again, no parentheses is required in Reverse Polish notation, i.e., 
AB+
```

Stack organised computers are better suitable for postfix notation.
Hence the traditional infix notation must be converted into postfix notation.

There are 3 levels of precedence for 5 binary operators as given below: 
```
Highest: Exponentiation (^)
Next highest: Multiplication (*) and division (/)
Lowest: Addition (+) and Subtraction (-)
```

For example – 

```
Infix notation: (A-B)*[C/(D+E)+F]
Post-fix notation: AB- CDE +/F +*
```

For example – 
```
Infix notation: (2+4) * (4+6)
Post-fix notation: 2 4 + 4 6 + *
Result: 60
```
The Stack evaluation for the above expression is as follows:

![image](https://github.com/user-attachments/assets/87b99868-9ca4-4d64-85e4-317b2cff6a34)
