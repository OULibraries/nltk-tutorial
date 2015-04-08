---
layout: topic
title: NLTK Overview
---
## What is NLTK

## Importing the NLTK toolkit

```
import nltk
```

What does this do? Python uses import as a way to include *libraries* into the current *namespace*. This just makes it available to us to refer to, so that python knows where to find it.

## Getting some text loaded

The NLTK library comes with a tool that can help us to download various texts and corpora that can be used as references for various kinds of Natural Language processing.

```
nltk.download()
```

Select "All Packages" and click Download

## We now have data

```
from nltk.book import *
```

This imports a bunch of full-texts of various books, Moby Dick, Sense and Sensibility, The Book of Genesis etc, Inaugural Address Corpus etc. This provides a convenient way for us to begin testing some NL concepts in Python.

The variables `text1` ... `textn` are special data objects containing a data structure (much like a list) that `nltk` tools know how to use.

## 

## Concordance

```
text1.concordance("Whale")

Displaying 25 of 1226 matches:
s , and to teach them by what name a whale - fish is to be called in our tongue
t which is not true ." -- HACKLUYT " WHALE . ... Sw . and Dan . HVAL . This ani
ulted ." -- WEBSTER ' S DICTIONARY " WHALE . ... It is more immediately from th
ISH . WAL , DUTCH . HWAL , SWEDISH . WHALE , ICELANDIC . WHALE , ENGLISH . BALE
HWAL , SWEDISH . WHALE , ICELANDIC . WHALE , ENGLISH . BALEINE , FRENCH . BALLE
least , take the higgledy - piggledy whale statements , however authentic , in
 dreadful gulf of this monster ' s ( whale ' s ) mouth , are immediately lost a
 patient Job ." -- RABELAIS . " This whale ' s liver was two cartloads ." -- ST
 Touching that monstrous bulk of the whale or ork we have received nothing cert
 of oil will be extracted out of one whale ." -- IBID . " HISTORY OF LIFE AND D
ise ." -- KING HENRY . " Very like a whale ." -- HAMLET . " Which to secure , n
restless paine , Like as the wounded whale to shore flies thro ' the maine ." -
. OF SPERMA CETI AND THE SPERMA CETI WHALE . VIDE HIS V . E . " Like Spencer '
t had been a sprat in the mouth of a whale ." -- PILGRIM ' S PROGRESS . " That
EN ' S ANNUS MIRABILIS . " While the whale is floating at the stern of the ship
e ship called The Jonas - in - the - Whale . ... Some say the whale can ' t ope
 in - the - Whale . ... Some say the whale can ' t open his mouth , but that is
 masts to see whether they can see a whale , for the first discoverer has a duc
 for his pains . ... I was told of a whale taken near Shetland , that had above
oneers told me that he caught once a whale in Spitzbergen that was white all ov
2 , one eighty feet in length of the whale - bone kind came in , which ( as I w
n master and kill this Sperma - ceti whale , for I could never hear of any of t
 . 1729 . "... and the breath of the whale is frequendy attended with such an i
ed with hoops and armed with ribs of whale ." -- RAPE OF THE LOCK . " If we com
contemptible in the comparison . The whale is doubtless the largest animal in c
```

This performs an analysis of the context of the word "whale" within the text of the novel Moby Dick. It shows us the first 25 time the word occured

If we want to know more about the function `concordance()` we can access some online help.

```
?text1.concordance

Type:        instancemethod
String form: <bound method Text.concordance of <Text: Moby Dick by Herman Melville 1851>>
File:        /Users/jduckles/lib/python2.7/site-packages/nltk/text.py
Definition:  text1.concordance(self, word, width=79, lines=25)
Docstring:
Print a concordance for ``word`` with the specified context window.
Word matching is not case-sensitive.
:seealso: ``ConcordanceIndex``
```

We can see in the line labeld Definition that the function `concordance()` takes three parameters, a word of interest, a width of output context and a number of lines to show.

## Challenge {.challenge}

Using Moby Dick `text1`, see if you can do the following:

-	What would we do to show 100 lines?
-	30 columns of context?
-	All lines with Whale?

## Other analysis

```
text1.similar('whale')


ship boat sea time captain deck world man pequod other whales air crew head water line thing side way wind

```
