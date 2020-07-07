# 1.3 Boolean Logic

Here are some questions for you to answer:
* Are the lights in the room you are in on or off?
* Was George Washington the president of the United States?
* Is George Washington the president of the United States today?
* True or False: Most birds can fly.
* Is 3 bigger than 4?
* Is 5 + 5 equal to 10?
* Pick an integer from 0 to 1.
* Is your computer screen on or off?

What do all of these questions have in common? They all have two possible answers: on or off, true or false, yes or no, zero or one. Since computers are made up of tiny wires and switches, they tend to be good at answering questions with only two possible answers. To deal with more complicated questions, the people building and programming computers have to find creative solutions. We will be looking at some of their techniques over the course of this class, but, for now, let's start with the basics.

## Boolean Logic
**Boolean logic**, also called Boolean algebra, is a form of mathematics where the only possible values are true and false. It is named after English mathematician George Boole, who described this form of logic in his book "The Laws of Thought" (published in 1854).

Like more typical forms of algebra, values can be combined together using operators and parentheses into formulas, and variables can even be used in those formulas.

### Boolean Operations
You are familiar with operations in mathematics like addition, subtraction, multiplication, and division. Those operations do not have much meaning in Boolean logic, but Boolean logic does have its own set of operations that can be used to calculate values.

|Operation  |Description    |
|-----------|---------------|
|NOT	    |The opposite of the given value|
|AND	    |Only true if both of the givens are true|
|OR	        |True if one or both of the givens are true<br>Put another way, only false if both of the givens are false|
|XOR (Exclusive Or)|Only true if one of the givens is true, but not both|

### Examples

| | |
|---------------|------------|
|NOT True	    |equals False|
|NOT (NOT True)	|equals True|
|True AND False	|equals False|
|True OR False	|equals True|

## Truth Tables
Occasionally, to help figure out problems, people make tables of the possible answers to a problem. Multiplication tables are a common example. However, no manmade multiplication table can give you every possible solution to the problem a × b. After all, the possibilities for a and b in that example are literally infinite.

However, since Boolean logic has only two possibilities for each value, it is possible, and common, to make tables with every possible combination of values for each Boolean logic formula. These tables are called **truth tables**.

The size of the truth table depends on the complexity of the formula and how many different variables are used. If there is only 1 variable, there will only be 2 rows. If there are 2 variables, there will be 2×2=4 rows. For *n* variables, there will be 2^*n*  rows. (Powers of two will recur frequently in this class.)

### Truth Tables for the Basic Boolean Operations
Here are the truth tables for each of the four Boolean operations described earlier. As you look at them, check to see if the results in the right column match the definitions above.
#### NOT
|P	    |[NOT P](http://www.gilfusion.com/boolean/truthtable.html?expression=NOT%20P)|
|-------|-----|
|True	|False|
|False	|True|
Here, the first column contains our variable, P, and its two possible values beneath, True and False. The second column contains our formula, NOT P. Each row beneath contains what NOT P would be if P was the value in that row: when P is True, NOT P is False, and when P is False, NOT P is True.
#### AND
|P	    |Q	    |[P AND Q](http://www.gilfusion.com/boolean/truthtable.html?expression=P%20AND%20Q)|
|-------|-------|-------|
|True	|True	|True|
|True	|False	|False|
|False	|True	|False|
|False	|False	|False|
This table is a little more complex because it includes two variables, P and Q. In the first two columns, we include every possible different combination that P and Q can have - there are four combinations. Then, the last formula lists in each row what P AND Q would be given the values of P and Q in that row.
#### OR, XOR
|P	    |Q	    |[P OR Q](http://www.gilfusion.com/boolean/truthtable.html?expression=P%20OR%20Q)|
|-------|-------|------|
|True	|True	|True|
|True	|False	|True|
|False	|True	|True|
|False	|False	|False|

|P	    |Q	    |[P XOR Q](http://www.gilfusion.com/boolean/truthtable.html?expression=P%20XOR%20Q)|
|-------|-------|-------|
|True	|True	|False|
|True	|False	|True|
|False	|True	|True|
|False	|False	|False|

## Questions
(Tip: To help with any truth tables, you can use [this interactive truth tables page](http://www.gilfusion.com/boolean/truthtable.html).)
1. What is the value of False AND False?\
    False OR False?\
    False XOR False?
2. Following the pattern above, fill in the truth table below for P AND NOT P. Are there any interesting patterns in the results?
	|P      |NOT P  |P AND NOT P|
    |-------|-------|-----------|
	| True  |   |   |
	| False |   |   |		
3. Fill in the truth table below for P OR NOT P. Are there any interesting patterns in the results?
    |P      |NOT P  |P AND NOT P|
    |-------|-------|-----------|
	|   |   |   |
	|   |   |   |	
4. How many rows would be needed in a truth table for P AND (NOT Q OR (S AND T))? Fill in a partial truth table with at least four of those rows.
	| P|Q|S|T|NOT Q|S AND T|NOT Q OR (S AND T)|P AND (NOT Q OR (S AND T))|
    |-|-|-|-|-----|-------|------------------|--------------------------|
    | | | | | | | | |
    | | | | | | | | |
    | | | | | | | | |
    | | | | | | | | |