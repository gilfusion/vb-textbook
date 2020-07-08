# 3.5 Counter-Controlled Loops
## Not-So-Infinite Loops
Infinite loops work in a few circumstances. Most of the time, however, we do not want our programs to run forever. There are two kinds of loops (that we'll be looking at) that eventually stop: counter-controlled loops, and condition-controlled loops. We will look at condition-controlled loops more closely in our next lesson, but, for now, let's take a look at counter-controlled loops.

## Counter-controlled Loops
**Counter-controlled loops** use a special variable, called the **counter**, that goes up (or down) each time through the loop, until a threshold is reached. For example, if the counter starts at 1 the first time through the loop, and the threshold is 10, the loop will run 10 times.

## A Counter by Any Other Name
Counter-controlled loops are very common in programs, and, as is such, a few names have become common for them over the years. Naming it `counter` is common, as is count. `Index` is another common term, especially when dealing with numbered items in lists, as is the abbreviation `idx`. Also, `i`, `j`, and `k` are sometimes used for counters, for historical reasons. 

It is okay to use these generic names in your programs, but, if you can come up with a more specific, more easily-understood name for your counter variables, by all means, use it.

## The `For` and `Next` Statements
In Visual Basic, while infinite loops could be made using the `Do` and `Loop` statements, counter-controlled loops are typically made with the `For` and `Next` statements. (Because of this, counter-controlled loops are also commonly called **For loops**.) The `For` statement marks the beginning of the loop, and includes the counter variable, the starting value, the ending value, and, optionally, the amount the variable goes up or down each time through the time. The `Next` statement marks the end of the loop, and it can optionally include the counter variable for clarity.

### Some Syntax Forms
```vb
For 𝘤𝘰𝘶𝘯𝘵𝘦𝘳 = 𝘴𝘵𝘢𝘳𝘵 To 𝘦𝘯𝘥

Next
```

```vb
For 𝘤𝘰𝘶𝘯𝘵𝘦𝘳 = 𝘴𝘵𝘢𝘳𝘵 To 𝘦𝘯𝘥

Next 𝘤𝘰𝘶𝘯𝘵𝘦𝘳
```

```vb
For 𝘤𝘰𝘶𝘯𝘵𝘦𝘳 = 𝘴𝘵𝘢𝘳𝘵 To 𝘦𝘯𝘥 Step 𝘴𝘵𝘦𝘱

Next
```

```vb
For 𝘤𝘰𝘶𝘯𝘵𝘦𝘳 = 𝘴𝘵𝘢𝘳𝘵 To 𝘦𝘯𝘥 Step 𝘴𝘵𝘦𝘱
	
Next 𝘤𝘰𝘶𝘯𝘵𝘦𝘳
```

### Example: Counter
```vb
Sub Main
    Dim count As Integer
    For count = 1 To 10
        Console.Clear()
        Console.WriteLine(count)
        Threading.Thread.Sleep(1000)
    Next
End Sub
```
Most of the statements in this program have been placed inside the `For` loop. The `For` loop itself uses a counter named `count` (creatively named, I know), starts at 1 and goes up to 10. Most counters are integers, and, by default, the counter goes up by one each time through the loop. The `Console.WriteLine` command displays the counter, so, each time through the loop, the number displayed goes up by one, from 1 to 10.

### Example: Broken Countdown
```vb
Sub Main
    Dim count As Integer
    For count = 10 To 1
        Console.Clear()
        Console.WriteLine(count)
        Threading.Thread.Sleep(1000)
    Next
End Sub
```

You might assume that this program does the reverse of the previous program and counts down from 10 to 1, but that is not the case. Remember that, by default, `For` loops count up by 1. This also means that, when the program checks to see if it has reached the threshold to stop, it checks if the counter is greater than the threshold. If the counter is greater than the threshold, it stops. Since, in this program, the counter starts greater than the threshold to stop, the code in the loop never runs. The loop stops before the first time through.

### Example: Countdown
```vb
Sub Main
    Dim count As Integer
    For count = 10 To 1 Step -1
        Console.Clear()
        Console.WriteLine(count)
        Threading.Thread.Sleep(1000)
    Next count
End Sub
```
The `For` loop in this program differs from the one in the previous program in two ways. First, this `For` loop includes the Step clause, which specifies how much the counter goes up or down each time through the loop. A side effect of this, if the increment is negative, is that is switches the comparison for the stopping threshold from a greater-than comparison to a less-than comparison. This program will successfully count down from 10 to 1. Also, this For loop also includes the optional labelling of the `Next` statement with the counter variable. This is completely optional and for readability's sake.

### Example: Rectangle
```vb
Sub Main()
    Console.Clear()
    For row = 1 To 5
        For column = 1 To 10
            Console.Write("*")
        Next column
        Console.WriteLine()
    Next row
End Sub
```

This program contains two `For` loops, one counting through rows, and one counting through columns. To keep the code readable, I labelled the `Next` statements in each `For` loop to make it easier to tell them apart. The outer loop displays 5 lines, and the inner loop displays 10 asterisks on each line.

There is one other curious feature of this program--the variables were not created before the `For` loops! The `For` statement can create the counter variable for you if it does not already exist. You can specify the data type of the counter using an As clause (like in a `Dim` statement), or you can let it infer the data type from the start and end values. In this case, `row` and `column` are created automatically as `Integer` variables.

### Example: Square
```vb
Sub Main
    Dim size As Integer
    size = CInt(Console.ReadLine())
    For row = 1 To size
        For column = 1 To size
            Console.Write("*")
        Next column
        Console.WriteLine()
    Next row
End Sub
```

This program adds a twist to the previous one. Before the loops begin, the program reads a number from the console and stores in a variable called `size`. This variable gets used as the ending value for both loops. (Any expression can be used for the starting value, ending value, or step value. They are not at all limited to just integer literals.) This means that the number entered will end up being the size of the square—the number of rows and columns in the square.

### Example: Shenanigans
```vb
Sub Main()
    Dim count As Integer
    For count = 1 To 10
        Console.Clear()
        Console.WriteLine(count)
        Threading.Thread.Sleep(1000)
        count = 1
    Next
End Sub
```

What does this program do? The answer is that it will display 1, and then it will display 2 repeatedly forever. Counters are variables, and they are not special variables, meaning that you can still use them in regular assignment statements, even inside the `For` loops they control. This can lead to easy-to-make, hard-to-find bugs, though, so it is not recommended by any means.

## Questions
```vb
For value = 1 To 25 Step 5
    Console.WriteLine(value)
Next value
```
1. What is the name of the counter in the program snippet above?
2. What numbers will be written to the console by that snippet?

```vb		
Dim count As Integer = 1
start:
If count > 25 Then Goto finish
Console.WriteLine(count)
count = count + 1
Goto start
finish:
```
3. What will be written to the console by the program snippet above?
4. Based on how a For loop works and how the snippet above works, can that snippet be shortened by rewriting it using a For loop? If so, do the rewrite.

## Notes
You can find the official documentation for the For and Next statements [here](https://docs.microsoft.com/en-us/dotnet/visual-basic/language-reference/statements/for-next-statement).