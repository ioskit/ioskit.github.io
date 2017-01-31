---
layout: feature
name: 'Properties'
iid: Properties
status: DONE
language: swift
abstract: "Properties associate values with a particular class, structure, or enumeration."
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

Properties associate values with a particular [Classes](/Classe), [Structures](/Structure) or [Enumerations](/Enumeration). Stored properties 
store [Constant](/Constant) and [Variable](/Variable) values as part of an instance, whereas computed properties calculate (rather than store) 
a value. Computed properties are provided by [Classes](/Classe), [Structures](/Structure) and [Enumerations](/Enumeration). Stored properties 
are provided only by classes and structures.

Stored and computed properties are usually associated with instances of a particular type. However, properties can also be associated with the 
type itself. Such properties are known as type properties.

In addition, you can define property observers to monitor changes in a property’s value, which you can respond to with custom actions. Property 
observers can be added to stored properties you define yourself, and also to properties that a subclass inherits from its superclass.

## Stored Properties

In its simplest form, a stored property is a constant or variable that is stored as part of an instance of a particular class or structure. 
Stored properties can be either variable stored properties (introduced by the var keyword) or constant stored properties (introduced by the let keyword).

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
   
In addition to stored properties, classes, structures, and enumerations can define computed properties, which do not actually store a value. 
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
   
If a computed property’s setter does not define a name for the new value to be set, a default name of newValue is used. Here’s an alternative 
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

A computed property with a getter but no setter is known as a read-only computed property. A read-only computed property always returns a value, 
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

Property observers observe and respond to changes in a property’s value. Property observers are called every time a property’s value is set, 
even if the new value is the same as the property’s current value.

You have the option to define either or both of these observers on a property:

* `willSet` is called just before the value is stored.
* `didSet` is called immediately after the new value is stored.

If you implement a `willSet` observer, it’s passed the new property value as a constant parameter. You can specify a name for this parameter as 
part of your `willSet` implementation. If you don’t write the parameter name and parentheses within your implementation, the parameter is made 
available with a default parameter name of `newValue`.

```
class StepCounter {
    var totalSteps: Int = 0 {
        willSet(newTotalSteps) {
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