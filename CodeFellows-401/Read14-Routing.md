# Read 14 - Routing within MVC and Core

## [ASP.NET MVC Routing Overview (C#)](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)
## [Routing in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing?view=aspnetcore-3.1)

Reviewing both of these, one thing that did occur to me is: I have no idea what the square-bracket values we keep seeing above method definitions are. They're used in xUnit (`[Fact]` and `[Theory]`), and now in MVC/ASP.NET Core Web Apps. Those, as it turns out, are [Attributes](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/z0w1kczw(v=vs.100)?redirectedfrom=MSDN), and you can even [make your own](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/sw480ze8(v=vs.100)).

Beyond that, it was interesting to start to get an idea of how Visual Studio builds an MVC project. At this point, I still feel like I have only the barest notion of how the different controllers are getting instantiated from Startup.cs, although this helped some.

When learning Xcode, I remember it helped *immensely* once I understood how Xcode assembled the various pieces of a project together into an executable application. So learning about Visual Studio building the Routing Table and a glimpse into the application's lifecycle (Global.asax, Startup.configure, etc...) feels like when I was just starting to put the pieces of an iOS app in Xcode together in my head.

It is also interesting *how* many different ways routing can be configured in an MVC app in Visual Studio. As we've only used one of those so far (I think?), I am looking forward to learning more about the others in this class and afterwards.