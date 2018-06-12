---
title: "Python Operators"
date: 2018-06-12T17:20:08Z
draft: false
author: "Adnan"
share: true
slug: "Python-Operators"
---

In this tutorial you will learn:

1. Arithmetic operators
2. Assignment operators
3. Comparison operators
4. Logical operators
5. Bitwise operators
6. Membership operators
7. Identity operators

Introduction:
-------------
Before we jump to the operators lets define what is an operator. An operator is a special symbol that python or any other programming language use to 
make some arithmetic, assignment or logical computation.<br/>

1 Arithmetic operators:
-----------------------
Arithmetic operators are used to perform mathematical operations that we are familliar with, like addition, subtraction, division and multiplication etc.

|Operator  |Explanation                                          											                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
|    +     |Addition operator: add two operands (10 + 3) 10 and 3 are the operands  											     |
|    -     |Subtruction operator: Subtract the right operand from the left  operand    											     |
|    /     |Division operator: Devide left operand by the right operand (the result of this division is always a float number)       |
|    *     |Multiplication operator: Multiply two operands                                                                           |
|    //    |Floor division operator: Devide left operand by the right operand (the result of this division is always an int number)  |
|    %     |Modulus operator: Devide left operand by the right operand (the result is the remainder of the division)                 |
|    **    |Exponent operator: Perfoms exponential calculation by rasing the left operand to the power of the right operand          |

Lets see some examples:

{{< highlight python "linenos=inline,linenostart=0" >}}
#Addition
a = 4 + 5
print("a =", a)

#Subtraction
b = 9 - 5
print("b =", b)

#Division
c = 20 / 3
print("c =", c)

#Multiplication
d = 2 * 4
print("d =", d)

#Floor division
e = 20 // 3
print("e =", e)

#Modulus
f = 10 % 2
print("f =", f)

#Exponent
g = 5 ** 2
print("g =", g)

{{< / highlight >}}

> OUTPUT: a = 9

> OUTPUT: b = 4

> OUTPUT: c = 6.66666666667

> OUTPUT: d = 8

> OUTPUT: e = 6

> OUTPUT: f = 0

> OUTPUT: g = 25

As you see this is how we can use these operators in python.<br/>
Lets take a look at the division operator, you see when we devide 20 by 3 (20 / 3) we get a floating point number : 6.66666666667, but
when we use the Floor division operator we get an integer number: 6, this effect is the same when we use the int() built-in function to convert a 
float number.<br/>
Now lets look at the modulus operators:
When we devide 10 by 2 the result will be 5 which mean there is zero remainder and this is the job of the modulus it devide two numbers and return the remainder of the
division.<br/>

2.Assignment operators:
-----------------------
We have already used an assignment operator which is  the '=' symbol.<br/>
We use the assignment operators to assign a value to a variable. In python we have like a shortcut assignment operators to assign a value to the variable.<br/>

|Operator   |Explanation                                                            |
|-----------|-----------------------------------------------------------------------|
|   =       |Assign value from right side operand to left side (x = 5)              |
|   +=      |Add and assign: (x += 5) this is equivalent to x = x + 5               |
|   -=      |Subtract and assign: (x -= 5) this is equivalent to x = x - 5          |
|   /=      |Devide and assign: (x /= 5) this is equivalent to x = x / 5            |
|   *=      |Multiply and assign: (x *= 5) this is equivalent to x = x * 5          |
|   %=      |Modulus and assign: (x %= 5) this is equivalent to x = x % 5           |
|   //=     |Floor division and assign: (x //= 5) this is equivalent to x = x // 5  |
|   **=     |Exponent and assign: (x **= 2) this is equivalent to x = x ** 2        |
|    >>=    |Bitwise right shift and assign                                         |
|    <<=    |Bitwise left shift and assign                                          |
|    ^=     |Bitwise XOR and assign                                                 |
|    ~=     |Bitwise NOT and assign                                                 |
|    \|=     |Bitwise OR and assign                                                  |
|    &=     |Bitwise AND and assign                                                 |

Lets see some code examples:

{{< highlight python "linenos=inline,linenostart=0" >}}
#Assign 5 to x
x = 5

#Add 5 and assign
x += 8
print("x :", x)

#Subtract and assign
x -= 2
print("x :", x)

#Devide and assign
x /= 2
print("x :", x)

#Multiply and assign
x *= 5
print("x :", x)

#Modulus and assign
x %= 2
print("x :", x)

#Exponent adn assign
x **= 5
print("x :", x)

#Floor division and assign
x //= 5
print("x :", x)

{{< / highlight >}}

> OUTPUT: x : 13

> OUTPUT: x : 11

> OUTPUT: x : 5.5

> OUTPUT: x : 27.5

> OUTPUT: x : 1.5

> OUTPUT: x : 7.59375

> OUTPUT: x : 1.0

3 Comparison operators:
------------------------
We use comparison operators to compare between values, the ruslt of the comparison will be a bool (True or False).

|Operator  |Explanation                                                                                                                                     |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
|    >     |Greater than: if the left operand is greater than the right operand the result will be True (5 > 2)                                             |
|    <     |Less than: if the left operand is less than the right operand the result will be True (2 < 5)                                                   |
|    ==    |Equal to: if both the left and right operands are equal the result will be True (5 == 5)                                                   		|
|    >=    |Greater than or equal: if the left operand is greater than or equal to the right operand the result will be True(5 >= 2) (5 >= 5) both are True |
|    <=    |Less than or equal: if the left operand is less than or equal to the right operand the result will be True (5 <= 2) (5 <= 5) both are True      |
|    !=    |Not equal to: if the left operand is different from the right operand the result will be True (5 != 2)                                          |

Lets see these operators in code:

{{< highlight python "linenos=inline,linenostart=0" >}}
#OUTPUT True
print(5 > 2)

#OUTPUT False
print(5 > 10)

#OUTPUT True
print(3 < 5)

#OUTPUT False
print(3 < 1)

#OUTPUT True
print(5 == 5)

#OUTPUT False
print(5 == 6)

#OUTPUT True
print(8 >= 8)

#OUTPUT False
print(8 >= 9)

#OUTPUT True
print(12 <= 15)

#OUTPUT False
print(12 <= 10)

#OUTPUT True
print(5 != 10)

#OUTPUT False
print(5 != 5)

{{< / highlight >}}

4 Logical operators:
--------------------
In python we have three logical operators ''and'', ''or'', ''not'', these operators return a boolean result based on the condition.

|Operator    |Explanation                                                                              |
|------------|-----------------------------------------------------------------------------------------|
|    and     |This will return True when both left and right operand are True                          |
|    or      |This will return True if one the operand is True                                         |
|    not     |This will return the inverse of the operand, if the operand is True it will return False |

Lest see some examples:

{{< highlight python "linenos=inline,linenostart=0" >}}
#OUTPUT True
x = (5 > 2 and 3 > 1)
print("x:", x)

#OUTPUT True
y = (5 == 5 or 5 > 8)
print("y:", y)

#OUTPUT False
z = (not 5 > 2)
print("z:", z)

{{< / highlight >}}

Lets take a look at this code:<br/>
In the first example we have assigned to ''x'' a logical operation, the first part is (5 > 2) this will return True, and the second part
is (3 > 1) which also return True, and by using the logical ''and'' operator: True and True will return a True. If one of the comparison operator returned False, then
the result of our logical operation will be False.<br/>
The second example is also devide in two part, the first is (5 == 5) which return True and the second part is (5 > 8) which return False, by using the ''or'' logical
operator the result will be True, because the ''or'' operator needs one of the two operand to be True to return True.<br/>
The last example is very simple the comparison operation (5 > 2) return True, and by using the ''not'' operator we get the inverse of the result which is False in our case.<br/>

5 Bitwise operators:
---------------------
Bitwise operators are used to perform a bit by bit operation.

|Operator  |Explanation         |
|----------|--------------------|
|   >>     |Bitwise right shift |
|   <<     |Bitwise left shift  |
|   &      |Bitwise AND         |
|  \|      |Bitwise OR          |
|   ~      |Bitwise NOT         |
|   ^      |Bitwise XOR         |

Lets see some examples:

{{< highlight python "linenos=inline,linenostart=0" >}}
#x = 3 in binary
x = 0b00000011

#y = 242 in binary
y = 0b11110010

a = x & y

'''
a = x & y

Lets see how that happened

x     = 00000011
y     = 11110010
-----------------
x & y = 00000010
'''

#OUTPUT 2
print(a)

{{< / highlight >}}

As you see the ''&'' operator works like that when it finds 1 1 it gives us 1, if it finds 1 0 or 0 1 or 0 0 it returns 0.<br/>
To read more about bitwise operations click [here](https://en.wikipedia.org/wiki/Bitwise_operations_in_C)

6 Membership operators:
-----------------------
Membership operators are used to check whether a value is in a sequence or not (like string, or list etc.)

|Operator  |Explanation                                             |
|----------|--------------------------------------------------------|
|   in     |It will return True if the value is in the sequence     |
|  not in  |It will return True if the value is not in the sequence |

{{< highlight python "linenos=inline,linenostart=0" >}}
x = "Hello World"

#OUTPUT True
print('H' in x)

#OUTPUT True
print('h' not in x)

{{< / highlight >}}

In the first example returns True because the uppercase 'H' is in pur sequence, and the second example returns True because the lowecase 'h' is not in the sequence.<br/>
This mean that you need to be careful with this because it's case sensitive 'h' is different from 'H'.<br/>

7 Identity operators:
---------------------
Identity operators are used to check if two variables are located in the same memory location.

|Operator  |Explanation                                                                                       |
|----------|--------------------------------------------------------------------------------------------------|
|    is    |It will return True if both left and right operand are located on the same location in memory     |
|   is not |It will return True if both left and right operand are not located on the same location in memory |

{{< highlight python "linenos=inline,linenostart=0" >}}
x = 5
y = 5.4

#OUTPUT False
print(x is y)

#OUTPUT True
print(x is not y)

a = "hello world"
b = "hello world"

#OUTPUT False
print(a is b)

#OUTPUT True
print(a is not b)

{{< / highlight >}}

In this example we see that the variables ''a'' and ''b'' are both identical but when we check ''a is b'' we get False this mean that each one is located
in a different location in memory. You can check the location of your variables using the id() built-in function:

{{< highlight python "linenos=inline,linenostart=0" >}}
x = 5 

#OUTPUT 49301269 THIS NUMBER WILL BE DIFFERENT ON YOUR MACHINE 
print(id(x))

{{< / highlight >}}

This is all for this lecture, I hope you enjoyed it.<br/>