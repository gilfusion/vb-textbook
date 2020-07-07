# 1.4 Binary Numbers and Arithmetic

As we learned previously, a computer fundamentally does three things: loads numbers, performs math operations on those numbers, and stores the resulting numbers. This statement raises two questions. First, how do computers, which are made up of wires and switches, handle numbers? Second, if everything a computer does involves numbers, how do we get from numbers to everything else we see computers handle?

In the last lesson, we looked at Boolean logic, which provides half the answer to that first question. The other half of the answer to that question lies in binary numbers. Before looking at binary numbers, however, we should make sure we understand how the numbers we are used to using actually work.

## Decimal Numbers
The numbers we typically use are called **decimal numbers**, or base 10 numbers.

Each digit in a decimal number can be one of ten possibilities (hence base 10): 0, 1, 2, 3, 4, 5, 6, 7, 8, or 9. (Perhaps not coincidentally, another term for a finger is a digit, and most people have ten of those.)

Decimal numbers can have a ones place, a tens place, a hundreds place, a thousands place, and so on. Each of these places, by the way, is a power of 10. 10⁰ = 1, 10¹ = 10, 10² = 100, 
10³ = 1000, and so on.

When you add decimal numbers, you usually add them starting at the rightmost place, adding digits from the same column and carrying to the next column if necessary.

## Binary Numbers
Computers cannot count with their fingers, so they need a different number system. Since they are based on wires and switches, and switches can be on or off, they use base 2 numbers, or **binary numbers**.

Each digit in a binary number can be one of only two possibilities: 0 or 1. By the way, binary digit is commonly abbreviated as **bit**.

Binary numbers have a ones place like decimal numbers, but they also have a twos place, a fours place, an eights place, a sixteens place, and so on. Each of these places is a power of 2. Powers of 2 show up frequently in computing, since, in binary at least, they make up nice round numbers.

### Powers of 2
|       |       |       |       |       |       |
|-------|-------|-------|-------|-------|-------|
|2⁰=1	|2¹=2	|2²=4	|2³=8	|2⁴=16	|2⁵=32  |
|2⁶=64	|2⁷=128	|2⁸=256	|2⁹=512	|2¹⁰=1024|2¹¹=2048|

### Binary Numbers from 0 to 15
When we write them, we can distinguish them from decimal numbers using either a prefix like “0b” (common in many programming languages), a prefix like “&B” (which the Visual Basic programming language uses), or a suffix like “₂” (used sometimes in math).
|           |           |           |           |
|-----------|-----------|-----------|-----------|
|0 = 0b0	|1 = 0b1	|2 = 0b10	|3 = 0b11   |
|4 = 0b100	|5 = 0b101	|6 = 0b110	|7 = 0b111  |
|8 = 0b1000	|9 = 0b1001	|10 = 0b1010|11 = 0b1011|
|12 = 0b1100|13 = 0b1101|14 = 0b1110|15 = 0b1111|

## Binary Addition
Addition in binary works much like addition for decimal numbers, adding up the numbers in the same column, and carrying also works the same. The biggest difference, though, is that, in binary, 1 + 1 = 10.

### Examples
```
Binary      Check
  1100        12
+    1       + 1
──────      ────
  1101        13
```
```
Binary      Check
  1001         9
+  110      +  6
──────      ────
  1111        15
```
```
Binary      Check
  ₁₁
  1110        14
+   11      +  3
──────      ────
 10001        17
```
```
Binary      Check
  ₁₁
 1001          9
+  11       +  3
─────       ────
 1100         12
```

## Questions
1. Add the binary numbers 0b110 and 0b101. (Tip: You can use this [interactive binary addition page](http://www.gilfusion.com/binary/addition.html).)
2. What is 27 in binary? (Hint: You can break it up into two numbers you know, then use binary addition to combine them.) 		
3. What do all the even numbers have in common in binary? 
4. Add the binary number 0b101 to itself. Add the binary number 0b111 to itself. Add the binary number 0b1011 to itself. What pattern do you notice when adding a binary number to itself? Using this pattern, add the binary number 011001101 to itself.