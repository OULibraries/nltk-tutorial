---
layout: topic
title: Counting and searching
---

# Counting things

Text as a string can be counted, the length is the number of total characters, including whitespace.

Example:
~~~{.python}
mytext = len('some text as a string')
print mytext
~~~

Running len() on a string counts characters, on a list of tokens, it counts words.

~~~{.python}
mytext = ['word1','word2']

len(mytext)
2
~~~

A simple way to tokenize text is to use the string method `.split()` to split on the character ' ' (space). This is not going to remove punctuation like a more sophisticated tokenizer, but it is a quick and dirty way to go from a string to a tokenized list.

~~~{.python}
# Simple way to tokenize
tokens = mytext.split(' ')

# More robust, separates punctuation, etc
tokens = nltk.word_tokenize(mytext)

len(tokens)
~~~


## Using NLTK to count things:

~~~{.python}
mystring = "It was the best of times, it was the worst of times"
tokens =
fd = nltk.FreqDist(tokens)
~~~

This gives us `FreqDist()` object

We can use this `fd` object now to look at the specifics of the frequency distribution of a text.
~~~{.python}
fd.<tab>

fd.keys()
fd.values()
fd.items()

fd.keys()[0:10]

%pylab inline
fd.plot()
~~~
