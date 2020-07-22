# Read 13 - Dependency Injection & Repository Design Pattern

## [Dependency injection in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-3.1)
## [Design the infrastructure persistence layer](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design#the-repository-pattern)
## [Repository Design Pattern](https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30)
## [30 Days of TDD: Day Five – Make Your Code SOLID](https://www.telerik.com/blogs/30-days-of-tdd-day-five-make-your-code-solid)
## [Why SOLID Matters](https://www.telerik.com/blogs/why-solid-matters)
## [The S.O.L.I.D Principles in Pictures](https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898)

Dependency injection reminds me a lot of loose coupling, which is hugely important for good, modular, software design. In C#, this seems to be built around interfaces, so, as an example, a client class can, rather than depending on a specific library/framework/dll/whatever, just hand another object that implements an interface knowing that with that implementation, everything the client class needs to be done will be. The more specific details of this for an ASP.NET Core Web App, will, I am sure, become much clearer tomorrow and subsequent days. But certainly for something like databases tables with model objects, I can see how implementing interfaces with dependency injection could make far more maintainable code.

Repository Design feels similar to general ideas around keeping software modular and simple, only applied to model objects.

SOLID is a set of principles for designing software meant (I believe) to make testing easier. Most of these felt similar to other principles of good software design, although there is one that stood out to me: The Liskov Substitution Principle. This states that if you replace any object in your program with another objects that inherits from the original, your program should not break. This makes intuitive sense to me, both in terms of what it is seeking to accomplish, and the (potential) difficulty of following this. In my experience of OOP programming, I have definitely overridden a superclass's method with a subclass in such a way that would have violated the Liskov Substitution Principle. This is similar to the "extend, never modify" notion of OOP inheritance (which is also covered under SOLID's "Open/Close Principle").