---
layout: feature
name: 'Switch'
iid: Switch
status: DONE
language: swift,objectivec
abstract: "A switch statement considers a value and compares it against several possible matching patterns."
links:
 - link:
    name: 'The Swift Programming Language: Control Flow'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID120
    description: ' - Apple Developer'
    type: reference
features:
 - For
---

A switch statement considers a value and compares it against several possible matching patterns. It then executes an appropriate block of code, based on the first pattern that matches successfully. A switch statement provides an alternative to the if statement for responding to multiple potential states.

```
let someCharacter: Character = "e"
switch someCharacter {
case "a", "e":
case "i", "o", "u":
    println("\(someCharacter) is a vowel")
case "b", "c", "d", "f", "g", "h", "j", "k", "l", "m",
"n", "p", "q", "r", "s", "t", "v", "w", "x", "y", "z":
    println("\(someCharacter) is a consonant")
default:
    println("\(someCharacter) is not a vowel or a consonant")
}
// prints "e is a vowel"
```

See also [Pattern Matching](/functional/PatternMatching).
