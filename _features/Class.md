---
layout: feature
name: 'Class'
iid: Class
status: DONE
language: swift,objectivec
abstract: "Classes and structures are general-purpose, flexible constructs that become the building blocks of your program’s code. 
You define properties and methods to add functionality to your classes and structures 
by using exactly the same syntax as for constants, variables, and functions."
code:
  gist: ac6040f564565c68b72054edf60e05b2
  iswift: 5erSyB
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - AccessControl
 - ClassMethod
 - Closure
 - Enumeration
 - Extension
 - Function
 - Protocol
 - Structure
 - TypeMethod
 - Subscripts
 - Properties
---

* TOC
{:toc}

# Comparison between Class and Structure

See also [Structure](/Structure) page.

<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th></th>
      <th>Class</th>
      <th><a href="/Structure">Structure</a></th>
      <th><a href="/Enumeration">Enumeration</a></th>
    </tr>
  </thead>
  <tbody>
    <tr><th>Properties</th>    <td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Methods</th>       <td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Subscripts</th>    <td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td><td>-</td></tr>
    <tr><th>Initializers</th>  <td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Extensions</th>    <td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Protocols</th>     <td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Reference Type</th><td><span class="glyphicon glyphicon-ok"></span></td><td></td>                                            <td>-</td></tr>
    <tr><th>Value Type</th>    <td></td>                                            <td><span class="glyphicon glyphicon-ok"></span></td><td>-</td></tr>
    <tr><th>Deinitializers</th><td><span class="glyphicon glyphicon-ok"></span></td><td></td>                                            <td>-</td></tr>
    <tr><th>Inheritance</th>   <td><span class="glyphicon glyphicon-ok"></span></td><td></td>                                            <td>-</td></tr>
  </tbody>
</table>


We consider creating a [Structure](/Structure) when one or more of the following conditions apply:

- The structure's primary purpose is to encapsulate a few relatively simple data values
- It is reasonable to expect that the encapsulated values will be copied rather than referenced when we assign or pass around an instance of the structure
- Any properties stored by the structure are themselves value types, which would also be expected to be copied rather than referenced
- The structure does not need to inherit properties or behavior from another existing type

Example of good candidates for structures include the following:

- The size of a geometric shape
- A point in a 3D coordinate system

# Inheritance

Rules for a subclass who inherits or not 'designated' and 'convenience' initializers of its superclass:

<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th>The subclass...</th>
      <th>Inherits Designated</th>
      <th>Inherits Convenience</th>
    </tr>
  </thead>
  <tbody>
    <tr><th>Doesn't define any initializers</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Implements all superclass's designated initializers</th><td></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
  </tbody>
</table>


<!--
# Code

Class in Swift support the following features:

1. Properties (type & instance)
1. Initializers
1. Deinitializers
1. Methods (type & instance)
1. Subclassing (inheritance)
1. Subscripts
-->

<!--
``
//
// Swift 3
//

import UIKit

/*
1) Properties (type & instance)
2) Initializers
3) Deinitializers
4) Methods (type & instance)
5) Subclassing (inheritance)
6) Subscripts
*/
class Vehicule {

  // 1) Type Properties 
  static var count = 0

  // 1) Instance Properties 
  var passengersCapacity = 4
  let zeroTo60: Float
  var color: UIColor

  // 2) Initializers (called 'designated' initializer)
  init(passengers: Int, zeroTo60: Float, color: UIColor = UIColor.black) {
    passengersCapacity = passengers
    self.zeroTo60 = zeroTo60
    self.color = color
    Vehicule.count += 1
  }

  // Use 'convenience' keyword for initializers who call another initializers (called 'convenience' initializer)
  convenience init(zeroTo60: Float) { self.init(passengers: 4, zeroTo60: zeroTo60) }

  convenience init() { self.init(zeroTo60: 6.0) }

  // 3) Deinitializers
  deinit {
    Vehicule.count -= 1
  }

  // 4) Type Method (you can use 'static' or 'class' keyword)
  class func printCount() {
    print("Count:", count) // Without the classname prefix ('Vehicule.')
  }

  // 4) Instance Method
  func start() {
    // print("(Silence)")
    fatalError("To override in subclass")
  }
}

// 6) Subclassing
// Only one super class, but multiple protocols
class ElectricVehicule : Vehicule {

  let rangePerCharge :Int
  
  // Assign non-optional properies before to call super class initializer
  // Only 'designated' initializer (vs. 'convenience' initializer) can call a superclass 'designated' initializer
  init(passengers: Int, zeroTo60: Float, rangePerCharge :Int) {
    self.rangePerCharge = rangePerCharge                   // assignement non-optional current class properies before...
    super.init(passengers: passengers, zeroTo60: zeroTo60) // ... to call superclass initializer
  }

  convenience init() { self.init(passengers: 4, zeroTo60: zeroTo60, rangePerCharge: 215) }

  // 'override' is mandatory
  override func start() {
    print("(Silence)")
  }

}

// 6) Subclassing
class MotorVehicule : Vehicule {

  let fuelEfficiency :Int
  
  init(passengers: Int, zeroTo60: Float, fuelEfficiency :Int) {
    self.fuelEfficiency = fuelEfficiency
    super.init(passengers: passengers, zeroTo60: zeroTo60)
  }

}

let myCar = Vehicule(passengers: 4, zeroTo60: 2.5)
var hisCar :Vehicule? = Vehicule()
print(Vehicule.count) // = 2

// 3) Implicit use of Deinitializers
hisCar = nil
print(Vehicule.count) // = 1

// By reference
let myWifeCar = myCar
myWifeCar.color = UIColor.red
// myCar.color == UIColor.red

// 4) Type Method
Vehicule.printCount()

// 4) Instance Method
myCar.start()

// 6) Subclassing
let teslaModelS = ElectricVehicule(passengers: 4, zeroTo60: 2.5, rangePerCharge: 315)
var teslaModel3 = ElectricVehicule? = ElectricVehicule()

let bugattiVeyron = MotorVehicule(passengers: 2, zeroTo60: 2.5, fuelEfficiency: 7)
```
-->
