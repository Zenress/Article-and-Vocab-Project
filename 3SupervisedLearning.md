# Supervised learning

- [Supervised learning](#supervised-learning)
  - [What is supervised learning?](#what-is-supervised-learning)
  - [How does supervised learning work?](#how-does-supervised-learning-work)
  - [Benefits and limitations](#benefits-and-limitations)
  - [Classification algorithms](#classification-algorithms)
  - [Regression models](#regression-models)

## What is supervised learning?

Supervised learning is one of the major sub catagories to Machine learning. Supervised learning is characterized by using labeled datasets to train a given algorithm to predict og categorize something.

## How does supervised learning work?

Like mentioned above, supervised learning works by using a labeled dataset. This means it tries to find the pattern for getting to the answer that the given label is. This way, when it sees data it hasn't seen before, it can use the pattern to predict what the answer will be, or categorize it.

For a supervised model you need to have a label for each row/record of data. This means that you basically have to have the answer that you want it to figure out the pattern for.

This means that supervised learning is especially good for classification and regression problems. I.e figuring out what category a news article belongs to, or predicting the volume of sales for a given date or upcoming year.

## Benefits and limitations

As you can see, there are a lot of positive things about supervised learning. But don't get too excited yet, as there are some important limitations as well as considerations that need to be made.

For one, training data needs to be balanced and cleaned. Garbarge, duplicate og irrelevant columns will skew the results, and therefore the algorithms will be less accurate. This means that the AI's understanding of the pattern will be greatly limited or just plain wrong.

Another one is the amount of data and the spread of it. With lower amounts of data you will not give the algorithms enough time to understand the pattern behind why the labels are like they are. With a smaller spread you will have problems with the algorithms being very narrow in the range it can predict or categorize, meaning it would be extremely bad at handling unknown data because it is far to tuned for the data you trained it on

Accuracy, making the AI too accurate on the data will also make it biased towards that data. Just like the case above.

This one isn't as much a limitation, it's more of a pitfall users can fall into without being none the wiser. That is the pitfall of choosing a bad supervised learning algorithm for your specific case. Deep learning algorithms can become insanely accurace without hitting the limitations above, the problem is that it takes more resources than most cases need. As well as the fact that most people don't need such an accurate model, especially if it takes a while to train to get that amount of accuracy. Therefore it's a good idea to consider what algorithms to use and keeping in mind what your usecase is. Don't go for a top of the line algorithm just because the results are good, think about what you need the model for.

Generally there are primarily 2 kinds of results people use supervised learning for. Classification and regression, below i'll introduce some algorithms. Just remember to think about your usecase

## Classification algorithms

- spam recognition
- sentiment analysis
- decision tree classifier
- binary decision tree

## Regression models

- linear regression
- logistic regression
- neural networks
- linear discriminant analysis
- decision trees
- similarity learning
- Bayseian logic
- support vector machines (SVMs)
- random forests
