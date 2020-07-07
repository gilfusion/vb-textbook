# 2.7 Data Types

Fundamentally, a computer does three things: loads numbers (from somewhere), performs math operations on those numbers, and stores the resulting numbers (somewhere). One of the big questions that this statement raises is "How do we get from numbers to everything else we see computers handle?" A big part of the answer to that is in data types.

A **data type** specifies the format that data is kept in on the computer--how much space it takes up, and how it is converted to and from its number form. Visual Basic provides access to a wide variety of data types--some we have seen already, and some we have not--and objects themselves can be seen as a kind of data type, since objects can contain information in the form of properties.

Here are some of Visual Basic's built-in data types:

## Integer Data Types
These data types can only hold integers, not fractions. The different integer data types take up different amounts of space on the computer and, as a result, the range of numbers they can hold also varies.
|Data Type  |Range	    |Size in bits 	|Size in bytes|
|-----------|-----------|---------------|-------------|
|```Byte```	    |0 to 255	|8	            |1
|```Short```	    |-32,768 to 32,767	|16	|2
|```Integer```	|-2,147,483,648 to 2,147,483,647	|32	|4
|```Long```	    |-9,223,372,036,854,775,808 through 9,223,372,036,854,775,807	|64	|8

<div style="color: gray">
(Each of these data types, with the exception of Byte, is signed—you can have positive or negative numbers. If you do not need negative numbers and want a higher range, Visual Basic also includes unsigned variants of these data types called ```UShort```, ```UInteger```, and ```ULong```, and if you really want a signed variant of ```Byte```, there is ```SByte``` available, too.)

(Have you heard of 32-bit and 64-bit computers? 32-bit computers do their arithmetic naturally on 32-bit numbers, and that is why 32 bits was chosen for the length of Integer. Bytes and short integers are usually added up as 32-bit Integers and shrunk back down, while slightly more complex formulas are used to make long integers work. 64-bit computers also do 64-bit arithmetic naturally, and a growing percentage of computers today are 64-bit computers.)
</div>
Most of the time in this class, if we need an integer data type, it will be ```Integer```. If you write a number in your code that is in the range for the ```Integer``` data type and does not have a decimal point, Visual Basic will store that number as an ```Integer``` unless you say otherwise.

## Floating Point Data Types
In math or science classes, you may have learned about the concept of **scientific notation**. The number 0.0000047 can be rewritten as 4.7×10^(−6). (Computers will often display this as 4.7E-6, where the "E" stands for "exponent".) **Floating point** data types hold both really large numbers and small fractions using a binary form of scientific notation. Visual Basic includes two floating point data types.
|Data Type	|Range (Biggest possible numbers)	|Precision (Smallest possible nonzero numbers)	|Size in bits	|Size in bytes|
|---|---|---|---|---|
|```Single```	|±-3.4028235E+38 	|±1.401298E-45	|32	|4
|```Double```	|±1.79769313486231570E+308	|±4.94065645841246544E-324	|64	|8

Floating point data types also have special values for representing positive and negative infinity and values that are not actual numbers.

Most of the time in this class, if we need a floating point data type, it will be ```Double``` (but I cannot promise that I will not slip up and use ```Single``` every once in a while). If you write a number in your code that has a decimal point, Visual Basic will store that number as a ```Double``` unless you say otherwise.

## Character Data Types
A **character** is a single symbol either stored on the computer or displayed on the screen. It may be a letter, a digit, a punctuation mark, or something else. Characters are converted to numbers using a **character set** and an **encoding**, which we learned about in the last unit. The character set that Visual Basic uses is called Unicode and the encoding it uses is called UTF-16, which means, appropriately enough, that most characters take up 16 bits or 2 bytes.

Visual Basic has two character data types: ```Char```, which contains one character, and ```String```, which contains many characters "strung" together to make text. Any time you type something in double-quotes in Visual Basic, you are making a String.

## Other Data Types
The ```Boolean``` data type stores a single True/False value. It can be stored in a single bit, but the amount of storage actually taken depends on the computer.
There is also a ```Date``` data type that stores dates and times. You can create dates in Visual Basic by typing the date and/or time between hash symbols, like ```#12/7/1941#``` or ```#3:00 PM#```, as we learned in our lesson on expressions.

## Identifying Data Types from Code
The ```Microsoft.VisualBasic.Information``` object has a function named TypeName that gives you a string containing the name of the data type of whatever was passed in as an argument.

### Examples
|Expression	                                |Result |
|-------------------------------------------|------ |
|```Information.TypeName(47)```	            |Integer|
|```Information.TypeName(#2017-10-22#)```	|Date   |
|```Information.TypeName(False)```	        |Boolean|

## Questions
1. What data type is ```"Hello, World!"```?
2. What data type is ```True```?
3. What data type is ```#2000-01-01#```?
4. How many bits are taken up by the number ```1```?
5. How many bits are taken up by the number ```1.0```?
6. What is the smallest data type you could use to hold a whole number from 1 to 100?
7. What is the smallest data type you could use to hold a fraction from 0 to 1?