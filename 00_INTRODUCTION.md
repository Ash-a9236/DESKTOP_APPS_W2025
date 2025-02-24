<span style="color:#8C8CF7">

# <span style="color:#C9A176">DESKTOP APPLICATIONS IN C# 00
## <span style="color:#C9A176">INTRODUCTION TO C# PROGRAMMING

<br>

<!--TABLE OF CONTENTS : to finish
<a href="#ArticleSection3"></a>

OBJECTS
* Instance Variables
* Properties-->

________
### <span style="color:#C9A176">01.00 OBJECTS
________________

<br>

> <span style="color:#2C6485"> For more information, see <a href="01_OBJECTS.md"><span style="color:#2C6485">**01_OBJECTS.md**</a>

*A good programming practice is to use objects to **hide** how the program works. This process is called <span style="color:C9A176">encapsulation</span>*

<span style="color:#C9A176">**OBJECTS**</span> are used in <span style="color:#C9A176">**OOP**</span> (Object Oriented Programming), a type of programming

<br>

Objects are instances of a <span style="color:#C9A176">class</span>. The class is the blueprint, the 'plans', and the object is one output of it

<br>

```cs
using System;

namespace Playground //the project (Playground)
{
    internal class Class01 //the object (Class01)
    {

    }
}
```

<br>

#### <span style="color:#C9A176">01.01 INSTANCE VARIABLES
---------------------
<br>

To create the blueprint of the car, we need to define certain <span style="color:#C9A176">attributes</span> the object has. 

Those attributes are called <span style="color:#C9A176">instance variables</span> and are defined at the <span style="color:#C9A176">top</span> of the class.

<br>

```cs
using System;

namespace Playground 
{
    internal class Class01
    {
        private int integer_1;
        private double double_1.1;
        private char character_A;
        private string string_word;
    }
}
```


<br>

#### <span style="color:#C9A176">01.02 PROPERTIES
---------------------
<br>

Since attributes are not accessible directly (to again, hide the inner workings of the code), we need to create <span style="color:C9A176">properties</span> which contains the <span style="color:C9A176">get</span> and <span style="color:C9A176">set</span> accessors of each attributes

Propeties are the method equivalent of the <span style="color:C9A176">this.</span> keyword, which references the instance of the class instead of the class variable

*in short, it references a created object of the class instead of the blueprint of the class*


```cs
using System;

namespace Playground 
{
    internal class Class
    {
        private string name;

        /*the properties need to be capitalized to 
        differenciate them from instance variables*/
        public string Name { 

            get { return name; }
            set { name = value; }
        }
    }
}
```

<br>

#### <span style="color:#C9A176">01.03 METHODS
---------------------
<br>

> <span style="color:#2C6485"> For more information, see <a href="./01_OBJECTS.md"><span style="color:#2C6485">**01_OBJECTS.md**</a>

Methods are basically <span style="color:C9A176">actions</span> an object can perform

They can take in input parameters, and have an output

to use them you need to <span style="color:C9A176">call</span> them either inside the class, or in the <span style="color:C9A176">driver program</span> (also called <span style="color:C9A176">Main</span>)

<br>

```cs
using System;

namespace Playground 
{
    internal class Class
    {
        private string name;

        //method
        public void PrintName (string name) { 
            Console.WriteLine("This is the name : " + name);
        }
    }
}
```

<br>

#### <span style="color:#C9A176">01.04 MAIN
---------------------
<br>

the main method, also called the <span style="color:C9A176">driver method</span> is where the code from one or multiple classes is executed

the Main method in the <span style="color:C9A176">Main class</span> is the primary method to execute the entire code


<br><br>

________
### <span style="color:#C9A176">02.00 COMPUTER MEMORY
________________

<br>


the computer memory is composed entirely of 0s and 1s called <span style="color:C9A176">bits</span>

<br>

#### <span style="color:#C9A176">02.01 BINARY
---------------------
<br>

the <span style="color:C9A176">binary system</span> counts in powers of <span style="color:C9A176">2</span> instead of our regular number system (decimal) which counts in powers of 10

binary numbers can only count in 0s and 1s therefore :

0000 = 0 (all set to 0)
<br>1000 = 1 (first position $2^0$ is set to 1 => $2^0$ * 1 = 1)
<br>0100 = 2 (position 1 ($2^0$) = 0 + position 2 ($2^1$) = 2 => 0 + 2 = 2)
<br>1100 = 3 (position 1 ($2^0$) = 1 + position 2 ($2^1$) = 2 => 1 + 2 = 3)
<br>0010 = 4 (position 1 ($2^0$) = 0 + position 2 ($2^1$) = 0 + position 3 ($2^2$) = 4 => 0 + 0 + 4 = 5)

etc.

<br>

a <span style="color:C9A176">byte</span> is composed of <span style="color:C9A176">8 bits</span>, therefore, <span style="color:C9A176">0000 0000</span>


| NAME | SYMBOL | SIZE (b) | SIZE (B) | SIZE (KB) | SIZE (MB) | SIZE (GB) |
|------|--------|----------|----------|-----------|-----------|-----------|
| BIT  |    b   |     1    |     -    |     -     |     -     |     -     |
| BYTE |    B   |     8    |     1    |     -     |     -     |     -     |
| KILOBYTE | KB |   8192   |    1024  |     1     |     -     |     -     |
| MEGABYTE | MB |  8388608 | 1048576  |  1024     |     1     |     -     |
| GIGABYTE | GB |     -    |1073741824| 1048576   | 1024      |      1    |
| TERABYTE | TB |     -    |     -    |1073741824 | 1048576   |    1024   |



<br>

#### <span style="color:#C9A176">02.02 CHARACTERS & ASCII
---------------------
<br>

> <span style="color:#2C6485"> For the ASCII reference sheet see  <a href="https://www.ascii-code.com/"><span style="color:#2C6485">**ASCII TABLE**</a>


characters such as letters and symbols are also represented in binary for computers.

to reference them, we use a reference sheet called the <span style="color:C9A176">ASCII code</span>, which uses 8 bit for every character

each letter has a reference number which *all programming languages understand* and can lead to programming errors when defining and setting data types and variables

(ex. char letter = 'a'; => char + 1; will return 'b' BUT int number = a; will return 96 since the ASCII for lower case a is 96)


<br>

#### <span style="color:#C9A176">02.03 OTHER SYSTEMS
---------------------
<br>

through programming we use different numbering system to be able to communicate more effectively with a computer (after all, computers think in binary, not in decimals)


| NAME | BASE | REFERENCE | DIGITS | EXAMPLE |
|------|------|-----------|--------|---------|
| DECIMAL | 10 | 0 - 9    | 0 - 9  | 54 |
| BINARY  | 2  | 0, 1     | 0 - 1  | 0010 1101 |
| OCTAL   | 8  | BINARY   | 0 - 7  | 7 (111 in binary) |
| HEXDACIMAL | 16 | BINARY | 1 - 9 + A - F | 01FA29 (is also used as colour code)|








for reference, <span style="color:C9A176">1 byte</span> is <span style="color:C9A176">0000</span> and will range from <span style="color:C9A176">0</span> to <span style="color:C9A176">255</span> (256 total values - the 0 value)


<br>
<br>

________
### <a id="actuallyCoding"><span style="color:#C9A176">03.00 ACTUALLY CODING</a>
________________

to code we need something called a <span style="color:C9A176">coding environment</span>, or <span style="color:C9A176">IDE</span> (Integrated Development Environment)

They are apps which contain everything you need to be able to code and then compile said code

They usually contain :
<br> &emsp; - Editor
<br> &emsp; - Compiler
<br> &emsp; - Debugger
<br> &emsp; - Terminal
<br> &emsp; - Version Control
<br> &emsp; - Code snippets & navigation
<br> &emsp; - Extensions and Plugins

> <span style="color:#2C6485"> For more information see  <a href="https://www.geeksforgeeks.org/what-is-ide/"><span style="color:#2C6485">**WHAT IS AN IDE?**</a>

IDE are usually paying, but they also usually have a <span style="color:C9A176">Communitiy Edition</span> which is free

Some popular IDEs include :
<br> &emsp; - Visual Studio Code
<br> &emsp; - Visual Studio 22
<br> &emsp; - IntelliJ IDEA
<br> &emsp; - Eclipse


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
```

<br>










<br><br><br><br><br><br><br>


Text colour : #8C8CF7 <br>
Highlight : <span style="color:#C9A176"> #C9A176</span> <br>
Notes : <span style="color:#2C6485">#2C6485</span>

<span style="color:#C9A176">made by ash-a9236 <br> Created February 2025<span>
