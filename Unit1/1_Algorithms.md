# 1.1 Algorithms

## What is an algorithm?
<a name="algorithm"></a>An **algorithm** is the list of steps needed to calculate the solution to a problem. This definition includes several components, as we will look at below:
- List of steps: A computer can, with some exceptions, only do one thing at a time. Therefore, any algorithm that a computer must perform should be planned to do only one thing at a time.[¹](#footnote1)
- Calculate: Fundamentally, a computer does three things: loads numbers (from somewhere), performs math operations on those numbers, and stores the resulting numbers (somewhere). Any algorithm that a computer must perform must be described in terms of moving numbers around or performing some form of mathematics or logic.
- Solution to a problem: The term problem here has a very broad meaning. You can think of a math problem from your homework as an example of a problem a computer program can solve. You can think of needing a piece of information as a problem a computer program (like an Internet search engine) can solve. You can even think about being bored as a problem a computer program can solve. That's why we have computer games! Some of these programs are simple and can be solved with only a few steps, while others are extremely complex and many require dozens, hundreds, thousands, or even millions of steps to solve!

Algorithms, depending on how they are going to be used, can be written in any number of ways. Code in programming languages is used when we want the algorithm to be in a form we want the computer to understand, but we can write it out in English for our own benefit first, to figure out how it works.

For the first half of this unit, we will be looking at algorithms written in plain English, for the most part, and you will be writing some algorithms of your own.

## Reading a sample algorithm
Let's look at a sample algorithm. Try to follow the steps to see what kind of answer you get. Look at the table below. You will be filling in and changing what’s in the value column throughout the algorithm.

|Label  |Value  |
|-------|-------|
|Input 1|       |
|Input 2|       |
|Temp A |       |
|Temp B |       |
|Temp C |       |

1. First, choose two numbers, and write them in the values for Input 1 and Input 2.
2. Write the number 1 in the value for Temp A.
3. Copy the value from Input 1 to Temp B.
4. Copy the value from Input 2 to Temp X.
5. If the value for Temp X is 0, go to step 9.
6. Multiply the values for Temp A and Temp B and put the answer in Temp A, replacing whatever value is already there.
7. Subtract 1 from the value for Temp X and put the answer back in Temp X, replacing whatever value is already there.
8. Go to step 5.
9. You are all done!

### Questions
(Tip: You can use an [interactive version of this algorithm](http://www.gilfusion.com/algorithms/algorithms.html) to help with the questions.)
1. What are the values stored in the Temp A, Temp B, and Temp X at the end of this algorithm when the numbers are 2 and 2? 3 and 2? 4 and 2? 5 and 2?
2. Write a mathematical formula that summarizes the relationship between three of the values at the end of the algorithm.
3. Try this algorithm a couple of more times with different combinations of numbers of your choice. (It is easier to do with smaller numbers, say, less than or equal to 5.) Do the results match the prediction of your mathematical formula?

## Writing a sample algorithm
Following the format above, can you complete this algorithm so that, at the end, Temp A contains the factorial of N? *(In case you have forgotten or do not know, the factorial of a number is the product of all the whole numbers up to that number – the factorial of 5, written as 5! , is 1×2×3×4×5. Another hint for this algorithm would be to consider the commutative property – 5! Is also 5×4×3×2×1.)*

|Label  |Value  |
|-------|-------|
|Input  |       |
|Temp A |       |
|Temp N |       |

1. First, choose a number, and write it in the value for Input.
2. Write the number 1 in the value for Temp A.
3. Copy the value from Input 1 to Temp N.
4. …

## Notes
¹ <a id="footnote1"></a>Again, there are exceptions, but those can get very, very, **very** complicated and are outside the scope of this class.