# Read 04 - Classes and Objects

## [Classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)
## [Constructors](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)
## [Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)
## [C# Heap(ing) Vs Stack(ing) In .NET - Part One](https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/)
## [Fundamentals of garbage collection](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)

One of the things that disappointed me about CF from the beginning was the relative lack of Object-Oriented Programming (OOP) in the teaching thus far.

I am sure there are a number of reasons for this. JavaScript isn't a full OOP language (a classless OOP language is missing out on the best parts...). Additionally there may have been attempts at teaching OOP principles earlier and it was found it was better to wait.

Really I just wanted to get to OOP because I find it freaking cool, and I want to share that with others. I still vividly remember the moment I learned what classes are, and objects, and inheritance, while studying Java, and I saw the kind of possibilities of what you can build.

These articles largely go over the basics of OOP: classes, inheritance (although not much on polymorphism), objects vs classes, constructors, properties, getters and setters, a little on public vs private, the heap and stack, and garbage collection. Although garbage collection (GC) isn't strictly OOP, although having robust GC in a full blown OOP environment is important, as one can create quite large objects. I do wonder how people who haven't been exposed to OOP will process this, after a couple of months of working in JavaScript.

One thing I learned (or maybe learned again): the heap vs stack article clarified that reference types (objects) are stored in the heap, while value types are stored, well, it depends, but largely in the stack.