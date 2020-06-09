# Read 07 - REST

## [A Conversation about REST with my brother](https://gist.github.com/brookr/5977550)

I found this kind of an odd way of introducing **REST** (Representational state transfer). I am certainly no expert, but my understanding is and was that REST brought about the changes it did because it granted a conceptual framework that allowed web services to share a common design: **RESTful**.

Before REST the interet was certainly used by machines to communicate with each other. The issue was that there was no standarized mode of requesting or transmitting data, so such communications were generally confined to simple ask-receive interactions. REST, with its concept of "resources" created the ability to have multiple systems all communicating with each other, exchanging data (JSON and XML), or even scripts and applets. The "state" in the name refers to the machine sharing a limited scope of its state through a web service/API.

All of that said, REST/RESTful is one of those things I've known about in concept for a while, but haven't explored the actual implementation of. I'm really looking forward to understanding it on a more funtional level.

Polymorphism, although the article only just touches on it, is amazing. Being able to have an object belong to some sort of protocol (I don't know what it's called in JS) and then being able to tell an object, without knowing what it even is, only that it subscribes to that protocol, to do something is so incredibly useful. I can see how polymorphism may tie into web services/APIs as we move forward.