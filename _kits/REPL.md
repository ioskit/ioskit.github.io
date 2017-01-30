---
layout: kit
iid: REPL
name: 'Read-Eval-Print-Loop'
shortName: REPL
abstract: "Read-Eval-Print-Loop is the interactive version of Swift programming language built and run from the command line interface"
language: swift
type: technology
status: iOS10
since: iOS8
xcode: xcode6
links:
 - link:
    name: 'Introduction to the Swift REPL'
    url: https://developer.apple.com/swift/blog/?id=18
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'Getting Started: Using the REPL'
    url: https://swift.org/getting-started/#using-the-repl
    description: ' - swift.org'
    type: reference
 - link:
    name: 'REPL and Debugger'
    url: https://swift.org/lldb/
    description: ' - swift.org'
    type: reference
kits:
 - Swift
 - InteractivePlaygrounds
---

Xcode 6.1 introduces yet another way to experiment with Swift in the form of an interactive Read Eval Print Loop, or REPL. 
Developers familiar with interpreted languages will feel comfortable in this command-line environment, 
and even experienced developers will find a few unique features. 

To get started, launch `Terminal.app` (found in `/Applications/Utilities`) and type `swift` command (without any other arguments) at the prompt. 
You’ll then be in the Swift REPL an interactive shell that will read, evaluate, and print the results of any Swift code you enter:
:

```
$ swift
Welcome to Apple Swift version 2.2. Type :help for assistance.
  1>
Interacting with the REPL is a great way to experiment with Swift. For example, if you enter the expression 1 + 2, the result of the expression, 3, is printed on the next line:
```


Interacting with the REPL is a great way to experiment with Swift. For example, if you enter the expression 1 + 2, 
the result of the expression, 3, is printed on the next line:

```
  1> 1 + 2
$R0: Int = 3
  2> println("Hello, \(name)")
Hello, Katherine
```
