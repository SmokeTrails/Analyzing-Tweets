# Analyzing Tweets!

The main question that me and my group were interested in answering was if you could use the content of
a tweet i.e. what words and phrases are used to predict the number of followers a tweeter has. We
found that this question was difficult to solve as there isn’t an obvious answer as to what types of
words a person with a high number of followers would use compared to a person with a low
number of followers.

We extracted 2000 tweets from the Twitter API with 2 features – the content of the tweet and the number
of followers the user had. The only thing we specified in the search parameters is that we wanted
to exclude retweets.

Some of the properties of our data are that we had a mean of 580 followers, and in addition, we
decided to split the number of followers into 3 groups – low (0 to 1000), medium (1001 to
10000), and high (> 10000), and we created a new categorical variable to represent this. Our data
had 1567 medium number of followers, 81 people with a high number, and 452 with a low
number.

We decided to use the Naïve Bayes Model to answer our research question. This is a supervised
model, and it works by splitting the classifying label based on what the probability is that it
is the true label. Some of the strengths of this model are that it is fast and easy to use, however, a
weakness, which we also fell into, is that it can perform poorly if the training dataset is not evenly
split up into the different labels. We decided to evaluate our model based on its accuracy.

When we ran our model, we had a testing accuracy of 75.5%, however, unfortunately our model
always predicted a medium number of followers as the label as this was the majority label in the
dataset. This means that our results are not significant and we can’t really draw any meaningful
conclusions, since our accuracy only represents the proportion of the majority label, and not the
accuracy of the model. If we had more time, we would spend significantly more time in refining
our data before we decide to put it through a model. We would do this by firstly attempting to
collect a larger number of observations, as well as to split the data into the training set in a way
that is representative of the overall dataset.

This project was completed using the Python programming language. Some of the libraries we used were:

- `NLTK` (Natural Language Toolkit)
- `pandas`
- `numpy`
- `scikit-learn`

The code used to complete this project can be found on this repository.
