---
layout: feature
name: 'Function'
iid: Function
status: DOING
language: swift,objectivec
abstract: "Functions are self-contained chunks of code that perform a specific task. You give a function a name that identifies what it does, and this name is used to 'call' the function to perform its task when needed."
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): A Swift Tour - Functions and Closures'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID463
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Language Guide - Functions'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Functions.html
    description: ' - Apple Developer'
    type: reference
features:
 - OperatorFunction
 - Closure
 - Block
 - Class
 - Tuple
---


<!-- ================================================== --><a name="DefiningAndCalling"></a>

## Defining and Calling

### Swift 3

A function is defined with:

- the `func` keyword
- the name of the function (`greet` above)
- the parameters (optional) (`person: String` above)... see 'Parameters' section above
- the return type (optional) (`-> String` above)

```
func greet(person: String) -> String {
    let greeting = "Hello, " + person + "!"
    return greeting
}

print(greet(person: "Anna"))
```

Without parameter and return type:

```
func greet() {
    print("Hello, John Doe!")
}

greet()
```

Those elements define the identifiant of the function.

For example, the following functions are all differents:

```
greet(person:) -> String
greet(people:) -> String
greet2(person:) -> String
greet(person:)
```


<!-- ================================================== --><a name="Parameters"></a>

## Parameters

### Swift 3

Each function parameter has both:

1. an argument label (used when calling the function)
1. and a parameter name. 

By default, parameters use their parameter name as their argument label.

```
func someFunction(_ parameterName1: Int, argumentLabel2 parameterName2: Int, parameterName3: Int, parameterName4: Int = 42) -> (count: Int, title: String) {
  return (parameterName1 + parameterName2, "\(parameterName3) - \(parameterName4)");
}
let _ = someFunction(1, argumentLabel2: 2, parameterName3: 3) // Use the unnamed constant to handle unused retrun value of a function
```


<!-- ================================================== --><a name="Nested"></a>

## Nested Functions

### Swift 3

Functions can be nested. Nested functions have access to variables that were declared in the outer function. You can use nested functions to organize the code in a function that is long or complex.

```
func returnFifteen() -> Int {
    var y = 10
    func add() { // This is a nested function
        y += 5
    }
    add()
    return y
}
returnFifteen()
```


<!-- ================================================== --><a name="VariableParameters"></a>

## Constant and Variable Parameters / In-Out Parameters

### Swift 1

Function parameters are constants by default. Trying to change the value of a function parameter from within the body of that function results in a compile-time error. This means that you can't change the value of a parameter by mistake.

However, you can deal with a function having a variable copy of a parameter's value to work with. You can avoid defining a new variable yourself within the function by specifying one or more parameters as variable parameters instead. Variable parameters are available as variables rather than as constants, and give a new modifiable copy of the parameter's value for your function to work with.

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

### Swift 3 - In-Out Parameters

Function parameters are constants by default. Trying to change the value of a function parameter from within the body of that function results in a compile-time error. This means that you can't change the value of a parameter by mistake. If you want a function to modify a parameter's value, and you want those changes to persist after the function call has ended, define that parameter as an "in-out" parameter instead.

You write an in-out parameter by placing the `inout` keyword right before a parameter's type. An in-out parameter has a value that is passed in to the function, is modified by the function, and is passed back out of the function to replace the original value.

You can only pass a variable as the argument for an in-out parameter. You cannot pass a constant or a literal value as the argument, because constants and literals cannot be modified. You place an ampersand (`&`) directly before a variable's name when you pass it as an argument to an in-out parameter, to indicate that it can be modified by the function.

```
func greet(person: String, greeting: inout String) {
    greeting += person + "!"
}

var greeting = "Hello, "
print(greeting)               //  // "Hello,"
greet(person: "Anna", greeting: &greeting))
print(greeting)               //  // "Hello, Anna!"
```



<!-- ================================================== --><div name="DefaultValueParameters"></div>

## Default Parameter Values

You can define a default value for any parameter in a function by assigning a value to the parameter after that parameter's type. If a default value is defined, you can omit that parameter when calling the function.

### Swift 3

```
func greet(person: String = "John Doe") -> String {
    let greeting = "Hello, " + person + "!"
    return greeting
}

print(greet(person: "Anna")) // "Hello, Anna!"
print(greet())               // "Hello, John Doe!"
```


<!-- ================================================== --><div name="VariadicParameters"></div>

## Variadic Parameters

A variadic parameter accepts zero or more values of a specified type. You use a variadic parameter to specify that the parameter can be passed a varying number of input values when the function is called. Write variadic parameters by inserting three period characters (`...`) after the parameter's type name.

### Swift 3

```
func greet(_ persons: String...) -> String {
    var greeting: String = "Hello"
    for person in persons {
        greeting += ", " + person
    }
    return greeting + "!"
}

print(greet("Anna", "John", "Jack")) // "Hello, Anna, John, Jack!"
```


<!-- ================================================== --><div name="ReturnTypes"></div>

## Return Types

### Swift 3

With return value:

```
func greet(person: String) -> String {
    let greeting = "Hello, " + person + "!"
    return greeting
}

print(greet(person: "Anna"))
```

Without return type:

```
func greet(person: String) {
    print("Hello, " + person + "!")
}

greet(person: "Anna")
```

With multiple return values :

See [Tuples](/Tuple) page for mor details...

```
func greet(person: String) -> (text: String, lenght: Int) {
    let greeting = "Hello, " + person + "!"
    return (greeting, greeting.characters.count)
}

print(greet(person: "Anna").text)
```


<!-- ================================================== --><div name="FunctionTypes"></div>

## Using Function Types

### Swift 3

Every function has a specific function type, made up of the parameter types and the return type of the function. You use function types just like any other types in Swift. 

For example, you can define a constant or variable to be of a function type and assign an appropriate function to that variable:

```
func addTwoInts(_ a: Int, _ b: Int) -> Int {
    return a + b
}

var mathFunction: (Int, Int) -> Int = addTwoInts

print("Result: \(mathFunction(2, 3))")
```


### Function Types as Parameter Types

You can use a function type such as (Int, Int) -> Int as a parameter type for another function. This enables you to leave some aspects of a function’s implementation for the function’s caller to provide when the function is called.

```
func printMathResult(_ mathFunction: (Int, Int) -> Int, _ a: Int, _ b: Int) {
    print("Result: \(mathFunction(a, b))")
}

printMathResult(addTwoInts, 3, 5) // Prints "Result: 8"
```


### Function Types as Return Types

You can use a function type as the return type of another function. You do this by writing a complete function type immediately after the return arrow (`->`) of the returning function.

```
func stepForward(_ input: Int) -> Int {
    return input + 1
}

func stepBackward(_ input: Int) -> Int {
    return input - 1 
}

func chooseStepFunction(backwards: Bool) -> (Int) -> Int {
    return backwards ? stepBackward : stepForward
}

var currentValue = 3
let moveNearerToZero = chooseStepFunction(backward: currentValue > 0)
// moveNearerToZero now refers to the stepBackward() function
```

Here, the return type of the `chooseStepFunction` function is: a function that takes an `Int` as single parameter and returns an `Int`.
