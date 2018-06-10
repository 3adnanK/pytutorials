---
title: "Multiple Assignment and Comments"
date: 2018-06-10T14:16:53Z
draft: false
author: "Adnan"
share: true
slug: "Multiple-Assignment-and-Comments"
---
In this tutorial you will learn:

1. Multiple assginment 
2. Comments

1 Multiple assginment:
----------------------
In the previous tutorial [Variables and Inputs/Outputs](https://3adnank.github.io/pytutorials/variables-and-io/) we saw how to make a variable and assign to it a value using the assignement sign '='.<br/>
In python we can create more than one variables on the same line, lets see an example:

{{< highlight python "linenos=inline,linenostart=0" >}}
x, y, z = 22, 23, 24

print(x, y, z)
{{< / highlight >}}

> OUTPUT: 22 23 24

As you see we have created 3 variables x, y and z then we have used the assginment sign '=' to asign the values to the variables.<br/>
The first value (22) will be assigned to the x variable and the value (23) will be assigned to the (y) variable and so on, each variable has to be in the same order of the value
that will be assigned to it.<br/>
We could also add multiple assginment statement '=' on the same line using the semicolons to seperate each assignement:

{{< highlight python "linenos=inline,linenostart=0" >}}
x = 22; y = 23; z = 24

print(x, y, z, end=', ')
{{< / highlight >}}

> OUTPUT: 22, 23, 24

As you see, it is the same way that we used to create a variable and assign to it a value, the only difference here is that we have added 3 variables on the same line
and to do that we have to add the semicolon ';' not the comma ','.<br/>
The semicolon will tell the python interpreter that this statement has ended.<br/>
In the next tutorial when you learn about operators you will learn how to make multi-line assignement, for now just learn how make multiple assginment on the same line.<br/>

2 Comments:
-----------
Comments are some text that we use to describe what our code does, this is very useful when you have alot of code, you will use comments to describe the work of each part of the code
this will make your code easier to read by other developers if you are working with a team.<br/>
In python we create a comment by using the hash ''#'' symbol.<br/>
Anything that follow the hash ''#'' symbol will be considered as comment and it will be ignored by the interpreter.<br/>
Note that the hash ''#'' symbol allows you to write a one line comment, lets see an example:

{{< highlight python "linenos=inline,linenostart=0" >}}
#here we using multiple assginment to assign values to our variables
x, y, z = 22, 23, 24

#we use the print function to print our variables
print(x, y, z)
{{< / highlight >}}

> OUTPUT: 22 23 24

As you see we have used comments to describe each part of our code and when we run the code our comments are ignored by the interpreter, only the variables are printed.<br/>
Now lets see what will happen if we use the hash symbol to write multi-line comments:

{{< highlight python "linenos=inline,linenostart=0" >}}
#here we using multiple assginment to 
assign values to our variables
x, y, z = 22, 23, 24

#we use the print function to print our variables
print(x, y, z)
{{< / highlight >}}

When you run this code you will get an error because the hash symbol allows us to write only one line comment.<br/>
To write multi-line comments we can add hash symbol on each line:

{{< highlight python "linenos=inline,linenostart=0" >}}
#here we using multiple assginment to 
#assign values to our variables
x, y, z = 22, 23, 24

#we use the print function to print our variables
print(x, y, z)
{{< / highlight >}}

> OUTPUT: 22 23 24

Or we can use triple quotes, either ''' or """ :

{{< highlight python "linenos=inline,linenostart=0" >}}
'''
here we using multiple assginment to 
assign values to our variables
'''
x, y, z = 22, 23, 24

#we use the print function to print our variables
print(x, y, z)
{{< / highlight >}}

> OUTPUT: 22 23 24


Exercices Section:
------------------

### Exercice 1:
Find the correct syntax:

1. x, y = 4, 5
2. x; y; = 4; 5
3. x, y; z = 4, 5, 6
4. x = 4, y = 5, z = 6
5. #this comment is<br/>
   a test comment.