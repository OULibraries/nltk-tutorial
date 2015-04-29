---
layout: topic
title: Working with your own text
---

http://www.gutenberg.org/ebooks/46036?msg=welcome_stranger


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
gal_text = nltk.Text(gal_tokens)
~~~


~~~{.python}
gal_text.concordance("moon")
~~~


~~~{.python}
gal_text.similar("moon")
~~~



~~~.{python}
%matplotlib inline
gal_text.dispersion_plot(["moon", "sun", "stars", "west", "eye"])
~~~


~~~{.python}
gal_text.common_contexts(["moon", "sun",])
~~~