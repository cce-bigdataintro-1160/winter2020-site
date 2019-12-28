# Python Data Visualization

### Agenda
* Visualizing data with Matplotlib
* Visualizing data with Seaborn
* About choosing the right plots
* Final Notes on Python Data Visualization

### Visualizing data with Matplotlib
* [matplotlib](https://matplotlib.org/index.html): Matplotlib official page
* [Anatomy of a Figure](https://matplotlib.org/_images/anatomy.png): Understand matplotlib basic objects: figures and axes

* Besides what we learned in last class, it's possible to create plots in matplotlib using a few different syntaxes
* We can generate grids with multiple plots and arrange the layout in different ways
* Matplotlib supports displaying images with the `show()` command, saving them to files with `savefig()` or displaying them automatically on Jupyter notebooks
* The words columns, features and dimensions will be used interchangeably and mean the same thing!!!
* Let's look at some [examples](https://github.com/cce-bigdataintro-1160/spring2019/tree/master/class6-notebook) in order to learn how to:
  * Create plots
  * Create figures and subplots (axes)
  * Save figures to files
  * Decorate and customize plots
  * Explore datasets through plots
  * Add multiple plots to the same subplot(ax)

1. Using the dataset you chose for your project. User `plt.show()` to plot one chart of each type:
  - line `plot` passing one column(feature)
  - `scatter` plot passing two columns(features)
2. Make sure to add a `title`, `xlabel` and `ylabel` on each of the previous plots
3. Put the the 2 plots above on the same figure and save it on a single file
4. You don't need to use multiple charts per figure anymore, just one is fine. Keep your `scatter` plot from the previous exercise and play with at least 2 of the `color`, `marker` and `alpha` parameters
5. Use one more feature(column) to play with the `s`(size) parameter of a `scatter` plot. 
* In order to do it first set it to a fixed value, like `s=10`. 
* Now try to set it to the value of another column of your dataset, like `s=df['<other column>']`. 
* What is the difference between those two techniques?
6. Do a multifeature plot! Plot 2+ overlapping `scatter` plots comparing one column to two other columns at the same time. Make sure to add a `legend` to make your multifeature chart easier to read.
7. Modify the previous chart from 6. to use the `s`(size) and `color` parameters.
8. Explore your dataset by plotting scatter plots comparing all columns 2 at a time. Tip, use nested for-loops for this!

### Visualizing data with Seaborn
* [seaborn](https://seaborn.pydata.org/): Seaborn official page
* [seaborn Examples Gallery](https://seaborn.pydata.org/examples/index.html): gallery with examples for reference
* [matplotlib cmaps](https://matplotlib.org/tutorials/colors/colormaps.html): matplotlib color maps to customize the seaborn plots color scheme

* Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
* For all exercises below look at the references in the seaborn [class6-notebook](https://github.com/cce-bigdataintro-1160/spring2019/tree/master/class6-notebook) in order to learn how to:
  * create the same plots we learned on matplotlib using seaborn
  * create categorical plots
  * create heatmaps
  * create joint and pair plots

1. Recreate the previous plots from matplotlib using seaborn: 
  * line plots -> `sns.lineplot`
  * scatter plots -> `sns.scatterplot` or `sns.jointploy`
  * histograms -> `sns.distplot`
2. Choose a categorical variable of your dataset and plot it using the following categorical plots: `sns.countplot` or `sns.violinplot`.
3. Create a correlation heatmap using `sns.heatmap`. Pass in the df.corr() to see the correlation heatmap for all of yours features!
4. Create the `sns.pairplot` for your entire dataset

### About choosing the right plots
* [Chart Suggestions](./viz-files/Advanced Presentation by Design - Chart.pdf): Chart suggestions from Advanced Presentation by Design by Andre Abela
* [Chart Suggestions Simplified](./viz-files/Graph Cheat Sheet.pdf): Simplified version of the chart suggestions
* [Charting Trends](https://trends.google.com/trends/explore?date=2018-03-03%202019-05-18&geo=US&q=matplotlib,seaborn,plotly,ggplot): Trends on the utilisation of charting libs

* It's very important to plot accordingly to the data you want to display(different data means different plots) and the information you want to convey. The chart suggestions above might help deciding what plots to use.
* Another strategy is to generate as many plots as possible and from it visually derive the 'best' ones

1. What the best way to display:
  * [Diabetes] Best way to understand how BMI affects/is affected by the Progression of Diabetes?
  * [Iris] To understand which has a larger variation between the Iris sepal length and Iris petal length? 
  * [Boston] To have a quick a understanding on what's the average, minimum and maximum prices of houses?
  * [Wine] To display what's the share of each class of Wine?
  * [Cancer] To display the relationship between 3+ features at the same time?

### Final Notes on Python Data Visualization
* All the concepts we're learning today can be applied to a multitude of tools for data visualization, that might differ in features and capabilities but where the basic concepts will be always the same!
* One important aspect is realize the power of mastering the programatic generation of plots. One can write a generic plotter that can receive many different types of datasets and produce those many plots automatically.
* Other aspects that can be configured programatically are automation, frequency, scheduling among other customizations
* Producing plots with python allows for access to data that could be otherwise difficult to read (databases, apis, shared directories, etc). Using python also makes it easy to make those plots available through: email, webpages, saved files on shared disks, etc
* The scale of data python can process is much higher than that of regular "office tools" making it able to process datasets that couldn't be handled otherwise. Notice that depending on the amount of data some techniques would still be required to "bucket" or "stream" the data.

### Optional homework(no need to submit)
* Read the machine learning introduction in: [this link](http://scipy-lectures.org/packages/scikit-learn/index.html#introduction-problem-settings), in particular, sections `3.6.1` to `3.6.5`. Don’t worry if this is a bit complex right now - it’ll really vary based on your math background.

### Recommended Readings
* [matplotlib Galleries](https://matplotlib.org/gallery/index.html): matplotlib Gallery with many plots to use for reference
* [matplotlib stylesheets](https://matplotlib.org/gallery/style_sheets/style_sheets_reference.html): List of all stylesheets available in matplotlib
* [matplotlib markers](https://matplotlib.org/api/markers_api.html): List of all markers available in matplotlib
* [matplotlib linestyles](https://matplotlib.org/gallery/lines_bars_and_markers/line_styles_reference.html): List of linestyles available in matplotlib
* [matplotlib Tutorials](https://matplotlib.org/tutorials/index.html): matplotlib Tutorials for Beginners, Itermediate and Advanced users
* [matplotlib Sample Plots](https://matplotlib.org/tutorials/introductory/sample_plots.html#sphx-glr-tutorials-introductory-sample-plots-py): Here you'll find a host of example plots with the code that generated them.

* [Visualization of Multi Dimensional data](https://towardsdatascience.com/the-art-of-effective-visualization-of-multi-dimensional-data-6c7202990c57): Excellent article about the challenges and solutions to visualize multi dimensional data

* [Plotly](https://plot.ly/python/): Plotly's Python graphing library makes interactive, publication-quality graphs online. 
* [Plotly Express](https://www.plotly.express/): A gallery displaying the simplified version of the plotly python library, meant to accelerate the usage of the library. 
* [ggplot](http://ggplot.yhathq.com/): ggplot is a plotting system for Python based on R's ggplot2

[Back To Main Page](./index.md)