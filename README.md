# Temporal-LM
Pretrained language models use a vocabulary to translate words into numbers. However, these numbers do not reflect the relationship between words before being fed into deep learning models.

This point is important because years mentioned in texts have no difference from other words, leading to the ignorance of continuous temporal trend. To be specific, the difference between articles in 1990 and those in 1998 is likely to be the same as the difference between articles in 1990 and those in 1992. Our goal is to find a way of telling language models that articles in 1990 are more similar to those in 1992 than those in 1998.

There are some ways we can try, such as mapping years into special positions in the vocabulary, replacing years by a special encoding schema and so on. For example, we can use four base system to change 1980 into 132330, and split it into 132 and 330. Assuming 132 and 330 refer to [unused1] and [unused2] repectively in the vocabulary, language models then would translate '1980' into '[unused1]','[unused2]'.

Above methods try to deconstruct the expression of time
discrete numerical values

We want to replace year by a soecial encoding schema 
