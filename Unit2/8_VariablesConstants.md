# 2.8 Variables and Constants

Now that we know the formats computer use to store data, we can now discuss additional places where data is stored. Properties are part of other objects, so when we want to store our own data, we need to create our own storage locations. These storage locations are usually variables. A **variable** is a named location in your computer's RAM where you can store information to be used later. (RAM—or **random access memory**—is the computer's short-term memory. It is erased when the power to the computer is turned off.)

## Variables in Visual Basic
Before you can use a variable in a Visual Basic program, you need to create it. Creating a variable reserves space in the computer's RAM and sets up a name you can use to access that space. As mentioned in the last topic, that amount of space reserved depends of the type of data the variable is supposed to hold. Most variables can only hold one type of data.

## The `Dim` Statement
Variables in Visual Basic are created using the `Dim` statement.
* (`Dim` originally stood for Dimension, since it controlled how much RAM was being reserved for the variable.)

The `Dim` statement has these parts:
```vb
Dim 𝘯𝘢𝘮𝘦 As 𝘵𝘺𝘱𝘦 = 𝘷𝘢𝘭𝘶𝘦
```
|               |       |
|---------------|-------|
| 𝘯𝘢𝘮𝘦	| the name of the variable
| 𝘵𝘺𝘱𝘦	| the type of data that the variable can hold (`Byte`, `Integer`, `Double`, `String`, `Boolean`, etc.)
| 𝘷𝘢𝘭𝘶𝘦	|the initial data stored in the variable
* (If you give a value, you may be able to omit the type, since, in many cases, Visual Basic can figure out the type from the value you give.)

### Examples
```vb
Dim number As Integer = 0
Dim guess As Integer
```
* (Visual Basic will complain if you attempt to use a variable before you store a value in it.)
```vb
Dim count = 0
```
* (In this case, Visual Basic determines that 0 is an integer, so it makes count an Integer variable).
```vb
Dim average = 0.0
```
* (In this case, Visual Basic determines that 0.0 could contain a fraction, so it makes average a Double variable.)

## Scope
The location where a variable is created in Visual Basic is important because of the concept of **scope**. Scope determines how much of the program can use the variable. If you create a variable inside a subprogram, it can only be used in that subprogram. If you create a variable inside an object (Class or Module) but not inside a subprogram, it can be used by any of the subprograms in that object, but not outside that object. (Visual Basic does not let you create variables outside objects for "Global" scope, though there are other programming languages that do.)

## The `Const` Statement
In addition to variables, Visual Basic also includes constants. While variables can vary - they can be changed using assignment statements - constants are constant - they cannot be changed.
Constants in Visual Basic are created using the `Const` statement. (Two guesses what that stands for.) The `Const` statement has the same parts as the `Dim` statement.
```vb
Const 𝘯𝘢𝘮𝘦 As 𝘵𝘺𝘱𝘦 = 𝘷𝘢𝘭𝘶𝘦
```
|               |       |
|---------------|-------|
|𝘯𝘢𝘮𝘦	    |the name of the constant
|𝘵𝘺𝘱𝘦	    |the type of data that the constant is
|𝘷𝘢𝘭𝘶𝘦	|the value stored in the constant
* (The value is required for constants, since you cannot change it later. This also means that you should be able to omit the type, since Visual Basic should be able to figure out the type from the value.)

### Examples
```vb
Const correct = 20
Const word As String = "no"
```

## Using Constants and Variables

Once they have been created, both constants and variables can be used in expressions and on the right-hand side of assignment statements. Since variables are designed to be mutable, or changeable, they can also be used on the left-hand side of assignment statements.

## Questions
```vb
Dim number As Integer = 0
```
1. What is the name of the variable created by the above statement?
2. What is the data type of the variable created by the above statement?
3. How many bytes of RAM are reserved for the variable created by the above statement?
```vb
Const correct = "yes"
```
4. What is the data type of the constant created by the above statement?
5. Write a statement that creates a constant named gravity holding the number 9.81.
6. Write a statement that creates a variable named velocity holding a floating-point number that only uses 32 bits.
7. Write a statement that stores into velocity the product of gravity and the number 5.6.