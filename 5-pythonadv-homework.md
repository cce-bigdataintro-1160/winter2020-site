Hey everyone!! Thanks for the great class, I feel we have a good understanding of Python basics and can move forward to looking into datasets:muscle:
As always, don't forget to fill up the Weekly Journal: https://forms.gle/QAe9Dm54xNwUxZqZA !!!! :rocket::rocket::rocket:

Here's the homework for this week and have an excellent week:

*PREPARATION*
Create a new repository on GitHub called python-homework and clone it locally.
Use this repository to push all the scripts for this week's homework. Send me the link your repository after you are done!

*BASIC*
Write a script called `FizzBuzz.py` that loops over all the integers from 1 to 100.
- For multiples of three print "Fizz"
- For multiples of five print "Buzz"
- For multiples of three and five print "FizzBuzz"
- If the number isn't a multiple of neither three of five, print the number itself


*ADVANCED*
Write a script called `FileReader.py` that opens the boston housing dataset file (name is `housing.data`) and prints every line in the file. I'm sending the boston housing dataset in the next message in this channel.


*REACH*
1) Enhance the `FileReader.py` from the Advanced section: before you print each line, split them into list of values
(i.e. `0.00632  18.00   2.310  0  0.5380  6.5750  65.20  4.0900   1  296.0  15.30 396.90   4.98  24.00`
would become `['0.00632', '18.00', '2.310', '0', '0.5380', '6.5750', '65.20', '4.0900', '1', '296.0', '15.30', '396.90', '4.98', '24.00']`)

2) Write a script called `Desktop.py` that lists all files on your Desktop. For each file checked, print if the file is a file or a directory.
Tip: The path for Desktop should be similar to `C:/Users/<username>/Desktop` on Windows, `/Users/<username>/Desktop` on Mac and `/home/<username>/Desktop` on Ubuntu.
Tip: you can use os.path.isfile and os.path.isdir to help on this task!
Tip: Make sure you have some files and dirs in your Desktop otherwise the script will do nothing!




Don't forget to check at the reference codes we saw in the class to help you do the homework! (https://github.com/cce-bigdataintro-1160/CEBD-1160-fall-2019-code/tree/master/3-python-notebook):book:

And don't hesitate if you have questions! Next class we finally meets pandas!:panda_face:




Hey everyone!! Hope you enjoyed meeting pandas and other Python libraries. We've put another tool in our toolbox to play with datasets, and this time a pretty powerful one. :wrench::hammer:
As always, don't forget to fill up the Weekly Journal @ https://forms.gle/QAe9Dm54xNwUxZqZ !!!!

Here's the homework for this week:

*PREPARATION*
Create a new repository on GitHub called pandas-homework and clone it locally.
Use this repository to push all the scripts for this week's homework. Send me the link your repository after you are done!

*BASIC*
1. Do exercises 1-7 (all) from the `Numerical Analysis with Numpy Arrays` section on the https://cce-bigdataintro-1160.github.io/CEBD-1160-fall-2019-site/5-pythonadv.html:
You can put all the solutions in a single script named `numpy-exercises.py`. If you prefer, you can split it into multiple scripts for each exercise like `numpy-exercises-1.py` ... `numpy-exercises-n.py`

2. Do exercises 1-12 (all) from the `DataFrames with Pandas` section on the https://cce-bigdataintro-1160.github.io/CEBD-1160-fall-2019-site/5-pythonadv.html:

You can put all the solutions in a single script named `pandas-exercises.py`. If you prefer, you can split it into multiple scripts for each exercise like `pandas-exercises-1.py` ... `pandas-exercises-n.py`

*ADVANCED*
1. This step should help you kickoff the final project for the course. All the steps should be done on the dataset you chose earlier in the course.
2. Create a python script `myproject.py`. Your script should:
  * load and organize the data in a pandas data frame format, please notice that some datasets will require that you manually fix the headers as they're not present in the dataset.
    * Tip: For the boston dataset, your separator will be `sep='\\s+'`. This will mitigate the problem with multiple spaces!
    * Tip: In order to fix the column names, you might have to manually assign the values to it as in the examples!
  * compute and print information and summary statistics on the dataset
  * compute and print correlations on the dataset

*REACH*
Both reach exercises involve updating your `myproject.py` script from the Advanced section.
1. Using the examples in 9-matplotlib_plotting.py as a reference, update your `myproject.py` and add:
  * Reference material https://github.com/cce-bigdataintro-1160/CEBD-1160-fall-2019-code/blob/master/4-python-advanced-notebook/9-matplotlib_plotting.py
  * Save an image plotting any 1 column from your dataset (line plot or histogram)
  * Save an image plotting any 2 columns from your dataset (scatterplot)
2. [Optional challenge] Update your `myproject.py` to make it capable of receiving arguments to make it generic for other datasets

Don't forget to check at the reference codes we saw in the class to help you do the https://github.com/cce-bigdataintro-1160/CEBD-1160-fall-2019-code/tree/master/4-python-advanced-notebook !:book:

And don't hesitate if you have questions! Next class we start on data visualization!:bar_chart::chart_with_upwards_trend: