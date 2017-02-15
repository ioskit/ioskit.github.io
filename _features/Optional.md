---
layout: feature
name: 'Optional'
iid: Optional
status: DONE
language: swift
abstract: "You use optionals in situations where a value may be absent."
code:
  gist: aa39f331d6008dd18a2157bc1a6618a7
  iswift: qBHwNO
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1)'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID330
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

* TOC
{:toc}

You use optionals in situations where a value may be absent.

<!--
```
// Defining
let possibleNumber = "123"
let convertedNumber = possibleNumber.toInt() // convertedNumber is inferred to be of type 'Int?' or 'Optional<Int>"


// Nil
var serverResponseCode: Int? = 404 // serverResponseCode contains an actual Int value of 404
serverResponseCode = nil           // serverResponseCode now contains no value


// if Statements and Forced Unwrapping
if convertedNumber != nil {
    println("convertedNumber contains some integer value.")
}
// prints "convertedNumber contains some integer value."


// Optional Binding
if let actualNumber = possibleNumber.toInt() {
    println("\'\(possibleNumber)\' has an integer value of \(actualNumber)")
} else {
    println("\'\(possibleNumber)\' could not be converted to an integer")
}
// prints "'123' has an integer value of 123"


// Implicitly Unwrapped Optionals
let possibleString: String? = "An optional string."
let forcedString: String = possibleString! // requires an exclamation mark
 
let assumedString: String! = "An implicitly unwrapped optional string."
let implicitString: String = assumedString // no need for an exclamation mark


// Nil-Coalescing Operator (Optional<AType> ?? AType)
let notOptionalString = possibleString ?? "default value"
```
-->