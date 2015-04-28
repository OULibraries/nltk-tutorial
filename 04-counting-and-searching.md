---
layout: topic
title: Counting and searching
---

# Counting things

Text as a string can be counted, the length is the number of total characters, including whitespace.

Example:
~~~ {.python}
mytext = len('some text as a string')
print mytext
~~~

Running len() on a string counts characters, on a list of tokens, it counts words.

~~~ {.python}
mytext = ['word1','word2']

len(mytext)
~~~

~~~ {.output}
2
~~~

A simple way to tokenize text is to use the string method `.split()` to split on the character ' ' (space). This is not going to remove punctuation like a more sophisticated tokenizer, but it is a quick and dirty way to go from a string to a tokenized list.

~~~ {.python}
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
~~~ {.python}
fd.<tab>

fd.keys()
fd.values()
fd.items()

fd.keys()[0:10]

%pylab inline
fd.plot()

~~~

## Get length of each word

~~~ {.python}
lengths = [len(w) for w in text6 ]
lenfd = nltk.FreqDist(lengths)
fd.tabulate()
~~~

## Normalizing Text

Removing punctuation.

~~~ {.python}

onlyalpha = [w for w in text6 if w.isalpha()]

fd = nltk.FreqDist(onlyalpha)
fd.plot(10)

~~~

Make all words lowercase

~~~ {.python}

onlylower = [w.lower() for w in onlyalpha]

~~~

Together

~~~ {.python}
onlyalphalower = [w.lower() for wi in text6 if w.isalpha()]
~~~

## Only unique words

Using python sets, analagous to mathematical sets, allowing only one record for each unique item encountered.

~~~ {.python}
set(text6)
~~~

## Stop words

~~~ {.python}
mystops = ['the', 'it','she', 'he']
mycleantext = [w for w in text6 if w not in mystops]

from nltk.corpus import stopwords
stops = stopwords.words('english')
mycleantext = [w for w in text6 if w not in stops]
~~~
