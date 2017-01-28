---
layout: feature
name: 'Class Method'
iid: ClassMethod
status: DONE
language: objectivec
abstract: "In Objective-C, a class is itself an object with an opaque type called Class. Classes can’t have properties defined using the declaration syntax shown earlier for instances, but they can receive messages: they are called Class methods."
links:
 - link:
     name: 'Programming with Objective-C, Objective-C Classes Are also Objects'
     url: https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/DefiningClasses/DefiningClasses.html#//apple_ref/doc/uid/TP40011210-CH3-SW18
     description: ' - Apple Developer'
     type: reference
features:
 - TypeMethod
---

In Objective-C, a class is itself an object with an opaque type called Class. Classes can’t have properties defined using the declaration syntax shown earlier for instances, but they can receive messages.

The typical use for a class method is as a factory method, which is an alternative to the object allocation and initialization procedure described in Objects Are Created Dynamically.

Class methods are like [Type Methods in Swift](/TypeMethod).

Class methods are denoted by the use of a `+` sign, which differentiates them from instance methods using a `-` sign:

{% gist cb8b5ac63d0a782e84a1 %}

<!--
<pre>
  <code class="swift">@interface SomeClass : NSObject
  
    + (void)someClassMethod;
    - (void)someInstanceMethod;
  
  @end</code>
</pre>

Then you can call the method like that:

<pre>
  <code class="swift">[SomeClass someClassMethod];</code>
</pre>

-->