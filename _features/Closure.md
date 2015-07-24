---
layout: feature
name: 'Closure'
id: Closure
status: DOING
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
---

Closures are self-contained blocks of functionality that can be passed around and used in your code. Closures in Swift are similar to blocks in C and [Objective-C](/ObjectiveC) and to lambdas in other programming languages.

Closures <u>can capture and store references to any constants and variables from the context in which they are defined</u>. This is known as closing over those constants and variables, hence the name “closures”. [Swift](/Swift) handles all of the memory management of capturing for you.

Global and nested functions, as introduced in [Functions](/Function), are actually special cases of closures. Closures take one of three forms:

* Global functions are closures that have a name and do not capture any values.
* Nested functions are closures that have a name and can capture values from their enclosing function.
* Closure expressions are unnamed closures written in a lightweight syntax that can capture values from their surrounding context.

Functions           | Named&nbsp;&nbsp;| Capture Values
--------------------|--------|---------------
Global              | Yes    | No
Nested              | Yes    | Can
Closure expressions&nbsp;&nbsp;| No     | Can



[Swift](/Swift)’s closure expressions have a clean, clear style, with optimizations that encourage brief, clutter-free syntax in common scenarios. These optimizations include:

* Inferring parameter and return value types from context
* Implicit returns from single-expression closures
* Shorthand argument names
* Trailing closure syntax

## Closure Expressions

