<span style="color:#8C8CF7">

# <span style="color:#C9A176">DESKTOP APPLICATIONS IN C# 01
## <span style="color:#C9A176">CONSOLE APPS

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
### <a id="baseConcepts"><span style="color:#C9A176">01.00 BASE CONCEPTS</a>
________________


When you compile and run the code, a new window will open either in the IDE's built-in terminal, or in your computer's terminal itself
it will contain the output of the code

If the code contains an error, the terminal will also display the error type and where it is, for easier debugging


<br>

```cs
using System;

namespace Playground 
{
    internal class Class
    {
        Console.WriteLine("Hello World !");
    }
}
```

Console :
```
Hello World !

Process finished with exit code 0
```

<br>

<span style="color:C9A176">Exit Codes</span> are codes which to tell how the program finished compiling and running

<span style="color:C9A176">0</span> means the process finished without an error


<br>

#### <a id="consoleErrors"><span style="color:#C9A176">01.01 CONSOLE ERRORS</a>
---------------------
<br>

when the code contains an error, the terminal will output an error message, which contains helpful information for the programmer to fix the problem

<br>

```cs
using System;

namespace Playground 
{
    internal class Class
    {
        Console.WriteLine("Hello World !") //missing the ';' closing the statment
    }
}
```

Console :

```
7:43

';' Expected
```

the console displayed the line:column where the error was detected, then gave back what went wrong, according to the compiler

Sometimes, the error is not a syntax error such as the example, but a logical or runtime errors

logical errors are when you expect and output, and the program gives you back another one but the build didn't fail. For example, you code '2+2', you expect '4', but the program gives you back '22'

runtime errors are errors that are in the logic of the code, for example, trying to access a string index that does not exist. Those usually give back error handling messages such as <span style="color:C9A176">indexOutOfBoundException</span>

<br>

```cs
using System;

class Program
{
    static void Main()
    {
        int a = 5;

        // Division by Zero
        Console.WriteLine(a / 0);
    }
}
```

Console :

```
Ln:8

System.DivideByZeroException: 'Attempted to divide by zero.'
```


<br>
<br>

________
### <a id="inputOutput"><span style="color:#C9A176">02.00 CONSOLE INPUT OUTPUT</a>
________________

printing with the console is the way to <span style="color:C9A176">output</span> in the console. Itcan be useful to display or ask information

printing can also be used to print some steps of the code along the way, to better be able to understand the output

there is different ways to print information on the console such as <span style="color:C9A176">Console.Write</span>



<br>

#### <a id="writeVsWriteLine"><span style="color:#C9A176">02.01 CONSOLE.WRITE</a>
---------------------
<br>

<span style="color:C9A176">Console.Write()</span> and <span style="color:C9A176">Console.WriteLine()</span> are two ways to output information on the console

The difference between the two is that <span style="color:C9A176">Console.WriteLine()</span> will return to the next line after the statement


a few symbols to better display with the WriteLine() :

| CODE | MEANING |
|------|---------|
|  \n  | will return to the next line <br> effective equivalent to Console.WriteLine() |
|  \t  | horizontal tab |
|  \"  | inserting double quotes |
|  \\  | inserting a backslash |


<br>

#### <a id="stringInterpolation"><span style="color:#C9A176">02.02 STRING INTERPOLATION</a>
---------------------
<br>

<span style="color:C9A176">string interpolation</span> is a way to print variables inside the WriteLine without having to break the string to insert the values themselves.

normally, we would print a statement like this : <span style="color:C9A176">("statement" + variable)</span> but at some point, it gets long a tedious. Therefore, we can use string interpolation to help us : <span style="color:C9A176">($"statement {variable}")</span>

<span style="color:C9A176">$</span> declares the string interpolation
<br> <span style="color:C9A176">{ }</span> enclose the variables

<br> 

```cs
using System;

class Program
{
    static void Main()
    {
        int num1 = 5;
        int num2 = 10;
        int sum = num1 + num2;

        //without string interpolation
        Console.WriteLine("The sum of " + num1 + " and " + num2 + " is " + sum);

        //with string interpolation
        Console.WriteLine($"The sum of {num1} and {num2} is {sum}");
    }
}
```

Console :

```
The sum of 5 and 10 is 15
The sum of 5 and 10 is 15
```


<br>

#### <a id="input"><span style="color:#C9A176">02.03 CONSOLE.READ</a>
---------------------
<br>

reading is the way to <span style="color:C9A176">input</span> from the conosle to the program. It is basically what makes a program <span style="color:C9A176">interactive</span>

to read from the console, we use <span style="color:C9A176">Console.Read()</span>

<br>

```cs
using System;

class Program
{
    static void Main()
    {
        string name;

        Console.WriteLine("Enter your name : ");
        name = Console.ReadLine();

        Console.Write($"Your name is {name}");
    }
}
```

Console :

```
Enter your name : 
ash-a9236
Your name is ash-a9236
```

<br>

*CAREFUL! The console will always read a <span style="color:C9A176">string</span>, so you might need to <span style="color:C9A176">cast</span> the variable type*


```cs
using System;

class Program
{
    static void Main()
    {
        int num;

        Console.WriteLine("Enter a number : ");
        num = int.Parse(Console.ReadLine()); //casts the integer type to the input
    }
}
```



<br><br><br><br><br><br><br>


Text colour : #8C8CF7 <br>
Highlight : <span style="color:#C9A176"> #C9A176</span> <br>
Notes : <span style="color:#2C6485">#2C6485</span>

<span style="color:#C9A176">made by ash-a9236 <br> Created February 2025<span>
