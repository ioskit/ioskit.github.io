---
layout: functional
name: 'Higher Order Function'
iid: HigherOrderFunction
status: DONE
abstract: "Higher-order functions can receive other functions as their parameters."
---

__Higher-order functions__ can receive other functions as their parameters.

[Swift](/Swift) provides higher-order functions such as `map`, `filter`, and `reduce`. Also, in [Swift](/Swift), we can develop our own 
higher-order functions and DSLs.

```
func addTwoInts(_ a: Int, _ b: Int) -> Int {
    return a + b
}

func printMathResult(_ mathFunction: (Int, Int) -> Int, _ a: Int, _ b: Int) {
    print("Result: \(mathFunction(a, b))")
}

printMathResult(addTwoInts, 3, 5) // Prints "Result: 8"
```

It implies that this language supports [First-class functions](/functional/FirstClassFunction).

See [Swift's Function](/Function) page for more details.
