# 3.5d Reading and Writing Code with For Loops

## Snippet #1
```vb
For time = 80 To 1 Step -1
    Console.Clear()
    For x = 1 To time
        Console.Write("*")
    Next
    Threading.Thread.Sleep(100)
Next time
Console.WriteLine()
Console.WriteLine("Press any key...")
Console.ReadKey(True)
```
### Questions
1. Describe what this program snippet does.
2. About how much time (in seconds) does it take for the program to reach the “Press any key…” message?
3. Adjust the code so that it takes the program 1 whole minute to reach the “Press any key…” message. (Try to keep the number of stars displayed the same.)

## Snippet #2
```vb
Console.Write("Enter number of grades: ")
Dim count = Val(Console.ReadLine())
Dim sum = 0.0
For time = 1 To count
    Console.Write("Enter a grade:")
    Dim grade = Val(Console.ReadLine())
    sum = sum + grade
Next
Dim average = sum / count
Console.Write("The average is ")
Console.WriteLine(average)
Console.WriteLine("Press any key...")
Console.ReadKey(True)
```
### Questions
4. Describe what this program snippet does.
5. Write the names of all the variables created in this program snippet, along with their data types.

## Snippet #3
```vb
Dim base = Val(Console.ReadLine())
Dim exp = Val(Console.ReadLine())
 
Dim product As Double = ___

    product = product * ___

Console.Write("The answer is: ")
Console.WriteLine(product)
Console.WriteLine("Press any key...")
Console.ReadKey(True)
```
### Questions
6. The program snippet to the left is supposed to use a loop to calculate an exponent. Finish the program snippet (add the loop and fill in the two blanks). A sample calculation is below.\
5⁴=5×5×5×5=625

## Snippet #4
```vb
Dim n = Val(Console.ReadLine())
Dim product As Double = ___

    product = product * ___

Console.Write("The answer is: ")
Console.WriteLine(product)
Console.WriteLine("Press any key...")
Console.ReadKey(True)
```
### Questions
7. The program snippet to the left is supposed to use a loop to calculate a factorial. Finish the program snippet (add the loop and fill in the two blanks). A sample calculation is below.\
5!=1×2×3×4×5=120

## Snippet #5
```vb
Console.Write("How many scores? ")
Dim count = Val(Console.ReadLine())
Dim sum As Integer = ___

    Console.Write("Enter score:")
    score = Val(Console.ReadLine())
    sum = ___

Console.Write("The total score is: ")
Console.WriteLine(score)
Console.WriteLine("Press any key...")
Console.ReadKey(True)
```
### Questions
8. The program snippet to the left asks for a number of scores. It is then supposed to ask for that many scores, add them up, and display the total. Finish the program snippet (add the loop and fill in the two blanks).