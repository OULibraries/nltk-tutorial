---
layout: topic
title: Working with your own text
---



~~~{.python}
import nltk
f = open("46036-0.txt")
data = f.read()
~~~


~~~{.python}
print data[1:100]
~~~


~~~{.python}
gal_tokens = nltk.wordpunct_tokenize(data)
gal_text = nltk.Text(galTokens)
~~~


~~~{.python}
gal_text.concordance("moon")
~~~
