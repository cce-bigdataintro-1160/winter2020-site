# Python Functions, Libraries & Numerical Analysis

### Agenda
* Homework Check
* Learn Hadoop and it's modules
* Explore data in Hadoop using SQL and Hive
* Homework

### Python Advanced Features

##### Goals
In this class we'll learn the basics of the Hadoop and Hive technologies.
* Discover what are the components that make up Hadoop and why they were created
* Use docker to quickly setup a development environment enabled for Hadoop and Hive
* Be able to manipulate hdfs files through the terminal and python
* Be able to create and query Hive tables through beeline and python

##### Learn Hadoop and it's modules
* [What is Hadoop](https://hadoop.apache.org/): The project description and its four main modules
* Hadoop has a distributed file system module that behaves a lot like a linux file system: [HDFS](https://hadoop.apache.org/docs/r1.2.1/images/hdfsarchitecture.gif)
* Hadoop has a resource manager that allows it to schedule work across multiple nodes: [YARN](https://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/yarn_architecture.gif)
* Hadoop has a processing engine that uses YARN do distribute work units accross multiple nodes: MR

* We can read and write data in/from hdfs in command line or using python code
<explain MR>

1.
2.
3.
4.
5.

##### Explore data in Hadoop using SQL and Hive
* [What is Hive](https://hive.apache.org/): The project description
* Hive project has software that facilidates reading, writing and managing datasets in HDFS and other file systems using SQL
* [Hive can use MR and YARN](https://cwiki.apache.org/confluence/download/attachments/27362072/system_architecture.png?version=1&modificationDate=1414560669000&api=v2) as an underlying engine for executing its tasks

* We can read and write data using SQL and Hive using the native client beeline or using python code 

1.
2.
3.
4.
5.

##### Final Notes on Hadoop and Hive
* Through the use of YARN as resource manager, Hadoop and MR were made possible 
* Hadoop and Hive have been the industry standard when it comes to Big Data storage and querying 
* But they're only the entry point for several other Big Data tools like Impala, Kudu, Presto, Spark and many others.
* The current landscape of the Big Data industry is currently being transformed by cloud technologies (AWS, GCP and Azure)

### Additional Exercises Material
* [Extra exercises](./5-pythonadv-exercises.md): Additional exercises to practice

### Optional homework(no need to submit)
* Reserch the following matplotlib types of plots: `bar` and `pie`
* Research the library `seaborn`, another plotting library based on `matplotlib`
* Research the library `plotly`, another plotting library widely used for data analysis

### Recommended Readings
* [Loading csv files in pandas](https://towardsdatascience.com/pandas-dataframe-playing-with-csv-files-944225d19ff): Tutorial explaining how to load CSV files in pandas DataFrames
* [Loading excel files in pandas](https://datatofish.com/read_excel/): Tutorial explaining how to load excel files in pandas DataFrames
* [Loading sql tables in pandas](https://stackoverflow.com/questions/10065051/python-pandas-and-databases-like-mysql): page explaining how to load sql tables in pandas DataFrames
* [Loading html tables in pandas](https://beenje.github.io/blog/posts/parsing-html-tables-in-python-with-pandas/): page explaining how to load html tables in pandas DataFrames

[Back To Main Page](./index.md)