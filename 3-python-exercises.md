##### The environment
1. Check what's the type of the following values in the python shell:
   * `1`
   * `3.14`
   * `"Big Data!"` and `'Big Data!'`
   * `True` and `False`
   * [1,2,"intruder",3]
2. Get some help on the value `True`

##### Numbers
1. Write an equation that uses division, multiplication, an exponent, subtraction and an addition that is equal to 42.5. Assign the result to the variable `result` and print it.
2. Find out if 45234 is divisible by 4

##### Strings
1. Given the string `big data` give two commands that can print `d`.
2. Given the string `big data` give two commands that can print `g da`
3. Reverse the string `big data` in two different ways
4. Given the strings `big` and `data`, produce the string `big data`

##### Booleans
1. Can you write an expression that evaluates if a string is a palyndrome? i.e. `'abba'` should be True and `'rock'` should be False.

##### Lists
1. Can you replace `big data` with `BIG DATA` in the list `['a',2,['b',4,5,'big data']]`
2. What's the difference between `[1,2,3] + [4]` and `[1,2,3].append(4)`
3. Find the unique elements in the list `[3,333,333,3,3,3333,3,3333,333,3,333333,3]`
4. Return all elements between(non-inclusive) 4 and 8 on the list `[1,2,3,4,5,6,7,8,9]`
5. Return the element `nested` in the list `[1,2,'a','b',[0,0,'nested'],5,'c']`
6. Count the occurrences of `token` on the list  `['rat','dog','cat','token','elephant','token','token']`

###### Using Scripts
1. Write another script called `hello_script.py`. It should take one number as input. If the number is equal to 42 print `Right answer to everything`. If the number is not 42 print `wrong answer`. If the input is not a number print `Sorry, invalid input, expecting number`.

##### Flow Control with Conditionals
1. A script that receives two numbers and prints the lesser of two numbers if both numbers are odd, but prints the greater one if one or both numbers are even!
2. A script that receives two parameters and prints True if the sum of both is 50 or if one of the integers is 20. If not, prints False

##### Loops
1. A script that prints the integers from 1 to 100. For multiples of three print "Fizz" instead , and for the multiples of five print "Buzz". For numbers which are multiples of both print "FizzBuzz"
2. Can you find the maximum or minimum integer value in a list.
3. If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Find the sum of all the multiples of 3 or 5 below 1000.

##### Error
1. Write a script that can convert a string into an int and print its value and type on the console. If the value can't be converted print: `bad string {} couldn't be cast to int`, correctly formatting the message.

##### Files
1. Open and print the titanic train.csv file. Prefix the line by `Male: ` and `Female: ` according to the gender of the person. Output the prefixed text and output the final count for each.

### Fetching Files in the web and cloud
* Let's also take a look of how to obtain files from urls and APIs
* In Big Data, the cloud is often used as a good storage option due to its size scalability, high level of data resilience and availability

1. Write a script that downloads the dataset `http://donnees.ville.montreal.qc.ca/dataset/5829b5b0-ea6f-476f-be94-bc2b8797769a/resource/c6f482bf-bf0f-4960-8b2f-9982c211addd/download/interventionscitoyendo.csv` to your local computer using the techniques seen in the examples.
2. Write a script that download the exchange rate for usd from `https://api.exchangerate-api.com/v4/latest/USD` and cumulatively stores it in a output file. 

### Writing Files
* Let's now take a look of how to write a file using Python

1. Write a script capable of reading all the lines of a csv file
2. It should then validate that each line has the same number of values as the header, any lines with a different number of values as the headers should be saved in a separate list
3. Write back to the same directory a "clean" version of the file
4. Write another file containing only the "invalid" lines of the file              