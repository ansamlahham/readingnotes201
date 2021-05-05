# Debugging
![](https://image.slidesharecdn.com/debugging-javascript-web-141030080414-conversion-gate02/95/debugging-javascript-1-638.jpg?cb=1415345877)

#### JavaScript can be hard to learn and everyone makes mistakes when writing it. This chapter will help you learn how to find the errors in your code. It will also teach you how to write scripts that deal with potential errors gracefully.


#### When you are writing JavaScript, do not expect to write it perfectly the first time. Programming is like problem solving: you are given a puzzle and not only do you have to solve it, but you also need to create the instructions that allow the computer to solve it, too.


#### When writing a long script, nobody gets everything right in their first attempt. The error messages that a browser gives look cryptic at first, but they can help you determine what went wrong in your JavaScript and how to fix it. 

JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.
1. RangeError
This is thrown when a number is outside an allowable range of values.
2. ReferenceError
 - This error is thrown when a reference made to a variable/item is broken. That is the variable/item doesnâ€™t exist.
3. SyntaxError
- This is the most common error we encounter. This error occurs when we type code that the JS engine can understand.
4. TypeError
- TypeError is used to indicate an unsuccessful operation when none of the other NativeError objects are an appropriate indication of the failure cause.
TypeError occurs when an operation is performed on a wrong data type. Maybe a boolean is expected but a sting is found.
5. URIError
- This indicates that one of the global URI handling functions was used in a way that is incompatible with its definition.
URI (Uniform Resource Indicator) in JS has the functions: decodeURI, decodeURIComponent, etc.
If we call any of them with the wrong parameter we will get a URIError
6. EvalError
This is used to identify errors when using the global eval() function. -This exception is not currently used within this specification. This object remains for compatibility with previous editions of this specification.
7. InternalError
- This error occurs internally in the JS engine, especially when it has too much data to handle and the stack grows way over its critical limit.
- This occurs when the JS engine is overwhelmed by too many recursions, too many switch cases, etc.

### Code Debugging

Programming code might contain syntax errors, or logical errors.

Many of these errors are difficult to diagnose.

Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

### JavaScript Debuggers
Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.

Built-in debuggers can be turned on and off, forcing errors to be reported to the user.

With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.

Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.

## [Check it out here using console.log method!](https://www.w3schools.com/js/tryit.asp?filename=tryjs_console)