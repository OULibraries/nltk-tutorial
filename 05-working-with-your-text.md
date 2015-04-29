---
layout: topic
title: Working with your own text
---

http://www.gutenberg.org/ebooks/46036?msg=welcome_stranger


~~~{.python}
import nltk
f = open("46036-0.txt")
gal_raw = f.read()
~~~


~~~{.python}
print gal_raw[1:100]
len(gal_raw)
~~~


~~~{.python}
gal_tokens = nltk.wordpunct_tokenize(gal_raw)
print gal_tokens[0:100]
len(gal_tokens)
~~~

~~~{.python}
gal_text = nltk.Text(gal_tokens)
print gal_text
len(gal_text)
~~~


~~~{.python}
gal_text.concordance("moon")
~~~


~~~{.python}
gal_text.similar("moon")
~~~

~~~{.python}
gal_text.count("sun")

gal_text.count("moon")
~~~







~~~.{python}
%matplotlib inline
gal_text.dispersion_plot(["moon", "sun", "stars", "west", "eye"])
~~~


~~~{.python}
gal_text.common_contexts(["moon", "sun",])
~~~

~~~{.python}
gal_text.collocations()
~~~


~~~{.python}
sorted(set(gal_text))
~~~

