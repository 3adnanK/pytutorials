---
title: "Python Strings"
date: 2018-06-20T18:20:55Z
draft: false
author: "Adnan"
share: true
slug: "Python-Strings"
---

In this tutorial you will learn:

1. String indexing and slicing
2. How to count the number of characters using len()
3. String operations
4. Some useful string methods

1 String indexing and slicing:
------------------------------
In the prevous tutorial (Python Data Types Part Two), we have seen how to access any character in a string using indexing method:

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Hello World"

#OUTPUT: H o
print(var[0], var[4])

{{< / highlight >}}
The index numbering in python and some other programming language start from zero (0).<br/>
Python has a very powerfull feature that let you slice any ordered sequence (string, list, tuple) called slicing.<br/>
Lets see an example:

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Hello World"

#OUTPUT: Hello
print(var[0:5])

#OUTPUT: Hello
print(var[:5])

#OUTPUT: World
print(var[6:])

{{< / highlight >}}
In this example we slice our string to two parts, the first is 'Hello' and the second is 'World'.<br/>
To use the slicing method we add two square brackets like the indexing method then we define the starting index, the index that we want to
start slicing from it if we don't define anything by default python will start from index zero '0', then we add colon and the end index, which define
the index where we want to stop slicing, the character at the 'stop index' will not be included in the sliced result the slicing will stop just before 
that index, if no stop index is defined python will continue to the end of the sequence.<br/>
We can also add a third number to our slicing method that allows us to set how the index of the sequence will be incremented.<br/>
Lets see an example to understand this clearly.

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Hello World"

#jump one character
#OUTPUT:HloWrd
print(var[::2])

{{< / highlight >}}

As you see to jump one character we set the step number to two, if we type one (1) instead of two (2) we will get the whole sequence: 'Hello World'.<br/>
So why 2 make us jump one character ? :<br/>
As you know 0 is the first index and to jump one character this means the next index after zero should be 2 because we want to jump 1 character,
now the next index after two should be 4 and the next is 6 and so on until the end of the sequence, if you notice each time we add 2 to
the previous index and this is how the number 2 in the step number means, it defines how much to add to the previous index to jump to the next index.<br/>
We can also use negative numbers for the step part:

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Hello World"

#OUTPUT: dlroW olleH
print(var[::-1])

{{< / highlight >}}


2 How to count the number of characters using len():
----------------------------------------------------
Python has a built-in function called len() this function take a sequence and return the length of it.

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Hello World"

#OUTPUT: 11
print(len(var))

{{< / highlight >}}
When you run this code the len() function will return an int number equale to 11 which means that our variable ''var'' contain 11 character: 10 alphabetical characters and 1 is 
the space between the two word.<br/>
 
3 String Operations:
--------------------
We can apply some arithmetic operators to manipulate a string object:<br/>
For example to concatenate two ore more strings objects we can use the addition '+' operator:<br/>
 
{{< highlight python "linenos=inline,linenostart=0" >}}
var1 = "Hello "
var2 = "World"

var3 = var1 + var2

#OUTPUT: Hello World
print(var3)

{{< / highlight >}}
As you see we have used the addition operator '+' to concatenate the two str object var1 and var2.<br/>
We can also use the multiplication operator '*' to multiply the string.<br/>
{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Hello "

#OUTPUT: Hello Hello Hello
print(var * 3)

{{< / highlight >}}
In this example we have repeated the word 'Hello' three times by multiplying our str object by 3 using the multiplication operator '*'.<br/>
We can also check if a sub string exists within a string or not by using the membership operator 'in':<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Apple"

#OUTPUT: True
print('p' in var)

#OUTPUT: False
print('s' in var)

{{< / highlight >}}

4 Some useful string methods:
------------------------------
In this section you learn some useful method that are part of the str object:

#### format:

Python str object has a method called format() that allows us to format our string.<br/>
Lets see an example:

{{< highlight python "linenos=inline,linenostart=0" >}}
var1 = "abc"
var2 = "def"

#OUTPUT: var1 = abc and var2 = def
print("var1 = {} and var2 = {}".format(var1, var2))

#OUTPUT: var1 = abc and var2 = def
print("var1 = {0} and var2 = {1}".format(var1, var2))

#OUTPUT: var2 = def and var1 = abc
print("var2 = {1} and var1 = {0}".format(var1, var2))

#OUTPUT: var1 = abc and var2 = def
print("var1 = {variable_one} and var2 = {variable_two}".format(variable_one=var1, variable_two=var2))

{{< / highlight >}}
As you see we can call format() on our string and pass to it the variables or the values that we want to be added to our string.<br/>
The format() method will look for any opened and closed curly braces '{}' and replace it with the specific value based on the order if no number or label has been set in 
between the curly braces.<br/>

### replace:

As you know the str object is immutable that mean we can't change or delete any character in the characters sequence using the indexing method, but the str object has method called 
replace() that takes three arguments: 

1. old: the character that we want to replace.
2. new: the character that we want to be replacing the old one.
3. count: this is an optional argument, it is the number of characters that we want to be replaced.

This method will create a new modified str boject and return it, it won't change the original str object.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "Apple"

#OUTPUT: Akkle
print(var.replace('p', 'k'))

#OUTPUT: Akple
print(var.replace('p', 'k', 1))

{{< / highlight >}}
In this example we have called the replace method two times:<br/>
In the first call we have set the character 'p' to be replaced by the character 'k' and ignored the third argument (count) and the result was that all the 'p' characters 
has been replaced by 'k'.<br/>
In the second call we have set the number '1' as third argument in the replace method which means that we want only one 'p' character to be replaced.<br/>

### lower and upper:

Python str object has a method called lower() that convert all uppercase characters to lowercase, and a method called upper() that convert all lowercase characters to 
uppercase:

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "HeLLo WoRld"

#OUTPUT: hello world
print(var.lower())

{{< / highlight >}}

### isalpha:

This method is used to check if the str object is a sequence of only alphabetical characters, it will return True if only alphabetical characters are in the sequence and False 
if not.

{{< highlight python "linenos=inline,linenostart=0" >}}
var = "MyUsername"
var2 = "Hello World"

#OUTPUT: True
print(var.isalpha())

#OUTPUT: False
print(var.isalpha())

{{< / highlight >}}
In this example we have called the 'isalpha()' method on two different variables, in the first call the method returns True, because our 'var' variable contain only alphabetical 
characters, but in the second call it returns False due to the space character in between 'Hello' and 'World' which is not part of the alphabetical characters.<br/>

### isdigit:

This method is similar to our previous method, but this time this method will check if the str objects is a sequence of digits.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
var1 = "variable1"
phone_number = "4452133684"
#OUTPUT: Fale
print(var.isdigit(var1))

#OUTPUT: True
print(var.isdigit(phone_number))

{{< / highlight >}}

### isalnum:

This method is the combination of the two previous methods 'isalpha' and 'isdigit', this will return True if the str object contain only alphabetical characters or only digits 
or both at the same time.

{{< highlight python "linenos=inline,linenostart=0" >}}
#OUTPUT: True
print("Hello".isalnum())

#OUTPUT: True
print("2455".isalnum())

#OUTPUT: True
print("Hello4452".isalnum())

{{< / highlight >}}

You can read more about str methods that can be very useful for you: [Python Docs](https://docs.python.org/3/library/stdtypes.html#index-31).