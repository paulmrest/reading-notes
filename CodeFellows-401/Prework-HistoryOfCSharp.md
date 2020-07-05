# 401 - Prework - History of C# and the .NET Framework

## [The history of C#](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-version-history)

MS's documentation is, as frequently noted, incredibly dry. This is no exception. I did, however, find it amusing how vehement the author of this article is in extolling the distance between C# and Java. That said, this made me remember how much I miss working in a big OOP language. JS is fun, and kind of nutty with what it will *try* to run, but I miss the kind of big powerful features in a language like Swift, Java, and C#.

I"m also looking forward to really diving into a couple of topics mentioned here: generics and lambda expressions. I've done some with both of those, but never had a chance to really understand them in any satisfactory way.


## [.Net Core Guide](https://docs.microsoft.com/en-us/dotnet/core/)
This is another of those chunks of documentation that has all kinds of details about how to install and setup and other specifics, but never actually bothers to tell you *what* .NET Core is. For that I had to look elsewhere, and the best answer I found was [a StackOverflow answer](https://stackoverflow.com/a/26908101/2149946). Runtime environments! Brings me back to learning Java, and hearing and reading endless meditations on how terrible Java is/was due to its RTE. Maybe .NET Core is better?


Regardless, this seems like something I'd need to actually get in and start implementing to grasp what it is capable of.


## Tooling Videos:
### [What is .NET](https://dotnet.microsoft.com/learn/dotnet/what-is-dotnet)
### [What is a .NET Hello World App](https://www.youtube.com/watch?v=uKoqBCyFATw&list=PLdo4fOcmZ0oWoazjhXQzBKMrFuArxpW80&index=3)
### [Basic Debugging](https://www.youtube.com/watch?v=feWeInify18&list=PLdo4fOcmZ0oWoazjhXQzBKMrFuArxpW80&index=4)
### [What is Managed Code](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)
### [What is the CLR](https://docs.microsoft.com/en-us/dotnet/standard/clr)

The title of the videos led me to think this would be more about .NET Core, but the videos were more about the basics of developing in .NET using Visual Studio. What .NET can be used to build, going over a fairly simply program in a kind of adjacent way (the video wasn't actually about building a Hello World program, but rather them talking about a simple banking program they built in another video series), and debugging. The debugging video just went over breakpoints, moving around in code in debugging mode, and some VS capabilities while debugging (like notes!).

The Managed Code and CLR articles were a good intro to both of those topics. I did find the Managed Code article personally interesting as it gave me another set of terms to talk and think about higher and lower-level languages (say C vs Swift). I always thought if more in terms of abstraction, but it is about the runtime environment managing things so you don't have to.


## [Introduction to the C# Language and the .NET Framework](https://docs.microsoft.com/en-us/dotnet/csharp/getting-started/introduction-to-the-csharp-language-and-the-net-framework)

This article is basically a big sales pitch for how C# is a modern OOP language, with all kinds of capabilities. Of particular interest to me is LINQ, as the ability to interact with data structures as a set, rather than iteratively, does seem like it could offer substantial advantages. Also, set-based operations have always escaped my intuitive grasp, so more interaction with them is something I'd like.

It is interesting how .NET compiles C# code into an intermediate language that conforms to CTS, so .NET/C# has all kinds of capabilities of interacting with libraries and other entities in CTS-compliant languages.


## [C# Arrays](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/)

There's not a lot I can say about this. C# arrays are strongly typed, have a static length, and otherwise conform to what one would expect in an OOP language that passes object-types as references to methods. There are implicitly typed arrays, although I don't know *what* does the work of typing those. There's also generics, which allows some flexibility around typing. Beyond that, C# arrays are like a lot of other OOP language arrays I've worked with (JS arrays are more like Python Lists or arrays in Swift).


## C# 7.0 in a Nutshell by Joseph and Ben Albahari
### Chapter 01: Introducing C# and the .NET Framework
### Chapter 02: C# Language Basics

Chapter 01 here went over a lot of the same stuff we saw in the previous articles. C# is a OOP language with strong type safety... CLR and IL and JIT and so on. One thing I found useful is the diagram on page 4 of my copy of the book showing where the different chapters in the book fit into the .NET Framework. I'd actually like to see a much larger and more detailed version of that chart for all programming books.

Chapter 02 goes into the basics of C# structure and syntax. Most of this is pretty standard modern OOP language stuff, although a few things stood out to me:

- Overriding keywords with *@*: so you can use keywords for identifiers as long as they are prefixed with the "@" symbol. So you could have a class called `false` as long as it was declared as `@false`.

- The `params` modifier on method declarations to allow it to accept any number of parameters.

- The `ref` local variable functionality, which is described as "esoteric". I'm not sure why that even exists, but I'm looking forward to finding out.

- Null-conditional operators: this reminds me of Swift optionals, with a similar syntax. This was something I understood in theory but was never able to do enough with Swift to really get a solid functional grasp of.

- Tuples: just because I really like tuples, and have missed being to use them in JS (although you can sort of use an object literal there as a substitute).