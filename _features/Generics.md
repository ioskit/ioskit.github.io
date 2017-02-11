---
layout: feature
name: 'Generics'
iid: Generics
status: DONE
language: swift
abstract: "Generics make it possible to write code that is not specific to a type and can be utilized for different types."
code:
  gist: 9d22636401c4e0897d8d997c968d46e2
  iswift: NlvQb0
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour, Generics'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-NoLink_23
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Language Guide, Generics'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html
    description: ' - Apple Developer'
    type: reference
features:
 - Type
 - Class
 - Structure
 - Enumeration
 - Extension
---

* TOC
{:toc}

[Swift](/Swift) is a [type-safe language](/functional/TypeSafety). Whenever we work with types, we need to specify them. For instance, a function can have 
specific parameters and return types. We cannot pass any type but the ones that are specified. What if we need a function that can handle more than one type?

Swift provides `Any` and `AnyObject` but it is not a good practice to use them unless we have to. Using `Any` and `AnyObject` will make our 
code fragile as we will not be able to catch type mismatching during compile time. __Generics__ are the solution to our requirement. 

Generic code enables you to write flexible, reusable functions and types that can work with any type, subject to requirements that you define. 
You can write code that avoids duplication and expresses its intent in a clear, abstracted manner.

Generics are a powerful features of [Swift](/Swift), and much of the [Swift](/Swift) standard library is built with generic code. 
For example, Swift’s [Array](/Array) and Dictionary types are both generic collections. 

Write a name inside angle brackets (`<` and `>`) to make a generic function or type.

This is a problem that Generics solve. Given the following function:

```
func swapTwoInts(_ a: inout Int, _ b: inout Int) {
    let temporaryA = a
    a = b
    b = temporaryA
}
var someInt = 3
var anotherInt = 107
swapTwoInts(&someInt, &anotherInt)
print("someInt is now \(someInt), and anotherInt is now \(anotherInt)")

```

If you have the same need with `String` or `Double`, you can can write exactly the same function by replacing `Int` types with `String` types... 
That provides code duplication. Generics allow to handle this situation:

```
func swapTwoValues<T>(_ a: inout T, _ b: inout T) {
    let temporaryA = a
    a = b
    b = temporaryA
}

var someInt = 3
var anotherInt = 107
swapTwoValues(&someInt, &anotherInt)
// someInt is now 107, and anotherInt is now 3
 
var someString = "hello"
var anotherString = "world"
swapTwoValues(&someString, &anotherString)
// someString is now "world", and anotherString is now "hello"
```

Where `T` is the __placeholder type name__, an example of __type parameter__. Once you specify a type parameter, you can use it to define the 
type of a function’s parameters, or as the function’s return type, or as a type annotation within the body of the function.

You can provide more than one type parameter by writing multiple type parameter names within the angle brackets, separated by commas.

In most cases, type parameters have descriptive names, such as `Key` and `Value` in `Dictionary<Key, Value>` (upper camel case names), which 
tells the reader about the relationship between the type parameter and the generic type or function it’s used in. However, when there isn’t 
a meaningful relationship between them, it’s traditional to name them using single letters such as `T`, `U`, and `V`, such as `T` in the 
`swapTwoValues(_:_:)` function above.

## Custom Generic Types

In addition to generic functions, [Swift](/Swift) enables you to define your own generic types. These are custom:
 
- [Classes](/Classe)
- [Structures](/Structure)
- [Enumerations](/Enumeration)

that can work with any type, in a similar way to `Array` and `Dictionary`.

This an example of a generic `Stack` structure that is a collection handling any type `Element`:

```
struct Stack<Element> {
    var items = [Element]()
    mutating func push(_ item: Element) {
        items.append(item)
    }
    mutating func pop() -> Element {
        return items.removeLast()
    }
}

var stackOfStrings = Stack<String>()
stackOfStrings.push("uno")
stackOfStrings.push("dos")
stackOfStrings.push("tres")
stackOfStrings.push("cuatro")
// the stack now contains 4 strings
let fromTheTop = stackOfStrings.pop()
// fromTheTop is equal to "cuatro", and the stack now contains 3 strings
```


## Extending a Generic Type

When you extend a generic type, you do not provide a type parameter list as part of the extension’s definition.

The following example extends the generic `Stack` type to add a read-only computed property called `topItem`, which returns the top item on 
the stack without popping it from the stack:

```
extension Stack {
    var topItem: Element? {
        return items.isEmpty ? nil : items[items.count - 1]
    }
}

if let topItem = stackOfStrings.topItem {
    print("The top item on the stack is \(topItem).")
}
// Prints "The top item on the stack is tres."
```

As example you can see the [Dictionary extension](https://github.com/apple/swift-corelibs-foundation/blob/master/Foundation/Dictionary.swift).


## Type Constraints

It is sometimes useful to enforce certain type constraints on the types that can be used with generic functions and generic types. 
__Type constraints__ specify that a type parameter must:
 
- inherit from a specific [Class](/Class)
- or conform to a particular [Protocol](/Protocol) or protocol composition.

For example, Swift’s Dictionary type places a limitation on the types that can be used as keys for a dictionary: the type of a dictionary’s keys must be hashable.

You write type constraints by placing a single class or protocol constraint after a type parameter’s name, separated by a colon, as part of the type parameter list:

```
func someFunction<T: SomeClass, U: SomeProtocol>(someT: T, someU: U) {
    // function body goes here
}
```


## Associated Types

When defining a [Protocol](/Protocol), it is sometimes useful to declare one or more associated types as part of the protocol’s definition. 
An __associated type__ gives a placeholder name to a type that is used as part of the protocol. The actual type to use for that associated 
type is not specified until the protocol is adopted. Associated types are specified with the `associatedtype` keyword.

```
protocol Container {
    associatedtype ItemType            // <<<<< a/ ItemType is an associated type
    mutating func append(_ item: ItemType)
    var count: Int { get }
    subscript(i: Int) -> ItemType { get }
}
```

The `Container` protocol declares an associated type called `ItemType`, written as `associatedtype ItemType`. The protocol does not define what 
`ItemType` is—that information is left for any conforming type to provide. Nonetheless, the `ItemType` alias provides a way to refer to the 
type of the items in a `Container`, and to define a type for use with the `append(_:)` method and subscript, to ensure that the expected 
behavior of any `Container` is enforced.

```
struct IntStack: Container {

    var items = [Int]()
    mutating func push(_ item: Int) {
        items.append(item)
    }
    mutating func pop() -> Int {
        return items.removeLast()
    }

    typealias ItemType = Int           // <<<<< b/ Optional as `type inference` in Swift
    mutating func append(_ item: Int) {
        self.push(item)
    }
    var count: Int {
        return items.count
    }
    subscript(i: Int) -> Int {
        return items[i]
    }
}
```

`IntStack` specifies that for this implementation of `Container`, the appropriate `ItemType` to use is a type of `Int`. 
The definition of `typealias ItemType = Int` turns the abstract type of `ItemType` into a concrete type of `Int` for this implementation of 
the `Container` protocol.

Thanks to [Swift’s type inference](/Type), you don’t actually need to declare a concrete `ItemType` of `Int` as part of the definition of `IntStack`. 
Indeed, if you delete the `typealias ItemType = Int` line from the code above, everything still works, because it is clear what type should be used for `ItemType`.

You can also make the generic `Stack` type conform to the `Container` protocol:

```
struct Stack<Element>: Container {
    // original Stack<Element> implementation
    var items = [Element]()
    mutating func push(_ item: Element) {
        items.append(item)
    }
    mutating func pop() -> Element {
        return items.removeLast()
    }
    // conformance to the Container protocol
    mutating func append(_ item: Element) {
        self.push(item)
    }
    var count: Int {
        return items.count
    }
    subscript(i: Int) -> Element {
        return items[i]
    }
}
```

You can extend an existing type to add conformance to a [Protocol](/Protocol). This includes a protocol with an associated type.


For example, Swift’s `Array` type already provides an `append(_:)` method, a `count` property, and a subscript with an `Int` index to retrieve its elements. 
These three capabilities match the requirements of the `Container` protocol. This means that you can extend `Array` to conform to the `Container`
protocol simply by declaring that `Array` adopts the protocol. You do this with an empty extension:

```
extension Array: Container {}
```


## Generic Where Clauses

It can be useful to define requirements for associated types. You do this by defining a generic where clause. A generic where clause enables 
you to require that an associated type must conform to a certain [Protocol](/Protocol), or that certain type parameters and associated types 
must be the same. 

A generic where clause starts with the `where` keyword, followed by constraints for associated types or equality relationships between types 
and associated types. You write a generic where clause right before the opening curly brace of a type or function’s body.

```
func allItemsMatch<C1: Container, C2: Container>(_ someContainer: C1, _ anotherContainer: C2) -> Bool
    where C1.ItemType == C2.ItemType, C1.ItemType: Equatable {
        
        // Check that both containers contain the same number of items.
        if someContainer.count != anotherContainer.count {
            return false
        }
        
        // Check each pair of items to see if they are equivalent.
        for i in 0..<someContainer.count {
            if someContainer[i] != anotherContainer[i] {
                return false
            }
        }
        
        // All items match, so return true.
        return true
}
```

The following requirements are placed on the function’s two type parameters:

- The `ItemType` for `C1` must be the same as the `ItemType` for `C2` (written as `C1.ItemType == C2.ItemType`).
- The `ItemType` for `C1` must conform to the `Equatable` protocol (written as `C1.ItemType: Equatable`).

Here’s how the `allItemsMatch(_:_:)` function looks in action:


```
var stackOfStrings = Stack<String>()
stackOfStrings.push("uno")
stackOfStrings.push("dos")
stackOfStrings.push("tres")
 
var arrayOfStrings = ["uno", "dos", "tres"]
 
if allItemsMatch(stackOfStrings, arrayOfStrings) {
    print("All items match.")
} else {
    print("Not all items match.")
}
// Prints "All items match."
```