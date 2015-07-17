---
layout: feature
name: 'Type methods'
id: MethodsTypeSwift
status: 
language: swift
abstract: "Instance methods are methods that are called on an instance of a particular type. You can also define methods that are called on the type itself. These kinds of methods are called Type methods."
links:
 - link:
     name: 'The Swift Programming Language, Methods'
     url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Methods.html#//apple_ref/doc/uid/TP40014097-CH15-ID241
     was: https://developer.apple.com/library/ios/documentation/Accelerate/Reference/AccelerateFWRef/_index.html
     description: ' - Apple Developer'
     type: reference
features:
 - MethodsClassObjectiveC
 - MethodsVisibilitySwift
---

Instance methods are methods that are called on an instance of a particular type. You can also define methods that are called on the type itself. These kinds of methods are called type methods.

Type methods are like [Class methods in Objective-C](/MethodsClassObjectiveC).

To define a Type method you have to use the `class` selector:

<pre>
  <code class="swift">class SomeClass {
  
     class func someTypeMethod() {
        // type method implementation goes here
     }
  
  }</code>
</pre>

Then you can call the method like that:

<pre>
  <code class="swift">SomeClass.someTypeMethod()</code>
</pre>

