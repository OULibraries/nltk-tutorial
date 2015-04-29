---
layout: topic
title: Bonus material
---


## Web accesible text


We can bring down text just by knowing the text's URL.

~~~ {.python}
import nltk
from urllib import urlopen
url = "https://www.gutenberg.org/cache/epub/1998/pg1998.txt"
text = urlopen(url)
raw = text.read().decode('utf-8')
type(raw)
len(raw)

thusspoke = nltk.Text(nltk.word_tokenize(raw))

~~~
