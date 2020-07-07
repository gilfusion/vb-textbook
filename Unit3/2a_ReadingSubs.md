# 3.2a Reading Code with Subprograms

Directions: Fill in the console output of each code example given.

### Snippet #1
```vb
Sub Main()
    WriteGreeting()
    Console.WriteLine(" How are you today?")
End Sub
Sub WriteName()
    Const Name As String = "Bob"
    Console.Write(Name)
End Sub
Sub WriteGreeting()
    Const Welcome = "Greetings! "
    Console.Write(Welcome)
    WriteName()
End Sub
```

### Snippet #2
```vb
Sub Main()
    Console.Write("Enter a number: ")
    WriteMyNumber()
    Dim yourNumber = Val("seventeen")
    Console.Write("Your number is ")
    Console.WriteLine(yourNumber)
End Sub
Sub WriteMyNumber()
    Dim myNumber = (Math.PI \ 1) * 2
    Console.Write("My number is ")
    Console.WriteLine(myNumber)
End Sub
```

### Snippet #3
```vb
Sub First()
    Console.WriteLine("I")
End Sub
Sub Second()
    Console.WriteLine("II")
End Sub
Sub Main()
    Third()
    Second()
    First()
End Sub
Sub Third()
    Console.WriteLine("III")
End Sub
```

### Snippet #4
```vb
Sub Main()
    Console.WriteLine("Hello")
    Main()
End Sub
```