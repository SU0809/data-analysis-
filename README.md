SOCIAL MEDIA SENTIMENT ANALYSIS
Summary
From the given dataset we were able to predict on which class i.e Positive or Negative does the given tweet fall into.The following data was collected from Analytics Vidhya's site.
Pre-processing
Removing Twitter Handles(@user)
Removing puntuation,numbers,special characters
Removing short words i.e. words with length<3
Tokenization
Stemming
Data Visualisation
Wordclouds
Barplots
Word Embeddings used to convert words to features for our Machine Learning Model
Bag-of-Words
TF-IDF
Machine Learning Models used
Logistic Regression
XGBoost
Decision Trees
Evaluation Metrics
F1 score
sns.countplot(train_original['label'])
sns.despine()

Why use F1-Score instead of Accuracy ?
From the above countplot generated above we see how imbalanced our dataset is.We can see that the values with label:0 i.e. positive sentiments are quite high in number as compared to the values with labels:1 i.e. negative sentiments.

So when we keep accuracy as our evaluation metric there may be cases where we may encounter high number of false positives.

Precison & Recall :-
Precision means the percentage of your results which are relevant.

Recall refers to the percentage of total relevant results correctly classified by your algorithm met

We always face a trade-off situation between Precison and Recall i.e. High Precison gives low recall and vice versa.

In most problems, you could either give a higher priority to maximizing precision, or recall, depending upon the problem you are trying to solve. But in general, there is a simpler metric which takes into account both precision and recall, and therefore, you can aim to maximize this number to make your model better. This metric is known as F1-score, which is simply the harmonic mean of precision and recall.

f1

So this metric seems much more easier and convenient to work with, as you only have to maximize one score, rather than balancing two separate scores.
