# 2.6 Functions
## What is a function?
In mathematics, a **function** is a relation such that there is only one output for each input, so each element of the domain is mapped to exactly one element in the range. Functions in programming are similar to functions in mathematics, with some important differences. A function in a program is essentially a subprogram with a result, called the **return value**.

Functions are also methods, meaning that they take in arguments like other methods (and, unlike functions in mathematics, there is no restriction to only one argument—there can be multiple arguments, or none at all).

Functions can be used in two different ways. They can be used like any other method as a command by itself. In this case, although the function may calculate a return value, the result is ignored. They can also be used wherever an expression is used—on the right-hand side of an assignment statement, in another method's argument list, or as part of a calculation.

### Sample Functions
#### The ```System.Console``` object
|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|```ReadLine```	|None	|String<br>(Quoted Text)	|Waits for the user of the program to type something in the console window and press Enter, then returns what the user typed
#### The ```System.Math``` object
|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|```Abs```	|1 Floating-point number	|Floating-point number	|Calculates and returns the absolute value of its argument
|```Cos```	|1 Floating-point number	|Floating-point number	|Calculates and returns the cosine of its argument, assuming its argument is an angle in radians
|```Sin```	|1 Floating-point number	|Floating-point number	|Calculates and returns the sine of its argument, assuming its argument is an angle in radians
|```Sqrt```	|1 Floating-point number	|Floating-point number	|Calculates and returns the square root of its argument
|```Tan```	|1 Floating-point number	|Floating-point number	|Calculates and returns the tangent of its argument, assuming its argument is an angle in radians
* The System.Math object also includes two helpful properties: E and PI.
#### The ```Microsoft.VisualBasic.Conversion``` object
|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|```Hex```	|1 Integer	|String	|Converts an integer from decimal to text containing its hexadecimal form
|```Oct```	|1 Integer	|String	|Converts an integer from decimal to text containing its octal form
|```Val```	|1 String	|Floating-point number	|Converts text to a number, or 0 if the conversion is not possible
Note that, in Visual Studio, the ```Microsoft.VisualBasic``` namespace is imported, so you can abbreviate ```Microsoft.VisualBasic.Conversion``` to just ```Conversion```. (In LINQPad, you would have to import it manually or use the full name.) Also, Visual Basic treats module objects, like the ```Conversion``` object, specially so that you do not need to use dot notation at all and just refer to the methods directly.

### Examples
```vb
System.Console.Title = System.Console.ReadLine()
```
* This command waits for the user to type something and press Enter, then assigns to title of the console window to what they wrote.
```vb
Console.WriteLine(Math.Abs(Conversion.Val(Console.ReadLine())))
```
* Remember from PEMDAS--parentheses first. Starting from the innermost parentheses, ```Console.ReadLine``` waits for the user to type something and press Enter, then ```Conversion.Val``` takes what they typed and converts it to a number. Next, ```Math.Abs``` takes the number from ```Conversion.Val``` and calculates its absolute value, and, finally, ```Console.WriteLine``` takes the absolute value from ```Math.Abs``` and displays it on the console window.
Also, according to the note above ```Conversion.Val``` could be shortened to just ```Val``` if you choose.

## Questions
1. What is a relation such that there is only one output for each input, so each element of the domain is mapped to exactly one element in the range?
2. In programming, what is the term for a method with a result?
3. What is the term for the result of a method?
```vb    
Math.Sqrt(Math.Abs(12 - 24))
```
4. What happens to the return value of the ```Math.Abs``` function in the above command?
5. What happens to the return value of the ```Math.Sqrt``` function in the above command?
```vb
Console.WriteLine(Val(Console.ReadLine()) + 2)
```
6. What would be displayed on the console window after the user typed 7?
7. What would be displayed on the console window after the user typed "dog"?
8. Modify the above line of code to calculate whatever the user typed in squared.