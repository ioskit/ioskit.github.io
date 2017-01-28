---
layout: feature
name: 'Error Handling'
iid: Error
status: DONE
language: swift
abstract: "Error handling is the process of responding to and recovering from error conditions in your program. Swift provides first-class support for throwing, catching, propagating, and manipulating recoverable errors at runtime."
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Error Handling'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ErrorHandling.html
    description: ' - Apple Developer'
    type: reference
features:
 - Class
---


Error handling is the process of responding to and recovering from error conditions in your program. Swift provides first-class support for:

1. Defining
1. Throwing
   1. Can use `guard`
   2. Initializers
1. Catching 
1. Propagating 
   1. Method throwing error should terminate signature with `throws`
1. Converting
   1. Use `try?` to handle an error by converting it to an optional value
1. Disabling
   1. Use `try!`
1. Clean up with `defer`


{% gist c4af7a94d2a3d15c0300c55e1988fee3 %}

<!--
```
    struct Item {
        var price: Int
        var count: Int
    }
    
    // 1) Defining
    // In Swift, errors are represented by values of types that conform to the Error protocol
    enum VendingMachineError: Error {
        case outOfStock
        case insufficientFunds(coinsNeeded: Int)
    }
    
    class VendingMachine {
    
        var inventory = [
            "Candy Bar": Item(price: 12, count: 7),
            "Chips": Item(price: 10, count: 4),
            "Pretzels": Item(price: 7, count: 11)
        ]
        var coinsDeposited = 0
        
        /*
         To indicate that a function, method, or initializer can throw an error, 
         you write the throws keyword in the functions declaration after its parameters.
         A function marked with throws is called a throwing function.
         Any code that calls this method must either handle the errors using 
         1/ a do-catch statement, 2/ try?, or 3/ try! or continue to propagate them
        */
        func vend(itemNamed name: String) throws { // 4.1) terminate signature with 'throws'
        
            // 2.1) Use 'guard' statements to exit the method early and throw appropriate errors 
            // if any of the requirements for purchasing a snack aren't met
            guard item.count > 0 else {
                throw VendingMachineError.outOfStock // 2) Throwing
            }
            guard item.price <= coinsDeposited else {
                throw VendingMachineError.insufficientFunds(coinsNeeded: item.price - coinsDeposited) // 2) Throwing
            }
            
            coinsDeposited -= item.price
            
            var newItem = item
            newItem.count -= 1
            inventory[name] = newItem
            
            print("Dispensing \(name)")
        }
    }
    
    let favoriteSnacks = [ "Alice": "Chips", "Bob": "Licorice", "Eve": "Pretzels", ]
    
    // 4.1) Propagating
    // Prefix call function throwing an Error with the `try` keyword
    func buyFavoriteSnack(person: String, vendingMachine: VendingMachine) throws {
    
        // The nil-coalescing operator (a ?? b) unwraps an optional a if it contains a value, 
        // or returns a default value b if a is nil
        let snackName = favoriteSnacks[person] ?? "Candy Bar"
    
        try vendingMachine.vend(itemNamed: snackName)
    }
    
    // 2.2) Throwing initializers can propagate errors in the same way as throwing functions
    struct PurchasedSnack {
        let name: String
    
        init(name: String, vendingMachine: VendingMachine) throws { // 2.2) Throwing initializers 
            try vendingMachine.vend(itemNamed: name)
            self.name = name
        }
    }
    
    var vendingMachine = VendingMachine()
    vendingMachine.coinsDeposited = 8
    
    // 3) Catching
    do {
        try buyFavoriteSnack(person: "Alice", vendingMachine: vendingMachine)
    } catch VendingMachineError.outOfStock {
        print("Out of Stock.")
    } catch VendingMachineError.insufficientFunds(let coinsNeeded) {
        print("Insufficient funds. Please insert an additional \(coinsNeeded) coins.")
    }
    // Prints "Insufficient funds. Please insert an additional 2 coins."
    
    
    //
    // 5) Converting Errors to Optional Values
    //
    
    func someThrowingFunction() throws -> Int {
        // ...
    }
    
    // You use 'try?' to handle an error by converting it to an optional value. 
    // If an error is thrown while evaluating the try? expression, the value of the expression is nil.
    let x = try? someThrowingFunction()
     
    // It is equivalent to:
    let y: Int?
    do {
        y = try someThrowingFunction()
    } catch {
        y = nil
    }
    
    func fetchData() -> Data? {
        if let data = try? fetchDataFromDisk() { return data }
        if let data = try? fetchDataFromServer() { return data }
        return nil
    }
    
    
    //
    // 6) Disabling Error Propagation
    //
    // Sometimes you know a throwing function or method won't, in fact, throw an error at runtime.
    // If an error actually is thrown, you'll get a runtime error.
    let photo = try! loadImage(atPath: "./Resources/John Appleseed.jpg")
    
    
    
    //
    // 7) Specifying Cleanup Actions
    //
    func processFile(filename: String) throws {
        if exists(filename) {
            let file = open(filename)
            
            // Use a 'defer' statement to execute a set of statements 
            // just before code execution leaves the current block of code.
            // Deferred actions are executed in reverse order of how they are specified that is, 
            // the code in the first defer statement executes after code in the second, and so on.
            defer {
                close(file)
            }
            while let line = try file.readline() {
                // Work with the file.
            }
            // close(file) is called here, at the end of the scope.
        }
    }
```
-->