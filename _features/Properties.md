---
layout: feature
name: 'Properties'
iid: Properties
status: DONE
language: swift
abstract: "Properties associate values with a particular class, structure, or enumeration."
code:
  gist: 25e8fa6b2efff41d97fee864bf906e70
  iswift: ezKqDw
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Properties'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Properties.html
    description: ' - Apple Developer'
    type: reference
features:
 - Class
 - Structure
 - Enumeration
---

* TOC
{:toc}

Properties associate values with a particular [Classes](/Classe), [Structures](/Structure) or [Enumerations](/Enumeration). 

Properties can be:

* Stored
  * store [Constant](/Constant) and [Variable](/Variable) values as part of an instance
  * provided only by [Classes](/Class) and [Structures](/Structure)
* Computed
  * calculate (rather than store) a value
  * provided by [Classes](/Class), [Structures](/Structure) and [Enumerations](/Enumeration)
  * a setter and an optional setter

Stored and computed properties are usually associated with instances of a particular type. However, properties can also be associated with the 
type itself. Such properties are known as type properties.

In addition, you can define property observers to monitor changes in a property's value, which you can respond to with custom actions. Property 
observers can be added to stored properties you define yourself, and also to properties that a subclass inherits from its superclass.


# Swift (3.0.1)

## Stored Properties

In its simplest form, a stored property is a [Constant](/Constant) (`let`) or [Variable](/Variable) (`var`) that is stored as part of an instance of a particular [Classes](/Class) or [Structures](/Structure). 

```
struct FixedLengthRange {
    var firstValue: Int
    let length: Int
}
var rangeOfThreeItems = FixedLengthRange(firstValue: 0, length: 3)
// the range represents integer values 0, 1, and 2
rangeOfThreeItems.firstValue = 6
// the range now represents integer values 6, 7, and 8
```

## Computed Properties
   
In addition to stored properties, [Classes](/Class), [Structures](/Structure) and [Enumerations](/Enumeration) can define computed properties, which do not actually store a value. 
Instead, they provide a getter and an optional setter to retrieve and set other properties and values indirectly.

```
struct Point {
    var x = 0.0, y = 0.0
}
struct Size {
    var width = 0.0, height = 0.0
}
struct Rect {
    var origin = Point()
    var size = Size()
    var center: Point {
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set(newCenter) {
            origin.x = newCenter.x - (size.width / 2)
            origin.y = newCenter.y - (size.height / 2)
        }
    }
}
var square = Rect(origin: Point(x: 0.0, y: 0.0),
                  size: Size(width: 10.0, height: 10.0))
let initialSquareCenter = square.center
square.center = Point(x: 15.0, y: 15.0)
print("square.origin is now at (\(square.origin.x), \(square.origin.y))")
// Prints "square.origin is now at (10.0, 10.0)"
```

## Shorthand Setter Declaration
   
If a computed property's setter does not define a name for the new value to be set, a default name of `newValue` is used. Here's an alternative 
version of the Rect structure, which takes advantage of this shorthand notation:
   
```
struct AlternativeRect {
    var origin = Point()
    var size = Size()
    var center: Point {
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set {
            origin.x = newValue.x - (size.width / 2)
            origin.y = newValue.y - (size.height / 2)
        }
    }
}
```

## Read-Only Computed Properties

A computed property with a getter but no setter is known as a __read-only computed property__. A read-only computed property always returns a value, 
and can be accessed through dot syntax, but cannot be set to a different value.

```
struct Cuboid {
    var width = 0.0, height = 0.0, depth = 0.0
    var volume: Double {
        return width * height * depth
    }
}
let fourByFiveByTwo = Cuboid(width: 4.0, height: 5.0, depth: 2.0)
print("the volume of fourByFiveByTwo is \(fourByFiveByTwo.volume)")
// Prints "the volume of fourByFiveByTwo is 40.0"
```

## Property Observers

Property observers observe and respond to changes in a property's value. Property observers are called every time a property's value is set, 
even if the new value is the same as the property's current value.

You have the option to define either or both of these observers on a property:

* `willSet` is called just before the value is stored.
* `didSet` is called immediately after the new value is stored.

If you implement a `willSet` observer, it's passed the new property value as a constant parameter. You can specify a name for this parameter as 
part of your `willSet` implementation. If you don't write the parameter name and parentheses within your implementation, the parameter is made 
available with a default parameter name of `newValue`.

```
class StepCounter {
    var totalSteps: Int = 0 {
        willSet(newTotalSteps) { // '(newTotalSteps)' is optional
            print("About to set totalSteps to \(newTotalSteps)")
        }
        didSet {
            if totalSteps > oldValue  {
                print("Added \(totalSteps - oldValue) steps")
            }
        }
    }
}
let stepCounter = StepCounter()
stepCounter.totalSteps = 200
// About to set totalSteps to 200
// Added 200 steps
stepCounter.totalSteps = 360
// About to set totalSteps to 360
// Added 160 steps
stepCounter.totalSteps = 896
// About to set totalSteps to 896
// Added 536 steps
```

## Type Properties

Instance properties are properties that belong to an instance of a particular type. Every time you create a new instance of that type, it has 
its own set of property values, separate from any other instance.

```
struct SomeStructure {
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 1
    }
}
enum SomeEnumeration {
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 6
    }
}
class SomeClass {
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 27
    }
    class var overrideableComputedTypeProperty: Int {
        return 107
    }
}
```

Type properties are queried and set with dot syntax, just like instance properties. However, type properties are queried and set on the type, 
not on an instance of that type. For example:

```
print(SomeStructure.storedTypeProperty)
// Prints "Some value."
SomeStructure.storedTypeProperty = "Another value."
print(SomeStructure.storedTypeProperty)
// Prints "Another value."
print(SomeEnumeration.computedTypeProperty)
// Prints "6"
print(SomeClass.computedTypeProperty)
// Prints "27"
```

<!--
```
struct Point {
    var x = 0.0, y = 0.0
}
struct Size {
    var width = 0.0, height = 0.0
}
struct Rect {
    var origin = Point()     // 1) implicit Stored property
    var size = Size()        // 1) implicit Stored property
    var center: Point {      // 2) Computed property
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set(newValue) {      // 3) '(newValue)' is optional = Shorthand Setter Declaration (`newValue` becames default name)
            origin.x = newValue.x - (size.width / 2)
            origin.y = newValue.y - (size.height / 2)
        }
    }
    var area: Double {       // 4) Read-Only Computed Properties
        return size.width * size.height
    }
    var totalSteps: Int = 0 { // 5) Property Observers
        willSet(newTotalSteps) { // '(newTotalSteps)' is optional, like setters
            print("About to set totalSteps to \(newTotalSteps)")
        }
        didSet {
            if totalSteps > oldValue  {
                print("Added \(totalSteps - oldValue) steps")
            }
        }
    }

	// 6) Type Properties
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 27
    }
    static var overrideableComputedTypeProperty: Int {
        return 107
    }
}
```
-->
