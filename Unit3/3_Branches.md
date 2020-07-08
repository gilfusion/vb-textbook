# 3.3 Conditional Branches

Earlier in this unit, we learned that a `Goto` statement is what was known as an **unconditional branch** – it moves the control flow to another point in this program whenever the statement is reached. In this lesson, we will look at **conditional branches**. Conditional branches split the control flow in different directions based on whether a **condition** is true or false.

Conditional branches are extremely common in programming. They allow the computer to make “decisions” based on criteria the programmer decides. For example, a program might ask its user for a password and use a conditional branch to either continue if the password is correct or display a message like “wrong password” if the password is wrong.

## Boolean Logic
In past units, we have looked at Boolean logic (or Boolean algebra). One of the primary uses of Boolean algebra in programming is to provide the conditions used in conditional branching.
Any expression with a Boolean result can be used as a condition in a conditional branch. Comparison expressions are common (like `password = "Abc123"`), but there are others, including some functions and properties with Boolean results.

### Boolean Functions and Properties
#### The `Microsoft.VisualBasic.Information` object
|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|`IsDate`	|1 String	|Boolean	|Checks to see if the string can be converted to a date
|`IsNumeric`	|1 String	|Boolean	|Checks to see if the string can be converted to a number

#### The `My.Computer.FileSystem` Object
|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|`DirectoryExists`	|1 String	|Boolean	|Checks to see if a directory (folder) with that name already exists
|`FileExists`	|1 String	|Boolean	|Checks to see if a file with that name already exists

#### The `My.Computer.Network` Object
|Property	|Expected kind of data	|Description|
|-----------|-----------------------|-----------|
|`IsAvailable`	|Boolean	|Whether or not the computer is connected to a network (This property is read-only; you cannot use it on the LHS of an assignment statement.)

### Short-circuiting logical operators
In the last unit, we learned about the `Not`, `And`, `Or`, and `Xor` operators. Visual Basic includes two more: `AndAlso` and `OrElse`. `AndAlso` has the same truth table as `And`, and `OrElse` has the same truth table as `Or`, but these new operators have an important difference.

Given the expression `5 / x < 1`, what is the result if x = 0? The answer is that, depending on the setting, the program might crash[¹](#footnote1). Since we know that 5⁄0 = ∞, and infinity is definitely not less than 1, we can try to rewrite the condition as `x <> 0 AndAlso 5 / x < 1`. What `AndAlso` does is check the first operand (the `x <> 0`) and, if it is false, it knows that it is impossible for the result to be true, so it doesn’t even look at the other side. (Remember that And can only be true if both are true; if one of them is false, the overall result is false.) `OrElse` has a similar “short-circuiting” behavior if the first operand is true.

## The `If`-`Then` Statement
The simplest form of conditional branching in Visual Basic is performed using `If`-`Then`. If the condition is met, the statements between the If and End If are run. If the condition is not met, they are skipped.

### Syntax
```vb
If 𝘤𝘰𝘯𝘥𝘪𝘵𝘪𝘰𝘯 Then
    'statements
End If
```

### Short Form
If you only need to fit put statement between the `If` and `End If`, you can choose to drop the `End If` statement and put that one thing you want to run on the end of the `If` Statement.
```vb
If 𝘤𝘰𝘯𝘥𝘪𝘵𝘪𝘰𝘯 Then … 'Only one statement
```
Some versions of BASIC prior to VB only had the short form (and some only let you put a `GoTo` statement in them). Today, though, use of the short form is generally discouraged.

### Example: Testing Input
```vb
Dim input As String
Dim inputNumber As Double
Dim result As Double
input = Console.ReadLine()
If Information.IsNumeric(input) Then
    inputNumber = Conversion.Val(input)
    result = inputNumber ^ 2
    Console.WriteLine(result)
End If
If Not Information.IsNumeric(input) Then
    Console.WriteLine("You didn't type a number!")
End If
```
This program snippet lets a user type a number into the console and displays the square of that number. In case the user decided not to type a number in (or they hit a wrong key by mistake), the snippet will tell them that what they typed was not a number. `If` statements are very common for making sure that people type into the program what they are supposed to type.

## `If`-`Then`-`Else` Block and Statement
A slightly more complicated form of branching is `If`-`Then`-`Else`. Here, if the condition is True, the statements between the `If` and `Else` are run. If the condition is False, the statements between the `Else` and `End If` are run. This is helpful if you want to do two different things under two opposite circumstances. This can often be done with two separate If blocks, but having an `If` and `Else` is generally more efficient and, in some cases, more readable.

### Syntax
```vb
If 𝘤𝘰𝘯𝘥𝘪𝘵𝘪𝘰𝘯 Then
    'Statements
Else
    'Other statements
End If
```

### Example #1: Testing Input
Here is the earlier example, rewritten to use If-Then-Else.
```vb
Dim input As String
Dim inputNumber As Double
Dim result As Double
input = Console.ReadLine()
If Information.IsNumeric(input) Then
    inputNumber = Conversion.Val(input)
    result = inputNumber ^ 2
    Console.WriteLine(result)
Else
    Console.WriteLine("You didn't type a number!")
End If
```
It is one line shorter than the previous version, since we no longer need two `End If`s. Also, `Else` is much shorter than `If Not Information.IsNumeric(input) Then`.

### Example #2: If Sort
This program lets the user type in two numbers and displays the two numbers in ascending order, no matter which order the user typed them.
```vb
Dim first As Double
Dim second As Double
first = Conversion.Val(Console.ReadLine())
second = Conversion.Val(Console.ReadLine())
If first < second Then
    Console.WriteLine(first)
    Console.WriteLine(second)
Else
    Console.WriteLine(second)
    Console.WriteLine(first)
End If
```

## Questions
1. Could the expression `x <> 0 And 12 \ x <> 0` result in a program crash? If so, how would you fix it?
2. Write an expression that checks if the folder “C:\Windows\System32” exists.
3. What is the output of the If Sort program above if the user enters 3 followed by 5? What if the user entered 7 followed by 4?
4. Write a statement that safely checks if x ÷ y is equal to 0.
5. Write a program snippet that displays “OK” on the console if the variable input can be converted to a number.
	
## Notes
You can find the official documentation for the If-Then-Else statement [here](https://docs.microsoft.com/en-us/dotnet/visual-basic/language-reference/statements/if-then-else-statement).
	
¹ <a id="footnote1"></a> The result of `x / y` is always a `Double`, so `x / 0` results in `∞`. The result of `x \ y`, however, is an `Integer`, which cannot be ∞, so `x \ 0` results in a program crash.