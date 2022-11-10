# Temporal-LM
Pretrained language models use a vocabulary to translate words into numbers. However, these numbers do not reflect the relationship or connection between words before being fed into deep learning models.

This means that, years in texts will be translated into discrete numerical values, which are indexes in the vocabulary, leading to the ignorance of continuous temporal trend. To be specific, the difference between articles in 1990 and those in 1998 is likely to be the same as the difference between articles in 1990 and those in 1992. Our goal is to find a way of telling language models that articles in 1990 are more similar to those in 1992 than those in 1998.

There are some ways we can try, such as mapping years into special positions in the vocabulary, replacing years by a special encoding schema and so on. For example, we can use four base system to change 1980 into 132330, and split it into 132 and 330. Assuming 132 and 330 refer to [unused1] and [unused2] repectively in the vocabulary, language models then would translate '1980' into '[unused1]','[unused2]'.

In a word, we try to deconstruct the expression of time to make language models aware that time is continuous. The similarity between texts should be inversely related to the gap of their published years. In the following work, we will focus on methods to deconstruct the expression of time and tasks that test whether a language model is time-aware or not.

This idea is inspired by Prof Benyou Wang in School of Data Science, The Chinses University of Hong Kong, Shenzhen. I am a master student in Dept. of Statistics, The London School of Economics and Political Science. Lei XIA, a master student in Dept. of Computer Science, The University of Hong Kong, works on this work together with me.
