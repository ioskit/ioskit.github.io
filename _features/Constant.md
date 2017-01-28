---
layout: feature
name: 'Constant'
iid: Constant
status: DONE
language: swift
abstract: "Defines with 'let'. Can not be modified."
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - Variable
 - Optional
---

Use `let` to make a constant. The value of a constant doesn’t need to be known at compile time.

<pre><code>let myConstant = 42
</code></pre>

A constant must have the same type as the value you want to assign to it. However, you don’t always have to write the type explicitly. Providing a value when you create a constant lets the compiler infer its type. In the example above, the compiler infers that `myConstant` is an integer because its initial value is an integer.

If the initial value doesn’t provide enough information (or if there is no initial value), specify the type by writing it after the variable, separated by a colon.

<pre><code>let myImplicitIntConstant = 42
let myExplicitIntConstant :Int = 42

let myImplicitStringConstant = "The Answer is \(myImplicitIntConstant)"
let myExplciitStringConstant :String = "42"
</code></pre>