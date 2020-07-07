# 1.7 Character Sets and Encoding
## Character Sets and Encoding
To recap, computers store numbers in binary, using Boolean logic behind the scenes to make it work. Programmers often write out binary numbers using a shorthand number system like octal or hexadecimal. The next question to raise is, since the only thing that computers can do is compute, that is, perform mathematical operations, how do they perform the other tasks we see them perform.

The answer is that everything on the computer, from letters and words to pictures and videos, has a number form that the computer can perform calculations on. Some of these number forms are simple, while others are extremely complex. One of the simpler things represented by numbers on the computer is text: letters, digits, and punctuation.

A **character** is a single symbol either stored on the computer or displayed on the screen. It may be a letter, a digit, a punctuation mark, or something else. Characters are converted to numbers using a character set and an encoding.

## Character Sets
A **character set** is a table matching character symbols to their numeric equivalent. There are many character sets in existence, covering characters from different languages to cover different needs. For many years, the dominant character set used in the United States was **ASCII** (which stands for the American Standard Code for Information Interchange). Today, the character set used on most computers in the world is **Unicode**. Unicode is a standard intended to include every character (or as close to every character as possible) from every language in the world.

### Partial ASCII Character Set
ASCII defines characters for the numbers 0 to 127. These numbers all fit within 7 bits, meaning that they can fit in a byte with a little room to spare. 0 to 31 and 127 are control codes for things like Backspace, Tab, and Return. For compatibility, Unicode also uses these same characters for its numbers 0 to 127.
|Code|Char|Code|Char|Code|Char|Code|Char|Code|Char|Code|Char|
|---|---|---|---|---|---|---|---|---|---|---|--- |
|32 	|	|48 	|0 	|64 	|@ 	|80 	|P 	|96 	|` 	|112 	|p |
|33 	|! 	|49 	|1 	|65 	|A 	|81 	|Q 	|97 	|a 	|113 	|q |
|34 	|" 	|50 	|2 	|66 	|B 	|82 	|R 	|98 	|b 	|114 	|r |
|35 	|# 	|51 	|3 	|67 	|C 	|83 	|S 	|99 	|c 	|115 	|s |
|36 	|$ 	|52 	|4 	|68 	|D 	|84 	|T 	|100 	|d 	|116 	|t |
|37 	|% 	|53 	|5 	|69 	|E 	|85 	|U 	|101 	|e 	|117 	|u |
|38 	|& 	|54 	|6 	|70 	|F 	|86 	|V 	|102 	|f 	|118 	|v |
|39 	|' 	|55 	|7 	|71 	|G 	|87 	|W 	|103 	|g 	|119 	|w |
|40 	|( 	|56 	|8 	|72 	|H 	|88 	|X 	|104 	|h 	|120 	|x |
|41 	|) 	|57 	|9 	|73 	|I 	|89 	|Y 	|105 	|i 	|121 	|y |
|42 	|* 	|58 	|: 	|74 	|J 	|90 	|Z 	|106 	|j 	|122 	|z |
|43 	|+ 	|59 	|; 	|75 	|K 	|91 	|[ 	|107 	|k 	|123 	|{ |
|44 	|, 	|60 	|< 	|76 	|L 	|92 	|\ 	|108 	|l 	|124 	|\| |
|45 	|- 	|61 	|= 	|77 	|M 	|93 	|] 	|109 	|m 	|125 	|} |
|46 	|. 	|62 	|> 	|78 	|N 	|94 	|^ 	|110 	|n 	|126 	|~ |
|47 	|/ 	|63 	|? 	|79 	|O 	|95 	|_ 	|111 	|o 	| 	| 

The Character Map program on Windows computers lets you view all the characters in the character set (that can be displayed in a particular font). In the bottom-left corner of the program is the selected character's character code, either ASCII in decimal, or Unicode in hexadecimal if it starts with "U+".

## Encoding
Once you have a number for the character, the next question becomes how to store that computer as bits. This is the character's **encoding**, and there may be multiple encodings for a character from the same character set. Most encodings for ASCII simply place one character in one byte. The word "Hello" has five letters. Each letter is a character, making five characters, and the encoding would store that in five bytes.

With Unicode, encoding gets more complex, because the numbers for many of the characters will not fit in one byte. (Originally, they could fit into two bytes, but it has since outgrown even that.) There are three common encodings for Unicode. **UCS-2** was the original Unicode encoding, where every character took two bytes (hence, UCS-2). This is not used much anymore, since there are some Unicode characters that do not fit in UCS-2's range. UCS-2 was largely replaced by **UTF-16** (2 bytes is 16 bits), where Unicode characters can take either 16 bits, like in UCS-2, or, if they do not fit in that range, they take 32 bits. Once the concept of different characters taking up different amounts of space was established, this led to the creation of **UTF-8**, where the character, depending on its character code, could take up 8 bits, 16 bits, 24 bits, or 32 bits. Characters in the ASCII range would only take up one byte (instead of two bytes with UCS-2 or UTF-16), both saving space and making them the same as how they would have been encoded with straight ASCII.

## Questions
You may use the Character Map program to help you answer these questions.
1. What is the character code for A? What is the character code for a? Write a simple math formula to convert an uppercase letter to lowercase.
2. How many bytes would the word "Hello" take up if it was encoded using ASCII? UTF-16? UTF-8? Which encoding takes up the most space?
3. How many bytes would the word "יהוה" (the Hebrew name for the LORD) take up if it was encoded using UTF-16? UTF-8? Which encoding takes up the most space?