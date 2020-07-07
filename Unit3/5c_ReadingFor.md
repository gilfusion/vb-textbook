# 3.5c Reading Code with For Loops

## Snippet #1
```vb
Dim counter As Double
For counter = 0 To 0.5 Step 0.15
    Console.WriteLine(counter)
Next
```
### Questions
1. How many lines are written to the console window by this program snippet?
2. What numbers are written to the console window by this program snippet?
3. What is the value stored in ```counter``` after this program snippet has run?

## Snippet #2
```vb
Const x As Double = 4.2
Const y As Integer = 4
Dim sum As Double = 0.0
For i = 1 To y
    sum = sum + x
Next i
Console.WriteLine(sum)
```
### Questions
4. How many times is the line ```sum = sum + x``` run?
5. What are the names of the constants used in this program snippet?
6. What are the names of the variables created in this program snippet, with their data types?
7. What is written to the console window by this program snippet?
8. Write out a version of this program snippet that performs the same calculation in a different way

## Snippet #3
```vb
Dim product = 1
For times = 1 To 10
    product = product * times
    Console.WriteLine(product)
Next
```
### Questions
9. How many lines are written to the console window by this program snippet?
10. What numbers are written to the console window by this program snippet?

## Snippet #4
```vb
For y = 1 To 5
    For x = 1 To 7
        Console.WriteLine("*")
    Next x
    Console.Write(" ")
Next y
```
### Questions
11. How many asterisks are written to the console window by this program snippet as it is originally? How many lines? How many columns?
12. There is a bug in this program snippet. It does not draw the shape it is supposed to. Change the program snippet to draw the following shape:
    ```
	*******
	*******
	*******
	*******
	*******
    ```

## Snippet #5
```vb
For x = 1 To 5
    For y = 1 To (x - 1) ^ 2
        Console.Write(" ")
    Next y
    For y = (x - 1) ^ 2 To x ^ 2
        Console.Write("*")
    Next y
    Console.WriteLine()
Next x
```
### Questions
13. Draw an approximation of what stars are written to the console window by this program snippet.
14. How many lines are written to the console window by this program snippet? How many columns (at its widest)?
15. Describe the shape of the stars written to the console window by this snippet.