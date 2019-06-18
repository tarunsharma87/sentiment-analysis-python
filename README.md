##Context
Opinion mining (sometimes known as sentiment analysis or emotion AI) refers to the use of natural language processing, text analysis, computational linguistics, and biometrics to systematically identify, extract, quantify, and study affective states and subjective information. > Source: https://en.wikipedia.org/wiki/Sentiment_analysis

##Content
This dataset was created for the Paper 'From Group to Individual Labels using Deep Features', Kotzias et. al,. KDD 2015

It contains sentences labelled with a positive or negative sentiment.

###Format:

sentence score

###Details:

***Score is either 1 (for positive) or 0 (for negative)***
The sentences come from three different websites/fields:

imdb.com amazon.com yelp.com

For each website, there exist 500 positive and 500 negative sentences. Those were selected randomly for larger datasets of reviews. We attempted to select sentences that have a clearly positive or negative connotaton, the goal was for no neutral sentences to be selected.

**Amazon**: contains reviews and scores for products sold on amazon.com in the cell phones and accessories category, and is part of the dataset collected by McAuley and Leskovec. Scores are on an integer scale from 1 to 5. We considered reviews with a score of 4 and 5 to be positive, and scores of 1 and 2 to be negative. We randomly partitioned the data into two halves of 50%, one for training and one for testing, with 35,000 documents in each set.

**IMDb**: refers to the IMDb movie review sentiment dataset originally introduced by Maas et al. as a benchmark for sentiment analysis. This dataset contains a total of 100,000 movie reviews posted on imdb.com. There are 50,000 unlabeled reviews and the remaining 50,000 are divided into a set of 25,000 reviews for training and 25,000 reviews for testing. Each of the labeled reviews has a binary sentiment label, either positive or negative. In our experiments, we train only on the labelled part of the training set.

**Yelp**: refers to the dataset from the Yelp dataset challenge from which we extracted the restaurant reviews. Scores are on an integer scale from 1 to 5. We again considered reviews with scores 4 and 5 to be positive, and 1 and 2 to be negative. We randomly generated a 50-50 training and testing split, which led to approximately 300,000 documents for each set. Sentences: for each of the datasets above, we extracted and manually labeled 1000 sentences from the test set, with 50% positive sentiment and 50% negative sentiment. These sentences are only used to evaluate our instance-level classi- fier for each dataset3. They are not used for model training, to maintain consistency with our overall goal of learning at a group level and predicting at the instance level.
