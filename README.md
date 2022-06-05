# Introduction to Machine Learning with Python (PV)

In this repository, we will learn about the new Machine Learning technologies and their implementations with Python. We will focus on applications and not mathematical derivations of Machine Learning algorithms.

## Section 1: Introduction to Machine Learning

In this sections, we will discuss:

- Why we work with data?
- Exploratory data analysis.
- Interpreting Machine Learning Results.
- Types of Machine Learning.
- Machine Learning cycle.
- Machine Learning packages.

Data analysis provides us with information that we cannot get otherwise. For instance, analysis marketing effectiveness by concluding and analysing findings. Data analysis is also heavily used in medicine when diagnosing illnesses. An advantage of machines over human doctors is that machines always follow a non-biased procedure and never gets tired. This eliminates any errors or productivity issues that doctors can encounter. Another use case for data analysis is proving or disproving an ideo or judgement as, regardless of the hypothesis the data analysis is what provides us with proof which is non-arguable.

But where do we get data from? Data can be retrieved from many sources, for instance, Application Programming Interface (API) data. Here we will retrieve the data we desire without the need to download, store, and even pay for data we do not actually require.

Whilst working with data and performing exploratory data analysis, the below highlights some fundamental steps to take:

- Loading the data: We must load the data from the data source and view it on a program such as Excel.
- Make sanity checks: In this step, we perform some standard or logical checks to test the reliability of the data. For instance, if there are values that seem odd, we should check this to validate the reliability of the data.
- Basic data exploration: Plotting the data, making tables, analysing metrics, studying the Min/Max/Mean ... etc values are basic steps for data exploration. This gives us a feel for the data, with any strong trends becoming immediately apparent. All our observed metrics should make sense, keeping an eye out for any odd findings.
- If anything else is required: In this step, we observe the business objectives and see whether anything else is required, for instance, additional data.

Machine Learning is a set of mathematical algorithms that return a probability or likelihood. For instance, if we have a set of images and our model classifies whether the image is a cat or not, this algorithm will output "there are cats in pictures 1,3,6 ...". However, this result should be interpreted as "it is likely that the animals in pictures 1,3 and 6 ... etc are cats". If we have a model that predicts the stock price tomorrow, our model may give is the output "desired stock will gain 0.5% tomorrow". However, this result should be interpreted as "it is likely that the stock will increase in price tomorrow". The likelihood depends on the quality of the model and nature of the data. It is never possible to make a prediction with a 100% probability.

There are 3 main types of Machine Learning:

- Supervised learning: The machine learning task of learning a function that maps an input to an output based on example input-output pairs.
- Unsupervised learning: A type of algorithm that learns patterns from untagged data. The hope is that through mimicry, which is an important mode of learning in people, the machine is forced to build a compact internal representation of its world and then generate imaginative content from it.
- Reinforced learning: An area of machine learning concerned with how intelligent agents ought to take actions in an environment in order to maximize the notion of cumulative reward.

The main areas of supervised learning are:

- Regression: Good to analyse continuous data. For example, currency rates, marketing effects, and pricing.
- Classification: Good to analyse discrete data. For example, image recognitiom, medical diagnostics, and whether a product will be bought.

The Machine Learning Cycle takes the following flow:

Formulate the problem -> Get data -> Format data -> Explore data -> Perform modelling -> Evaluate the model -> Analyse results -> Deploy model

One of the most famous and important Machine Learning packages is called Scikit-learn (sklearn). Scikit-learn provides the following functions:

- Regression
- Classification
- Clustering
- Data preparation
- Model evaluation

**Note:** Other packages include TensorFlow, Keras, theano, PyTorch, and Microsoft Cognitive Toolkit. The website for Scikit-learn is: https://scikit-learn.org/stable/

Let's take a look at a sample dataset from Scikit-learn:

```
from sklearn.datasets import load_boston
boston_dataset = load_boston()
X, y = boston_dataset['data'], boston_dataset['target']
feature_names = boston_dateset['feature_names']
```

This dataset comes in Bunch type, which can be thought of as a dictionary (dict). We will create a datafrom fro this data:

```
boston_df = pd.DataFrame(X, columns = feature_names)
boston_df['target'] = y
```

## Linear Regression

In this section, we will cover:

- Mathematical formulation of a regression problem.
- Linear Regression with Scikit-learn.
- Interpreting linear regression results.
- Improving a regression model.

A simple linear function takes the following equation:

Y = mX + c

where: m is the gradient (or slope)
       c is the constant

A linear equation with a several variables takes the following form:

Y = m1X1 + m2X2 + m3X3 + ... + mnXn + c

where: m1, m2, m3, ..., mn are the gradients (or slopes)
       X1, X2, X2, ..., Xn are the variables
       c is the constant

