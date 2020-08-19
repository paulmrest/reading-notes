# Read 33 - OAuth

## [Facebook, Google, and external provider authentication in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/?view=aspnetcore-2.1&tabs=visual-studio)
## [Authenticate with OAuth 2.0 in ASP.NET Core 2.0](https://www.jerriepelser.com/blog/authenticate-oauth-aspnet-core-2/)

It's a little odd that we're not being given a specific delegate for OAuth. The first article mentions Facebook and Google, and the second one GitHub.

Isn't the difficulty of OAuth in the fact that it's implemented by every delegate a little differently? So wouldn't be better for us to be reading about whichever delegate we're going to be using? Maybe it's GitHub, as the second article goes pretty in-depth on that (I think).

All of that said, OAuth is another of those things I've known about for a couple of years, but haven't had a chance to play around with. I know it's a open authorization standard that allows a site/app/etc. to use some "trusted" service like Facebook or Google to authenticate for them. So the user, rather than creating an account on Jo's Jangles and Jammboreens, is given the option to sign in using that third party service.

This is quite common now. It certainly can be a good thing if the delegate is responsible with your data, or a very bad if they are not. That said, I'll be interested in seeing which delegate we'll end up using, and all the particular headaches of their specific requirements.