# Supervised learning

- [Supervised learning](#supervised-learning)
  - [What is supervised learning?](#what-is-supervised-learning)
  - [How does supervised learning work?](#how-does-supervised-learning-work)
  - [Benefits and limitations](#benefits-and-limitations)
    - [Data Balance and cleanness](#data-balance-and-cleanness)
    - [Data amount and spread](#data-amount-and-spread)
    - [Accuracy](#accuracy)
    - [Usecase](#usecase)
  - [Classification algorithms](#classification-algorithms)
    - [Decision Tree Classifier](#decision-tree-classifier)
    - [K-nearest neighbor](#k-nearest-neighbor)
    - [Naive Bayes](#naive-bayes)
  - [Regression models](#regression-models)
    - [Linear Regression](#linear-regression)
    - [Logistic Regression](#logistic-regression)
    - [Random Forests](#random-forests)

## What is supervised learning?

Supervised learning is one of the major sub catagories to Machine learning.
Supervised learning is characterized by using labeled datasets to train a given algorithm to predict og categorize something.

## How does supervised learning work?

Like mentioned above, supervised learning works by using a labeled dataset.
This means it tries to find the pattern for getting to the answer that the given label is.
This way, when it sees data it hasn't seen before, it can use the pattern to predict what the answer will be, or categorize it.

For a supervised model you need to have a label for each row/record of data.
This means that you basically have to have the answer that you want it to figure out the pattern for.

This means that supervised learning is especially good for classification and regression problems.
I.e figuring out what category a news article belongs to, or predicting the volume of sales for a given date or upcoming year.

## Benefits and limitations

As you can see, there are a lot of positive things about supervised learning.
But don't get too excited yet, as there are some important limitations as well as considerations that need to be made.

### Data Balance and cleanness

Training data needs to be balanced and cleaned.
Garbarge, duplicate og irrelevant columns will skew the results, and therefore the algorithms will be less accurate.
This means that the AI's understanding of the pattern will be greatly limited or just plain wrong.

### Data amount and spread

With lower amounts of data you will not give the algorithms enough time to understand the pattern behind why the labels are like they are.
With a smaller spread you will have problems with the algorithms being very narrow in the range it can predict or categorize.
Meaning it would be extremely bad at handling unknown data, because it is far to tuned for the data you trained it on

### Accuracy

Making the AI too accurate on the data will also make it biased towards that data.
Just like the case above.

### Usecase

This one isn't as much a limitation, it's more of a pitfall users can fall into without being none the wiser.
That is the pitfall of choosing a bad supervised learning algorithm for your specific case.

Deep learning algorithms can become insanely accurace without hitting the limitations above, the problem is that it takes more resources than most cases need.
As well as the fact that most people don't need such an accurate model, especially if it takes a while to train to get that amount of accuracy.
Therefore it's a good idea to consider what algorithms to use and keeping in mind what your usecase is.
Don't go for a top of the line algorithm just because the results are good, think about what you need the model for.

Generally there are primarily 2 kinds of results people use supervised learning for.
Classification and regression, below i'll introduce some algorithms.
Just remember to think about your usecase

## Classification algorithms

This section is for the algorithms that classify something by predicting which class the values you entered are.
Classes could be e.g positive and negative for Sentiment Analysis

Classification problems to solve can often be broadly split into two categories: Binary classification problems and multi-calss classification.

For Binary classification, you can only predict whether something is one or the other.
You can only predict two possible things at all times.

In Multi-class classification you can predict multiple classes as the name suggests.

### Decision Tree Classifier

Is an algorithm that functions by making a yes/no (e.g., bigger than/less than) condition that continually split the dataset until it finds a sequence of nodes that points to a class in your dataset.
It repeats the process until conditions that point to your classes are done.

**Usecase:** It's simple, fast and robust.
Works well and is most often just the best algorithm to implement in many cases.

### K-nearest neighbor

Is an algorithm that works by grouping datapoints by proximity to eachother and in turn creating groupings.
Classifying something using this algorithm involves it figuring out how many datapoints of each class are in it's proximity.
Thereby taking the most common class in the proximity and saying that is the class of what you are trying to classify.

**Usecase:** A sample usecase could be that you have a lot of datapoints that are labeled with classes, but a couple that aren't, using k-nearest neighbor on the ones that aren't labeled allows you to label them.

### Naive Bayes

Is an algorithm that works by using a group of simple probability classifiers and applying that together with Bayes theorem.

**Usecase:** Naive Bayes classifiers are really scalable, this means that for really big classification problems, this algorithm might be the better options.

## Regression models

This section is for algorithms that fit under the Regression umbrella, this means that these algorithm generally work by plotting a line of best fit through datapoints.
Also called Predictive analysis

### Linear Regression

One of the most common algorithms to be used for Regression.
This algorithm works by modelling the relationship between two variables and estimating the response using a line-of-best-fit.

This in turn allows you to predict on something in the future because this line of best fit extends infinitely.
It does get more inaccurate the longer away from the datapoints that you predict.
So let's say you want to predict gas prices in 2 years, 5 years and 20 years.
The accuracy will be vastly lower on the 20 year one vs 5 years or even 2 years.

**Usecase:** The usecase for linear regression is very simple, it's fast and easy for predicting future values.
The problems are that it might not fit what you want to do, and you might need a Logistic Regression instead maybe.

### Logistic Regression

In it's most simple form this algorithm is binary.
However it can become more complicated when you add more values it can output.
Logistic regression works by having a threshold for when it should round up or down to one class or another.
For multiple values this means that you would have more thresholds.

**Usecase:** For example if you want to check if something is spam.
It doesn't help if you say something is 40% chance for a spam, you want to know if it's spam or not.
So with logistic regression it would tell you 0 or 1, meaning either spam or not(for binary logistic regression)

### Random Forests

This algorithm is a bit special since it uses multiple decision tree classifiers to predict with. This means that if you use 9 decision trees and ask it to predict something. If 6 of them predict 1 and the last 3 predict 0, then averaging the results and rounding the number to it's nearest whole we get 1 as the result.

In actuality, random forests are a lot more complicated with things like **Ensemble learning:** using multiple models trained over the same data and averaging the results like we did above, which is also called Bootstrapping which is one of the ways we do ensemble learning.
