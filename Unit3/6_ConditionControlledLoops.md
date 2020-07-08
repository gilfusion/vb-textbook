# 3.6 Condition-Controlled Loops

**Condition-controlled loops** repeat a section of code, and whenever they reach the beginning (or the end) of the loop, they check a Boolean condition to see if the loop should continue. Visual Basic includes several condition-controlled loops, and we will be looking at two of them.

## The `Do While` and `Loop` Statements
```vb
Do While 𝘤𝘰𝘯𝘥𝘪𝘵𝘪𝘰𝘯

Loop
```
The `Do While`…`Loop` block repeats as long as the condition is true. The condition is checked before entering the loop the first time and before each time it repeats. If, when the condition is checked, it is false, the loop stops repeating, and the program continues running after the `Loop` statement. (Since the condition is checked before the loop is entered the first time, it is possible that the code in the loop may never be run.)

### Example: Countdown
```vb
Dim counter = 10
Do While counter > 0
    Console.WriteLine(counter)
    counter = counter - 1
Loop
```
This sample is another way of making a countdown. The counter starts at 10. Then, on starting the loop, the computer checks to see if the counter is greater than 0. Since it is, it then runs the code in the loop, displaying the number and changing the counter down to 9. The loop repeats, checking the counter again each time before going back through.

## The `Do Until` and `Loop` Statements
```vb
Do Until 𝘤𝘰𝘯𝘥𝘪𝘵𝘪𝘰𝘯

Loop
```
The `Do Until`…`Loop` block is the same as the `Do While`…`Loop` block, except that it repeats until the condition is true, or it repeats as long as the condition is false. Another way of writing the exact same loop, therefore, would be:
```vb
Do While Not 𝘤𝘰𝘯𝘥𝘪𝘵𝘪𝘰𝘯

Loop
```
The `Do Until`…`Loop` block exists mostly for convenience and readability's sake.

### Example: Countdown
```vb
Dim counter = 10
Do Until counter = 0
    Console.WriteLine(counter)
    counter = counter - 1
Loop
```
Here is the countdown example from above, rewritten to use `Do Until`. While the example above repeats as long as the counter was greater than zero, this one repeats until the counter equals zero.[¹](#footnote1)

## More Examples
### Example: Typing Commands
```vb
Dim command = ""
Do Until command = "exit"
    command = Console.ReadLine()
    If command = "north" Then
        MoveNorth()
    ElseIf command = "south" Then
        MoveSouth()
    ElseIf command = "west" Then
        MoveWest()
    ElseIf command = "east" Then
        MoveEast()
    End If
Loop
```

This example, based on code commonly found in many text-based computer games, combines `Do Until` with `If` and `ElseIf`. The player of the game is asked to type a command. If they type “north”, “south”, “east”, or “west”, the game would do something to move them in that direction (the actual code for that is placed in subroutines I did not include here). The player will be able to keep entering commands until they type “exit”. At that point, the game would end.

### Example: Average
```vb
Dim sum = 0
Dim count = 0
Dim input = 0
Do While input >= 0
    input = Val(Console.ReadLine())
    If input >= 0 Then
        sum = sum + input
        count = count + 1
    End If
Loop
Dim average = sum / count
Console.WriteLine("Average: " & average)
```

This code snippet lets the user of the program type as many numbers as they want, and, once they type a negative number, it exits and shows the average of all the numbers they typed.

## Questions
1. One quirk of the average example above is that `input >= 0` is checked twice, once in the `Do While` statement and once in the `If` statement. What would happen if the `If` and `End If` statements were removed? Try the code snippets both ways with this sample data: 5, 0, 10, 7, and -2.

```vb
Do While DateTime.Now.Hour < 15
    Console.WriteLine(DateTime.Now)
    System.Threading.Thread.Sleep(60000)
Loop
```
2. Assuming the program snippet above is started at 12:30 PM, when does it finish?
3. How often does the program snippet display a message?

## Notes
¹ <a id="footnote1"></a> What if the counter was less than zero? In this example, we can determine that the counter should never be less than zero, but could also change the `=` to `<=` if we want to be extra sure.