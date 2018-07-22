---
title: "Flow Control"
date: 2018-07-22T12:12:30Z
draft: true
draft: false
author: "Adnan"
share: true
slug: "Flow-Control"
---

In this tutorial you will learn:

1. Python if, elif and else Statement
2. Python for Loop
3. Python while Loop
4. Python break and continue Statement

1 Python if, elif and else Statement:
-------------------------------------
These statements are used when we want to make some decisions in our program to run some codes for a specific condition.
The if statement will first take a test expression and will run the code only if the result of the test expression is True.
Lets see an example on that:

{{< highlight python "linenos=inline,linenostart=0" >}}

user_age = int(input('Please enter you age: '))

if user_age >= 18:
    print("You are an adult")

{{< / highlight >}}

As you see we have created a variable called 'user_age' that will contain the user age after asking him about his age, then we used the if statement followed by a test expression 
that check if the user_age is greater than or equal to 18.
If the test expression (user_age >= 18) is True then the code inside our if body will be executed and print 'You are an adult', but if the test expression is False the code inside 
the if body will not be executed.
Try to run this code and enter different age and see the result.<br/>

If you run the previous code and enter an age that is less than 18 nothing will happen and the program will end, which will looks wierd for the user when he enter his age,
what we want to do now is to add another message that will be printed only when the user is less than 18.
To do that we can use another if statement or the else statement.

{{< highlight python "linenos=inline,linenostart=0" >}}

user_age = int(input('Please enter you age: '))

if user_age >= 18:
    print("You are an adult")

if user_age < 18:
    print("You are a minor")

{{< / highlight >}}

{{< highlight python "linenos=inline,linenostart=0" >}}

user_age = int(input('Please enter you age: '))

if user_age >= 18:
    print("You are an adult")
else:
    print("You are a minor")

{{< / highlight >}}

As you see here when you run the code in both code blocks you will get the same result if you eneter an age less than or greater than 18.
But in the first code block we will first check if the age is greater or equal to 18, if the result is False it will jump to the next if statement and check 
if the user_age is less than 18, so as you see the program has performed two check test the first is (user_age >= 18) and the second is (user_age < 18).<br/>
Now lets see the second code block, we first ask the user his age then we apply a test expression and check if it's True or False, if True the message "You are adult"
will be executed but if it's False automaticaly the message "You are a minor" will be executed and no second check will be run.<br/>

Now lets say we want to add another condition that check if the user age is greater than or equal to 13 and print to the user a message that tells him that he is a teenager.<br/>
To do that we will add the 'elif' statement to our previous code.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}

user_age = int(input('Please enter you age: '))

if user_age >= 18:
    print("You are an adult")
elif user_age >= 13:
    print("You are a teenager")
else:
    print("You are a minor")

{{< / highlight >}}

When your run this code and enter your age the fist condition will check if the user_age is greater or equal to 18 and run the code inside the if body if it's True, nothing new until now, 
if the first test expression is False the second statement (elif) which combine the two statement else and if (else if) will run and check if the 'user_age' is greater than or equal to 13 if 
it's True the message "You are a teenager" will be printed out, if False the message inside the 'else' body will be printed out.<br/>
So lets see clearly what is the diffence between using multiple 'if' statement and 'elif and else' statement.

{{< highlight python "linenos=inline,linenostart=0" >}}

user_age = int(input('Please enter you age: '))

if user_age >= 18:
    print("You are an adult")
if user_age >= 13:
    print("You are a teenager")
if user_age < 13:
    print("You are a minor")

{{< / highlight >}}

When you run this code and enter 35 for the user_age the output will be:<br/>
>>'You are an adult'<br/>
>>'You are a teenager'<br/>

Ooops that's not what we want to print as a message for the user, because he can't be adult and teenager at the same time.<br/>
What caused this error here is the multiple if statement, as i mentioned before when you add multiple if statement the program will pass through them one by one.
So in this example after geting the user input which was (35) the first if statement will check if the value is greater or equal to 18, which is True so the code will run and print 'you are an adult', 
then the second if statement will be executed and check if user_age is greater or equal to 13 which is True because 35 >= 13 and this cause the code inside the second if statement 
to run and print out the message "You are a teenager", then the third if statement will be executed and check if the user_age is less than 13 which is False (35 < 13), so the code inside 
the third if statement body will not be executed.<br/>
On the other hand when we use 'else, elif' statements the code inside the body of both of them will not be executed if the statement that is before them is True.<br/>

2 Python for loop:
--------------------
Imagine that we have list or a sequence that contain alot of items more than 50 or 100 item, how can you go through each item in the list? if we try to access each item using the indexing method 
this will be a nightmare for us. To deal with such thing python provide the 'for' statement which will run through all the list element.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}

#list of numbers
list_of_numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

sum = 0

for number in list_of_numbers:
    sum += number

print("the sum is:", sum)

{{< / highlight >}}

In this example we have created a list of numbers and a variable called 'sum' which we will use it to contain the sum of all the numbers in the list.<br/>
Then we use the 'for' statement to iterate over our sequence (list_of_numbers) followed by the variable 'number' which will contain the current extracted element on every iteration, after that 
we use the 'in' statement followed by the sequence that we want to iterate over it.<br/>
You can name the variable 'number' any name you want, i named it 'number' because it describe its own content.<br/> 
The for statement can be used on other sequence like (string, tuple and dictionary).<br/>
Lets see some examples:<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}

user_info = {'user_name':'mike', 'age':24, 'job':'Full Stack Developer'}

'''
To extract both key and value of a dictionary we have to use .items()
on the dict var.
'''
for key, val in user_info.items():
    print(key,":", val)

#OUTPUT:
'''
>> user_name : mike
>> age : 24
>> job : Full Stack Developer
'''
	
name = 'Mike'
for character in name:
    print(character)
	
#OUTPUT
'''
>> M 
>> i 
>> k
>> e
'''

{{< / highlight >}}

3 Python while loop :
----------------------
While loop is used to repeat a block of code as long as the test expression is True.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}

counter = 0 

while counter < 5:
    print("Hello")
	counter += 1

#OUTPUT
'''
>> Hello
>> Hello
>> Hello
>> Hello
>> Hello
'''
{{< / highlight >}}
As you see we add a test expression after the 'while' statement, then we add the code that we want it to be repeated, here we want to print the word 'Hello' 
then we add 1 to the counter variable to increment it by one on each iteration, if we don't do that the loop will run forever because the test expression will always be True.<br/>

4 Python break and continue Statement :
---------------------------------------
Some time when we are dealing with loops we want to stop or skip the iteration based on some condition, to do that we can use break and continue.<br/>
Lets say that we want to iterate over a string and stop the iteration when we find a specific character, to do that we will specify our test condition then we use the break statement
to stop the loop.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}

var = "Hello World"

for character in var:
    if character == ' ':
	    break
	 print(character)

#OUTPUT
'''
>> H
>> e
>> l 
>> l 
>> o
'''
{{< / highlight >}}
In this code the we iterate over the string 'Hello World' and check if the character is a space if the test expression is True the loop will stop due to the break statement otherwise 
it will print the character.<br/>
Now lets say that we want to iterate over a sequence and we want to skip a specific item in that sequence, to do that we use the continue statement.<br/>

{{< highlight python "linenos=inline,linenostart=0" >}}

var = "MikiMiki"

for character in var:
    if character == 'i':
	    continue
	 print(character)

#OUTPUT
'''
>> M
>> k
>> M 
>> k
'''
{{< / highlight >}}
As you see in this example the test expression is set to check if the current character is 'i' then continue which will skip the rest of the code block go to the next item in the 
sequence.<br/>