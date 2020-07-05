# 401 - Read 01 - Exception Handling

## [How to debug for absolute beginners](https://docs.microsoft.com/en-us/visualstudio/debugger/debugging-absolute-beginners?view=vs-2019)

Pretty cut and dry. Tells you to think through your assumptions on your code, and consider what your code is actually doing. Then has a step-by-step on using the debugger.

One thing not really mentioned here is the value of printing things to the console for debugging. If you're building a data structure, rather than stepping through your code and seeing what it looks like at each iteration, you can just console print it at each iteration and see a complete picture of what happened.

## [How to use the try/catch block to catch exceptions](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/how-to-use-the-try-catch-block-to-catch-exceptions)

Rather than letting the execution of your program halt every time it encounters an error, you can enclose code that can produce an error in a `try{}` block. One or more `catch` statements following the `try` will then catch the designated error and execute their code.

One thing I have been curious about with error handling is how commercial software will have some kind of error logging. Is this generally an ErrorHandling class that uses a singleton and writes those errors to a file? Or is there another way this is done?

## [Statement keywords](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/statement-keywords)

Something that stood out to me here is the `yield` keyword. Specifically when used on a return statement, it causes the return to be done iteratively, so each element is returned one at a time, rather than in a single structure. I'm not entirely sure why you'd want to be able to do that, but I'm interested in finding out more!

## C# 7.0 in a Nutshell by Joseph and Ben Albahari
### Chapter 04: Advanced C#
### Pages 158 - 166

A more detailed look at the try/catch logic than the above Microsoft article. A few things stood out to me here:
- There is a "catch all" option for `catch` statements: System.Exception (all exceptions are subclasses of this).
- I haven't done much, if anything, with a `finally` block, either in previuos CF classes or before that. Curious to see ways that's used.
- System.Exception has a StackTrace and an InnerException property. The StackTrace makes sense, although I'd not thought of what properties in an error object allow it to display its stack trace. The InnerException also makes sense, but is just interesting structurally that an error can contain another error inside of it.

## [Wikipedia: Therac-25](https://en.wikipedia.org/wiki/Therac-25)

This is amusing, and horrifying, in just how confident the engineers were in something desgined to shoot radiation at live humans. Not testing the software with the actual hardware it was going to be integrated with until they were building the first production unit is just nuts. It's also telling that one of the causes of the error was a certain combination of commands which seems like a very common one for a technician. No matter how well you think you understand your system, it needs to be tested wtih actual users...

I am also curious what those number displayed along with the MALFUNCTION signified. Did the manufacter even know?

## [Wikipedia: Ariane 5](https://en.wikipedia.org/wiki/Ariane_5)

The history of rocketry is full of hilarious and absurd errors, of which only a few, thankfully, have resulted in loss of life. Ariane 5 501 is one of the most famous ones (right up there with a Russain technician hammering angular velocity sensors into place upside down, resulting the Proton-M [crashing spectactularly](https://youtu.be/vqW0LEcTAYg) in 2013). Reusing software and hardware from the Ariane 4 seems like potentially a good place to start, but then you need to test it. This flaw was particularly bad because the subsystem that caused the loss of vehicle didn't even need to be running in the Ariane 5 after launch, but was because it hadn't been changed from the 4.
