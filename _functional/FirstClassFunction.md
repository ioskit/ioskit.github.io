---
layout: functional
name: 'First Class Function'
iid: FirstClassFunction
status: DOING
abstract: "First-class functions are types that can be stored, passed, and returned."
---

Functions are __first-class__ types in [Swift](/Swift) as they are in languages such as [Ruby](/Ruby), [JavaScript](/JavaScript), and [Go](/Go) 
so they can be stored, passed, and returned. 

First-class functions empower functional programming style in [Swift](/Swift).

```
func addTwoInts(_ a: Int, _ b: Int) -> Int {
    return a + b
}

var mathFunction: (Int, Int) -> Int = addTwoInts

print("Result: \(mathFunction(2, 3))")
```

See [Higher-order functions](/functional/HigherOrderFunction).

See [Swift's Function](/Function) page for more details.
