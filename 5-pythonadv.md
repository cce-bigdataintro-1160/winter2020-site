# Python Libraries for Data Manipulation

### Agenda
* Importing and Using Libraries
* Numerical Analysis with Numpy Arrays
* DataFrames with Pandas
* Plotting Charts with MatPlotLib

### Importing and Using Libraries
* In order to facilitate reading and manipulating datasets, we'll need to use a few libraries like numpy, pandas and matplotlib
* Libraries are packages of classes and functions previously written to be reused as components 
* In order to import packages in Python they either have to:
  * be part of the [standard library](https://docs.python.org/3/library/) 
  * be installed manually using pip 
  * be installed manually using the os package manager
  * be installed manually using PyCharm
* After the installation, using libraries is as simple as using `import` statements like `import sys` or `import numpy as np`
* you can check the available methods in each lib by using the functions `dir` and `help` or using your IDE (PyCharm) help
* Let's take a look together at the standard libraries `time`, `random`, `os` and `sys` in the CEBD-1160-code project

1. In `pandas-notebook` project do the following exercise in pairs:
2. Write a python script that prints a message every 3 seconds 
3. Add a random number to your message.
4. Allow the user to provide a string argument that gets added to your message

### Numerical Analysis with Numpy Arrays

* Numpy is a Linear Algebra Library for Python, and it's very fast because of it's native bindings
* The most important concept in Numpy are Arrays that look a lot like lists, and Matrixes that look like tables
* Many Data Science libs like pandas, sklearn and matplotlib rely on Numpy as base, and consequently take Numpy Arrays as inputs and outputs to it's methods
* Let's take a look together at numpy in the CEBD-1160-code project

1. In `pandas-notebook` project do the following exercise in pairs:
2. Create your first array with the elements `[1,22.4,5,35,4,6.7,3,8,40]` and print it. Experiment what the following functions do: `ndim`, `shape`, `size` and  `dtype`.
3. Create your first matrix with the elements `[['a', 'b'],['c', 'd'],[3, 3]]` and print it. Experiment what the following functions do: `ndim`, `shape`, `size` and `dtype`
4. Create numpy 1 dimension array using each of the functions `arange` and `rand`
5. Create numpy 2 dimensions matrix using each of the functions `zeros` and `rand`
6. Create an array containing 20 times the value `7`. Reshape it to a 4 x 5 Matrix
7. Create a 6 x 6 matrix with all numbers up to 36, then print:
* only the first element on it
* only the last 2 rows for it
* only the two mid columns and 2 mid rows for it
* the sum of values for each column

### DataFrames with Pandas
* Library meant to help with data analysis using two new data structures: Series and DataFrames
* At first it will resemble a lot like numpy Arrays, but the big difference is that we can assign labels to our n dimensional, making it possible to create DataFrames, a table structure that can be used very similarly to Excel or SQL tables
* Has many productivity functions to facilitate data visualization, manipulation and cleaning
* Has many data loaders making it capable of integrating with many sources like csvs, xlsx, sql and html pages
* Let's take a look together at pandas in the CEBD-1160-code project

1. In `pandas-notebook` project do the following exercise in pairs
2. Load the [insurance.csv](python-files/insurance.csv) in a DataFrame using pandas. Explore the dataset using functions like `to_string()`, `columns`, `index`, `dtypes`, `shape`, `info()` and `describe()`. Use this DataFrame for the following exercises.
3. Print only the column `age`
4. Print only the columns `age`,`children` and `charges`
5. Print only the first 5 lines and only the columns `age`,`children` and `charges`
6. What is the average, minimum and maximum `charges` ?
7. What is the `age` and `sex` of the person that paid `10797.3362`. Was he/she a smoker?
8. What is the `age` of the person who paid the maximum charge?
9. How many insured people do we have for each `region`?
10. How many insured people are children?
11. What do you expect to be the correlation between `charges` and `age`, `bmi` and `children`? 
12. Using the method `corr()`, check if your assumptions were correct.


### Plotting Charts with MatPlotLib
* Use the Matplotlib library to generate simple plots from Datasets
* One of the main libraries for scientifical data exploration, allows for quick prototyping and has all basic functionalities
* Was built with the MATLAB interface as a reference
* Compatible with Jupyter notebooks, facilitating it's usage on interactive python clients
* Has a very rich gallery page with tons of examples that can be copied and modified
* Allows users to save figures in high resolution for printing and supports many different formats
* Let's take a look together at matplotlib in the CEBD-1160-code project

1. Still using the same DataFrame from the previous exercise [insurance.csv](python-files/insurance.csv) plot the chart for `charges` and save it as `charges_plot.png`
2. plot the histogram for `bmi` and save it as `bmi_hist.png`
3. plot the scatterplot for `age` vs `charges` and save it as `age_charge_scatter.png`
4. Re-do the previous items, adding the title, x label and y label for each item.
5. Think about the exercise 12 from the previous section. Do the plots match what we saw with the correlation function?

### Final Notes on Python Libraries
* These utilities are widely used in the industry and represent some of the most essential building blocks for data analysis
* Many worksplaces have unexplored datasets that can produce interesting insights, looks around for excel, csv, databases or html you can play with
* There are many other more specialized libraries and tools like: pyspark, tensorflow, plotly, but all of them require the basic understanding and assimilation of the concepts we learned
* In conjunction with the right tools we have to always be curious and try to figure new insights we can extract out of the data. These tools are meant to leverage expertise and not to replace it
* After learning all of those utilities, we'll put this in practice by continuing the creation of our final project using the chosen dataset

### Additional Exercises Material
* [Extra exercises](./5-pythonadv-exercises.md): Additional exercises to practice

### Recommended Readings
* [Importing Libraries](https://docs.python.org/3/tutorial/modules.html#importing-from-a-package): How to import python existing libraries

* [numpy Docs](https://www.numpy.org/devdocs/): numpy Documentation
* [numpy Quick Start](https://www.numpy.org/devdocs/user/quickstart.html): A few quick recipes to use Numpy

* [Pandas Docs](http://pandas.pydata.org/pandas-docs/stable/): main pandas documentation page
* [pandas Quick Start](http://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html): A few quick recipes to using DataFrames

* [matplotLib Galleries](https://matplotlib.org/gallery/index.html): matplotlib Gallery with many plots to use for reference
* [matplotLib Docs](https://matplotlib.org/contents.html): Matplotlib Documentation
* [matplotLib Tutorials](https://matplotlib.org/tutorials/index.html): matplotlib Tutorials for Beginners, Itermediate and Advanced users.

* [Loading csv files in pandas](https://towardsdatascience.com/pandas-dataframe-playing-with-csv-files-944225d19ff): Tutorial explaining how to load CSV files in pandas DataFrames
* [Loading excel files in pandas](https://datatofish.com/read_excel/): Tutorial explaining how to load excel files in pandas DataFrames
* [Loading sql tables in pandas](https://stackoverflow.com/questions/10065051/python-pandas-and-databases-like-mysql): page explaining how to load sql tables in pandas DataFrames
* [Loading html tables in pandas](https://beenje.github.io/blog/posts/parsing-html-tables-in-python-with-pandas/): page explaining how to load html tables in pandas DataFrames

[Back To Main Page](./index.md)