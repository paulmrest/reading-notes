# Read 30 - Hash Tables

## [Hashtables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
## [What is a HashTable Data Structure - Introduction to Hash Tables , Part 0](https://youtu.be/MfhjkfocRR0)
## [Basics of Hash Tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
## [Hash table](https://en.wikipedia.org/wiki/Hash_table)

This is actually a data structure I've not worked with before, so I'm quite excited.

I actually didn't know before reading this that hash tables employ an array of linked lists to store data. That makes so much sense from an efficiency perspective, as computing a hash value from a key is, in general, much faster than iterating over a large array, or similar one-dimensional data structure.

I'm immensely curious about how the hash function is optimized for different use cases, as both a very shallow and a very deep hash table could both be inefficient. Do most hash table implementations just choose a middle of the road hash function, or are there those that try to dynamically predict what kinds of keys will be used based off the first one? Or, better yet, are there those that build/select a hash function based off the already present keys? If a hash table is being used frequently, I could see the value in re-mapping everything to a new hash table with a different hash function.

It's also curious that I didn't dig into this further when I was working Java, as HashMap is not an uncommon data structure to use. Or maybe I did and it just didn't stick?