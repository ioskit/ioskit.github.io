---
layout: functional
name: 'Immutability'
iid: Immutability
status: DONE
abstract: "The capability to define immutable values—in other words, constants— is one of the key concepts in functional programming. Once constants are initialized, they cannot be altered."
---

[Swift](/Swift) makes it easy to define immutable values—in other words, constants—and empowers functional programming as immutability is 
one of the key concepts in functional programming. Once constants are initialized, they cannot be altered. 

Although it is possible to achieve immutability in languages such as [Java](/Java), it is not as easy as [Swift](/Swift). To define any 
immutable type in [Swift](/Swift), the `let` keyword can be used no matter if it is a custom type, collection type, or a `struct` type.

```
let pi = 3.14159
pi = 4 // failed!
```

See [Swift's Constant](/Constant) page for more details.
