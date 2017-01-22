---
layout: feature
name: 'Function'
iid: Function
status: DOING
language: swift,objectivec
abstract: ""
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - OperatorFunction
 - Closure
 - Block
---

<div name="Nested"></div>

## Nested Functions

TODO.


<div name="VariableParameters"></div>

## Constant and Variable Parameters

*[Swift](/Swift) feature.*

Function parameters are constants by default. Trying to change the value of a function parameter from within the body of that function results in a compile-time error. This means that you can’t change the value of a parameter by mistake.

However, you can deal with a function having a variable copy of a parameter’s value to work with. You can avoid defining a new variable yourself within the function by specifying one or more parameters as variable parameters instead. Variable parameters are available as variables rather than as constants, and give a new modifiable copy of the parameter’s value for your function to work with.

As a *variable copy*, future new values of the parameter, assigned inside the function, are not available from outside.

To define a Variable parameter we use the `var` prefix before the name of the parameter.

```
func alignRight(var string: String, totalLength: Int, pad: Character) -> String { let amountToPad = totalLength - count(string)
    if amountToPad < 1 {
        return string }
    let padString = String(pad)
    for _ in 1...amountToPad {
        string = padString + string
    }
    return string 
}
let originalString = "hello"
let paddedString = alignRight(originalString, 10, "-")
// paddedString is equal to "-----hello"
```


<div name="InOutParameters"></div>

## In-Out Parameters

TODO.


<div name="ReturnTypes"></div>

## Return Types

TODO.


<div name="FunctionTypesAsReturnTypes"></div>

### Function Types as Return Types

```
func stepForward(input: Int) -> Int {
    return input + 1
}

func stepBackward(input: Int) -> Int {
    return input - 1 
}

func chooseStepFunction(backwards: Bool) -> (Int) -> Int {
    return backwards ? stepBackward : stepForward
}
```

Here, the return type of the `chooseStepFunction` function is: a function that takes an `Int` as single parameter and returns an `Int`.
