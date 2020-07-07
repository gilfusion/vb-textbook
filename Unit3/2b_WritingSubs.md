# 3.2b Writing Code with Subprograms

Subprograms have two main purposes:
* To give names to parts of the program to make it easier to identify what those parts of the program do.
* To reduce repetition in a program - if a relatively complex set of steps is done multiple times, it may be better to move those steps into a subprogram that can be called whenever those steps need to be done.
With this in mind, rewrite the programs below with more subprograms. Use Visual Studio and/or LinqPad to help you.

## Snippet #1
```vb
Dim inputStr As String
Dim firstNumber As Double
Dim secondNumber As Double
Dim thirdNumber As Double
Dim fourthNumber As Double
Dim fifthNumber As Double
Dim average As Double
Sub Main()
    Console.WriteLine("Enter a number: ")
    inputStr = Console.ReadLine()
    firstNumber = Val(inputStr)
    Console.WriteLine("Enter a number: ")
    inputStr = Console.ReadLine()
    secondNumber = Val(inputStr)
    Console.WriteLine("Enter a number: ")
    inputStr = Console.ReadLine()
    thirdNumber = Val(inputStr)
    Console.WriteLine("Enter a number: ")
    inputStr = Console.ReadLine()
    fourthNumber = Val(inputStr)
    Console.WriteLine("Enter a number: ")
    inputStr = Console.ReadLine()
    fifthNumber = Val(inputStr)
    average = (firstNumber + secondNumber + 
               thirdNumber + fourthNumber + 
               fifthNumber) / 5
    Console.WriteLine("The average is " & average)
End Sub
```

## Snippet #2
```vb
Dim angle As Double = 0.0
Sub Main()
    Console.WriteLine("Unit Circle")
    Console.WriteLine("==== ======")
    Console.WriteLine()
    Console.WriteLine("Angle: " & angle)
    Console.WriteLine("Sine: " & Math.Sin(angle))
    Console.WriteLine("Cosine: " & Math.Cos(angle))
    Console.WriteLine("Tangent: " & Math.Tan(angle))
    Console.WriteLine()	
    angle = Math.PI / 2
    Console.WriteLine("Angle: " & angle)
    Console.WriteLine("Sine: " & Math.Sin(angle))
    Console.WriteLine("Cosine: " & Math.Cos(angle))
    Console.WriteLine("Tangent: " & Math.Tan(angle))
    Console.WriteLine()	
    angle = Math.PI
    Console.WriteLine("Angle: " & angle)
    Console.WriteLine("Sine: " & Math.Sin(angle))
    Console.WriteLine("Cosine: " & Math.Cos(angle))
    Console.WriteLine("Tangent: " & Math.Tan(angle))
    Console.WriteLine()	
    angle = 3 * Math.PI / 2
    Console.WriteLine("Angle: " & angle)
    Console.WriteLine("Sine: " & Math.Sin(angle))
    Console.WriteLine("Cosine: " & Math.Cos(angle))
    Console.WriteLine("Tangent: " & Math.Tan(angle))
    Console.WriteLine()	
End Sub
```