---
title: "Python Data Types Part One"
date: 2018-06-11T15:04:47Z
draft: true
draft: false
author: "Adnan"
share: true
slug: "Python-Data-Types-Part-One"
---
In this tutorial you will learn:

1. Numbers
2. Type conversion

Introduction:
-------------
Python data-type is a classification that specifies the type of value a variable has.
Since everything in python is an object, every type in python have his own specific methods and attributes that can be used on this type.
(we will discuss more about Ojbects later and see how to create our own data type).<br/>

This tutorial will be devided in two part the first part which is the current tutorial will be about the numbers data-types and 
the second part will be about some more complex data-types like list and tuple.

1 Numbers and type():
---------------------
Python support different type of numbers like int (Integers), float (floating point) and complex (complex number).<br/>

* Integer is a number that is not a fraction, it can be negative or positive number: (23, 65, -5)
* Floating point is a number that contain floating decimal like: (25.6, 75.0, 55.33, -33.45)
* Complex number is a number that can be expressed in the form a + bi, in python the i is replaced by j : (23 + 4i).
You may not use this type unless you have some math problem that use this type. Actually i have never used this type in my code
but it is good to know about it in case you need it.
You can read more about complex number [here](https://en.wikipedia.org/wiki/Complex_number)

Now lets some examples:

{{< highlight python "linenos=inline,linenostart=0" >}}
#int type
x = 24

#float type
y = 65.25

#complex type
z = 24 + 3j

{{< / highlight >}}

When you run this code each variable type will be defined based on its own value.<br/>
Python automaticaly knows what type the variable is based on the value assigned to it.<br/>

In python we can use a built-in function called '''type()''' to see the type of our variables, lets see an example of that:

{{< highlight python "linenos=inline,linenostart=0" >}}
#int type
x = 24
print(type(x))

#float type
y = 65.25
print(type(y))

#complex type
z = 24 + 3j
print(type(z))

{{< / highlight >}}

> OUTPUT: \<class 'int'\>

> OUTPUT: \<class 'float'\>

> OUTPUT: \<class 'complex'\>

As you see the '''type''' function tells us the type of each variable.<br/>

The numbers that we have been using and what we always use and see around us are decimal (base 10) number system, but there is some other number systems
that can be used by programmers like: binary (base 2), octal (base 8) and hexadecimal (base 16).<br/>
In python we can represent these numbers by adding a special prefix.<br/>

|Number System  |Prefix         |
|---------------|---------------|
|Binary         | '0b' Or '0B'  |
|Octal          | '0o' Or '0O'  |
|Hexadecimal    | '0x' Or '0X'  |

Lets see this in code:

{{< highlight python "linenos=inline,linenostart=0" >}}
#binary
x = 0b01101

#octal
y = 0o15

#hexadecimal
z = 0xD

print(x, y, z, sep=', ')
{{< / highlight >}}

> OUTPUT: 13, 13, 13

As you see we have printed the number 13 in a three different number systems.<br/>
You can read more about the different type of number systems [here](https://www.rapidtables.com/math/number/Numeral_system.html).

2 Type conversion:
------------------
In python we can convert one type of number to another type. Lets see an example :

{{< highlight python "linenos=inline,linenostart=0" >}}
#int
x = 55
print(type(x))

#float 
y = 33.45
print(type(y))

#convert x from int to float
x = float(x)
print("converted x", type(x))

#convert y from float to int
y = int(y)
print("converted y", type(y))

#convert string to complex
z = complex('3 + 4j')
print(type(z))

{{< / highlight >}}

> OUTPUT: \<class 'int'\>

> OUTPUT: \<class 'float'\>

> OUTPUT: converted x \<class 'float'\>

> OUTPUT: converted y \<class 'int'\>

> OUTPUT: \<class 'complex'\>

As you see we have converted int type to float and float to int, using the '''int()''', '''float''' and '''complex''' built-in functions.<br/>
In part two of this tutorial we will learn more about some other important types like list, tuple and string.<br/>
