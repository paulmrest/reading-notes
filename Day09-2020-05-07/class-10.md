# Read 10 - JS Debugging

## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 10 - Error Handling & Debugging

Understanding how JS code gets executed is essential to not only writing software, but debugging it when something (inevitably) goes wrong. **Lexical scope**, **the stack**, and the **order of execution** are all core concepts of how JS code gets interpreted and run.

While there are errors that simply give an unexpected result, there are also errors that throw an **exception** and produce a **Error** object. Error objects come in several types, in addition the generic `Error` type, there is also the `RangeError`, the `SyntaxError`, etc... Error objects are created with several properities and can be queried like any object.

When an execption is hit in your code, you have to **debug** it. There are two main approaches to debugging code:

* Logging data to the console: this allows you as a developer to display what is happening inside your functions, classes, etc... In addition to `console.log`, there is also `console.error`, `console.assert` (which allows a condition to be tested and only logs to the console if that condition is false), and others. It is important to note that debugging code should always be removed from software before it is merged into a production branch.

* Breakpoints: most places that can run JS (mainly web browsers for our purposes) include the ability to view the code and set **breakpoints** in the code. If you know where the error is occurring (and modern browswers all give the line number where the exception occurred), you can set a breakpoint at or just before that point, and then step through the code, and see how the data is being manipulated.

In real-world applications, code that can potentially generate exceptions is placed in a **try, catch, and finally** statement. The potentially exception producing code is placed in the `try` block, the code that catches and handles that exception is in the `catch` block, and then the `finally` block is always executed, regardless of whether there was an exception. Try, catch, and finally statements allow software to hit exceptions and keep going, while potentially logging error information somewhere.