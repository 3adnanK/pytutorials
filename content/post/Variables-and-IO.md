---
title: "Variables and Inputs/Outputs"
date: 2018-06-06T14:14:37Z
draft: false
author: "Adnan"
share: true
slug: "variables-and-IO"
---

In this tutorial you will learn:
1. What is a variable
2. How to make variables in python
3. How to use print to display variables
4. How to read user inputs

1 What is a variable:
=====================
To understand what is a variable lets imagine that we have two boxes, the first box contain some clothes and the second one
contain some video games CD's as you see our two boxes are containers that holdes some objects.<br/>
Now lets say the we want to get our video games CD's, to do that we simply open the box that contain the video games, but
how can we know which box does it contain the CD's ? if the two boxes looks the same, this is actually not
a big problem for two boxes but if we have much more boxes it will be a very difficult task to find the specific box that we want.<br/>
To solve this problem we add a label to the box, the label will describe the content of this box so that we can destinguish between the boxes.<br/>

Variables are simply just like this boxes we create them to hold some data that we use during the program life cycle, each variable has a name that describe
its content.<br/>

Now that you know what is a variable, lets see how to make one in python.

2 How to make variables in python:
==================================
To make a variable in python we first define the name of our variable and then we use the '=' sign that we call it the assignement sign to assign values to our variable.

{{< highlight python "linenos=inline,linenostart=0" >}}
video_games_CDs = 65
{{< / highlight >}}

As you see we have asigned 65 to the video_games_CDs variable, this variable name describe its content so that 65 means the number of CDs that we have.<br/>

In python and other programming language we have some rules to follow to create a correct variable name, this rules are the following:

* Variable can only be a combination of letters lowercase or uppercase(a-z)(A-Z) or digits (0-9) or an underscore _
  Exmeple: MyVariable, my_variable, my_Variable1
  
* Variable can only start with letter or underscore, it can not start with digits

* Variable can not contain any special symbol like @, #, $, %, !, * etc...

* Variable can not be a special keyword (special keyword are some names reserved by python)

* Variables in python are case-sesitive which mean that MyVariable and myvariable are two different variables.

The list of reserved keywords:
|------|---------|-------|--------|---------|------|
|None  |class    |is     |lambda  |nonlocal |raise |
|True  |and      |not    |if      |global   |for   |
|False |assert   |in     |elif    |import   |from  |
|as    |del      |or     |except  |with     |      |
|def   |else     |return |try     |while    |      |
|break |continue |yield  |finally |pass     |      |

Now lets see some examples:
{{< highlight python "linenos=inline,linenostart=0" >}}
continue = 5
{{< / highlight >}}
When you run the code you will get a ''SyntaxError: invalid syntax''
this is because our variable name does not follow the rules of python variables.<br/>

Now you know how to create a variable now lets see how to print it.

3 How to use print to display variables:
========================================
We use the print() function to outpout anything to our console window (we will learn more about functions in later tutorial).<br/>
Lets print now our video_games_CDs variable.

{{< highlight python "linenos=inline,linenostart=0" >}}
video_games_CDs = 65
print(video_games_CDs)
{{< / highlight >}}
> OUTPUT: 65

As you see our print function prints out the value of our variable.</br>
We can add more argument to the print function by seperating each argument with a comma ','

{{< highlight python "linenos=inline,linenostart=0" >}}
cars = 3
houses = 2

print("Hey i have", cars, "cars and", houses, "houses")
{{< / highlight >}}
> OUTPUT: Hey i have 3 cars and 2 houses

In this example we have passed 5 arguments to our print function which demonstrate that we can add as much as we want of arguments.<br/>
Note that if we want to pass a string (which is a data type in python, we will learn more about string later in another tutorial)
we use the double quotes "" we can also use single quotes ''.<br/>

Now lets see this example:
{{< highlight python "linenos=inline,linenostart=0" >}}
print("Blue", "Silver", "Red")
{{< / highlight >}}
> OUTPUT: Blue Silver Red

When your run this code you will see that each number is seperated by space, this is because the default arguments in the print function are seperated by space
but we can change that by passing 'sep' argument to the print function.<br/>
lets see how to do that:

{{< highlight python "linenos=inline,linenostart=0" >}}
print("Blue", "Silver", "Red", sep=', ')
{{< / highlight >}}
> OUTPUT: Blue, Silver, Red

As you see our values are now seperated with comma and a space, you can define any seperator you want.<br/>
Now lets see another useful argument that can be passed to the print function.
{{< highlight python "linenos=inline,linenostart=0" >}}
print("Hello")
print("World")
{{< / highlight >}}
> OUTPUT: Hello<br/>
> OUTPUT: World
		
When you run this code you will see that each word is printed on a seperate line, this is due to the default value of the ''end'' argument
this argument define how do we want to end the world in the print function, by default it is end line, which force the interpreter to return to the line
when the print function outpout its content.<br/>
Lets see an example on how to change this default end line.
{{< highlight python "linenos=inline,linenostart=0" >}}
print("Hello", end=" ")
print("World")
{{< / highlight >}}
> OUTPUT: Hello World
As you see we have changed the value of the ''end'' argument from end line which is represented by ''\n'' to an empty space this caused the interpreter
to output the next value of the print function on the same line of the first print function output.<br/>
Now that you know how to create a variable in print it out lets see how to read user inputs.<br/>

4 How to read user inputs:
==========================
To read user input in python we use the input() function.
{{< highlight python "linenos=inline,linenostart=0" >}}
user_name = input("Please enter your name: ")
print("The user name is:", user_name)
{{< / highlight >}}
When you run this code the interpreter or the console window will prints out the message that we defined in the input function
now the program will wait us until we type somthing and hit enter.<br/>
When you enter your name and hit enter, the value will be assigned to the user_name variable and it will be printed in the print function.<br/>

NOTE:
-----
print(): is a function in python 3.x but in python 2.x is a statement: print "something".<br/>
input(): is a function that read use inputs in python 3.x, but in python 2.x we use raw_input() function to read user inputs.<br/>

Exercices Section:
==================
This section will contain some exercices to practice what you have learned.

Exercice 1
----------
Which one of this variables name is correct:
* Age = 56
* $My_age = 45
* __userName = 'KANIKI'
* break = 2
* @email = "email@mail.com"

Exercice 2
----------
Write a program that ask the user to write his name and age, and assign the values to (user_name and user_age)
then print the name and the age of the user like the following:
OUTPUT: Hi my name is your_username and i am you_userage

Exercice 3
----------
month = 3
day = 16
year = 2018
use the sep argument of the print function to print the variables like the following result:
OUTPUT: 16/3/2018
