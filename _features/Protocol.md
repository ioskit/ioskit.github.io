---
layout: feature
name: 'Protocol'
iid: Protocol
status: DOING
language: swift,objectivec
abstract: "Are like 'interfaces' in other OO languages. Use protocol to declare a protocol. Classes, enumerations, and structs can all adopt protocols."
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - Class
 - Extension
 - Generics
---

* TOC
{:toc}

A protocol is an abstract type representation that has no implementation body (like an interface in other languages), 
and types (both struct and class) can adopt protocols at definition time.


## Associated Types

When defining a protocol, it is sometimes useful to declare one or more associated types as part of the protocol’s definition. 
An __associated type__ gives a placeholder name to a type that is used as part of the protocol. The actual type to use for that associated 
type is not specified until the protocol is adopted. Associated types are specified with the `associatedtype` keyword.

See "Associated Types" in [Generics](/Generics) page.


{% gist baa5fbb7e378dee6137deccab29894b0 %}

<!--
```
// Defining
protocol ExampleProtocol {
    var simpleDescription: String { get }
    mutating func adjust()
}


// Adopting
class SimpleClass: ExampleProtocol {
    var simpleDescription: String = "A very simple class."
    var anotherProperty: Int = 69105
    func adjust() {
        simpleDescription += "  Now 100% adjusted."
    }
}


// Using
var a = SimpleClass()
a.adjust()
```
-->