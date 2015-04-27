---
layout: topic
title: Getting python installed
---





## Lists and Loops


~~~{.python}
names = ['Turing', 'Hopper', 'Babbage', 'Lovelace', 'Hamilton']
~~~


~~~{.python}
names[0]
names[3]
names[-1]
~~~


~~~{.python}

for person in names :
   print person

~~~


## Strings


~~~{.python}
sentence = "The quick brown fox jumps over the lazy dog."
~~~


### Some useful string functions

~~~{.python}
sentence.lower()
len(string)

~~~


### Unicode: Here be dragons

~~~{.python }
snakes = ['蟒蛇', 'الثعبان', 'питон']

snakes[0]

print snakes[1]
~~~

## Slicing

~~~{.python}
firstword = sentence[0:2]

firstword = sentence[:2]

last = sentence[:-1]

lastword = sentence[-4:]





~~~





## Tokenizing

~~~
sentence.split()



~~~
