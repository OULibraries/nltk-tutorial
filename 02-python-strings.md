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


```
mystring = "The quick brown fox jumped over the lazy dog"
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

### Chaining

```
mystring.count('i')
1

mystring.lower().count('i')
2
```


## Lists


```
mylist = [1,2,3,4]

otherlist = ['a','b','c',1,2,3]

```

Lists can have heterogeneous data types. The data types of each element do not have to be the same. So a list is a way to organize a collection of things. List items can be any python object. In the example above our lists contained integers and a mix of integers and single character strings.

We can turn a string of words into a list using the `.split()` method.

```

mystring = 'The quick brown fox jumped over the lazy dog'
mystring.split(' ')

mytokens = mystring.split(' ')
```

## Tokenizing

NLTK contains a better tokenizer

```
newtokens = nltk.word_tokenize('''This is a sentence full of tokens, by tokenizing the string, I can make a list of the tokens''')

print newtokens
['This',
 'is',
 'a',
 'sentence',
 'full',
 'of',
 'tokens',
 ',',
 'by',
 'tokenizing',
 'the',
 'string',
 ',',
 'I',
 'can',
 'make',
 'a',
 'list',
 'of',
 'the',
 'tokens']
 ```



## Slicing

~~~{.python}
firstword = sentence[0:2]

firstword = sentence[:2]

last = sentence[:-1]

lastword = sentence[-4:]
~~~


We can slice parts of a list out using a special notation. We use a pair of square brackets `[]` and a range of values we'd like to extract from the list.

```
newtokens[0:4]
```

Start at index zero and go up to but not including index 4.
