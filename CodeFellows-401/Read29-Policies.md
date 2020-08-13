# Read 29 - Policies

## [Policy-based authorization in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/security/authorization/policies?view=aspnetcore-2.1)
## [Custom Authorization Policy Providers using IAuthorizationPolicyProvider in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/security/authorization/iauthorizationpolicyprovider?view=aspnetcore-2.1)

The content of the first link was largely what we've been doing since Async-Inn. I did notice that you can assign policies to methods in Razor Pages, which makes sense, but was certainly something I learned.

The second link is definitely far more interesting. That you can delegate creating policies to a class that implements IAuthorizationPolicyProvider is something I can see a lof ot potential for, as it would make sense that you'd want policies to be able to dynamically update or load an entirely different set of them based on some outside input. Then you can have multiple IAuthorizationPolicyProvider classes. I'd like to see how we end up implementing this in our e-Commerce Stores.