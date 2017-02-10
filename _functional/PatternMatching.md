---
layout: functional
name: 'Pattern Matching'
iid: PatternMatching
status: DONE
abstract: "Pattern matching is the ability to destructure values and match different switch cases based on correct value matches."
---

__Pattern matching__ is the ability to destructure values and match different switch cases based on correct value matches. Pattern matching 
capabilities are existent in languages such as [Scala](/Scala), [Erlang](/Erlang), and [Haskell](/Haskell). 

[Swift](/Swift) provides powerful switch-cases and if-cases with where clauses as well. It provides the [Switch](/Switch) statement to compare 
a value against different matching patterns. The related statement will be executed once the pattern is matched. Unlike most other C-based 
programming languages, Swift does not need a `break` statement for each case and supports any value types. `Switch` statements can be used 
for range matching and `where` clauses in `switch` statements can be used to check for additional conditions. The following example presents 
a simple `switch` statement with an additional conditional checking:

```
   let aNumber = "Four or Five"
   switch aNumber {
       case "One":
           let one = "One"
       case "Two", "Three":
           let twoOrThree = "Two or Three"
       case let x where x.hasSuffix("Five"):
           let fourOrFive = "it is \(x)"
       default:
           let anyOtherNumber = "Any other number"
   }
```
