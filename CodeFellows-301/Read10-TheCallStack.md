# Read 10 - The Call Stack

## [MDN - Call Stack](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
## [Understanding the JavaScript call stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
## [JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

Really understanding how the call stack works, the call stacks printed with error messages, and how to debug code is vital to developing software.

For myself, I think about the call stack as a thread. It begins somewhere, depending on the langauge, program, etc., and winds its way through your code, jumping up levels and back down again, winding around and around in the same place (or into a third dimension) with a recursive function, and eventually being pulled back again to its origin having completed whatever the code path it went down did. Although of course the stack is a more literal interpretation of what's happening in the hardware.

Being able to print relevant data/entries/states to the console is a hugely important part of debugging, as sometimes (as like today!) the error your're fighting with originates in a librarie's file, not one of your own. Furthermore, when working with back-end code you can't throw breakpoints into a browser's developer console and step through a problem area.

One thing I still don't have a deep grasp of is proper error handling with try...catch blocks. How one can throw and error deep in a call stack and have it percolate up to a handler further up (well, down, in the traditional view of the call stack). I'm glad we're using try...catch statements now, but I want to see more complex and comprehensive error handling.

Finally, it's worth nothing that JS is different from most langauges in that you don't compile it before hand, and then run it. It is simply run in the browser, generally by an interpreter, but that does vary from browser to browser. So while in most langauges compiler errors will catch errors, in JS, everything is a runtime error.