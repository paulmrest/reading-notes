# Read 10 - Stacks & Queues

## [Stacks and Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

There's not a lot I can say about stacks and queues. They're both 1d data-structures with rules around how you add and remove items from the structure.

Stacks are frequently visualized as a pile of disks with holes in the middle, placed onto a rod so they can't be slid out of the stack. As any one-year-old playing with a toy like this knows, such an arrangement is First-in-Last-Out (FILO) (whatever you put on the stack first ends up at the bottom, and everything else needs to be taken off before you can get access to it again). Extending off FILO, stacks are also Last-in-First-Out (LIFO), which, again is obvious from the common visualization and toy versions: whatever you added last, is at the top of the stack.

Queues are basically the opposite in order of operation for adding/removing items. The queue flows one direction or the other (they are generally visualized as horizontal, like a line of people, but could just as easily be visualized as a stack with a catch mechanism instead of a base), so they are FIFO and LILO. Anything added to a queue needs to flow all the way through it, as other items are removed (ahem, dequeued). So whatever you added to a queue first, is dequeued first.

I will add this: stacks and queues are a common data construct in inventory systems, as inventory systems frequently use both FILO and FIFO. And despite the relative simplicity of stacks and queues as data structures, inventory systems are generally very complicated and hard to get working right. I've never quite understood why they are so hard to implement. Maybe one day I'll try my own.