# 3.4 Infinite Loops
## Loops and Infinite Loops
Another common control structure in many computer programs is a **loop**. A loop simply repeats a section of code, either infinitely or until a certain condition is met. Loops can be made using the Goto statement, as was seen in the example in that section.

**Infinite loops**, as the name suggests, continue repeating forever (or until you force the program to quit or turn off the computer, whichever comes first). <span style="color: darkgray">(The street address where Apple Inc.'s headquarters was from 1993 to 2017 is 1 Infinite Loop.)</span>

### Intentional and Unintentional Infinite Loops
Intentional infinite loops are rare - most loops will include some way of exiting the loop, if for no other purpose than gracefully ending the program, but some of these loops do exist. Here are some potential uses for an infinite loop:
* A clock that continually updates the time
* An internet service that is continually available to respond to requests
* Programs running on some devices without an operating system (like games on old video game systems) may need to be able to run until the power is turned off

Unintentional infinite loops are far more common, where the way of exiting the loop was either forgotten or does not work properly.

### The Halting Problem
<span style="color: darkgray">One of the most famous unsolved problems in computer science is the halting problem. This problem asks how to determine, for all possible computer programs, whether the program finishes or not. In 1936, the mathematician Alan Turing wrote a proof demonstrating that the halting problem is unsolvable in the universal case. (Some cases are solvable, but not all of them.) This opened the door for the possibility that some problems cannot be solved, at least using computers and computational theory alone.</span>

## The ```Do``` and ```Loop``` Statements
To deliberately create an infinite loop, you can use the ```Do``` and ```Loop``` statements. (There are variations of these statements that we will learn soon that will eventually stop repeating.) The beginning of the loop is marked with the ```Do``` statement and the end of the loop is marked with the ```Loop``` statement. The statements within the loop are also typically indented to make it easier to see that they are within a control structure.

### Example: Clock
```vb
Sub Main
    Do
        Console.Clear()
        Console.WriteLine(My.Computer.Clock.LocalTime)
        Threading.Thread.Sleep(1000)
    Loop
End Sub
```

In this example, all the other statements in the Main subprogram are placed within the loop. The statements clear the console, display the current time on the console, and wait 1000 milliseconds (or 1 second). Since the program repeats forever, this creates the effect of a clock that updates every second.

## Question
1. Describe three ways learned so far to make the same code repeat “forever”.