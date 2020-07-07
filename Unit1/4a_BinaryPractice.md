# 1.4a Binary Numbers and Arithmetic Practice

## Binary Numbers from 0 to 15
(Tip: Each number is the previous number plus one, so you can use the [interactive binary addition page](http://www.gilfusion.com/binary/addition.html) to help you. There is also an [interactive page](http://www.gilfusion.com/binary/fifteen.html) that walks you through each number from 3 to 15 using this method.)
|           |           |           |           |
|-----------|-----------|-----------|-----------|
|0 = 0b0	|1 = 0b1	|2 = 0b10	|3 =    |
|4 = 0b100	|5 =    	|6 =    	|7 = 0b111  |
|8 = 0b1000	|9 =    	|10 =       |11 =       |
|12 =       |13 = 0b1101|14 =       |15 =       |

## Binary Addition

```
  1101
+  110
──────
```
```
  1111
+   11
──────
```
```
  1010
+  101
──────
```
```
  1100
+ 1010
──────
```
```
  1011
+  101
──────
```
```
  1111
+ 1111
──────
```
```
  0010 1111
+ 0100 1010
───────────
```
```
  0001 0111
+ 0110 0011
───────────
```
```
  0011 0111
+ 0011 0111
───────────
```

1. What is a simple way to add a number to itself (or multiply by two)?
2. What would you guess is a simple way to divide by two?

## Boolean Algebra and Binary Arithmetic
Another way of performing Boolean algebra is by using 1 to represent true and 0 to represent false. Computers use this internally to make binary arithmetic work.
|A	|B	|C	|A XOR B	|(A XOR B) XOR C	|A AND B	|(A XOR B) AND C	|(A AND B) OR ((A XOR B) AND C)	|Binary A+B+C|
|---|---|---|-----------|-------------------|-----------|-------------------|-------------------------------|------------|
|1	|1	|1						
|1	|1	|0						
|1	|0	|1						
|1	|0	|0									
|0	|1	|1						
|0	|1	|0						
|0	|0	|1						
|0	|0	|0

3. What is the connection between the Boolean algebra formulas and binary addition?