---
layout: project
type: project
image: images/stocknews.jpeg
title: Share Market Index Prediction with News Dataset using 1D CNN+RNN
permalink: projects/stocknews
# All dates must be YYYY-MM-DD format!
date: 2020-10-04
labels:
  - Share Market Finance
  - 1D CNN
  - Word Embeddings
  
summary: Predicting the rise or fall value for Stock Market (Dean Jones Industrial Index) Index using 8 years of Reddit News Dataset using 1D CNN + RNN architecture.
---

<br><br>
####Introduction:

Predicting Stock market behavior is a hot topic among the NLP researchers. RNNs, LSTMs, GRUs have proven greatly efficient when dealing with Sequential data. But it turns out that other than RNNs, CNNs too are really effective in extracting features from the text. Although, we can directly feed text to an RNN but there are cases when the sequences are really long which makes it harder to use RNN since they're computationally expensive. 
**In this project, we have used 1D CNN-RNN architecture. The original work behind using 1D CNNs with RNNs was proposed in this paper titled "Combination of Convolutional and Recurrent Neural Network for Sentiment Analysis of Short Texts".**
<br><br>
As an example, consider there are twenty news headlines that run on each day (which is an understatement in the first place considering that the number of headlines is in thousands), it  would be a really long sequence to process with RNN. Training an RNN model on such large sequences will be a massive computational expense. 
<br>
However, we can use 1D CNN as they are really faster and significantly less expensive than RNN. In a 1D CNN architecture, the filter can move only in one direction instead of moving in both two directions (x and y axis) as in 2D convolution.

<br><br>
In this project, I have used a stock market price index data to implement the 1D CNN-RNN architecture. Generally speaking, a stock market index, along with a multitude of other factors, also gets affected by the news headlines that run daily on television and newspapers. Highly negative news impacts the stock market negatively and positive news impacts the stock market positively. Here, I have modeled the relationship between the news and the stock market price of an index.
<br><br>
 **My assumption in modelling the stock price in this exercise is that news headlines that run on a particular day affect the opening stock price of an index the very next morning.** The model architecture is basically built with following two steps,
 
 - Extracting textual features using 1-dimensional CNN
 - Feeding the textual features to an RNN

<br><br>
Following is the architecture diagram for an example sentence taken from the paper mentioned above.<br>
<div class="ui large rounded images">
  <img class="ui image" src="../images/Arch_from_paper.png">
</div>
<br><br>
As can be seen in the above architecture, multiple convolutional layers are applied in parallel to the 'feature representation' of the text. The feature representation of the text can be one-hot encoding or vector representation like word2vec, glove, etc. The output of the multiple convolutional layers are concatenated and RNN layer works on the top of it. 
<br>
As we know, to do any classification or regression, we need the fully-connected layer as the output layer. So, fully-connected layer sits on the top of RNN.<br>
The value that the model should predict is the opening price of the stock market. Since the variable is continuous, it's a regression problem. And therefore, 'softmax' output is not added (as is used for classification and not regression). As a matter of fact, there will be no activation to bound the output.

 ### General flow of a Text related Business Problem:
 
 <div class="ui large rounded images">
  <img class="ui image" src="../images/textmining.png">
</div>
<br><br>

### Approach:
Now, there could be two ways to model the price index based on the news: we could either predict the absolute opening price of the next day, or we could predict the rise or fall in the opening price of the next day based on the previous day.
<br><br>
***Predicting the rise or fall seems more logical in this case since we're trying to analyse the effect of the news on the price index.***
<br><br>

**Preparing Sequences:**
<br><br>
- Change the words present in the headlines into integers,
- Pad the headlines to bring the news of each day to a fixed length.
<br><br>
For each day, there are multiple headlines and each headline has a variable length. Therefore, the padding task was two-fold:
<br>
- For a headline having less than 16 words, append it as it. For a headline that is longer than 16 words, truncate it from the right and append the first 16 words only.
- Combine all the headlines into a single headline and pad it to a length of 200 words in case it is shorter than 200 words. In case it is longer than 200 words, truncate it from the right side.

**HyperParameters:**
<br><br>
The hyperparameters in case of 1D CNN are:

- Filter size (w): It's denoted by 'w' because you can think of the filter as a moving window convolving in one direction over the text.
- Padding size (p)
- Stride (s)
- Pooling size (m)
- Number of filters (k)

### Performance:

The Mean Squared error on the test data compared with predicted values is 0.8%, which is very good. To get a better understanding, on unnormalizing the predicted values, the mean absolute error comes out to be 87.12 while the standard deviation of the test dataset is ~139. This shows the effective performance of our 1D CNN+RNN model.
<br><br>
Finally, I have also picked up some random news headlines from 2017 reddit news, and seen how the index rise/fall evaluates.
