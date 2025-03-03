<span style="color:#8C8CF7">

# <span style="color:#C9A176">DESKTOP APPLICATIONS IN C# 01
## <span style="color:#C9A176">OPERATIONS

<br>

<!--TABLE OF CONTENTS <br>
<br> 01 . . [<span style="color:#B9C3D6">Base Concepts](#baseConcepts)
<br> &emsp; 01.01 . . [<span style="color:#B9C3D6">Instance Variables](#instanceVariables)
<br> &emsp; 01.02 . . [<span style="color:#B9C3D6">Getters & Setters](#gettersAndSetters)
<br> &emsp; 01.03 . . [<span style="color:#B9C3D6">Properties](#properties)
<br> &emsp; 01.04 . . [<span style="color:#B9C3D6"> Methods](#methods)-->



<br>
<br>

________
### <a id="arithmetics"><span style="color:#C9A176">01.00 ARITHMETICS OPERATORS</a>
________________

| OPERATION | OPERATOR | EXAMPLE |
|-----------|----------|---------|
| Addition  |       +  | a + b   |
| Substraction |    -  | a - b   |
| Multiplication |  *  | a * b   |
| Division  |       /  | a / b   | 
| Remainder (mod) | %  | a % b   |
| | | |
|  x = x + a |      += | x += a  |
|  x = x - a |      -= | x -= a  |
|  x = x * a |      *= | x *= a  |
|  x = x / a |      /= | x /= a  | 
|  x = x % a |      %= | x %= a  |
| | | |
|  x = x + 1 |      ++ | x++     |
|  x = x - 1 |      -- | x--     |




<br>
<br>

________
### <a id="relational"><span style="color:#C9A176">02.00 RELATIONAL OPERATORS</a>
________________

| OPERATION    | OPERATOR | EXAMPLE |
|--------------|----------|---------|
| Greater than |     >    |  a > b  |
| Lesser than  |     <    |  a < b  |
| Greater or Equal | >=   |  a >= b |
| Lesser or Equal |  <=   |  a <= b |
||||
| Equal to     |      ==  |  a == b |
| Not Equal to |      !=  |  a != b |





<br>
<br>

________
### <a id="logicGates"><span style="color:#C9A176">03.00 LOGIC GATES</a>
________________

<br>

| GATE  | OPERATOR | EXAMPLE |
|-------|----------|---------|
| AND   |    &&    |  a && b |
| OR    |    || fcyc yv g vg     |  a || b |
| NOT   |     !    |  a ! b  |   

<br>

> <span style="color:#2C6485"> For more information on the logic gates see  <a href="https://www.codeproject.com/articles/237465/understanding-logic-gates"><span style="color:#2C6485">**LOGIC GATES**</a>


<br>

AND GATE

| OP 01 | OP 02 | RESULT |
|-------|-------|--------|
|   0   |   0   |  false |
|   0   |   1   |  false |
|   1   |   0   |  false |
|   1   |   1   |  true  |

<br>

OR GATE

| OP 01 | OP 02 | RESULT |
|-------|-------|--------|
|   0   |   0   |  true  |
|   0   |   1   |  true  |
|   1   |   0   |  true  |
|   1   |   1   |  true  |

<br>

NOR GATE

| OP 01 | OP 02 | RESULT |
|-------|-------|--------|
|   0   |   0   |  true  |
|   0   |   1   |  false |
|   1   |   0   |  false |
|   1   |   1   |  false |





<br>
<br>

________
### <a id="descisionMaking"><span style="color:#C9A176">04.00 DESCISION MAKING</a>
________________


when the compiler does operations, it will make descisions on what to evaluate first. It is the computer equivalent of the <span style="color:C9A176">PEDMAS</span> we learnt in school, and works the same way

To prioritize or clarify an equation (for you and the computer), you can add parenthesis

Computers usually evaluate : 

1. Parenthesis
2. Multiplication / Division / Remainder (Mod)
3. Addition / Substraction

<br>

The compiler will also, in control flow statments, ignore certain parts of a condition to accelerate the execution

for example :

<br> 

```cs
using System;

class Program
{
    static void Main()
    {
        int num1 = 5;
        int num2 = 10;
        int num3 = 3;

        if (num1 > num2 || num1 > num3) { //since num1 is smaller than num2, the compiler will skip the second condition (num1 > num3) because already the condition is false
            Console.WriteLine(num1);
        } else {
            Console.WriteLine(num2);
        }
    }
}
```























<br><br><br><br><br><br><br>


Text colour : #8C8CF7 <br>
Highlight : <span style="color:#C9A176"> #C9A176</span> <br>
Notes : <span style="color:#2C6485">#2C6485</span>

<span style="color:#C9A176">made by ash-a9236 <br> Created February 2025<span>
