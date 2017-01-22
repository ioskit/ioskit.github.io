---
layout: feature
name: 'Class'
iid: Class
status: DOING
language: swift,objectivec
abstract: "Use class followed by the class’s name to create a class."
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - ClassMethod
 - TypeMethod
 - Closure
 - Extension
 - Protocol
 - Enumeration
 - Structure
features_:
 - Variable
 - MethodsVisibility
---

# Comparison between Class and Structure

<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th></th>
      <th>Class</th>
      <th>Structure</th>
    </tr>
  </thead>
  <tbody>
    <tr><th>Properties</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Methods</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Subscripts</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Initializers</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Extensions</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Protocols</th><td><span class="glyphicon glyphicon-ok"></span></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Reference Type</th><td><span class="glyphicon glyphicon-ok"></span></td><td></td></tr>
    <tr><th>Value Type</th><td></td><td><span class="glyphicon glyphicon-ok"></span></td></tr>
    <tr><th>Deinitializers</th><td><span class="glyphicon glyphicon-ok"></span></td><td></td></tr>
    <tr><th>Inheritance</th><td><span class="glyphicon glyphicon-ok"></span></td><td></td></tr>
  </tbody>
</table>

# Code

Class in Swift support the following features:

1. Properties (type & instance)
1. Initializers
1. Deinitializers
1. Methods (type & instance)
1. Subscripts


{% gist ac6040f564565c68b72054edf60e05b2 %}

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
5) Subscripts
*/
class Vehicule {

  // 1) Type Properties 
  static var count = 0

  // 1) Instance Properties 
  var passengersCapacity = 4
  let zeroTo60: Float
  var color: UIColor

  // 2) Initializers
  init(passengers: Int, zeroTo60: Float, color: UIColor = UIColor.black) {
    passengersCapacity = passengers
    self.zeroTo60 = zeroTo60
    self.color = color
    Vehicule.count += 1
  }

  // You have to use 'convenience' keyword for initializers who call another initializers
  convenience init(zeroTo60: Float) { self.init(passengers: 4, zeroTo60: zeroTo60) }

  convenience init() { self.init(zeroTo60: 6.0) }

  // 3) Deinitializers
  deinit {
    Vehicule.count +-= 1
  }

  // 4) Type Method (you can use 'static' or 'class' keyword)
  class func printCount() {
    print("Count:", count) // Without the classname prefix ('Vehicule.')
  }

  // 4) Instance Method
  func start() {
    print("(Silence)")
  }
}

let teslaModelS = Vehicule(passengers: 4, zeroTo60: 2.5)
let teslaModel3 :Vehicule? = Vehicule()
print(Vehicule.count) // = 2

// Implicit use of Deinitializers
teslaModel3 = nil
print(Vehicule.count) // = 1

// By reference
let p100d = teslaModelS
p100d.color = UIColor.red
// teslaModelS.color == UIColor.red

// Type Method
Vehicule.printCount()

// Instance Method
teslaModelS.start()
```
-->