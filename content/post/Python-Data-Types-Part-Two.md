---
title: "Python Data Types Part Two"
date: 2018-06-14T01:12:23Z
draft: false
author: "Adnan"
share: true
slug: "Python-Data-Types-Part-Two"
---

In this tutorial you will learn:

1. Strings
2. List
3. Tuple
4. Set
5. Dictionary

1 Strings:
----------
We have already been using this type in prevoius tutorials, this data type is actualy a sequence of characters enclosed within single ('') or double quotes ("").<br/>
Strings (called ''str'' in python) are an immutable sequence which means we can't change any of the charachters in the sequence.<br/> 
Lets make this more clear to you with an example:

{{< highlight python "linenos=inline,linenostart=0" >}}
name = "Itachi"

#OUTPUT: I t a c h i
print(name[0], name[1], name[2], name[3], name[4], name[5])

#OUTPUT: TypeError 'str' object doesn't support items assignment 
name[0] = 'K'
{{< / highlight >}}

Like we said before strings are just a sequence of charachters each charachter has its own index number, the index numbers start with zero, this mean that the first charater
in our sequence is at the index 0 and the second character is at the index 1 and so on.<br/>
To access any of these charachters we use the indexing method by typing the variable name that contain the string value followed by an opend square bracket '[' and a closed square bracket ']' 
and in between these brackets we put the index number of the charachter that we want to access it (variable_name[index_number]).<br/>
In the last statment we have tried to assign the value 'K' to the first index which is 0, but when we run the code we get a TypeError telling us that 'str' doesn't support
items assignment, because the strings are immutable.<br/>
Now lets see another example:

{{< highlight python "linenos=inline,linenostart=0" >}}
#OUTPUT: SyntaxError
var = 'I can't stop coding'

#Solutions
#var = "I can't stop coding"
#var = 'I can\'t stop coding'

{{< / highlight >}}
When you run this code you will get a SyntaxError caused by the single quote in (can't).<br/>
When you strat a string with a single quote the python interpreter will search for the second single quote which define the end of the string, 
and in our case the interpreter has found the single quote before the end of our string which caused the syntax error.<br/>
To avoid this error we can use two methods the first is to use double quotes when we want to use single quote in our charachters sequence or 
we use the single quote when we want to use double quotes in our charachters sequence.<br/>
The second method is to use the backslash symbol (\\) to escape any single or double quotes used in our charachters sequence.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
'''
If you start your string with single quote you escape only the single quotes
that are presented in your string.
'''
var = 'text that contain both "double quotes" and \'single quotes\''

'''
If you start your string with double quotes you escape only the double quotes
that are presented in your string.
'''
var1 = "text that contain both \"double quotes\" and 'single quotes'"

{{< / highlight >}}

You can use the str() built-in function to convert a number to str.

{{< highlight python "linenos=inline,linenostart=0" >}}
var = 45

#OUTPUT: <class 'int'>
print(type(var))

var = str(var)

#OUTPUT: <class 'str'>
print(type(var))
{{< / highlight >}}

You will learn more about strings in the next tutorial.

2 List:
-------
List is a mutable sequence of items, which means that we can change the items in the list.<br/>
List items can be all of the same type or different types.<br/>
List items are enclosed within brackets [].

{{< highlight python "linenos=inline,linenostart=0" >}}
var = [1, 2, 3, 5.5, 7.3, 'hi']

#OUTPUT: <class 'list'>
print(type(var))

#OUTPUT: 1 5.5 hi
print(var[0], var[3], var[-1])

#Replace list items
var[0] = 44

#OUTPUT: 44
print(var[0])

{{< / highlight >}}
In this example we have created a list that contain some items with different types int, float and str.<br/>
To access these items we use the same indexing method that we have used with strings.<br/>
The new syntax here is ''var[-1]'', the -1 means the last item in the sequence, we can use the negative numbers in the indexing method
to access the items from the right side of the sequence: (-2 means the second item from the right and -3 is the third item from the right and so on ...).<br/>

3 Tuple:
--------
Tuple is same as list, both are an ordered sequence of items but the difference between tuple and list is that tuple is immutable which means that we can't modify its content, 
and the items are enclosed within parentheses '()'.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
var = (1, 2, 3, 5.5, 7.3, 'hi')

#OUTPUT: <class 'tuple'>
print(type(var))

#OUTPUT: 1 5.5 hi
print(var[0], var[3], var[-1])

{{< / highlight >}}
As you see we access the tuple's items using the same method that we have used in both list and str.<br/>
Note: To create a tuple that contain only one item you need to add comma after the item: (1,), if you don't do that the interpreter
will consider it as an integer assginment not a tuple.<br/>

4 Set:
------
Set is an unordered collection of unique items enclosed within curly braces '{}', this mean that we can't use the indexing method to access the items and all the items are uniques, 
that mean no repeated items.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
var = {1, 2, 3, 4, 4, 2, 5, 1, 1, 'hi', 'hi'}

#OUTPUT: <class 'set'>
print(type(var))

#OUTPUT: {1, 2, 3, 4, 5, 'hi'}
print(var)

#OUTPUT: TypeError
print(var[0])

{{< / highlight >}}
When you run this code, the second print function ''print(var)'' will print only unique items all the repeated items are removed.<br/>
When we try to access the first item using the indexing method we get an error, because set doesn't support the indexing method.<br/>
Note: When you print your set, the result won't be always ordered like list and tuple.<br/>
You will learn more about sets in an upcoming tutorial.<br/>

5 Dictionary:
-------------
Dictionary is an unordered collection of Key-Value pairs enclosed within curly braces '{}' and each Key-Value is seperated by colon ':'.<br/>
The key can be any immutable type like tuple, string and numbers.<br/>
The value can be any type.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}
var = {'key':'value', 'banana':35}

#OUTPUT: <class 'dict'>
print(type(var))

#OUTPUT: 35
print(var['banana'])

{{< / highlight >}}
As you see in the first statement we have created our dictionary then we have printed the type of our variable, and finally we have printed the value of the key 'banana',
this is how we access the values in our dictionary.<br/>

In an upcoming tutorials you will learn more about these types (string, list, set, dict).