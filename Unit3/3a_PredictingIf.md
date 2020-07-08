# 3.3a Predicting If-Then-Else Results

Below are six program snippets. To the right of each snippet are five possible inputs that someone could enter via `Console.ReadLine`. Find and write down the outputs of each program (what is displayed using `Console.WriteLine`).

## Snippet #1
```vb
Dim grade As Integer
grade = Conversion.Val(Console.ReadLine())
If grade >= 65 Then
    Console.WriteLine("You pass!")
Else
    Console.WriteLine("You failed.")
End If
```
|Input	|Output|
|-------|------|
|15
|64
|65
|70
|150

## Snippet #2
```vb
Dim number As Double
number = Conversion.Val(Console.ReadLine())
If number >= 0 Then
    Console.WriteLine(Math.Sqrt(number))
Else
    Console.WriteLine("Imaginary")
End If
```
|Input	|Output|
|-------|------|
|144
|-169
|36
|0
|-1

## Snippet #3
```vb
Dim input As String
Dim inputNumber As Double
input = Console.ReadLine()
If Information.IsNumeric(input) Then
    inputNumber = Conversion.Val(input)
    If inputNumber < 10 Then
        Console.WriteLine(inputNumber)
    Else
        Console.WriteLine(inputNumber - 10)
    End If
Else
    Console.WriteLine(input.ToUpper())
End If
```
|Input	|Output|
|-------|------|
|hello
|25
|WELCOME!
|-2
|1

## Snippet #4
```vb
Dim grade As Integer
grade = Conversion.Val(Console.ReadLine())
If grade >= 65 Then
    If grade > 100 Then
        Console.WriteLine("What?")
    Else
        Console.WriteLine("You passed!")
    End If
Else
    If grade = 0 Then
        Console.WriteLine("What happened?")
    Else
        Console.WriteLine("You failed.")
    End If
End If
```
|Input	|Output|
|-------|------|
|0
|15
|65
|100
|150

## Snippet #5
```vb
Const distance = 25
Dim time As Double
time = Conversion.Val(Console.ReadLine())
If time = 0 Then
    Console.WriteLine("That’s impossible!")
Else
    Dim speed = distance / time
    If speed > 50 Then
        Console.WriteLine("That’s fast!")
    Else
        Console.WriteLine("Not bad.")
    End If
End If
```
|Input	|Output|
|-------|------|
|fast
|0
|-0.5
|0.25
|5

## Snippet #6
```vb
Dim letter As String
Dim letterCode As Integer
letter = Console.ReadLine()
letterCode = Strings.AscW(letter)
If letterCode < &H20 Then
    Console.WriteLine("Control Character")
ElseIf letterCode = &H20 Then
    Console.WriteLine("Space")
ElseIf letterCode >= &H30 AndAlso 
       letterCode <= &H39 Then
    Console.WriteLine("Digit")
ElseIf letterCode >= &H41 AndAlso
       letterCode <= &H5A Then
    Console.WriteLine("Uppercase")
ElseIf letterCode >= &H61 AndAlso
       letterCode <= &H7A Then
    Console.WriteLine("Lowercase")
Else
    Console.WriteLine("Punctuation")
End If
```
|Input	|Output|
|-------|------|
|57
|HELLO!
|.com
|&nbsp;&nbsp;&nbsp;&nbsp;this
|3D!!!