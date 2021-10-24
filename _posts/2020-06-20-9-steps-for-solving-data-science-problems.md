---
excerpt: This article contains the list of nine steps you must take today to solve any machine learning problem in your organization.
layout: single
tags: 
    - machine-learning
    - tutorial
---

W Edwards Deming, an American statistician who helped develop the sampling techniques which are used by the U.S. Department of the Census and the Bureau of Labor Statistics once said, "If you can't describe what you are doing as a process, you don't know what you're doing."

While learning Machine Learning, I was always faced by this problem of not knowing the exact sequence of steps of any data science process. There are surely excellent resources out there which explain the individual steps in sophisticated detail and manner, but there wasn't a source which could give me a bird's eye view of the entire process. After learning all the individual steps from numerous different sources, I wrote myself this process containing nine steps that I would like to share here.

This is a high-level introduction and for more details about every step, it is recommended to go into depth using the available literature. It is assumed that the reader is familiar with some of the machine learning techniques and associated literature before reading this article.

## Step 1: Problem Formulation
Laden with the knowledge of machine learning algorithms, it is easy to forget that the purpose of Machine Learning is solving problems with the help of data. That can either involve predictive analytics where one tries to predict the future or exploratory analytics where one seeks to answer the questions of how and why something happened. We use Data Sciences not because we want to apply some fancy convoluted neural networks using a TPU, but simply we want to answer some questions which will help our organization, our country, and our planet to become better. Thus, it is absolutely important to start with what it is that you want to get answered using your data.

## Step 2: Data Cleaning
Once you know the problem statement, it is important to clean the data. Some statistics say that for more than 80% of the time, Data Science involves data cleaning. Data Cleaning ensures if the data has been entered correctly or if there are spelling mistakes or if a different schema of entering information has been used at different places, for example, pounds or kilograms for a column containing weight information.

One of the most important topics in Data Cleaning is Missing Values Treatment. Depending upon the problem in mind, one can either chose to drop missing values or replace them with either zero or mean of the remaining columns. Which is the best method can be debated, however most of the times what helps is relooking at my business problem to make a decision here.

## Step 3: Exploratory Data Analysis
Once the data is cleaned, it is important to understand the data by taking a bird's eye view. I normally look at the data types of the variables first and see if they match with what they should be. The second step that I do is looking at the distribution of variables of interest. I also see how many categorical and numerical variables are there. Calculating some statistics like mean, median, quartiles too help to have an understanding of the data. Depending upon the use-case, it may also be helpful to check if some variables are correlated with each other. Autocorrelation and Multicollinearity tests from Statistics help me here. Many times some of the simple questions can be answered visually by looking at the graph. While analysing NASA Airfoil Data, I figured by looking at the pair-plot that Linear Regression may not be the best machine learning algorithm in this case. My favourite library for visualization is Seaborn, which is built on top of Matplotlib, so all functionalities of Matplotlib are also there.

## Step 4: Data Preparation and Preprocessing
Many Machine Learning algorithms such as Support Vector Machines require preprocessing of the data before they can be used. Coding of categorical variables is also needed before it can be ingested into the model. sklearn offers many inbuilt preprocessing classes like MinMaxScaler() or StandardScaler(). One Hot Encoding can also be done using get_dummies() function of pandas. This step may not always be needed depending upon the machine learning algorithm.

## Step 5: Feature Selection
Datasets that you will get will vary in their sizes. For answering some of the business problems, one may not require all the variables (or features). Talking to an expert is a prudent decision to take at this stage. Depending upon their judgement, you could save yourself a lot of time in deciding which features to keep and which ones to drop in the model. Another strategy could be to use functions built in the Machine Learning algorithms to see the relative importance of features in explaining the seen variability in the model. The third strategy which is very scientific is to use Applied Machine Learning. This could be counterintuitive as one might ask how is it possible to use ML when we want to use ML for our model. Principal Component Analysis can be used to extract important features from the dataset.

Feature Engineering is not the same as Feature Selection.

## Step 6: Model Development
This is probably the step that is most famous in the community of data scientists. Depending upon the problems, one may need to use a supervised learning algorithm or an unsupervised learning algorithm. Some algorithms are faster and some are slower. Currently, Random Forests and Gradient Boosting Random Forests are very popular in solving some of the greatest machine learning problems. If you can afford time and money, using Neural Networks using TensorFlow can also be a very good decision at this stage.

## Step 7: Hyperparameter Tuning and Cross-Validation
This is my favourite part of the machine learning process. It is very important to make the model in the best manner possible. Overfitting and underfitting both are serious problems in the process of model development. Using false techniques and false parameters may make the generalization process for universe difficult. Using GridSearchCV in sklearn helps to simultaneously perform hyperparameter tuning and cross-validation while making ML models. The example on the website of sklearn for this technique is helpful to understand the entire process. Using tuned hyperparameters give the power to a machine learning algorithm in order to perform in the best way possible.

## Step 8: Model Evaluation
Having tuned the hyperparameters and checking for accuracy score, it is time to evaluate the model in detail. Confusion Matrix, Precision, Recall, Accuracy, and f-Score are some of the most important measurements used for classification problems. This article and the introduction on KDNuggets explain them in an excellent manner in detail. For the regression problem, R Square can be a good measurement for model evaluation. Most of the times, when I do the above seven steps with careful detail, my evaluation matrices give me a satisfactory response on my model and hyperparameters choice.

## Step 9: Communication
The last and very crucial step is to communicate the results of the machine learning algorithm to the relevant audience in the language they understand. Most of the times the management would not be interested in looking at the ROC Curve and AUC. They would be interested in your recommendations and suggestions as a data scientist on the problems they asked. No matter how excellent a data scientist you are, if you fail to influence your audience, your algorithms would just stay on your PC and not used in the real world. Thus, communication of the result is an extremely important step of the Data Science Process.

I hope that I am able to explain the process of data science in nine simple steps to you. As mentioned earlier, all the steps may not be required and some of the steps have to be executed again to arrive at an optimised situation. This list is exhaustive, as all the finer techniques can always be incorporated in the given sequence. If you see that one can change this, let me know and I would be happy to edit the content that I wrote.