# 2.9 Data as Objects

A big features of languages like Visual Basic is that almost everything in the language is an object and can be used like an object. Every piece of data is an object, with its available properties and methods being determined by its data type. Some data types have many properties and methods, while others only have a few.

For example, every piece of data includes this method listed below.

|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|```ToString```	|None	|String	|Makes a text form of whatever the object contains. If it cannot figure it out, it gives the name of the data type.

### Examples
```vb
Console.WriteLine(12.ToString())

Dim x As String
Dim y As Boolean
y = True
x = y.ToString()
```

Behind the scenes, Visual Basic lets you use the ```ToString``` method a lot for making data readable so you can display it for your users or use it to search for problems in your program.

## Strings As Objects
Most of the built-in data types do not have many methods with them. The big exception is strings. Strings have lots of methods and one property that give you different pieces of information about that particular string or change the string into a different one. Let's look at several of them.

|Property	|Expected kind of data	|Description|
|-----------|-----------------------|-----------|
|```Length```	|Integer	|How many characters this particular string object contains
	
|Method	|Arguments	|Expected Return Value	|What It Does|
|-------|-----------|-----------------------|------------|
|```StartsWith```	|1 string	|Boolean	|Tests if the string object starts with the string from the argument (case does matter) and returns true or false
|```EndsWith```	|1 string	|Boolean	|Tests if the string object ends with the string from the argument
|```Contains```	|1 string	|Boolean	|Tests if the string object contains the string from the argument
|```IndexOf```	|1 string	|Integer	|Returns how many characters after the beginning the argument string is within the string object, or -1 if the argument isn't in there.
|```PadLeft```	|1 integer	|String	|Creates a new string with spaces added to the beginning of the string until its length is the integer argument
|```PadRight```	|1 integer	|String	|Creates a new string with spaces added to the end of the string until its length is the integer argument
|```Substring```	|1 or 2 integers	|String	|Creates a new string with a piece of the string object. The first number says how many characters after the beginning to start (0 means to start at the beginning of the string), and the second number says how long the substring should be. If the second number is omitted, the substring gets all the remaining characters from the string object.
|```TrimStart```	|None	|String	|Creates a new string with extra spaces removed from the beginning
|```TrimEnd```	|None	|String	|Creates a new string with extra spaces removed from the end
|```Trim```	|None	|String	|Creates a new string with extra spaces removed from both the beginning and the end
|```ToUpper```	|None	|String	|Creates a new string with all the lowercase characters changed to uppercase
|```ToLower```	|None	|String	|Creates a new string with all the uppercase characters changed to lowercase

### Examples
|Code	|Console Output|
|-------|--------------|
|```Console.WriteLine("Hello".StartsWith("lo"))```	|<pre style="background-color: black; color: white">False</pre>
|```Console.WriteLine("Hello".EndsWith("lo"))```	|<pre style="background-color: black; color: white">True</pre>
|```Console.WriteLine("Hello".Contains("lo"))```	|<pre style="background-color: black; color: white">True</pre>
|```Console.WriteLine("Hello".PadLeft(10))```	|<pre style="background-color: black; color: white">     Hello</pre>
|```Console.WriteLine("Hello".PadRight(10))```	|<pre style="background-color: black; color: white">Hello     </pre>
|```Console.WriteLine("  Hello  ".TrimStart())```	|<pre style="background-color: black; color: white">Hello  </pre>
|```Console.WriteLine("  Hello  ".TrimEnd())```	  |<pre style="background-color: black; color: white">Hello</pre>
|```Console.WriteLine("  Hello  ".Trim())```	|<pre style="background-color: black; color: white">Hello</pre>
|```Console.WriteLine("Hello".ToUpper())```	|<pre style="background-color: black; color: white">HELLO</pre>
|```Console.WriteLine("Hello".ToLower())```	|<pre style="background-color: black; color: white">hello</pre>
|```Console.WriteLine("Hello".PadRight(10).ToUpper())```	|<pre style="background-color: black; color: white">HELLO     </pre>
|```Dim message As String<br>message = "Greetings"<br>Console.WriteLine(message.PadLeft(2).ToUpper())```	|<pre style="background-color: black; color: white">  GREETINGS</pre>

## Questions
```vb
Dim message = " WeLcOmE To CoMpUtEr ClAsS "
```
1. What is the data type of the variable ```message```?
2. What is ```message.Length```?
3. What is ```message.Trim().Length```?
4. What is ```message.Trim().ToUpper()```?
5. What is ```message.Trim().ToUpper().Length```?
6. Write a line of code that displays ```message```, with its own extra spaces removed, turned to lowercase, and with spaces added to the end to make its length 40.