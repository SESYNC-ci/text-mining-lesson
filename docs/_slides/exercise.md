---
---

## Exercises

### Exercise 1

Now that you've learned a bit about extracting strings, try using regex to extract 
money values from the e-mail body content. 

### Exercise 2

We plotted the number of characters in each word above.  Word frequency in a document-term matrix might also be interesting. Try plotting a histogram of the number of times a word appears. 

### Exercise 3

What terms are associated with the word pipeline ("pipelin" after trimming)?  How might you visualize this? 


## Solutions



### Solution 1



~~~r
str_extract_all(content(email), '\\$\\S+\\b') 
~~~
{:title="Solution" .text-document}


~~~
[[1]]
character(0)

[[2]]
character(0)

[[3]]
character(0)

[[4]]
character(0)
~~~
{:.output}


### Solution 2



~~~r
ggplot(words, aes(x = total)) +
       geom_histogram(binwidth = 1)
~~~
{:title="Solution" .text-document}
![ ]({% include asset.html path="images/exercise/unnamed-chunk-3-1.png" %})
{:.captioned}

The frequency of some words isn't very informative.  You can filter by term or by total number of occurrences. 







