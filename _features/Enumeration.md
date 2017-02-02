---
layout: feature
name: 'Enumeration'
iid: Enumeration
status: DOING
language: swift,objectivec
abstract: "An enumeration defines a common type for a group of related values and enables you to work with those values in a type-safe way within your code."
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): A Swift Tour, Enumerations and Structures'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Language Guide, Enumerations'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html
    description: ' - Apple Developer'
    type: reference
features:
 - Class
 - Structure
 - Subscripts
 - Properties
 - Extension
 - Protocol
---

An enumeration defines a common type for a group of related values and enables you to work with those values in a type-safe way within your code.

Alternatively, enumeration cases can specify associated values of any type to be stored along with each different case value, much as unions or 
variants do in other languages. You can define a common set of related cases as part of one enumeration, each of which has a different set of values 
of appropriate types associated with it.

Enumerations in Swift are first-class types in their own right. They adopt many features traditionally supported only by classes: see [Class](/Class) 
page for a comparison between Class and Enumeration.


# Swift (3.0.1)

## Defining

Use `enum` to create an enumeration. Like [Classes](/Class) and all other named types, enumerations can have methods associated with them.

```
// This enumeration has 13 'enumeration cases'
enum Rank: Int {
    case ace = 1 // '= 1' is optional
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
}
let ace = Rank.ace
let aceRawValue = ace.rawValue
```

Wording:

* Like other types in Swift, their names (such as CompassPoint and Planet) should start with a capital letter
* Give enumeration types singular rather than plural names (consider the whole name, aka `CompassPoint.west`)

By default, Swift assigns the raw values starting at zero and incrementing by one each time, but you can change this behavior by explicitly specifying values. 

You can also use strings or floating-point numbers as the raw type of an enumeration. Use the rawValue property to access the raw value of an enumeration case.

Use the `init?(rawValue:)` initializer to make an instance of an enumeration from a raw value.

```
if let convertedRank = Rank(rawValue: 3) {
    let threeDescription = convertedRank.simpleDescription()
}
```

## Method

As for [Classes](/Class), you can define methods on enumerations:

```
enum Rank: Int {
    case ace = 1 // '= 1' is optional
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
    func simpleDescription() -> String {
	  return "This is the Rank enumeration"
    }
}
```


## Referring

Notice the two ways that the hearts case of the enumeration is referred to above: 

1. When assigning a value to the hearts constant, the enumeration case `Suit.hearts` is referred to by its full name because the constant doesn’t have 
an explicit type specified. 
1. Inside the switch, the enumeration case is referred to by the abbreviated form `.hearts` because the value of `self` is already known to be a suit. 

You can use the abbreviated form anytime the value’s type is already known:

```
var directionToHead = CompassPoint.west
directionToHead = .east // At this place, the type is known
```


## Raw value

If an enumeration has raw values, those values are determined as part of the declaration.

It is possible to have enumeration cases having values associated with the case—these values are determined when you make the instance, and they can be different for each instance of an enumeration case.

```
enum ServerResponse {
    case result(String, String)
    case failure(String)
}

let success = ServerResponse.result("6:00 am", "8:09 pm")
let failure = ServerResponse.failure("Out of cheese.")
 
switch success {
case let .result(sunrise, sunset):
    print("Sunrise is at \(sunrise) and sunset is at \(sunset).")
case let .failure(message):
    print("Failure...  \(message)")
}
```

Notice how the sunrise and sunset times are extracted from the `ServerResponse` value as part of matching the value against the switch cases.


## Matchning

You can match individual enumeration values with a `switch` statement

```
enum Rank: Int {
    case ace = 1
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
    func simpleDescription() -> String {
        switch self {
        case .ace:
            return "ace"
        case .jack:
            return "jack"
        case .queen:
            return "queen"
        case .king:
            return "king"
        default:
            return String(self.rawValue)
        }
    }
}
let ace = Rank.ace
let aceRawValue = ace.rawValue
```

A switch statement must be exhaustive when considering an enumeration’s cases. If a case is omitted, this code does not compile, because it does not 
consider the complete list of the enumeration cases. Requiring exhaustiveness ensures that enumeration cases are not accidentally omitted.

When it is not appropriate to provide a case for every enumeration case, you can provide a `default` case to cover any cases that are not addressed explicitly.



## Code Summary

{% gist 7ab927e65e4d4e9ba90dc0fbb2b8eafb %}

<!--
// This enumeration has 14 'enumeration cases'
enum Rank: Int {                            // 1) Defining
    case ace = 1                            // '= 1' is the optional zero-based starting raw value
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
	case joker(String)                      // Custom raw value associated to this case.
    func simpleDescription() -> String {    // 3) Method
        switch self {                       // 4) Matching with 'switch'
        case .ace:
            return "ace"
        case .jack:
            return "jack"
        case .queen:
            return "queen"
        case .king:
            return "king"
        default:
            return String(self.rawValue)
        }
    }
}
var card = Rank.ace
card = .jack                                // At this place, the enumeration type is known, so it is optional
let aceRawValue = ace.rawValue
```
-->
