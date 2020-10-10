---
layout: project
type: project
image: images/spellcheck.jpg
title: 1. Spelling Corrector Application
permalink: projects/spellingcorrectorapp
# All dates must be YYYY-MM-DD format!
date: 2020-06-15
labels:
  - Natural Language Processing
  - Lexical Processing
  - Edit Distances
summary: An advanced Lexical Processing based application - Spelling Corrector using Laventein Minimum Edit Distance technique. A ready to use app for spelling correction on english text data.
---

<img class="ui medium right floated rounded image" src="../images/vacay-home-page.png">

In Natural Language Processing, some of the basic lexical processing techniques that we often use are removing stop words, tokenisation, stemming and lemmatization. These preprocessing steps are applicable in almost every text analytics application.
Even after going through all these preprocessing steps, a lot of noise could still be present in the data. For example, spelling errors which happen by mistake as well as by choice (informal words such as 'lol', 'awsum' etc.). Misspellings need to be corrected in order to stem or lemmatize efficiently. The problem of misspellings is so common these days, especially in text data from social media, that it makes working with text extremely difficult, if not dealt with.
To handle such situations, here I have built a Spell Correction application where all the misspelt words will be canonicalised to the base form, which would be the correct spelling of that word, and use Minimum edit distance technique. 
<br><br>
An **edit distance** is a distance between two strings which is a non-negative integer number.
<br><br>An edit operation can be one of the following:
- Insertion of a letter in the source string. e.g., to convert ‘color’ to ‘colour’, we need to insert the letter ‘u’ in the source string.
- Deletion of a letter from the source string. e.g., to convert ‘Matt’ to ‘Mat’, we need to delete one of the ‘t’s from the source string.
- Substitution of a letter in the source string. e.g., to convert ‘Iran’ to ‘Iraq’, yweou need to substitute ‘n’ with ‘q’.

<br><br>The seed document ‘big.txt’ is nothing but a book. It’s the book ‘The Adventures of Sherlock Holmes’ present in text format at project Gutenberg’s website. 

In this application, I have created one edit and two edits based spelling corrections. The edits_one() function creates all the possible words that are one edit distance away from the input word. Most of the words that this function creates are garbage, i.e. they are not valid English words. For example, if I pass the word ‘laern’ (misspelling of the word ‘learn’) to edits_one(), it will create a list where the word ‘lgern’ will be present since it is an edit away from the word ‘laern’. But it’s not an English word. Only a subset of the words will be actual English words.
Similarly, the edits_two() function creates a list of all the possible words that are two edits away from the input word. Most of these words will also be garbage.
 
For the complete code, please refer to the code at Source: <a href="hhttps://github.com/akhilsn/Python-Applications/tree/master/Spell_Corrector"><i class="large github icon"></i>akhilsn/spellcorrectionapp</a>
