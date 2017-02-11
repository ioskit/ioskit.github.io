---
layout: feature
name: 'Extension'
iid: Extension
status: DOING
language: swift,objectivec
abstract: "Use extension to add functionality to an existing type, such as new methods and computed properties."
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - Protocol
 - Generics
---

TODO.

```
extension Int: ExampleProtocol {
    var simpleDescription: String {
        return "The number \(self)"
    }
    mutating func adjust() {
        self += 42
    }
}
println(7.simpleDescription)
```

## Extending a Generic Type

You can also extends [Generics](/Generics) types.