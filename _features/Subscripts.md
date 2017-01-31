---
layout: feature
name: 'Subscripts'
iid: Subscripts
status: DONE
language: swift
abstract: "Classes, structures, and enumerations can define subscripts, which are shortcuts for accessing the member elements of a collection, list, or sequence. You use subscripts to set and retrieve values by index without needing separate methods for setting and retrieval."
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Subscripts'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Subscripts.html#//apple_ref/doc/uid/TP40014097-CH16-ID305
    description: ' - Apple Developer'
    type: reference
features:
 - Class
 - Structure
 - Enumeration
---

[Classes](/Classe), [Structures](/Structure), and [Enumerations](/Enumeration) can define subscripts, which are shortcuts for accessing the 
member elements of a collection, list, or sequence. You use subscripts to set and retrieve values by index without needing separate methods 
for setting and retrieval. For example, you access elements in an Array instance as `someArray[index]` and elements in a Dictionary instance 
as `someDictionary[key]`.

You can define multiple subscripts for a single type, and the appropriate subscript overload to use is selected based on the type of index 
value you pass to the subscript. Subscripts are not limited to a single dimension, and you can define subscripts with multiple input parameters 
to suit your custom type’s needs.

## Syntax

Subscripts syntax is similar to both instance method syntax and computed property syntax. You write subscript definitions with:
 
* the `subscript` keyword, 
* and specify one or more input parameters 
* and a return type, in the same way as instance methods. 
* Unlike instance methods, subscripts can be read-write or read-only. 

For getter and setter behavior:

```
subscript(index: Int) -> Int {
    get {
        // return an appropriate subscript value here
    }
    set(newValue) {
        // perform a suitable setting action here
    }
}
```

For read-only behavior (getter):

```
subscript(index: Int) -> Int {
    // return an appropriate subscript value here
}
```

For example:

```
struct TimesTable {
    let multiplier: Int
    subscript(index: Int) -> Int {
        return multiplier * index
    }
}
let threeTimesTable = TimesTable(multiplier: 3)
print("six times three is \(threeTimesTable[6])")
// Prints "six times three is 18"
```


## Subscript Usage
   
The exact meaning of “subscript” depends on the context in which it is used. Subscripts are typically used as a shortcut for accessing the 
member elements in a collection, list, or sequence. You are free to implement subscripts in the most appropriate way for your particular 
class or structure’s functionality.


## Subscript Options

Subscripts can:
 
* take any number of input parameters, and these input parameters can be of any type. 
* return any type
* use variadic parameters, but they can’t use in-out parameters or provide default parameter values

```
struct Matrix {
    let rows: Int, columns: Int
    var grid: [Double]
    init(rows: Int, columns: Int) {
        self.rows = rows
        self.columns = columns
        grid = Array(repeating: 0.0, count: rows * columns)
    }
    func indexIsValid(row: Int, column: Int) -> Bool {
        return row >= 0 && row < rows && column >= 0 && column < columns
    }
    subscript(row: Int, column: Int) -> Double {
        get {
            assert(indexIsValid(row: row, column: column), "Index out of range")
            return grid[(row * columns) + column]
        }
        set {
            assert(indexIsValid(row: row, column: column), "Index out of range")
            grid[(row * columns) + column] = newValue
        }
    }
}
```