---
layout: feature
name: 'Optional'
iid: Optional
status: DOING
language: swift
abstract: "You use optionals in situations where a value may be absent."
links:
 - link:
    name: 'The Swift Programming Language: The Basics, Optionals'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID330
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'Optionals in Swift'
    url: https://blog.sabintsev.com/optionals-in-swift-c94fd231e7a4
    description: ' - To nil or not to nil'
    type: tutorial
features:
 - Variable
 - Constant
---

TODO.

<pre><code>let possibleNumber = "123"
let convertedNumber = possibleNumber.toInt()
// convertedNumber is inferred to be of type "Int?", or "optional Int"
</code></pre>

##nil

<pre><code>var serverResponseCode: Int? = 404
// serverResponseCode contains an actual Int value of 404
serverResponseCode = nil
// serverResponseCode now contains no value
</code></pre>


##if Statements and Forced Unwrapping

<pre><code>if convertedNumber != nil {
    println("convertedNumber contains some integer value.")
}
// prints "convertedNumber contains some integer value."
</code></pre>


##Optional Binding

<pre><code>if let actualNumber = possibleNumber.toInt() {
    println("\'\(possibleNumber)\' has an integer value of \(actualNumber)")
} else {
    println("\'\(possibleNumber)\' could not be converted to an integer")
}
// prints "'123' has an integer value of 123"
</code></pre>


##Implicitly Unwrapped Optionals

<pre><code>let possibleString: String? = "An optional string."
let forcedString: String = possibleString! // requires an exclamation mark
 
let assumedString: String! = "An implicitly unwrapped optional string."
let implicitString: String = assumedString // no need for an exclamation mark
</code></pre>
