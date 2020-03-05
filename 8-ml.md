# Machine Learning in Big Data

### Agenda
* Machine Learning Concepts
* scikit-learn
* Acquiring and loading data
* Preparing the data
* Linear Regression
* Logistic Regression
* About choosing the best algorithms
* Final Notes on Machine Learning

### Machine Learning Concepts
* Machine learning is an Artificial Inteligence subfield, that focuses on the study of algorithms that can create models to predict or group data by inferring information from existing data
* It's about building programs with tunable parameters that are adjusted automatically so as to improve their behavior by adapting to previously seen data, in contrast to regular programs where the programmer has to explicitly write every single instruction.

1. In groups of two, take five minutes to research 1 example of each of the following category of ML problems: Supervised Classification, Supervised Regression and Unsupervised Learning
2. Can you convert a regression problem into a classification problem? When would that be interesting?

* We'll be focusing on Supervised Learning, in particular regression and classification problems

* Some important glossary:
  * X is a matrix where each row represents a sample (a.k.a. instance, record) and each column represents a feature (a.k.a. dimension, attribute, independent variable)
  * y: is a vector containing our variable to be predicted, also called target, label or dependent variable
  * estimator: is an object that can train a ML model after a mathematical algorithm
  * model: is the predictor function created by the estimator
  * Accuracy: percentage of correct predictions the generated model can make
  * Error: the sum of the errors made for each example in training or validation sets. Unlike accuracy, loss is not a percentage.
  
* A general Machine Learning Process Lifecycle
![](ml-files/Slide1.jpeg?raw=true)

### scikit-learn
* [sklearn tutorial](http://scipy-lectures.org/packages/scikit-learn/index.html#introduction-problem-settings): tutorial showing how to use python and sklearn to solve ML problems
* [sci-kit learn testimonials](https://scikit-learn.org/stable/testimonials/testimonials.html): Non-exhaustive list of companies using sci kit learn

* The scikit-learn project started as scikits.learn, a Google Summer of Code project, now under active community development. It's widely used as one of the simplest and most effective tools to practice Machine Learning
* It's based on numpy and pandas, making it easy to use and compatible with matplotlib and seaborn. Between it's advantages it's based on fairly high level concepts with an easy to use interface
* sklearn has [estimators](http://scipy-lectures.org/packages/scikit-learn/index.html#a-recap-on-scikit-learn-s-estimator-interface) that expose a standardized interface for each ML algorithm
* Handles most modern ML algorithms, except Deep Learning, where Tensor Flow, Keras and PyTorch take place

### Acquiring and loading data
* [Loading External Datasets](https://scikit-learn.org/stable/datasets/index.html#external-datasets): sklearn recommended ways to load datasets

* Generally, scikit-learn works on any numeric data stored as numpy arrays or scipy sparse matrices. Other types that are convertible to numeric arrays such as pandas DataFrame are also acceptable
* Using one of the many pandas read methods is a great start: 'read_csv', 'read_excel', 'read_html', 'read_json', 'read_parquet', 'read_sql', 'read_sql_query', 'read_sql_table' and 'read_table'. Besides these there are other libs capable of loading virtually any type of data!
* Data has to be large enough to allow algorithms to converge, but handling large volumes of data can be cumbersome. Ideal size is on a case-by-case basis, but should be as little as necessary.
* Too small datasets can lead to biases and consequently invalid prediction models
* For the class and project we'll now [load our data straight from sklearn sample datasets](http://scipy-lectures.org/packages/scikit-learn/index.html#loading-the-iris-data-with-scikit-learn), as that data has been already prepared for running ml algorithms 

1. For this exercise we'll use one of the following datasets: boston, cancer, diabetes, wine or iris 
2. Load your chosen dataset using the the sklearn dataset load methods. Now print the loaded dataset `keys()`, `data.shape`, `target.shape` and `feature_names`
3. Assign the `data` to a variable named X representing our samples
4. Assign the `target` to a variable named y representing our targets

### Preparing the data
* The first step is to visualize and make sure that you have a conceptual understanding of what each column represents towards your final objective. All tools we learned in the last classes are essential in this step: 
  * pandas DataFrames summaries, statistics and correlation
  * plotting datasets techniques
  
* After a preliminary data exploration, preparation and cleaning are the most time consuming part of a ML process
* The next steps involves data manipulation operations to minimize noise and prepare the dataset for sklearn, that uses only numerical features: 
  * dealing with missing data: dropping or filling values
  * transforming/encoding textual data with numerical values
  * encoding categorical features with dummy variables
  * feature selection/drop features: removing features manually or with an algorithm

* Machine Leaning algorithms will require a `training dataset` to create the model and a `test dataset` to validate the resulting model. 
  * Supervised algorithms require that each dataset is divided in to an X matrix(features) and a y array (labels)
  * Unsupervised algorithms only require the X matrix(features)

* We'll use sklearn `model_selection.train_test_split` method to split the datasets, with a test dataset size between 30%-40% (common range for smaller sets)

1. For your chosen dataset, create the train and test splits. Print the shape of the full initial dataset and then the shape of each of the 4 split datasets `X_train, X_test, y_train, y_test`

### Supervised Learning: Linear Regression - for Regression problems
* [Linear regression, or least squares method](http://scipy-lectures.org/packages/scikit-learn/auto_examples/plot_linear_regression.html#a-simple-linear-regression) is a supervised ML [estimator/algorithm](http://scipy-lectures.org/packages/scikit-learn/index.html#a-recap-on-scikit-learn-s-estimator-interface) from sklearn meant to predict continuous features
* We'll use labelled data to try to predict unlabelled data values using known feature values 
* The simplest form of Linear Regression can be defined by the formula `Y = a + bX` whereas the Least Squares algorithm is applied until an optimal fit is found
![](ml-files/linear-regression.png?raw=true)
* Let's look at some [examples](https://github.com/cce-bigdataintro-1160/spring2019/tree/master/class7-notebook) in order to create a model to predict data

1. Using either the boston or diabetes datasets train a Linear Regression Model
2. Print the resulting coeficients of your model

* You can measure your model quality by using a few methods:
  * Plotting the real vs predicted values
  * Calculating and plotting the residuals (actual - predicted values)
  * Calculating the error: MAE, MSE or RMSE

1. Plot a scatter plot comparing your test targets versus your predicted targets
2. Print the resulting RMSE (Root Mean Square Error). In order to improve this model should we increase or decrease the RMSE?

### Logistic Regression - for Classification problems
* [Logistic regression](http://scipy-lectures.org/packages/scikit-learn/auto_examples/plot_iris_knn.html) is a supervised ML [estimator/algorithm](http://scipy-lectures.org/packages/scikit-learn/index.html#a-recap-on-scikit-learn-s-estimator-interface) from sklearn meant to predict categorical features
* Because Linear Regression is unsuitable to predict the probability of a target, Logistic Regression adds [Sigmoid/Logistic](https://en.wikipedia.org/wiki/Sigmoid_function) function over the linear regression, limiting the result in a probability score from 0 to 1 
* We'll use labelled data to try to predict unlabelled data class/categories using known feature values
* On multiclass linear regression, the class with the highest probability "wins"
![](ml-files/logistic-regression.png?raw=true)
* Let's look at some [examples](https://github.com/cce-bigdataintro-1160/spring2019/tree/master/class7-notebook) in order to create a model to predict data

1. Using either the iris, cancer or wine datasets train a Logistic Regression Model
2. Print the resulting coeficients of your model

* [Measuring classification results with sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_recall_fscore_support.html): how to analyse the metrics returned by the `metrics.classification_report`
* [Measuring classification results explained](https://towardsdatascience.com/accuracy-precision-recall-or-f1-331fb37c5cb9): Reference explaining the difference between Accuracy, Precision, Recall and the F1Score on classification

1. Print your model score, classification_report and confusion_matrix
2. Print the resulting f1-score for your model In order to improve this model should we increase or decrease the f1-score?

### About choosing the best algorithms
* [scikit-learn algorithm cheatsheet](https://scikit-learn.org/stable/tutorial/machine_learning_map/index.html): excellent starting point for deciding which algorithm to use when training models
* [Supervised Learning algorithms](https://scikit-learn.org/stable/supervised_learning.html): sklearn list of supervised learning algorithms
* Scikit-learn strives to have a uniform [interface](http://scipy-lectures.org/packages/scikit-learn/index.html#a-recap-on-scikit-learn-s-estimator-interface) making it exceptionally easy to try different algorithms
* But selecting hyperparameters can be a way more challenging task as these can be specific for each algorithm, and due to the fact that more complexity leads to the overfitting and underfitting problem

### Final Notes on Machine Learning
* We've seen simple forms of ML algorithms, but they can be leveraged with hundreds, thousands or millions of features

* Examples of Supervised Learning
  * web search score
  * credit/mortgage/insurance risk
  * pricing forecast
  * advertisement targeting
  * optical character recognition/natural language processing
  * spam filtering
  * document verification
  * medical imagery
  * fraud detection
  
* Examples of Unsupervised Learning
  * cyber security and intrusion detection
  * factory anomaly detection
  * product recommendations and suggestions (Netflix, Spotify, etc)
  * customer(or product) classification

* Examples of more complex uses that mix multiple types of ML
  * financial models
  * robotics
  * chatbots
  * self driving cars
  * sentiments analysis  
  * computer vision

* Another important aspect is the capability of models to be [persisted](https://scikit-learn.org/stable/modules/model_persistence.html) 
* This allows for later [serving](https://towardsdatascience.com/a-flask-api-for-serving-scikit-learn-models-c8bcdaa41daa) the model on a api!

### Recommended Readings
* [ML Glossary](https://developers.google.com/machine-learning/glossary/): A very extensive glossary for Machine Learning Concepts

* [Machine learning](https://www.coursera.org/learn/machine-learning): A course to look behind the algorithms
* [An Introduction to Statistical Learning](https://www-bcf.usc.edu/~gareth/ISL/): Excellent book on the math behind Machine Learning

* [sklearn tutorials](https://scikit-learn.org/stable/tutorial/index.html): Many sklearn tutorials including how to work with textual data and some video resources
* [Free Machine Learning Books](https://github.com/josephmisiti/awesome-machine-learning/blob/master/books.md): Extensive list of free ML books

* [Standardization and scaling](https://scikit-learn.org/stable/modules/preprocessing.html#standardization-or-mean-removal-and-variance-scaling): Guide on standardization and normalization
* [Scalers Comparison](https://scikit-learn.org/stable/auto_examples/preprocessing/plot_all_scaling.html): Comparison between multiple different scaling methods

* [Exposing models on API](https://towardsdatascience.com/a-flask-api-for-serving-scikit-learn-models-c8bcdaa41daa): A short tutorial showing how to present and re-use models using python's Flask framework

[Back To Main Page](./index.md)