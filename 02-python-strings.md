---
layout: topic
title: Python Strings
---

## Variables

## Lists 

Lists are one of the most basic ways that we structure and organize information.

They're also one of the most common ways to structure data in Python.


~~~{.python}
names = ['Turing', 'Hopper', 'Babbage', 'Lovelace', 'Hamilton']

numlist = [1,2,3,4]

~~~

Unline some other programming languages, list can contain mixed types
of things. They're just an ordered sequence of stuff.

~~~{.python}
mixedlist = ['a','b','c',1,2,3]
~~~

We can select individual pieces of our lists

~~~{.python}
names[0]
names[3]
names[-1]
~~~

we can slice out sublists from them

~~~{.python}
mixedlist[0:2]

mixedlist[3:-1]

mixedlist[3:]

~~~

we can count the items in a list

~~~{.python}
len(names)

len(mixlist[0:2])
~~~



And we can use loops to do something to all the tiems in a list. 


~~~{.python}
for person in names :
   print person
~~~




## Strings

Strings are a construct in Python that represent an ordered sequence of characters.
Characters include letters, numbers, whitspace, and punctuation.

~~~{.python}
sentence = "The quick brown fox jumped over the lazy dog."
~~~

They have a lot in common with lists.

You can pull out individual items in a string using indexes.


~~~{.python}
sentence[0]
sentence[-1]
~~~

You can use slicing to make substrings


~~~{.python}
firstword = sentence[0:2]
lastword = sentence[-4:0]
~~~


You can count the characters in a string

~~~{.python}
len(sentence)
~~~


and you can loop over the characters

~~~{.python}
for letter in sentence:
  print letter
~~~






### Strings know how to do lots of things

Strings in Python are objects.

Objects, in this context, are just a way for Python to group some data together with a bunch of actions that can be perfomed on that data. 

~~~{.python}
mystring = 'I am a string'

mystring.<tab>
~~~


mystring.capitalize  mystring.expandtabs  mystring.isdigit     mystring.ljust       mystring.rindex      mystring.splitlines  mystring.upper
mystring.center      mystring.find        mystring.islower     mystring.lower       mystring.rjust       mystring.startswith  mystring.zfill
mystring.count       mystring.format      mystring.isspace     mystring.lstrip      mystring.rpartition  mystring.strip
mystring.decode      mystring.index       mystring.istitle     mystring.partition   mystring.rsplit      mystring.swapcase
mystring.encode      mystring.isalnum     mystring.isupper     mystring.replace     mystring.rstrip      mystring.title
mystring.endswith    mystring.isalpha     mystring.join        mystring.rfind       mystring.split       mystring.translate
```

~~~{.python}
mystring.lower()
~~~
~~~{.result}
'i am a string'
~~~

~~~{.python}
mystring.upper()
~~~
~~~{.result}
'I AM A STRING'
~~~

~~~{.python}
mystring.count('a')
~~~
~~~{.output}
2
~~~


~~~{.python}
one_string = "one fish"
two_string = "two fish"

print one_string +", " + two_String
~~~
~~~{.output}
one fish, two fish
~~~




~~~{.python}
mystring.isalpha();
sentence.isalpha();
~~~


### Chaining Methods

~~~{.python}
mystring.count('i')
~~~
~~~{.output}
1
~~~

~~~{.python}
mystring.lower().count('i')
~~~
~~~{.output}
2
~~~


### Spliting a string in to tokens


We can turn a string of words into a list using the `.split()` method.

~~~{.python}

sentence.split(' ')
mytokens = sentence.split(' ')
~~~
