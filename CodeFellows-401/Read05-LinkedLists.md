# Read 05 - Linked Lists

## [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)
## [What’s a Linked List, Anyway? [Part 1]](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
## [What’s a Linked List, Anyway? [Part 2]](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

Linked lists are data structures consisting of discrete nodes. Each node is either linked to just the next node:

### Singly Linked

```
| NODE |next] -> | NODE |next] -> | NODE |next] -> ...
```
Or both the preceding and succeeding notes:

### Doubly Linked

```
[prev| NODE |next] <=> [prev| NODE |next] <=> [prev| NODE |next] <=> ...
```

Unlike arrays, linked lists are more dynamic, and can have elements inserted and removed ad nauseam. They exist in memory with each node occupying its own chunk of space, with a link to one or more other nodes. So when a new node is added, or a node removed, it is simply a matter of changing the links of the surrounding nodes.

That said, there is a cost to this ease. Linked lists are more costly, both in terms of time and space, to work with, as compared to arrays. Inserting a new node into a linked list is O(n). A general rule of thumb is to use arrays when the structure can just stay static after its creation, and potentially use a linked list otherwise. Although there are other data structures that may be more appropriate to a given use.

***

The above articles all largely cover the same topics in different ways. One thing mentioned in the Medium articles is circular linked lists. I am wondering what a good use-case for a circular linked list might be.