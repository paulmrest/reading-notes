# Read 06 - Node, Express, and APIs

## [What Is Node and When Should I Use It?](https://www.sitepoint.com/an-introduction-to-node-js/)

This was fascinating. I had no idea that **Node.js** had such a major effect on the history of web development. I found a few things particuarly interesting:

* You can run JS code from the terminal (`node my-js-file.js`). Coupled with a lightweight code editor like Sublime Text or Notepad++, being able to run code outside of a project in VSCode or another IDE quickly and easily strikes me as quite useful. I've been using repl.it for running my test code for the Code Challenges, and even on my new computer, it frequently freezes or even crashes. Being to just run pure JS in the terminal avoids all that.

* That before the Node Express framework server requests were synchronous is fascinating. I have some experience with manually managing multi-threaded programming in Objective-C, and I can absolutely imagine how having a separate thread for every request made on a server was taxing on resources. I would like to dive more into [libuv](https://github.com/libuv/libuv) to understand the implementation of this event-driven execution.

* It also never occurred to me before reading this that prior to Node's Express framework, servers had to be set up using a different language. While any good develoepr can jump around between language, it is more difficult to jump around between languages in the same phase of a project. Being able to use/re-use JS in the server strikes me as greatly simplifying things.