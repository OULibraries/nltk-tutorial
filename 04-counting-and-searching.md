---
layout: topic
title: Counting and searching
---

# Counting things

Text as a string can be counted, the length is the number of total characters, including whitespace.

Example:
```
mytext = len('some text as a string')
print mytext
```

Running len() on a string counts characters, on a list of tokens, it counts words.

```

```

A simple way to tokenize text is to use the string method `.split()` to split on the character ' ' (space). This is not going to remove punctuation like a more sophisticated tokenizer, but it is a quick and dirty way to go from a string to a tokenized list.

~~~{.python}
# Simple way to tokenize
tokens = mytext.split(' ')

# More robust, separates punctuation, etc
tokens = nltk.word_tokenize(mytext)

len(tokens)

~~~


## Using NLTK to count things:

fd = nltk.FreqDist(tokens)

This gives us `FreqDist()` object
