A Swift Tour
===============

Tradition suggests that the first program in a new language should print the words “Hello, world” on the screen. In Swift, this can be done in a single line:
```
println("Hello, world")
```

If you have written code in C or Objective-C, this syntax looks familiar to you—in Swift, this line of code is a complete program. You don’t need to import a separate library for functionality like input/output or string handling. Code written at global scope is used as the entry point for the program, so you don’t need a main function. You also don’t need to write semicolons at the end of every statement.

This tour gives you enough information to start writing code in Swift by showing you how to accomplish a variety of programming tasks. Don’t worry if you don’t understand something—everything introduced in this tour is explained in detail in the rest of this book.
>> N O T E
>> For the best experience, open this chapter as a playground in Xcode. Playgrounds allow you to edit the code listings and see the result immediately.``

Simple Values
====

Use let to make a constant and var to make a variable. The value of a constant doesn’t need to be known at compile time, but you must assign it a value exactly once. This means you can use constants to name a value that you determine once but use in many places.
```
1| var myVariable = 42
2| myVariable = 50
3| let myConstant = 42
```

A constant or variable must have the same type as the value you want to assign to it. However, you don’t always have to write the type explicitly. Providing a value when you create a constant or variable lets the compiler infer its type. In the example above, the compiler infers that myVariable is an integer because its initial value is a integer.

If the initial value doesn’t provide enough information (or if there is no initial value), specify the type by writing it after the variable, separated by a colon.
```
1| let implicitInteger = 70
2| let implicitDouble = 70.0
3| let explicitDouble: Double = 70
```

>> E X P E R I M E N T
>> Create a constant with an explicit type of F loat and a value of 4 .

Values are never implicitly converted to another type. If you need to convert a value to a different type, explicitly make an instance of the desired type.
```
1| let label = "The width is "
2| let width = 94
3| let widthLabel = label + String(width)
```
And so on...
