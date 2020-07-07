# 2.3 Objects and Methods
## Objects
In computer science, an **object** is any entity that can be manipulated by the commands of a programming language, such as a value, variable, function, or data structure . For our purposes, an object is a package of related features and options that you can use and customize in your program.

## Methods
To perform actions with an object, you must use one of its **methods**. A method is a subprogram associated with an object. In Visual Basic, to use a method, type the name of the object, followed by a dot, followed by the name of the method. (This is called dot notation.) Some methods require additional information, called **arguments**, in order to run. If the method you are using needs an argument or arguments, place them in a list, separated by commas and surrounded by parentheses. Each argument will be an expression.
* <span style="color: darkgray">(Some programmers will also use the term "**parameter**" to refer to an argument. There are subtle differences between a parameter and an argument - technically, a parameter is where the information goes inside the method. We will cover this in more detail later when we get to making our own methods.)</span>
### Examples
```vb
System.Console.Clear
```
* Note that, in Visual Basic and several other languages, the object's name itself may contain dot notation. In this case, the name of the object is System.Console, and the name of the method is Clear.
	Also, this command can also be written as
    ```vb
    System.Console.Clear()
    ```
    Some programming languages require the empty list of arguments in parentheses, and, although Visual Basic does not, it is a good habit to always include them anyways.
* (This method actually does not work in LINQPad. Instead, you can use the command
    ```vb
    Util.ClearResults()
    ```
    ```Util``` is a special object only available in LINQPad.)
```vb
System.Threading.Thread.Sleep(1000)
```
* In this case, the name of the object is System.Threading.Thread, and the name of the method is Sleep.
* This method requires an integer argument to run properly (specifically, how many milliseconds to "sleep"). Your program will not work at all if the number is omitted. Also, when you include an argument, the parentheses are required.
```vb
My.Computer.FileSystem.CopyFile("original.docx", "duplicate.docx")
```
* This method requires two string (quoted text) arguments to run properly (specifically, where to copy from and where to copy to). The arguments are, again, surrounded by parentheses like the previous example, and there is a comma between the two arguments. For readability's sake, we usually add a space after the comma like we would in English, although it is optional. If the line of code is getting really long, you can also press Enter after the comma, and Visual Basic will interpret the two lines as a single long line.

## Questions
1. What is the term for a package of related features and options that you can use and customize in your program?
2. What notation is used to access the methods of an object?
```vb
My.Computer.Network.Ping("www.faithheritageschool.org")
```
3. What is the name of the object in the above command?
4. What is the name of the method in the above command?
5. How many arguments does the above command have?
* By the way, this command is used as one of the ways to test to see if a website is accessible.
```vb
System.Console.Beep(262, 1000)
```
6. What is the name of the object in the above command?
7. What is the name of the method in the above command?
8. How many arguments does the above command have?
* By the way, this command plays a 262-hertz tone (about middle C) for 1000 milliseconds (or 1 second).