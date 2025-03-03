<span style="color:#8C8CF7">

# <span style="color:#C9A176">DESKTOP APPLICATIONS IN C# 01
## <span style="color:#C9A176">C# OBJECTS

<br>

TABLE OF CONTENTS <br>
<br> 01 . . [<span style="color:#8C8CF7">Base Concepts](#baseConcepts)
<br> &emsp; 01.01 . . [<span style="color:#B9C3D6">Instance Variables](#instanceVariables)
<br> &emsp; 01.02 . . [<span style="color:#B9C3D6">Getters & Setters](#gettersAndSetters)
<br> &emsp; 01.03 . . [<span style="color:#B9C3D6">Properties](#properties)
<br> &emsp; 01.04 . . [<span style="color:#B9C3D6"> Methods](#methods)



<br>
<br>

________
### <a id="baseConcepts"><span style="color:#C9A176">01.00 BASE CONCEPTS</a>
________________


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

#### <a id="instanceVariables"><span style="color:#C9A176">01.01 INSTANCE VARIABLES</a>
---------------------
<br>

To create the blueprint of the car, we need to define certain <span style="color:#C9A176">attributes</span> the object has. 

Those attributes are called <span style="color:#C9A176">instance variables</span> and are defined at the <span style="color:#C9A176">top</span> of the class.

Since they belong to the class itself and the instance of an object of that class, those variables are always contant to the class and therefore easier to manipulate <span style="color:#C9A176">inside</span> of the class

<br>

```cs
using System;

namespace Playground 
{
    internal class Class01
    {
        private int integer_1 = 24;
        private double double_1 = 5.6;
        private char character = 'a';
        private string word = "this is a sentence actually";
    }
}
```
<br>

#### <a id="gettersAndSetters"><span style="color:#C9A176">01.02 GETTERS & SETTERS</a>
---------------------
<br>

getters and setters, also called the <span style="color:#C9A176">accessor methods</span> are base methods used to modify the values of the instance variable of an object

those methods can be called <span style="color:#C9A176">outside</span> of the class, instead of the actual instance variables to further hide and protect the code

if we do not define the accessor methods for an instance variable is is <span style="color:#C9A176">impossible</span> to access it outside of the class itself

in C#, we call the getters and setters of the class inside of the <span style="color:#C9A176">properties</span>


<br>

#### <a id="properties"><span style="color:#C9A176">01.03 PROPERTIES</a>
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

#### <a id="methodsIntro"><span style="color:#C9A176">01.04 METHODS</a>
---------------------
<br>


> <span style="color:#2C6485"> For more information, see [<span style="color:#2C6485">**03.00 METHODS**](#methods)

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

#### <a id="main"><span style="color:#C9A176">01.05 MAIN</a>
---------------------
<br>

the main method, also called the <span style="color:C9A176">driver method</span> is where the code from one or multiple classes is executed

the Main method in the <span style="color:C9A176">Main class</span> is the primary method to execute the entire code

<br><br>

________
### <a id="variables"><span style="color:#C9A176">02.00 VARIABLES</a>
________________

<br>

variables can be different <span style="color:C9A176">data types</span>, which we define, to tell the computer what 'stuff' something is

For example, if we want to define a simple integer (number), like 4, the compilier doesn't know what '4' is, therefore, we add <span style="color:C9A176">int</span> in front of it, thus defining 4 for the computer

<br>

#### <a id="primitive"><span style="color:#C9A176">02.01 PRIMITIVE</a>
---------------------
<br>

primitive data types are data that is <span style="color:C9A176">directly referenced</span> in the memory of the computer as a series of bytes (0 and 1)

they can hold a maximum value defined by the number of bytes they are defined to occupy in the computer memory

| NAME | SYMBOL | SIZE | MIN VALUE | MAX VALUE | 
|------|--------|------|-----------|-----------|
| integer | <span style="color:C9A176">int</span> | 4 bytes | -2 147 483 648 | 2 147 483 647 |
| double | <span style="color:C9A176">double</span> | 8 bytes | -1.79769313486232 e 308 | 1.79769313486232 e 308 |
| float | <span style="color:C9A176">float</span> | 4 bytes | -3.402823 e 38 | 3.402823 e 38 |
| boolean | <span style="color:C9A176">bool</span> | 1 byte | false | true |
| character | <span style="color:C9A176">char</span> | 2 bytes |  | |



<br>

#### <a id="nonPrimitive"><span style="color:#C9A176">02.02 NON-PRIMITIVE</a>
---------------------
<br>

in programming languages, non-primitive data types are data types which are actually <span style="color:C9A176">classes</span>

non-primitive data types are <span style="color:C9A176">not directly referenced</span> in the memory but the computer rather holds the <span style="color:C9A176">memory address</span> of the class

in C# the only non-primitive data type (for now) is the <span style="color:C9A176">string</span>. It is easier to see it in java as it is written with a capitalized s (String), therefore defining it as a class

the string is a sequence of characters

non-primitive data types also contain methods which can be used to modify them (for example : <span style="color:C9A176">.toUpper()</span> which capitalizes every letter of a given string)

<br>

```cs
using System;

namespace Playground 
{
    internal class Class
    {
        private string name = "John Doe";

        //method
        public void PrintName (string name) { 
            Console.WriteLine(name); //will print the memory address, not the value

            name.toString(); //will print the value of the string : John Doe
        }
    }
}
```


<br>
<br>

________
### <a id="methods"><span style="color:#C9A176">03.00 METHODS</a>
________________

<br>

As mentionned earlier, methods are small paragraphs of codes that are made to perform one <span style="color:C9A176">action</span>

They contain 3 parts

1. header
2. body
3. return

<br>

The <span style="color:C9A176">header</span> is where you declare <span style="color:C9A176">how</span> the method will work

The <span style="color:C9A176">body</span> is where you code the <span style="color:C9A176">action</span>

The <span style="color:C9A176">return</span> is what your method will <span style="color:C9A176">give back</span>

<br>

```cs
using System;

namespace Playground 
{
    internal class Class
    {
        public void makeSound () {
            Console.Write("bing!");
        }
    }
}
```

<br>

#### <a id="methodHeader"><span style="color:#C9A176">03.01 HEADER</a>
---------------------
<br>

The header of the method is written as such :

accessor static/non-static returnType name (input parameter list) {}

The <span style="color:C9A176">accessor</span> is how visible your method is going to be :

| ACCESSOR  | VISIBLE TO | NOT VISIBLE TO |
|-----------|------------|----------------|
| <span style="color:C9A176">public</span>    | all        |      -         |
| <span style="color:C9A176">protected</span> | file <br> class <br> inherited class <br> | non-derived class |
| <span style="color:C9A176">private</span>   | file <br> class | inherited class <br> non-derived class |
| <span style="color:C9A176">internal</span>  | within assembly  | out of assembly |

<br>
<br>

Wether a method is static or not is how you want to defined where it belongs
<br>

a <span style="color:C9A176">static</span> method <span style="color:C9A176">belongs to the class</span>

```cs
public static void randomMethod () {}
```

<br>

a <span style="color:C9A176">non-static</span> method belongs to an <span style="color:C9A176">instance of a class</span>, or in other words, to an object itself

```cs
public void randomMethod () {}
```
<br>

<br>

Next, the <span style="color:C9A176">return type</span> of a method is what you want your method to give you back. It can be all the data types + void

Apart from void, all return types will need a return statment in the method

```cs
public static int randomMethod () {
    return 5;
}
```
<br>

```cs
public void randomMethod () {
    Console.WriteLine("This is a random method!");
}
```
<br>

```cs
public static string randomMethod () {
    return "Hello World!";
}
```
<br>

the <span style="color:C9A176">input parameters</span> are variables you give to your method

They allow the methods to be more general 

```cs
public static string printFullName (string firstName, string lastName) {
    string fullName = firstName + " " + lastName;
    return fullName;
}
```

<br>

```cs
public static void printAccount (string name, int accountNum, double balance) {
    Console.WriteLine($"ACCOUNT {accountNum}\n   NAME : {name}\n   BALANCE : {balance, C}");
}
    /*
    It will print this :
    ACCOUNT 456531
        NAME : randomName
        BALANCE : $8025.63
    */
```

<br>

#### <a id="methodBody"><span style="color:#C9A176">03.02 BODY</a>
---------------------
<br>

A method body is what performs the actions, the calculations, etc. of the method, and in general, the class

A good method only performs one or very few actions and is smaller than 50 lines of code

<br>

```cs
public static int numberSum (int num1, int num2) {
    int sum = num1 + sum2;
    return sum;
}
```


<br>

#### <a id="methodReturn"><span style="color:#C9A176">03.03 RETURN</a>
---------------------
<br>

When a method performed the desired aciton(s), it will <span style="color:#C9A176">return a result</span>

if a method contains control flow statements, there might be the need of <span style="color:#C9A176">multiple returns</span> through the body to handle every option possible

Furtheremore, returns can allow us to break out of a method early and avoid error messages or unecessary use of the computer ressources

<br>

```cs
public static int getBiggerNum (int num1, int num2) {
    if ((num1 || num1) == null) {
        break; //breaks out of the method if eithe number is null
    }
    
    if (num1 > num2) {
        return num1;
    } else {
        return num2;
    }
}
```








<br><br><br><br><br><br><br>


Text colour : #8C8CF7 <br>
Highlight : <span style="color:#C9A176"> #C9A176</span> <br>
Notes : <span style="color:#2C6485">#2C6485</span>

<span style="color:#C9A176">made by ash-a9236 <br> Created February 2025<span>


