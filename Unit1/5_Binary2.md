# 1.5 Binary Numbers and Arithmetic, Part 2

## Converting from Decimal to Binary
The process for converting a decimal number to a binary number is straightforward but long. Take the number and divide it by 2 using long division. The remainder is your ones digit. Take the quotient and divide it by 2 to get the next digit to the left, and repeat until the quotient is zero.

### Example #1
Follow the divisions below from right to left.

Decimal number: 47
|	|	|	|	|	|   |
|---|---|---|---|---|---|
|1⁄2=0 1⁄2	|2⁄2=1 0⁄2	|5⁄2=2 1⁄2	|11⁄2=5 1⁄2	|23⁄2=11 1⁄2	|47⁄2=23 1⁄2|
Binary number: 101111

### Example #2
Decimal number: 24
|	|	|	|	|	|
|---|---|---|---|---|
|1⁄2=0 1⁄2	|3⁄2=1 1⁄2	|6⁄2=3 0⁄2	|12⁄2=6 0⁄2	|24⁄2=12 0⁄2|
Binary number: 11000

## Converting from Binary to Decimal
Similarly, a process for converting a binary number is straightforward. Take each bit, multiply it by its place (the number in the ones place by 1, in the twos place by 2, in the fours place by 4, etc.), and add all the numbers together.

### Example #1
Binary number: 101111
```
   1	 0    1	   1    1    1
× 32  × 16  × 8  × 4  × 2  × 1
────  ────  ───  ───  ───  ───
  32     0    8    4    2    1
```
Decimal number: 32+0+8+4+2+1=47

### Example #2
Binary number: 11000
```
   1    1	 0    0    0
× 16  × 8  × 4  × 2  × 1
────  ───  ───  ───  ───
  16    8    0    0    0
```
Decimal number: 16+8+0+0+0=24

## Binary Negation and Subtraction
In binary, like with decimal numbers, subtracting one number from another is the same as finding the negation of that number and adding it to the other one. Therefore, to subtract binary numbers, we need to know how to negate them. This is a two-step process.

The first step is to find the **ones complement**. The ones complement of a binary number is simply flipping all the bits in the number, turning all of the 0s into 1s and vice versa.
The second step is to find the **twos complement**. The twos complement of a binary number is simply the number's ones complement plus 1.

Computers usually work with a fixed number of bits (like 32 or 64) and drop any extra bits to make this work correctly.

### Negation Examples
|Decimal	|Original number	|Ones complement	|Twos complement	|Decimal|
|---|-----------|-----------|-----------|---|
|47	|0010 1111	|1101 0000	|1101 0001	|-47|
|24	|0001 1000	|1110 0111	|1110 1000	|-24|
### Subtraction Example
In decimal, 47 − 24 = 23.

Using 8-bit binary numbers, 

0010 1111 - 0001 1000 = 0010 1111 + 1110 1000 = 1 0001 0111

Since we drop the leading 1 to make the number 8 bits, the result is 0001 0111, which is binary for 23.

## Connecting Boolean Logic to Binary Numbers
The main reason for using Binary numbers is because it is easy to construct Boolean logic circuits to handle them, with 0 taking the place of False and 1 taking the place of True. Ones complement is a simple concept for Boolean logic to handle: apply the NOT operator to each bit. 

The other operations can be broken down into Boolean formulas, as well. Here are a couple. Adding three binary bits (two numbers and a possible bit carried in) requires two formulas, one for the right bit, and one for the left bit or the bit carried to the next column.
* S = A XOR B XOR C<sub>in</sub>, where S is the sum, A and B are bits from the numbers being added, and C<sub>in</sub> is the bit carried in
* C<sub>out</sub> = (A AND B)OR ((A XOR B)AND C<sub>in</sub> ), where A, B, and C<sub>in</sub> are the same as above, and C<sub>out</sub> is the bit carried out to the next column