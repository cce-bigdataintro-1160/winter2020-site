# Data Preparation

### Agenda
* Pandas DataFrames manipulation, cleanup and preparation
* Data cleanup and preparation for sklearn
* Introduction to Jupyter Notebooks
* Where do I go from here?
* Final Project

### Data preparation
Goal for today will be to review everything we learned so far, play with data preparation and kickoff the final project development!

### Pandas DataFrames manipulation, cleanup and preparation
* A review of what we've [seen](https://github.com/cce-bigdataintro-1160/CEBD-1160-fall-2019-code/tree/master/4-python-advanced-notebook)
* Let's check a few new DataFrame operations:
  * Concatenating DataFrames
  * Renaming columns
  * Replacing values
  * Mapping values

### Data cleanup and preparation for sklearn
* An overview of some important data preparation techniques:
  * Filling up missing data
  * Encoding categorical features with dummy variables
  * Producing numerical data from textual data
  * Dropping columns with small impact or that add 'noise' (not really correlated)
* This way we should have only numerical values for sklearn

### Introduction to Jupyter Notebooks
* [Jupyter Notebooks](https://jupyter.org/) is a web application that allows you to write documents that can contain Python code
* These documents can be executed by parts, which can make data exploration much easier to organize
* It can be used to facilitate all the steps we performed in PyCharm before, but in an interactive way
* In many companies, you'll have a central server hosting the [Jupyter Hub](https://jupyter.org/hub) application
* You can install Jupyter locally for development purposes, either instaling it from its website or with the [Anaconda](https://www.anaconda.com/) platform
* Using the `%matplotlib inline` directive, all plots will be immediatelly plotted in Jupyter!   
* Let's re-do some of our examples using a Jupyter Notebook now.

1. What are activities are easier to do in Jupyter using notebooks? What activities are easier to do in PyCharm using scripts? 

### Where do I go from here?
* Well, this will depend a lot on where do you want to go :)
* A few more guided exercises to warmup: [Data Carpentry](https://datacarpentry.org/lessons/)
* A good starting point to develop ML skills: [Kaggle Getting Started Competitions](https://www.kaggle.com/competitions?sortBy=grouped&group=general&page=1&pageSize=20&category=gettingStarted)
* A more advanced challenge with unprocessed data [Montreal Open Data](http://donnees.ville.montreal.qc.ca/)
* [Other Datasets](https://github.com/awesomedata/awesome-public-datasets)
* Study other Computer Science topics like web development and microservices in order to deploy ML models
* [CCE Big Data Diploma](https://www.concordia.ca/cce/programs/big-data.html)

![](https://media.giphy.com/media/1n4FT4KRQkDvK0IO4X/giphy.gif?raw=true)

* [Reality will be more like](https://media.giphy.com/media/3o85xxSZvFZgD4wXde/giphy.gif) 
* ...but persist!!!

### Additional Exercises Material
* [Putting it all together...](./9-data-preparation-exercises.md)
* Don't hesitate to consult the material from previous classes to do the exercise!

### Final Project
* [Final project instructions/template](https://github.com/cce-bigdataintro-1160/cebd1160_project_template)
* [Final project example](https://github.com/cce-bigdataintro-1160/cebd1160_project_template/tree/gkexample)

* You may use the template structure to guide your thinking, but don't feel constrained by it, add and modify sections as you see fit
* Back your claims using plots and data obtained using your dataset analysis skills
* Make sure to add references for libraries and methods you're using  
* You can look for other people that "solved" your dataset on Google. You might find many ideas that you hadn't thought of!
* The objective will be to both start your data skills portfolio and also exercise your data presenting(and storytelling) skills! 
* Use [markdown](https://guides.github.com/features/mastering-markdown/) formatting to make your project look good, by creating sections and embedding pictures.

* FAQ
  * Can I change my originally chosen dataset?
    
    Yes!

  * Can I change my originally chosen question?
    
    Yes too!

  * Is it mandatory to make a final project?
    Yesss! Presenting results and storytelling is a very important skill in Big Data and any successful career in tech!

  * How should I present my final project?
    
    Sky is the limit! You'll have 5-10 minutes to present to everyone in the class your data project. You can use the readme.md GitHub page, a power point presentation or whatever means you prefer (that you know is installed in class)

  * Can I change the csv dataset instead of the sklearn one?
    
    Yes, but take the risks into account, they haven't been 'prepared'!

  * How many plots should I add to my project?
    
    There isn't really a limit, try to stick with the "best" ones in order to explain each section of your template!

  * How do I format/style my project to look as good as the sample project?
    
    Look at the raw version of it [here](https://raw.githubusercontent.com/cce-bigdataintro-1160/cebd1160_project_template/gkexample/README.md)!!!

  * How long should my presentation be?
    
    5-10 minutes!    

  * Is there a specific algorithm I should use?
    
    You can use as many algorithms as you want and compare their results. Besides don't hesitate to try to optimize your score using feature selection or any other techniques you might find interesting!

  * I'm really stuck! I don't know exactly if my question is good or how to solve it...
    
    Google for inspiration! The reasons those datasets were chosen is because they've been largely used in Machine Learning literature. This means you'll find awesome inspiration around the internet, which I recommend you read and understand thoroughly to help you!
    Some other ideas you can use to improve your project: 
    * compare different algorithms and hyperparameters to find out what are the best solutions for your problem
    * analyze some discrepancy in your data (for example, if you expected some feature to have high impact on your prediction, but it doesn't, you could analyze what's the cause of that)
    * optimize what's the combination of features that can lead you to the best performance
    * transform your dataset to enrich it during the preparation phase
    * challenge your own results and question with other data (maybe even external data)

### About 
* [How to show you master bigdata](https://pixelastic.github.io/pokemonorbigdata/)
* [Database Ranking](https://db-engines.com/en/ranking)
* [A ton of big data related technologies](https://github.com/onurakpolat/awesome-bigdata)
* [Draft for professsions](./10-professions.md)

[Back To Main Page](./index.md)