# 3.5b For Loop Shape Challenges

## Template
```vb
Imports System
Public Module ForLoops
    Public Sub Main()
        Dim size = CInt(Console.ReadLine())
        For row = 1 To size
            For col = 1 To size
                Console.Write("*")
            Next
            Console.WriteLine()
        Next
    End Sub
End Module
```

## Challenges
1. Square ■
2. Triangle ◣
3. Triangle ◢
4. Triangle ▲ <br>(Think ◢◣)
5. Diamond ◆
6. Frame □