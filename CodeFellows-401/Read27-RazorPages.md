# Read 27 - Razor Pages

## [Introduction to Razor Pages in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/?view=aspnetcore-2.2&tabs=visual-studio)
## [Introduction to ASP.NET Core Razor Pages - Damian Edwards](https://youtu.be/yyBijyCI5Sk)
## [Razor Pages with ASP.NET Core 2](https://gunnarpeipman.com/aspnet-core-razor-pages/)
## [Tutorial: Get started with Razor Pages in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/razor-pages-start?view=aspnetcore-2.1&tabs=visual-studio)
## [MVC vs Razor Pages - A quick comparison](https://jonhilton.net/razor-pages-or-mvc-a-quick-comparison/)

Razor Pages is one of those things that conceptually, at least at a high level, seems simple enough. It's templating that includes code in the template itself, therefore reducing (eliminating?) the need for controllers.

I'm not exactly clear *why* this is a useful. Certainly I can see why having less files, and less need to connect Axle A to Socket B, could be useful, but then stuffing more functionality into the same file(s) also moves away from modularization (and yes, how modular a particular design pattern is certainly somewhat subjective).

My additional Googling around the phrase "advantages of Razor Pages" turned up answers that were basically in line with the above... less files, "better" organized. I suppose this may be become more clear to me as we built out our ECommerce app and add the zillions and zillions of pages/views/files that will eventually make it up. Right now, it really isn't.

One thing that is interesting to me is the different design pattern that Razor Pages (sort of?) offers. I really mainly know MVC, and I've known for a while that other design patterns exist, but just haven't explored them in depth. The Damian Edwards video mentions MVVM, which I've looked up before, and again this evening. Similar to Razor Pages, it makes sense, in a high-level sense, but the actual implementation and advantages of that design pattern are not immediately apparent to me.