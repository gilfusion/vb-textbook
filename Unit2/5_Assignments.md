# 2.5 Assignment Statements and Properties
## Assignment Statements
The most common form of statement in many programming languages like Visual Basic is an **assignment statement**. An assignment statement gets and/or calculates values and stores them somewhere on the computer. The place where the value has been stored is said to have been assigned that value.

To have an assignment statement, you need three things: a destination (where the value is assigned), the assignment operator (an = sign), and a source expression (where the value is calculated or taken from). The destination is often called the **left-hand side** (LHS) of an assignment statement, and the source is often called the **right-hand side** (RHS) of the statement, similar to how those terms are used in mathematics regarding sides of an equation. The right-hand side can be any expression, while the left-hand side is limited to properties and variables (more or less). We will learn about properties in this section and variables later in the unit.

|Left-Hand Side	|Assignment Operator	|Right-Hand Side|
|---------------|-----------------------|---------------|
|Destination	|                    	|Source
|Property or Variable	|=	            |Property, Variable, or any other kind of expression

## Properties
In addition to methods, Visual Basic objects can also include **properties**, where information and settings about an object are stored. Most properties can be used on the RHS of an assignment statement (or in any other expression, for that matter), and many can also be used on the LHS, meaning that they can be changed.

Do you remember the Properties window from the Windows Forms Application? Controls in Windows Form Application projects are also objects, and their properties can be changed in your code using assignment statements in addition to changing them using the Properties window.

### Sample Properties
#### The System.Console object
|Property	|Expected kind of data	|Description    |
|-----------|-----------------------|---------------|
|`BackgroundColor`	|Console Color<br>(see below)	|The color behind any text written to the console window after this point
|`ForegroundColor`	|Console Color	|The color of any text written to the console window after this point
|`Title`	|String<br>(Quoted Text)	|The text displayed in the title bar of the console window

The `BackgroundColor` and `ForegroundColor` properties can only be set from the properties of the `System.ConsoleColor` object. Visual Studio will display the possibilities in the autocomplete list when you use it.
(None of these properties are available in LINQPad's version of `System.Console`.)
#### Most Windows Form Application control objects
|Property	|Expected kind of data	|Description    |
|-----------|-----------------------|---------------|
|`BackColor`	|Color (see below)	|The background color of the control
|`ForeColor`	|Color	|The color of the text displayed on the control
|`Left`	|Integer	|The x-coordinate of the left side of the control
|`Tag`	|Anything	|An extra piece of data for you to keep with the control
|`Text`	|String	|The text displayed on the control
|`Top`	|Integer	|The y-coordinate of the top of the control

The `BackColor` and `ForeColor` properties can only be set to color values. You can find a large number of color values in the properties of the `System.Drawing.Color` object (or just `Color` object for short). Visual Studio will display the possibilities in the autocomplete list when you use it.
#### Examples
```vb
Console.BackgroundColor = ConsoleColor.Red
System.Console.Title = "Contoso Examples Ltd."
Button1.Left = Button2.Left
```

## Tip
Visual Studio's autocomplete feature uses icons to show the difference between methods, properties, and other things. You can read more about it [here](5b_AutoComplete.md).

## Questions
1. What symbol is used for the assignment operator?
2. What term describes the destination portion of an assignment statement?
3. What term describes the source portion of an assignment statement?
4. Describe what the following line of code does.
```vb
Console.ForegroundColor = ConsoleColor.Yellow
```	
5. Write a line of code that changes the title of the console to your name.
6. Write a line of code that changes the background color of Button3 to magenta.