---
layout: project
type: project
image: images/airline1.jpg
title: Airline Information System Chatbot Application
permalink: projects/info_extraction
# All dates must be YYYY-MM-DD format!
date: 2020-10-12
labels:
  - Information Extraction System
  - Named Entity Recognition
  - Chunking
  - CRF
  - Chatbot
summary: A Question answer Chatbot application for a Airline Travel Information System
---

### Problem Statement:
Even though textual data is widely available, the complexity of natural language makes it extremely difficult to extract useful information from text. In this project, I've built an Information Extraction (IE) system application that can extract structured data from unstructured textual data. A key component in information extraction systems is Named-Entity-Recognition (NER). I've used various techniques and models for building NER systems in this projects, as listed later below.
<br><br>
In this project we build a conversational flight-booking system, which can show relevant flights when given a natural-language query such as “Please show me all morning flights from Bangalore to Mumbai on next Monday.” For the system to be able to process this query, it has to extract useful named entities from the unstructured text query and convert them to a structured format, such as the following dictionary/JSON object:
<br><br>
  {source: 'Bangalore', 
  destination: 'Mumbai',
  day: 'Monday', 
  time-of-day: 'morning'}
<br><br>
Using these entities, we could query a database and get all relevant flight results. In this project, I have used Named-Entity Recognition system with I-O-B labels. The building models for the entity recognition are,
<br>
- Rule Based techniques:
  - Regular expression based techniques
  - Chunking
<br>  
- Probabilistic Models:
  - Unigram
  - Naive Bayes Classifier
  - Decision Trees
  - Conditional Random Fields (CRFs)
<br>

### Dataset:
I've used the ATIS (Airline Travel Information Systems) dataset to build an IE system. The ATIS dataset consists of English language queries for booking (or requesting information about) flights in the US.

<br><br>
Please find the complete project @ Source: <a href="https://github.com/akhilsn/Natural_Language_Processing/tree/main/Airline%20Travel%20Information%20System%20Chatbot"><i class="large github icon"></i>akhilsn/Gesture Recognition</a>
<br><br>

### Approach:
Our objective is to **build an information extraction system** which can extract entities relevant for booking flights (such as source and destination cities, time, date, budget constraints etc.) in a **structured format** from a given user-generated query.

A structured format could be a dictionary, a JSON, etc. - basically anything that can be parsed and used for looking up relevant flights from a database.

#### About Information Extraction:

**Information Extraction (IE)** refers to the task of extracting structured information from unstructured text data. In this case, we want to extract all pieces of information from a query which are useful in making a flight reservation, such as source and destination cities, date of travel, price range etc. 

Other examples of IE tasks are extracting information about stock market announcements from financial news (which could be useful for predicting stock prices etc.), extracting structured information from large corpora of documents such as encyclopedias, government documents etc.

Most IE tasks start with the task of **Named Entity Recognition (NER)** - identifying mentions of *entities* in the text. The general process of information extraction is described below.

#### Information Extraction Pipeline

A generic IE pipeline schema, is shown below.
<br>
<div class="ui large rounded images">
  <img class="ui large right floated rounded image" src="../images/ie-architecture.png">
</div>
<br><br>
#### Preprocessing 

The usual preprocessing steps are - if the raw input data is in the form of paragraphs, it is converted into sentences using a **sentence segmenter**, then broken down into tokens using **tokenisation**, and finally each token is **POS tagged**.

#### Models for Entity Recognition

I've built a variety of models for entity recognition, i.e. to predict the sequence of IOB tag of words. We'll try the two broad approaches - **rule-based models** and **probabilistic models**.

### Results:

**Rule Based**.<br>
-ChunkParse score:
  - IOB Accuracy:  65.2%%
  - Precision:     31.7%%
  - Recall:        40.9%%
  - F-Measure:     35.7%%
  
**UnigramChunker**:<br>
-ChunkParse score:
  - IOB Accuracy:  66.3%%
  - Precision:     37.5%%
  - Recall:        18.5%%
  - F-Measure:     24.8%%
  
**BigramChunker:**<br>
-ChunkParse score:
  - IOB Accuracy:  70.6%%
  - Precision:     43.5%%
  - Recall:        38.8%%
  - F-Measure:     41.0%%
 
**Naive Bayes:**<br>
-ChunkParse score:
  - IOB Accuracy:  91.7%%
  - Precision:     75.9%%
  - Recall:        85.1%%
  - F-Measure:     80.3%%
<br>*Significant improvement here over basic Unigram/Bigram Chunkers.*

**Decision Tree:**<br>
-ChunkParse score:
  - IOB Accuracy:  94.9%%
  - Precision:     83.9%%
  - Recall:        87.2%%
  - F-Measure:     85.5%%
  
 **CRF:**<br>
The state of the art are found on using CRFs that gives an overall f1-score of about 93% on the test folds and 97% on training folds. 
