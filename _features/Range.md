---
layout: feature
name: 'Range'
iid: Range
status: DONE
language: swift
abstract: "A interval over a comparable type, from a lower bound up to, (including or not) an upper bound."
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Range Operators'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID73
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'API Reference: Generic Structure, Range'
    url: https://developer.apple.com/reference/swift/range
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'API Reference: Generic Structure, Closed Range'
    url: https://developer.apple.com/reference/swift/closedrange
    description: ' - Apple Developer'
    type: reference
features:
 - For
---

* TOC
{:toc}

## Closed Range

An interval over a comparable type, from a lower bound up to, and including, an upper bound. 
You create instances of ClosedRange by using the closed range operator (`...`):

```
for index in 1...5 {
    print("\(index) times 5 is \(index * 5)")
}
// Write 5 lines
```

It is possible to use double:

```
let underFive = 0.0...5.0
print(underFive.contains(3.14))     // Prints "true"
print(underFive.contains(6.28))     // Prints "false"
```

It is also possible to use characters:

```
let lowercase = "a"..."z"
print(lowercase.contains("c"))      // Prints "true"
print(lowercase.contains("5"))      // Prints "false"
```

Ranges can be used to access arrays:

```
var accounts = ['11', '22', '33']
accounts[3...5] = ['44', '55', '66']
print(accounts)                     // Prints ['11', '22', '33', '44', '55', '66']
```

See also:

- [ClosedRange](https://developer.apple.com/reference/swift/closedrange): An interval over a comparable type, from a lower bound up to, and including, an upper bound.
- [ClosedRangeIndex](https://developer.apple.com/reference/swift/closedrangeindex): A position in a CountableClosedRange instance.
- [ClosedRangeIterator](https://developer.apple.com/reference/swift/closedrangeiterator): An iterator over the elements of a CountableClosedRange instance.


## Half Closed Range

You create Half Closed Range instances by using the half-open range operator (`..<`).

```
for index in 1..<5 {
    print("\(index) times 5 is \(index * 5)")
}
// Write 4 lines
```

You can use a Range instance to quickly check if a value is contained in a particular range of values. For example:

```
print(underFive.contains(3.14))     // Prints "true"
print(underFive.contains(6.28))     // Prints "false"
print(underFive.contains(5.0))      // Prints "false"
```

Range instances can represent an empty interval, unlike ClosedRange.

```
let empty = 0.0..<0.0
print(empty.contains(0.0))          // Prints "false"
print(empty.isEmpty)                // Prints "true"
```

## Instance Properties

- `count: Bound.Stride`: The number of values contained in the range.
- `customMirror: Mirror`: 
- `debugDescription: String`: A textual representation of the range, suitable for debugging.
- `description: String`: A textual representation of the range.
- `isEmpty: Bool`: A Boolean value indicating whether the range contains no elements.
- `lowerBound: Bound`: The range’s lower bound.
- `upperBound: Bound`: The range’s upper bound.

```
var fingers = 1..<6
print(fingers.count)                // Prints "5"
print(fingers.upperBound)           // Prints "6"
```

## Instance Methods

- `func clamped(to: Range<Bound>)`: Returns a copy of this range clamped to the given limiting range.
- `func contains(Bound)`: Returns a Boolean value indicating whether the given element is contained within the range.
- `func overlaps(CountableClosedRange<Bound>)`: Returns a Boolean value indicating whether this range and the given range contain an element in common.
- `func overlaps(CountableRange<Bound>)`: Returns a Boolean value indicating whether this range and the given range contain an element in common.
- `func overlaps(ClosedRange<Bound>)`: Returns a Boolean value indicating whether this range and the given range contain an element in common.
- `func overlaps(Range<Bound>)`: Returns a Boolean value indicating whether this range and the given range contain an element in common.

```
var fingers = 1..<6
print(fingers.contains(5))          // Prints "true"
print(fingers.contains(6))          // Prints "false"
```

## stride

The `stride` functions enable us to iterate through ranges with a step other than one. There are two stride functions: the stride to function, which 
iterates over exclusive ranges, and stride through, which iterates over inclusive ranges. Let's consider the following example:

```
let fourToTwo = Array(stride(from: 4, to: 1, by: -1)) // [4, 3, 2]
let fourToOne = Array(stride(from:4, through: 1, by: -1)) // [4, 3, 2, 1]
```
