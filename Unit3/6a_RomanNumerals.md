# 3.6a Roman Numerals

## Function header
```vb
Function GetRomanNumeral(number As Integer) As String
```
This line creates a function named ```GetRomanNumeral```. It takes one Integer argument and has a String as its result. We can use this function elsewhere in our program like any other function, the only difference being that we made it ourselves.

Inside our function block, the Integer argument will be available to us as a variable named number.

## Ignoring invalid numbers
We will only be converting numbers from 1 to 4999 to Roman numerals, rejecting the others.
```vb
If number <= 0 OrElse number >= 5000 Then	
    Return "Out of range"
End If
```
This block of code checks for negative numbers, zero, and numbers of 5000 or higher.

The ```Return``` command quits the function and sends the result back to whichever other function or subprogram was using this function. In this case, we are sending a String that says “Out of range”.

## Setting up the result
```vb
Dim result As String = ""
```
We will be adding letters onto the end of this String as we go.

## Thousands
```vb
Do While number >= 1000
    result = result & "M"
    number = number - 1000
Loop
```
This block of code does a couple of things.  First, it will add an “M” to our result. Then, it will drop the number by 1000. At every point from here on out in the program, the variable ```number``` will contain how much of the number is left, that has not yet been factored into the Roman numeral.

This is repeated as long as the remaining number is over 1000. If the original number was 3500, it will repeat 3 times, as the number drops to 2500, then 1500, then 500 and the result becomes M, then MM, then MMM.

## 900
```vb
If number >= 900 Then
    result = result & "CM"
    number = number - 900
End If
```
Once the thousands are taken out, there is only the possibility for a single 900 to appear. Therefore, in this case, you can use an If block rather than a Do While block, although Do While will still work.

500 (D) and 400 (CD) work similarly to 900.

## The rest of the numbers
100 (C) works like 1000, 90 (XC), 50 (L), and 40 (XL) work like 900, 500, and 400.

10 (X), 9 (IX), 5 (V), 4 (IV), and 1 (I) also follow similar patterns.

## Wrapping it up
```vb
    Return result
End Function
```
Again, the ```Return``` command quits the function and sends the result back to whichever over function or subprogram was using this function. In this case, we are sending back the String from the variable we have been working on.