##### What is pseudocode
* [Pseudocode in Wikipedia](https://en.wikipedia.org/wiki/Pseudocode): Article describing Pseudocode and what's it used for
* it's nothing more than expressing your objectives in a speech-like language before you start coding, avoiding complex details that would otherwise clutter your line of thought
* can be written in a way that it resembles the programming language, to facilitate implementation
* can be refined multiple times until it becomes almost code

1. Write pseudocode for a program that reads the titanic file and saves two other files one for the male passengers and another for the female passengers

##### Creating your own functions
* [Function Definition](https://docs.python.org/3/tutorial/controlflow.html#defining-functions): Overview of how to define a function
* A function is a block of reusable code that can be written once and executed later (or never)
* The advantage of using functions is that you can write it once but call it multiple times, saving time and code
* Functions can receive values (aka parameters) and can return a result to the function caller
* We already know a few built-in functions like `len`, `help`, `open` and `enumerate`, they come from the [python standard library](https://docs.python.org/3/library/index.html)

Exercise 1
1. Create a new script called `functions.py`.
2. Create a function called `file_summary` that receives a file path as a parameter (of type string) and returns the following string: `The file <filename> has <n> lines`
3. Create a function called `print_disclaimer` that receives the paths of multiple files and prints: `This program will print the summary for the following files: <filenames>`
4. Conclude your script by calling both functions for: titanic `train.csv`, titanic `test.csv` and `insurance.csv` 

Exercise 2
1. We'll be using the titanic `train.csv` file for this exercise, and we'll categorize the gender of the passengers as `0` for male and `1` for female
2. In order to do that create a function called `categorize_gender` that receives a line of the titanic file as a parameter and returns `0` if the passenger is man or `1` if is a woman
```
def categorize_gender(row):
   ???
   return row + [0 or 1]
```

3. Iterate over each row of the file applying your function
4. Add the result of your function call to each row of the dataset, producing a new list
5. Print your new list with an extra field