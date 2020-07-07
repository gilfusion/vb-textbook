# 1.6 Octal and Hexadecimal Numbers
## Octal and Hexadecimal Numbers
### Bits and Bytes
In the last lesson, we learned that a bit is a binary digit. There are also terms for binary numbers of certain lengths. A binary number that is 4 bits long is called a **nibble**, and a binary number that is 8 bits long is called a **byte**.

The amount of storage space in memory or on a data storage device like a hard drive or flash drive is generally measured in bytes or a unit derived from bytes.

In the metric system, 1 kilometer is 1000 meters, so it would be clear to expect that 1 kilobyte (kB) is 1000 bytes. Unfortunately, in the technology world, there are two conflicting definitions for kilobyte. One definition does say that 1 kilobyte is 1000 bytes, but the other definition says that 1 kilobyte is 1024 bytes. Why 1024? 1024 was chosen because it was the closest power of 2 to 1000. To attempt to fix this confusion, another unit was created for 1024 bytes, called a kibibyte (KiB).

|Decimal Unit	|Binary Unit|
|---|---|
|1 kB (kilobyte) = 1000 bytes	|1 KB = 1 KiB (kibibyte) = 1024 bytes
|1 MB (megabyte) = 1000 kB (1 million bytes)	|1 MB = 1 MiB (mebibyte) = 1024 KB
|1 GB (gigabyte) = 1000 MB (1 billion bytes)	|1 GB = 1 GiB (gibibyte) = 1024 MB
|1 TB (terabyte) = 1000 GB (1 trillion bytes)	|1 TB = 1 TiB (tebibyte) = 1024 GB
|1 PB (petabyte) = 1000 TB (1 quadrillion bytes)	|1 PB = 1 PiB (pebibyte) = 1024 TB
|1 EB (exabyte) = 1000 PB (1 quintillion bytes)	|1 EB = 1 EiB (exbibyte) = 1024 PB
|1 ZB (zettabyte) = 1000 EB (1 sextillion bytes)	|1 ZB = 1 ZiB (zebibyte) = 1024 EB
|1 YB (yottabyte) = 1000 ZB (1 septillion bytes)	|1 YB = 1 YiB (yobibyte) = 1024 ZB

## Number Systems
Decimal and binary are two examples of different base number systems (base 10 and 2, respectively). Binary numbers quickly get long and tedious to write, so computer programmers use two other number systems as "binary shorthand" in programming.

### Octal
The first of these number systems to be used is the octal number system. As the name implies, it is base 8, meaning that it only uses the digits 0 through 7. Octal numbers have a ones place, but they also have an eights place, a sixty-fours place, a five-hundred-twelves place, and so on. Why base 8? 8 is also a power of 2, 2³ to be specific, so binary numbers can be quickly converted to octal numbers and vice versa, 3 bits at a time.

### Hexadecimal
Octal numbers have largely been displaced by hexadecimal numbers. Hexadecimal numbers are base 16 numbers (*hex* = 6 plus *deci* = 10). Since 16 is 2⁴, hexadecimal numbers can also be easily converted to binary numbers, 4 bits at a time. Also, since 4 bits is one nibble, one digit of a hexadecimal number is equivalent to a nibble, and since 8 bits is one byte, two hexadecimal digits is equivalent to a byte. This property led to hexadecimal being more popular in use than octal. The possible digits in hexadecimal numbers start with 0 through 9, then add A through F for the numbers 10 to 15. Hexadecimal numbers have a ones place, a sixteens place, and two-hundred-fifty-sixes place, and so on.

#### Examples
Octal numbers can be marked with prefixes like “0o” or “&O” or a suffix like “₈”. Hexadecimal numbers can be marked with prefixes like “0x” or “&H” or a suffix like “₁₆”.
|Binary	    |Octal	|Decimal	|Hexadecimal|
|-----------|-------|-----------|-----------|
|0b0	    |0o0	|0	        |0x0
|0b1	    |0o1	|1	        |0x1
|0b10	    |0o2	|2	        |0x2
|0b11	    |0o3	|3	        |0x3
|0b1000	    |0o10	|8	        |0x8
|0b1010	    |0o12	|10	        |0xA
|0b1111	    |0o17	|15	        |0xF
|0b10000	|0o20	|16	        |0x10
|0b11111111	|0o377	|255	    |0xFF

## Questions
1. How many bytes are in one binary megabyte (mebibyte)? In one binary gigabyte (gibibyte)?
2. In octal, what is 0o5 + 0o4?
3. In hexadecimal, what is 0x9 + 0x2?
4. What is the binary number 0b1010 1000 in hexadecimal? In octal?
5. What is the decimal number 4096 in hexadecimal? In octal?