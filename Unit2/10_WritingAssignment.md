# 2.10 Unit 2 Writing Assignment

1. Choose a programming language (not Visual Basic) to research and, in a paragraph, answer the following questions about it:
	* What is it called?
	* When was it created?
	* Who created it?
	* For what main purpose was it created?
2. Find and write the code for the "Hello, World!" project in that programming language.
3. Compare this "Hello, World!" project to the Visual Basic "Hello, World!" project from earlier in this unit ([Click here](4_SystemConsole.md), also copied below). In a paragraph or two, describe some similarities and differences between the two languages, based on those projects, make a case for which language you would consider to be the easiest to read and write. (Note that different factors may apply to reading as opposed to writing.)
	* This assignment in total should be at least two paragraphs, plus the code.
	* Remember to cite your sources.

## “Hello, World!” in Visual Basic
“Hello, World!” is traditionally one of the first programs many programmers learn in a programming language. Here is how it looks in a Visual Basic Console Application.

```vb
Module HelloWorld
    Sub Main()
        Console.WriteLine("Hello, World!")
        Console.ReadKey(True)
    End Sub
End Module
```