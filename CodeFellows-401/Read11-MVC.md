# Read 11 - MVC

## [Overview of ASP.NET Core MVC](https://docs.microsoft.com/en-us/aspnet/core/mvc/overview?view=aspnetcore-2.2)
## [Introduction to ASP.NET Core with Visual Studio 2017](https://channel9.msdn.com/Series/Introduction-to-ASP.NET-Core-with-Visual-Studio-2017?l=LU6ABeE6C_8206218965)

I'm not sure which videos exactly we were supposed to watch, as they're not numbered. I watched the "Getting Started with ASP.NET Core", "Introduction to ASP.NET Core", "Routing and MVC", and "Creating a Form" videos.

This all felt very similar to the way you build a project in Xcode (at least back in the days of Objective-C). Creating a new project gives you a whole slew of default class and configuration files, and you add model, controller, and view classes to build out the functionality of your project. There's all kinds of built-in libraries and frameworks that I won't be familiar with until I actually do this for a while.

One thing I did notice: the diagram they kept showing for MVC was like this:

```
    v<<<[Model]<<<^
[View]          [Controller]
    ^>>>[User]>>>^
```

Which according to the MVC ideas that I learned is wrong. The model should *never* directly talk to the view; everything should pass through the controller. The "Overview of ASP.NET Core MVC" article even has this in its definition of the model: "The controller creates and populates these ViewModel instances from the model." So yeah... the model shouldn't be touching the view directly.

Finally, Microsoft *desperately* needs some production help with their videos. While full of all kinds of interesting technical tidbits, these videos were so boring.

## [Create a web app with ASP.NET Core MVC](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/?view=aspnetcore-3.1)

This felt similar to the video (skimming it, as instructed). Yep, very similar to building out a project in Xcode. Although of course in iOS dev you don't have access to full-blown SQL for your model, but rather SQLite wrapped in a library called CoreData. I did notice that you apparently don't need SSMS to work with a SQL database, but rather Visual Studio has its own built in functionality there.