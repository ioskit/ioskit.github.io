---
layout: feature
name: 'Closure'
iid: Closure
status: DONE
language: swift
abstract: "Closures are self-contained blocks of functionality that can be passed around and used in your code. Closures in Swift are similar to blocks in C and Objective-C and to lambdas in other programming languages."
links:
 - link:
    name: 'The Swift Programming Language, Functions and Closures'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID463
    description: ' - Apple Developer'
    type: reference
 - link:
     name: 'The Swift Programming Language, Closures'
     url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html
     description: ' - Apple Developer'
     type: reference
features:
 - Function
 - Block
---

## Presentation

Closures are self-contained blocks of functionality that can be passed around and used in your code. Closures in Swift are similar to [Blocks](/Block) in C and [Objective-C](/ObjectiveC) and to lambdas in other programming languages.

Closures <u>can capture and store references to any constants and variables from the context in which they are defined</u>. This is known as closing over those constants and variables, hence the name “closures”. [Swift](/Swift) handles all of the memory management of capturing for you.

<pre><code>{ ( param1 :Type1, param2 :Type2 ) -> ReturnType in
	// a line of code
	// another line of code
	return returnValue
}</code></pre>

Global and nested functions, as introduced in [Functions](/Function), are actually special cases of closures. Closures take one of three forms:

* Global functions are closures that have a name and do not capture any values.
* Nested functions are closures that have a name and can capture values from their enclosing function.
* Closure expressions are unnamed closures written in a lightweight syntax that can capture values from their surrounding context.

Functions           | Named&nbsp;&nbsp;| Capture Values
--------------------|--------|---------------
Global              | Yes    | No
Nested              | Yes    | Can
Closure expressions&nbsp;&nbsp;| No     | Can


<table class="table table-striped table-hover">
  <thead>
    <tr><th>Functions</th><th>Named</th><th>Capture Values</th></tr>
  </thead>
  <tbody>
  	<tr><td>Global</td><td>Yes</td><td>No</td></tr>
	<tr><td>Nested</td><td>Yes</td><td>Can</td></tr>
	<tr><td>Closure expressions</td><td>No</td><td>Can</td></tr>
  </tbody>
</table>

[Swift](/Swift)’s closure expressions have brief syntax in common scenarios. These optimizations include:

* Inferring parameter and return value types from context
* Implicit returns from single-expression closures
* Shorthand argument names
* Trailing closure syntax

## Closure Expression Syntax

### The sorted sample

[Nested functions](/Functions#Nested) are a convenient to define self-contained blocks of code. However, it is sometimes useful to write shorter versions of function-like constructs without a full declaration and name. This is particularly true when you work with functions that take other functions as one or more of their arguments.

As sample we shall use a Swift’s standard function called `sorted`, which sorts an array of values of a known type according to the sorting closure provided in parameter.
The initial [Array](/Array) to sort is: `let names = ["Chris", "Alex", "Ewa", "Barry", "Daniella"]`
In this case the function parameter needs to be a function of type `(String, String) -> Bool`: the two `String` elements to compare in parameter and a `Bool` as result.



### From the named function...

We can use a classic named function:
<pre><code>func backwards(s1: String, s2: String) -> Bool { return s1 > s2
}
var reversed = sorted(names, backwards)
// reversed is equal to ["Ewa", "Daniella", "Chris", "Barry", "Alex"]
</code></pre>

But the wanted behaviour is concentrated in the single 2nd line!



### ... To the closure

So, a better way here is to use a closure:

<pre><code>reversed = sorted(names, { (s1: String, s2: String) -> Bool in 
	return s1 > s2 
})</code></pre>



### On a single line

or on a single line:

`reversed = sorted(names, { (s1: String, s2: String) -> Bool in return s1 > s2 })`



### Without (inferred) types

Because the sorting closure is passed as an argument to a function, [Swift](/Swift) can infer the types (of parameters, type of return). This means that a lot of things do not need to be written: `(String, String)`, `Bool`, return arrow `->` and parentheses around parameters:

`reversed = sorted(names, { s1, s2 in return s1 > s2 } )`



### Without (obvious) return

Single-expression closures can implicitly return the result of their single expression: the `return` keyword can be omitted:

`reversed = sorted(names, { s1, s2 in s1 > s2 } )`



### With anonymous parameters

Swift automatically provides shorthand argument names to inline closures, which can be used to refer to the values of the closure’s arguments by the names `$0`, `$1`, `$2`, and so on.

`reversed = sorted(names, { $0 > $1 } )`



### Or only the operator

Swift’s `String` type defines its string-specific implementation of the greater-than operator `>` as a function that has two parameters of type `String`, and returns a value of type `Bool`. This exactly matches the function type needed for the sorted function’s second parameter. Therefore, you can simply pass in the greater-than operator, and Swift will infer that you want to use its string-specific implementation:

`reversed = sorted(names, > )`

For more about operator see [Operator Functions](/OperatorFunctions).



### Summary

`reversed = sorted(names, { (s1: String, s2: String) -> Bool in return s1 > s2 })`

`reversed = sorted(names, { s1, s2 in return s1 > s2 } )`

`reversed = sorted(names, { s1, s2 in s1 > s2 } )`

`reversed = sorted(names, { $0 > $1 } )`

`reversed = sorted(names, > )`



## Trailing Closures

When a closure is passed to a function as the last parameter it can be defined just after the body of the function instead of in the parameters list:

`reversed = sorted(names, { $0 > $1 } )`

can become:

`reversed = sorted(names) { $0 > $1 }`

That is most useful when the closure is sufficiently long that it is not possible to write it inline on a single line. As an example, Swift’s Array type has a map(_:) method which takes a closure expression as its single argument. The closure is called once for each item in the array, and returns an alternative mapped value (possibly of some other type) for that item. These closures can be long in numerous scenarios.


## Variable Parameters

As a [Function](/Function), you can use [Variable Parameters](/Functions#VariableParameters) in a closure. So that the parameter’s value can be modified within the closure body, rather than declaring a new local variable and assigning the passed value to it.

As a reminder, variable parameters are *variable copy*: future new values of the parameter, assigned inside the function, are not available from outside.



## Capturing Values

<pre><code>func makeIncrementer(forIncrement amount: Int) -> () -> Int {
    var runningTotal = 0
    func incrementer() -> Int {
        runningTotal += amount
        return runningTotal 
    }
    return incrementer 
}

let incrementByTen = makeIncrementer(forIncrement: 10)
incrementByTen() // returns a value of 10 
incrementByTen() // returns a value of 20 
incrementByTen() // returns a value of 30

let incrementBySeven = makeIncrementer(forIncrement: 7) 
incrementBySeven() // returns a value of 7
incrementByTen() // returns a value of 40
</code></pre>

In this code, the nested function `incrementer` take a *reference* (and not just a copy of its initial value!) to the `runningTotal` variable defined from its surrounding function.

Capturing a reference ensures that `runningTotal` does not disappear when the call to `makeIncrementer` ends, and ensures that `runningTotal` is available when the `incrementer` function will be called.

However, because it does not modify `amount`, and `amount` is not mutated outside it, `incrementer` actually captures and stores a copy of the value stored in `amount`. This value is stored along with the new `incrementer` function.

Swift determines what should be captured by reference and what should be copied by value. You don’t need to annotate amount or runningTotal to say that they can be used within the nested incrementer function. Swift also handles all memory management involved in disposing of runningTotal when it is no longer needed by the incrementer function.

If you assign a closure to a property of a class instance, and the closure captures that instance by referring to the instance or its members, you will create a strong reference cycle between the closure and the instance. Swift uses capture lists to break these strong reference cycles. For more information, see Strong Reference Cycles for Closures.



## Closures Are Reference Types

In the example above, `incrementBySeven` and `incrementByTen` are constants, but the closures these constants refer to are still able to increment the `runningTotal` variables that they have captured. This is because functions and closures are reference types.

Whenever you assign a function or a closure to a constant or a variable, you are actually setting that constant or variable to be a reference to the function or closure. In the example above, it is the choice of closure that `incrementByTen` refers to that is constant, and not the contents of the closure itself.

This also means that if you assign a closure to two different constants or variables, both of those constants or variables will refer to the same closure:

<pre><code>
let alsoIncrementByTen = incrementByTen
alsoIncrementByTen() // returns a value of 50
</code></pre>



## Conclusion

Functions and closures are reference types.

A closure is a good feature when:

* you want write a short way function (anonymous function and parameters with inferred types)
* who can use variables from the calling context

But, as behaviour is inlined, be carful that closures prevent reuse.
