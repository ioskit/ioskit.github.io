---
layout: feature
name: 'Type'
iid: Type
status: DOING
language: swift
abstract: ""
links__:
 - link:
    name: 'The Swift Programming Language, Functions and Closures'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID463
    description: ' - Apple Developer'
    type: reference
features:
 - Constant
 - Variable
 - Function
 - Tuple
---

* TOC
{:toc}

See also [other languages supporting Type Safety and Type Inference](/languages)

## Type safety

```
var aString :String = "text"
aString = 123 // Failed
```

## Type inference

```
var aString = "text"
aString = 123 // Failed, because aString infered as String
```

## Type Annotation

```
var aString :String // aString is annotated as a String
```

## Type Alias

```
typealias AudioSample = UInt16
var maxAmplitudeFound = AudioSample.min
```
