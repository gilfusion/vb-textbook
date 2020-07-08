# 3.2 Subprograms

Modern computer software often performs many different tasks. Try to count each button in the latest version of Microsoft Word, and you will see what I mean. Keeping track of all of that functionality can be very difficult in one long program, so a number of features have been developed over the years to allow programmers to split up their programs into more manageable chunks. One of these features is subprograms.

A **subprogram** (also sometimes called a **procedure** or **subroutine**) is a small segment of a program that performs a specific task[¹](#footnote1).  Subprograms can then be used elsewhere in the program to perform that task as a step of that part of the program. As we learned in the previous unit, methods and functions are made using subprograms.

## How Subprograms Work
Subprograms also change the control flow of the program, redirecting it from one part of the program into the subprogram, then, once the subprogram is done, the control flow goes back to where it left off in the other part of the program.

To do this, when your program goes into the subprogram, it keeps track of where it was in a part of memory called the **stack**. Every time a subprogram is used (and subprograms can use other subprograms), a layer is added to the stack, and every time a subprogram is done, it goes back to the stack to remember where it was, go back there, and remove that layer from the stack. (In theory, if your program went into a lot of subprograms, the memory for the stack could fill up completely, leading to an error called a **stack overflow**. Given how much memory computers have today, this should not be a problem in most working programs, but mistakes can sometimes still lead to stack overflows.)

## Sub Main
Every Visual Basic console application you have created so far has included one subprogram: the Main subprogram. This is the subprogram that Windows uses to start your program.
```vb
Sub Main()

End Sub
```
Now we know that the `Sub` in `Sub Main` stands for subprogram or subroutine. Everything between the `Sub` statement and the `End Sub` statement is part of the Main subprogram.

## Event Handlers
Other Visual Basic project types like Windows Form or WPF applications use different subprograms to respond to different events.
```vb
Private Sub ApplyButton_Click(sender As Object, e As EventArgs) Handles ApplyButton.Click

End Sub
```
The important things to note here are the `Sub` for subprogram and the `Handles ApplyButton.Click` that connects the subprogram to the event.[²](#footnote2)

## Creating Other Subprograms
Creating a simple subprogram is straightforward: inside the module and outside the other subprograms, insert the keyword `Sub` followed by the name of the subprogram (which follows the same rules as the name for a variable) and an optional pair of parentheses. The end of the subprogram is marked by an `End Sub` statement.

### Example
```vb
Module Module1
    Sub Main()

    End Sub

    Sub DoSomething()

    End Sub
End Module
```
This example creates a subprogram named `DoSomething`. Most subprograms tend to be named with a verb or verb phrase. (`Main` is an exception.)

## Calling Other Subprograms
The term used for using a subprogram is **calling** the subprogram. Visual Basic includes a few options for calling subprograms. The simplest is to use the name of the subprogram, followed by a pair of parentheses. (The parentheses are even optional.) For cases where the simple case may confuse the computer, Visual Basic also includes the `Call` statement. To use the `Call` statement, insert the keyword `Call` followed by the name of the subprogram and the pair of parentheses. (`Call` can also be used to call methods of objects - just insert the keyword `Call` before the command as you would normally write it.)

### Examples
```vb
Sub Main
    DoSomething        'without parentheses
    DoSomething()      'with parentheses
    Call DoSomething   'with Call but no parentheses
    Call DoSomething() 'with Call and parentheses
End Sub

Sub DoSomething
    Call Console.WriteLine("Hello, World!")
End Sub
```

## Recursion
Can a subprogram call itself? Yes. The term for this is **recursion**. When a subprogram calls itself, it adds a new layer to the stack and gets fresh variables for that run through the subprogram. The second run of the subprogram will eventually reach that call again, though, add another layer to the stack, and start a third time. Since, at this point, we don't know how to stop the subprogram from calling itself, it will continue until the stack overflows and your program crashes. So, let's not do that.

Can a subprogram call the `Main` subprogram again? Yes, it can. However, at this point, we should not do that either, since this will lead to an indirect form of recursion, with alternating layers of `Main` and the other subprogram until the stack overflows.

Recursion is a legitimate programming technique, but we are not yet ready for it.

## Question
1. A medieval combat game includes subprograms for the player to make a choice and subprograms for attacking, retreating, and using a catapult. The main subprogram calls the choice subprogram, and the choice subprogram calls the attack, retreat, and catapult subprograms. Write the code for *creating* and *calling* those subprograms. You do not need to fill in the rest of the subprograms.
		
## Notes
¹ <a id="footnote1"></a> Sources: http://www.dictionary.com/browse/subroutine and https://en.wikipedia.org/wiki/Subroutine\
² <a id="footnote2"></a> The declarations in parentheses are optional, as is the `Private` keyword. We may take a look at those later.