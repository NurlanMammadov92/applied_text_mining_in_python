# Assignment 2 - Introduction to NLTK

In part 1 of this assignment you will use nltk to explore the Herman Melville novel Moby Dick. Then in part 2 you will create a spelling recommender function that uses nltk to find words similar to the misspelling. 


## Part 1 - Analyzing Moby Dick



### Example 1

How many tokens (words and punctuation symbols) are in text1?

*This function should return an integer.*



### Example 2

How many unique tokens (unique words and punctuation) does text1 have?

*This function should return an integer.*



### Example 3

After lemmatizing the verbs, how many unique tokens does text1 have?

*This function should return an integer.*



### Question 1

What is the lexical diversity of the given text input? (i.e. ratio of unique tokens to the total number of tokens)

*This function should return a float.*



### Question 2

What percentage of tokens is 'whale'or 'Whale'?

*This function should return a float.*


### Question 3

What are the 20 most frequently occurring (unique) tokens in the text? What is their frequency?

*This function should return a list of 20 tuples where each tuple is of the form `(token, frequency)`. The list should be sorted in descending order of frequency.*



### Question 4

What tokens have a length of greater than 5 and frequency of more than 150?

*This function should return an alphabetically sorted list of the tokens that match the above constraints. To sort your list, use `sorted()`*



### Question 5

Find the longest word in text1 and that word's length.

*This function should return a tuple `(longest_word, length)`.*


### Question 6

What unique words have a frequency of more than 2000? What is their frequency?

"Hint:  you may want to use `isalpha()` to check if the token is a word and not punctuation."

*This function should return a list of tuples of the form `(frequency, word)` sorted in descending order of frequency.*



### Question 7

What is the average number of tokens per sentence?

*This function should return a float.*




### Question 8

What are the 5 most frequent parts of speech in this text? What is their frequency?

*This function should return a list of tuples of the form `(part_of_speech, frequency)` sorted in descending order of frequency.*



## Part 2 - Spelling Recommender

For this part of the assignment you will create three different spelling recommenders, that each take a list of misspelled words and recommends a correctly spelled word for every word in the list.

For every misspelled word, the recommender should find find the word in `correct_spellings` that has the shortest distance*, and starts with the same letter as the misspelled word, and return that word as a recommendation.

*Each of the three different recommenders will use a different distance measure (outlined below).

Each of the recommenders should provide recommendations for the three default words provided: `['cormulent', 'incendenece', 'validrate']`.




### Question 9

For this recommender, your function should provide recommendations for the three default words provided above using the following distance metric:

**[Jaccard distance](https://en.wikipedia.org/wiki/Jaccard_index) on the trigrams of the two words.**

*This function should return a list of length three:
`['cormulent_reccomendation', 'incendenece_reccomendation', 'validrate_reccomendation']`.*



### Question 10

For this recommender, your function should provide recommendations for the three default words provided above using the following distance metric:

**[Jaccard distance](https://en.wikipedia.org/wiki/Jaccard_index) on the 4-grams of the two words.**

*This function should return a list of length three:
`['cormulent_reccomendation', 'incendenece_reccomendation', 'validrate_reccomendation']`.*


### Question 11

For this recommender, your function should provide recommendations for the three default words provided above using the following distance metric:

**[Edit distance on the two words with transpositions.](https://en.wikipedia.org/wiki/Damerau%E2%80%93Levenshtein_distance)**

*This function should return a list of length three:
`['cormulent_reccomendation', 'incendenece_reccomendation', 'validrate_reccomendation']`.*
