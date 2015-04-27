---
layout: topic
title: Getting python installed
---

## Lists and Loops


~~~{.python}
names = ['Turing', 'Hopper', 'Babbage', 'Lovelace', 'Hamilton']

numlist = [1,2,3,4]

mixedlist = ['a','b','c',1,2,3]
~~~

Lists can have heterogeneous data types. The data types of each
element do not have to be the same. So a list is a way to organize a
collection of things. List items can be any python object. In the
example above our lists contained integers and a mix of integers and
single character strings.



~~~{.python}
names[0]
names[3]
names[-1]
~~~



~~~{.python}
for person in names :
   print person
~~~


### Slicing a list

~~~{.python}
mixedlist[0:2]

mixedlist[3:-1]

mixelist[3:]

~~~



## Strings

```
sentence = "The quick brown fox jumped over the lazy dog."
```


Strings are objects that have methods, we can call those methods to manipulate our string.

```
mystring = 'I am a string'

mystring.<tab>
mystring.capitalize  mystring.expandtabs  mystring.isdigit     mystring.ljust       mystring.rindex      mystring.splitlines  mystring.upper
mystring.center      mystring.find        mystring.islower     mystring.lower       mystring.rjust       mystring.startswith  mystring.zfill
mystring.count       mystring.format      mystring.isspace     mystring.lstrip      mystring.rpartition  mystring.strip
mystring.decode      mystring.index       mystring.istitle     mystring.partition   mystring.rsplit      mystring.swapcase
mystring.encode      mystring.isalnum     mystring.isupper     mystring.replace     mystring.rstrip      mystring.title
mystring.endswith    mystring.isalpha     mystring.join        mystring.rfind       mystring.split       mystring.translate
```

```
mystring.lower()
'i am a string'
```

```
mystring.upper()
'I AM A STRING'
```

```mystring.count('a')
2
```


### Slicing a string


firstword = sentence[0:2]
lastword = sentence[-4:0]



### Chaining Methods

```
mystring.count('i')
1

mystring.lower().count('i')
2
```



We can turn a string of words into a list using the `.split()` method.

```

mystring = 'The quick brown fox jumped over the lazy dog'
mystring.split(' ')

mytokens = mystring.split(' ')
```
