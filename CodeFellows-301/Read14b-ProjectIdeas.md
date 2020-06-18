# Read 14b - Project Ideas

As this week has kind of kicked my butt in terms of available time, I really haven't had a chance to think much about projects.

That said, I did think of an idea about six months ago that I am excited to now know enough to take on, although I don't know if the idea is too big for a 301 project.

***

## Project Idea 01:

A web app that allows you to determine whether your local bars will be overrun with loud sports fans because an important game is on. I initially conceived of this as a way of avoiding this, as I've been in the situation of going to a dive bar with a friend and being surprised by it being insanely crowded and loud. Since then, people have pointed out that it could be used for the opposite scenario: wanting a loud bar overrun with screaming sport fans.

### Needed APIs:
* Bars/restaurants by location: this would just be like something like Yelp where the user enters a city/neighborhood/address/latitude and longitude, and we get a list of bars (and restaurants with bars). Preferably, this would be a based on a set of keywords like "sports bar".
* Scheduled sport games by location and date/time: this I haven't found yet, but I haven't had time to really dig into this. I'd need an API that returns all the popular sport games that are happening on a specific date (taking into account current time so the user isn't warned of games that happpened too long to still be underway). Then some logic around how "big" the game is, and whether the game is regionally relevant to the user's location.

So the user would be given a list of local bars and restaurants parsed either by the API's keyword, or by some internal logic (just looking for the word "sport" to occur multiple times in the description and reviews would do it). Then each of those bars would be have a "sportiness" rating, which would indicate how likely the bar is to be full (or get full in the near future) of loud sports fans. Click on the sportiness rating would give the reason why (NFL: The T-Rexes are playing The Shadows at 3 PM).