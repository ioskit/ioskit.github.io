---
layout: feature
name: 'Enumeration'
iid: Enumeration
status: DOING
language: swift,objectivec
abstract: "An enumeration defines a common type for a group of related values and enables you to work with those values in a type-safe way within your code."
code:
  gist: 7ab927e65e4d4e9ba90dc0fbb2b8eafb
  iswift: PUoss6
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

* TOC
{:toc}

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
    case ace
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
}
let ace = Rank.ace
```

Wording:

* Like other types in Swift, their names (such as CompassPoint and Planet) should start with a capital letter
* Give enumeration types singular rather than plural names (consider the whole name, aka `CompassPoint.west`)


## Raw value

If an enumeration has raw values, those values are determined as part of the declaration.

By default, Swift assigns the raw values starting at zero and incrementing by one each time, but you can change this behavior by explicitly specifying values. 

Raw values can be strings, characters, or any of the integer or floating-point number types. Each raw value must be unique within its enumeration declaration. Use the `rawValue` property to access the raw value of an enumeration case.

```
enum Rank: Int {
    case ace = 1 // '= 1' is the optional zero-based starting raw value
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
}
let aceRawValue = ace.rawValue
```

Use the `init?(rawValue:)` initializer to make an instance of an enumeration from a raw value. As no case may be found for a given raw value, the 
return type is an [Optional](/Optional): `nil` will be returned if no case is found.

```
if let convertedRank = Rank(rawValue: 3) {
    let threeDescription = convertedRank.simpleDescription()
}
```

__Warning:__ Raw values are not the same as associated values...


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





## Associated Values

You can define Swift enumerations to store associated values of any given type, and the value types can be different for each case of the enumeration 
if needed. Enumerations similar to these are known as _discriminated unions_, _tagged unions_, or _variants_ in other programming languages.

These values associated with the case—these values are determined when you make the instance, and they can be different for each instance of an enumeration case.

For example, imagine an inventory tracking system to be able to store UPC 2D barcodes as a tuple of four integers (number system, manufacturer code, 
product code, check digit), and QR code barcodes as a string of any length. In Swift, an enumeration to define product barcodes of either type might look like this:

```
enum Barcode {
    case upc(Int, Int, Int, Int)
    case qrCode(String)
}
var productBarcode = Barcode.upc(8, 85909, 51226, 3) // value of 'Barcode.upc' with an associated tuple value of (8, 85909, 51226, 3).
productBarcode = .qrCode("ABCDEFGHIJKLMNOP")
```

These enumeration can be used like that:

```
switch productBarcode {
    // case .upc(let numberSystem, let manufacturer, let product, let check): // this line is equivalent to:
    case let .upc(numberSystem, manufacturer, product, check):
        print("UPC: \(numberSystem), \(manufacturer), \(product), \(check).")
    // case let .qrCode(productCode):                                         // this line is equivalent to:
    case .qrCode(let productCode):
        print("QR code: \(productCode).")
}
```

__Warning:__ Raw values are not the same as associated values:

* Raw values are set to prepopulated values when you first define the enumeration in your code, like the three ASCII codes above. The raw value for a particular enumeration case is always the same. 
* Associated values are set when you create a new constant or variable based on one of the enumeration’s cases, and can be different each time you do so.




## Recursive Enumerations

A recursive enumeration is an enumeration that has another instance of the enumeration as the associated value for one or more of the enumeration cases. 
You indicate that an enumeration case is recursive by writing `indirect` before it, which tells the compiler to insert the necessary layer of indirection.

For example, here is an enumeration that stores simple arithmetic expressions:

```
enum ArithmeticExpression {
    case number(Int)
    indirect case addition(ArithmeticExpression, ArithmeticExpression)
    indirect case multiplication(ArithmeticExpression, ArithmeticExpression)
}
```

You can also write `indirect` before the beginning of the enumeration, to enable indirection for all of the enumeration’s cases that need it.

```
indirect enum ArithmeticExpression {
    case number(Int)
    case addition(ArithmeticExpression, ArithmeticExpression)
    case multiplication(ArithmeticExpression, ArithmeticExpression)
}
```

For example, the expression `(5 + 4) * 2` has a number on the right hand side of the multiplication and another expression on the left hand side of the 
multiplication. Because the data is nested, the enumeration used to store the data also needs to support nesting—this means the enumeration needs to 
be recursive. The code below shows the `ArithmeticExpression` recursive enumeration being created for `(5 + 4) * 2`:

```
let five = ArithmeticExpression.number(5)
let four = ArithmeticExpression.number(4)
let sum = ArithmeticExpression.addition(five, four)
let product = ArithmeticExpression.multiplication(sum, ArithmeticExpression.number(2))
```

A recursive function is a straightforward way to work with data that has a recursive structure. For example, here’s a function that evaluates an arithmetic expression:

```
func evaluate(_ expression: ArithmeticExpression) -> Int {
    switch expression {
    case let .number(value):
        return value
    case let .addition(left, right):
        return evaluate(left) + evaluate(right)
    case let .multiplication(left, right):
        return evaluate(left) * evaluate(right)
    }
}
 
print(evaluate(product))
// Prints "18"
```


<!--

// This enumeration has 14 'enumeration cases'
enum Rank: Int {                            // 1) Defining
    case ace = 1                            // '= 1' is the optional zero-based starting 'raw value'
    case two, three, four, five, six, seven, eight, nine, ten
    case jack, queen, king
	case misc(String)                   // 5) Custom 'associated value' for this case (ex: String = 'joker', 'rules').
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
