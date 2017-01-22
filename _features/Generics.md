---
layout: feature
name: 'Generics'
iid: Generics
status: DOING
language: swift
abstract: "Write a name inside angle brackets to make a generic function or type. You can make generic forms of functions and methods, as well as classes, enumerations, and structures."
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour, Generics'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-NoLink_19
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'The Swift Programming Language: Language Guide, Generics'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID179
    description: ' - Apple Developer'
    type: reference
features_:
 - Variable
---

TODO.

Write a name inside angle brackets to make a generic function or type.

<pre><code>func repeat< Item>(item: Item, times: Int) -> [Item] {
    var result = [Item]()
    for i in 0..<times {
        result.append(item)
    }
    return result
}
repeat("knock", 4)</code></pre>

You can make generic forms of functions and methods, as well as classes, enumerations, and structures.

<pre><code>// Reimplement the Swift standard library's optional type
enum OptionalValue< T> {
    case None
    case Some(T)
}
var possibleInteger: OptionalValue< Int> = .None
possibleInteger = .Some(100)</code></pre>

Use `where` after the type name to specify a list of requirements—for example, to require the type to implement a protocol, to require two types to be the same, or to require a class to have a particular superclass.

<pre><code>func anyCommonElements < T, U where T: SequenceType, U: SequenceType, T.Generator.Element: Equatable, T.Generator.Element == U.Generator.Element> (lhs: T, rhs: U) -> Bool {
    for lhsItem in lhs {
        for rhsItem in rhs {
            if lhsItem == rhsItem {
                return true
            }
        }
    }
    return false
}
anyCommonElements([1, 2, 3], [3])</code></pre>
