---
layout: feature
name: 'Variable'
iid: Variable
status: DONE
language: swift
abstract: "Defines with 'var'. Can be modified"
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - Constant
 - Optional
---

Use `var` to make a variable. The value of a variable doesn’t need to be known at compile time.

<pre><code>var myVariable = 42
myVariable = 50
</code></pre>

A variable must have the same type as the value you want to assign to it. However, you don’t always have to write the type explicitly. Providing a value when you create a variable lets the compiler infer its type. In the example above, the compiler infers that `myVariable` is an integer because its initial value is an integer.

If the initial value doesn’t provide enough information (or if there is no initial value), specify the type by writing it after the variable, separated by a colon.

<pre><code>var myImplicitIntVariable = 42
myImplicitIntVariable = 50
var myExplicitIntVariable :Int
var anotherExplicitIntVariable :Int = 42

var myImplicitStringVariable = "The Answer is \(anotherExplicitIntVariable)"
var myExplciitStringVariable :String = "42"
</code></pre>