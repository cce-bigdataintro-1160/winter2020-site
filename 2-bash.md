# Operating the Shell

### Objectives
* A brief introduction to Operating systems and Linux
* Learn what's the shell
* Be able to Navigate through the file system
* Work with Files and Directories
* Use External Tools and Gnu Core Tools to enhance your shell skills
* Finding files and contents in files
* Write loops to iterate over lists
* Create scripts to automate basic processes
* Scheduling commands and scripts with the crontab

### A brief introduction to OS and Linux
* [Operating Systems](https://en.wikipedia.org/wiki/Operating_system): An operating system provides facilities to interface between applications and hardware using low level libraries and drivers.
* The most important resources it will manage are:
  * Inputs: Mouse, Keyboard, Sensors, Network
  * Outputs: UI, Disk, Network 
  * Processing (or In-Memory) state: Applications, scripts, programs
  * Storage (or Persistent) state: File systems/Disk
  
* Why learn Linux?  
  * Big Data Software will try to leverage these resources to work in a coordinated and distributed way across many "commodity hardware" nodes
  * Most of the [Big Data](https://github.com/onurakpolat/awesome-bigdata) open source software was built to run on Linux distributions only.
  * Large sets of data are hard to move: it's easier to work remotely on a Linux server with access to the data
  * Will make more sense in the Infrastructure course, but knowing the basics will help you deal with working on Mac and with Docker
* [The Linux Ancestry](https://en.wikipedia.org/wiki/Unix#/media/File:Unix_history-simple.svg): An image describing where Linux comes from
* [Linux list of distributions](https://en.wikipedia.org/wiki/List_of_Linux_distributions): A description of existing Linux distributions. The most widely used are Ubuntu, Debian and CentOS(RedHat)

### What's Bash?
* Terminal: a program that displays a text output window and accepts user inputs
* Shell: a command processor that typically runs in a terminal, processing inputs transforming them into outputs
* Bash: a very popular implementation of a shell, present in most modern Linux distributions

* [The shell](./bash-git-files/shell.png): An image depicting the utility of the shell, interfacing inputs and outputs towards the kernel(core) of Linux
* [Bash, the Unix Shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell)): A wikipedia page on the most popular Linux shell

### Be able to Navigate through the file system
* We'll now learn the basics in order to navigate in a file system
* root or `/` is the equivalent to `c:\` in Windows
* Your home directory or `/Users/<username>` is the equivalent to `C:\Users\<username> in Windows, and it's where you have full permissions to read and write files

![](bash-git-files/fshierarchy.png)

* [Filesystem Hierarchy Standard - Linux Standard Directories](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard): The basic file system organization in Linux
* [Navigation shell commands](https://github.com/cce-bigdataintro-1160/CEBD-1160-fall-2019-code/blob/master/class2-notebook/2-navigation_shell_commands.sh)
* [The man command - manual](http://www.linfo.org/man.html): A utilitary tool to read the manual for any shell command

1. Find out what's your username. Find your home directory and list its contents.
2. Change directory to `/` and list the contents of this directory. Why is this a special directory?
3. Change directory to `/var/log` and list its files. What do we have here?
4. From the previous dir `/var/log` type `cd ~`, check your new directory using `pwd`.
5. Test the following commands: `cd .`, `cd ..`, `cd /` and  `cd ~`. Can you explain what each of those symbols mean?
6. From your home directory test both commands and explain the difference: `cd Desktop` and `cd /Desktop`
7. What command can give you the most recently modified file in your home directory? Hint, use `man ls` to find the right flags to use.
8. Download the file [titanic.zip](bash-git-files/titanic.zip) and locate it through the shell by navigating and listing it. Tip: it will be in your Downloads directory, inside the your home directory.

### Work with Files and Directories
* Let's spend some time getting to know the most basic file operations we can do on a file system.
* Files and directories have permissions attached to them, that can be seen using the `ls -l` command
* The permissions for users, groups and others follow the syntax `drwxrwxrwx` where d stands for directory, r for read, w for write and x for execute
* Let's look at the example in code project

1. Create a directory called `learning-shell` in your home directory
2. Download the file [random_datasets.zip](bash-git-files/random_datasets.zip)
3. Copy it from your `~/Downloads` directory into your `learning-shell` directory
4. Unzip it using `unzip random-datasets.zip`
5. Look at those files contents by printing some files in your directories using `cat` or `less`. What is the difference between the two?
6. Lets organize this by first moving all files that start with `construction-spending` into the directory `construction-data`
7. Rename `Iris.csv` into `Iris_Classification.csv` and move it into `iris-species`
8. Delete the `delete-me` directory.
9. Create a file (using `nano` or `vi` editors) called `a_dataset.csv` write a few lines in it and save it.

### Use External Tools and Gnu Core Tools to enhance your shell skills
* A quick view on other tools available to explore and manipulate files, the following will help us solve the most common data manipulation problems: identify csv file headers, provide file dimensions, select slices of files, split files and concatenate files
* [Gnu Core Utils](http://www.gnu.org/software/coreutils/manual/html_node/): A list of all standard shell commands present on any Unix distribution
* Let's look at the example in code project

1. Unzip (using the terminal) our [titanic.zip](bash-git-files/titanic.zip), 
2. Provide the shape/dimensions of the file `train.csv`?
3. List the first 5 rows of the file. Now list the last 5.
4. Print only the lines 3 to 5 of the file?
5. Print this file last 5 lines save the output to train_tail.csv
6. Fetch the file `remorquages.csv` from the API as in our examples.
7. Can you explain the command `grep John remorquages.csv | wc -l` and why would you use it?
8. Split the train.csv file in multiple files with 20 lines each.

### Finding files and contents in files
* Let's look at the example in code project

1. Find the person called `Torborg` in the [titanic](bash-git-files/titanic.zip) file `train.csv`
2. Count how many people were male and female in the file
3. Count how many people called `John` are in the file and how many of them are male or female
4. Find all csv files in your home directory. Play with the `-maxdepth` flag to see the difference.
5. List all the `grep` commands you did today.

### Create scripts to automate basic processes
* Any file containing shell commands can be executed as a shell script
* Shell script files will usually have a `.sh` extension and begin with the shebang line: `#!/bin/bash`
* In order to execute a script, first make it executable by adding the x permission right to it with `chmod +x <name of script>.sh`
* Then run it using `./<name of script>.sh`

1. Use the titanic files to test these scripts!
2. Write a script that prints the name and number of lines for each of the `.csv` files in the directory /Users/<username>/to_loop/*.csv
3. Write a script that takes the first n lines of all files in '/Users/<myusername>/to_clean/*.csv' and creates and output file with their contents. n should be a parameter provided when running the script. 
  
### Scheduling commands and scripts with the crontab
* The crontab is a command scheduler that allows us to run commands on predefined schedules
* Its widely used for maintenance tasks, like cleaning up directories and backing up data
* Uses a [crontab schedule expression](https://crontab.guru/) to describe the execution times
* Use the commands `crontab -e` to edit and `crontab -l` to list the existing scheduled commands
* Let's schedule our crontab to save the current date at every minute to the file dates.txt on the home directory as an example

### Additional Exercises Material
* [Extra exercises](./2-bash-exercises.md): Additional exercises to practice Git

### Final notes on Linux and Shell
* Let's review what we've learned today
* The concepts we learned today apply for pretty much any filesystem, including the ones used for Big Data like HDFS, S3, GCS and AS
* Manipulating data in shell can save you a lot of time as those tools tend to be extremely lightweight.
* A few real life use cases for using the shell to deal with data are:
  - organization (mv, rm, cp, split)
  - exploration (wc, grep, find, ls, cat)
  - cleaning (cut, uniq, sort, sed)
  - validation and detecting corrupted files (head, tail, md5, wc)
  - maintenance and capture using a cron scheduler (cron, curl, wget)
  - cleanup and backup (cp, rm)
* Mastering the shell is essential if you want to engage in a Big Data Devops / DataOps career! Most tools installation, maintenance and troubleshooting will require understanding of these concepts.
* Experience will have you quickly know when usin shell is easier/faster then using Python. Try Googling for: "how to delete files older than 30 days in linux" or "how to find largest files in linux"

### Recommended References
* [Shell Interactive Manual](https://explainshell.com/): A web version of the man and the help of all shell commands
* [Software Carpentry Unix](https://swcarpentry.github.io/shell-novice/): A full lesson teaching how to use the shell from A to Z. We'll be doing this as part of the homework for this week.

### Advanced exercises material
* [crontab tutorial](https://www.ostechnix.com/a-beginners-guide-to-cron-jobs/): a beginners tutorial for using the crontab
* [cmdchallenge](https://cmdchallenge.com/): Can you complete these challenges from 

[Back To Main Page](./index.md)