---
layout: kit
iid: swift 
name: 'Swift'
status: DOING
type: language
since: iOS8
icon: /resources/images/kits/Swift/swift-hero_2x.png
kits:
 - InteractivePlaygrounds
 - REPL
 - AutomaticReferenceCounting
 - ObjectiveC
xcode: xcode6
links:
 - link:
     name: 'The Swift Programming Language: About Swift'
     url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/
     description: ' - Apple Developer'
 - link:
     name: 'Swift - Overview'
     url: https://developer.apple.com/swift/
     description: ' - Apple Developer'
 - link:
     name: 'Swift Cheat Sheet and Quick Reference'
     url: http://www.raywenderlich.com/73967/swift-cheat-sheet-and-quick-reference
     description: ' - Ray Wenderlich'
abstract: "An innovative new programming language for Cocoa and Cocoa Touch."
features:
  TypeSafety: true
  TypeInference: true
  Generics: true
  Immutability: true
  StatelessProgramming: true
  PureFunction: true
  FirstClassFunction: true
  HigherOrderFunction: true
  PatternMatching: true
---

* TOC
{:toc}

Swift is an innovative new programming language for Cocoa and Cocoa Touch. Writing code is interactive and fun, the syntax is concise yet expressive, 
and apps run lightning-fast. Swift is ready for your next iOS and OS X project — or for addition into your current app — because Swift code works 
side-by-side with Objective-C.

A strength of Swift as an open source hybrid language is the ability to support both __Object-Oriented Programming (OOP)__ and __Functional Programming__.


## Main topics

* [Classes](/Class), [Extensions](/Extension), [Protocols](/Protocol) and [Access Control](/AccessControl)
* [Classes](/Class), [Structures](/Structure) and [Enumerations](/Enumeration)
* [Constants](/Constant), [Variables](/Variable) and [Optionals](/Optional)
* [Functions](/Function) and [Closures](/Closure)
* [Generics](/Generics)
* [Error handling](/Error)
* [Automatic Reference Counting (ARC)](/AutomaticReferenceCounting)
* [Read-Eval-Print-Loop](/REPL) and [Interactive Playgrounds](/InteractivePlaygrounds)


See also the comparison with other [Languages](/languages)

## Object-Oriented Programming (OOP)

Software is divided into smaller pieces such as (packages,) [Classes](/Class), interfaces or [Protocols](/Protocol), and methods or [Functions](/Function).

In OOP, connecting the building blocks to each other is not as easy as dividing them. Connection between different objects may propose strong coupling 
between them. Coupling is the biggest source of complexity in OOP. A change in a module or class could force change in all coupled modules and classes. 
Also, a particular module or class might be harder to reuse and test because of coupled modules or classes.

Software engineers try to loosen coupling by structuring the software well and applying different principles and design patterns. For instance:

* Single responsibility
* Open-closed
* Liskov substitution
* Interface segregation 
* Dependency inversion 

or __SOLID__ principles when applied together properly tend to make software easy to maintain and extend.

Even though it is possible to decrease the coupling and simplify software structures, managing the memory, referencing to instances, and testing 
different objects remains difficult because, in OOP, objects are open to change and mutation.

In functional programming, functions are the fundamental building blocks. In OOP, programs are composed of classes and statements, which change the 
state of classes when executed.

OOP is categorized as __imperative programming__.


&nbsp;

## Functional Programming

In functional programming, __pure functions__ are the most important building blocks. They:
 
* do not rely on data outside of themselves 
* do not change data that exists outside of them. 

Pure functions:
 
* are easy to test because they will always provide the same results
* can be executed on different threads or cores without any mechanisms to handle multithreading and multiprocessing. 

This is a very important benefit of functional programming over OOP as multicore programming mechanisms are very complex to handle in OOP though is 
becoming more important day by day because hardware engineers have finally hit the speed limit of light. So, in order to have more cycles per second, 
hardware engineers are adding more processors to chips. Functional programming eliminates the need for a complex multicore programming mechanism, and 
as pure functions are not dependent on any instances or data outside of themselves, it is easy to change them without changing other parts.

Functional programming is a __declarative programming__ style.

Theoretically, functional programming employs the concepts of __category theory__, which is a branch of mathematics. It is not necessary to know the 
category theory to be able to program functionally but studying it will help us grasp some of the more advanced concepts such as functors, applicative 
functors, and monads.

As opposed to OOP, functional programming avoids using mutable states. Avoiding mutable states makes it easier to test, read, and understand the code 
although it is not easy to avoid mutable states in some cases such as file and database operations.

Swift has features empowering it as a functional programming language:

* [Type Safety](/functional/TypeSafety) and [TypeInference](/functional/TypeInference)
* [Immutability](/functional/Immutability) with the `let` keyword to easily define [Constants](/Constant)
* [Stateless Programming](/functional/StatelessProgramming) with [Structures](/Structure) and [Enumerations](Enumeration) that are passed by values
* [Functions](/Function):
  * [Pure functions](/functional/PureFunction), which do not rely on data outside of themselves and they do not change data that exists outside of them 
  * [First-class types](/functional/FirstClassFunction), so they can be stored, passed, and returned
  * [Higher-order functions](/functional/HigherOrderFunction), so they can receive other functions as their parameters
* [Pattern Matching](/functional/PatternMatching)
* Closures
