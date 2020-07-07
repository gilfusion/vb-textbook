# 2.8a Reading Code with Variables

## Problem #1
Below is a program snippet. Beside each line of code, write down what each variable contains after that line has executed. If the variable has not been changed by the line of code, you may leave it blank to save time. If the variable does not exist yet, write a line across the box.
|Code   |numStr |num	|sum	|count	|average    |
|-------|-------|-------|-------|-------|-----------|
|```Console.WriteLine("Welcome To My App")```
|```Dim numStr As String = ""```
|```Dim num As Double = 0.0```
|```Dim sum = 0.0```
|```Dim count As Integer = 0```
|```Dim average = 0.0```
|```numStr = "15"```
|```num = Conversion.Val(numStr)```
|```sum = sum + num```
|```count = count + 1```
|```numStr = "12a"```
|```num = Conversion.Val(numStr)```
|```sum = sum + num```
|```count = count + 1```
|```numStr = "abc"```
|```num = Conversion.Val(numStr)```
|```sum = sum + num```
|```count = count + 1```
|```average = sum / count```
|```Console.WriteLine(average)```

## Problem #2
Below is a program snippet. Beside each line of code, write down what each variable contains after that line has executed. If the variable has not been changed by the line of code, you may leave it blank to save time. If the variable does not exist yet, write a line across the box.

|Code	|whole	|first	|rest	|test   |
|-------|-------|-------|-------|-------|
|```Console.WriteLine("Welcome To My App")```
|```Dim whole = ""```
|```Dim first = ""```
|```Dim rest = ""```
|```first = "v"```
|```rest = "iSUAL"```
|```whole = first.ToUpper() & rest.ToLower()```	
|```first = "b"```
|```rest = "aSiC"```
|```whole = first.ToUpper() & rest.ToLower()```
|```Dim test = whole.Contains("V")```
|```Console.WriteLine(test)```
|```test = whole.Contains("c")```
|```test = whole.Contains("C")```
|```test = whole.StartsWith("c")```
|```test = test Or whole.EndsWith("c")```
|```Console.WriteLine(test)```