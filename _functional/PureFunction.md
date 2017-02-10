---
layout: functional
name: 'Pure Function'
iid: PureFunction
status: DONE
abstract: "Pure functions do not rely on data outside of themselves and they do not change data that exists outside of them. They provide the same result each time that they are executed"
---

In functional programming, __pure functions__ are the most important building blocks. Pure functions do not rely on data outside of themselves 
and they do not change data that exists outside of them. Pure functions are easy to test because they will always provide the same results 
each time that they are executed.
 
```
func addTwoInts(_ a: Int, _ b: Int) -> Int {
    return a + b
}

print("Result: \(addTwoInts(2, 3))")
```

__Pure Function is a way of programming, not an intrinsic property of languages.__ 

This property of pure functions is called referential transparency and makes it possible to conduct equational reasoning on the code.

Pure functions can be executed on different threads or cores without any mechanisms to handle multithreading and multiprocessing. This is a 
very important benefit of functional programming over OOP as multicore programming mechanisms are very complex to handle in OOP. Also, 
programming for multicore computers is becoming more important day by day because hardware engineers have finally hit the speed limit of light. 
Computer clocks will not be getting faster in the near future so, in order to have more cycles per second, hardware engineers are adding more 
processors to chips. There seems no end to how many processors we will have in our computers. A higher number of processors to be used for a 
program means a more complex multithreading and multicore mechanism to handle.

Functional programming eliminates the need for a complex multicore programming mechanism, and as pure functions are not dependent on any 
instances or data outside of themselves, it is easy to change them without changing other parts.
