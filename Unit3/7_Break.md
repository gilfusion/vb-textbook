# 3.7 Breaking Out of Loops

The loops we have looked at so far only let you exit the loop in between cycles. This can occasionally lead to slightly awkward code like the average example in the previous section, where the same check needed to be performed twice, once in the Do While statement and again in an If statement inside the loop.

To do this, we will use an `Exit` statement, also referred to as a **break statement** (in many other programming languages, the keyword using for this statement is break). Visual Basic includes multiple versions of the Exit statement, depending on what you are trying to break out of: `Exit Do` exits `Do` loops, `Do While` loops, and `Do Until` loops, while `Exit For` exits `For` loops. There is also an `Exit Sub` statement to exit the current subroutine.

## Example: Average
```vb
Dim sum = 0
Dim count = 0
Dim input = 0
Do
    input = Val(Console.ReadLine())
    If input < 0 Then
        Exit Do
    End If
    sum = sum + input
    count = count + 1
Loop
Dim average = sum / count
Console.WriteLine("Average: " & average)
```
Here is the average example from the last section rewritten using `Exit Do`.

Some programmers oppose the use of break statements, considering them little better than `Goto`s. These programmers prefer **Single Entry/Single Exit control flow**, where there is only one way to get into the loop (from the beginning) and there is only one way to get out of the loop (by the condition or counter). This is a programming philosophy that some programmers believe in and others find impractical.

## Questions
```vb
For x = 1 To 20
    If x > 10 Then
        Exit For
    End If
    Console.WriteLine("Hey there!")
Next
```
1. How many times does the program snippet above write the phrase “Hey there!” to the console?
2. Rewrite the program snippet to omit the Exit For statement.
```vb
Dim number = 100
Do
    If number < 10 Then
        Exit Do
    End If
    Console.WriteLine(number)
    number = number / 2
Loop
```
3. What number(s) does the program snippet above write on the console?
4. Rewrite the program snippet to omit the `Exit Do` statement.