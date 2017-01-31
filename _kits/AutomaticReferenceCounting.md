---
layout: kit
iid: arc
name: 'Automatic Reference Counting (ARC)'
shortName: ARC
status: iOS10
since: iOS4
type: technology
deprecated_: ContactsUI
abstract: "automates memory management for Objective-C and Swift objects."
icon:
xcode: xcode42
prefixe:
kits:
 - Swift
 - ObjectiveC
links:
 - link:
     name: 'Transitioning to ARC Release Notes'
     url: https://developer.apple.com/library/content/releasenotes/ObjectiveC/RN-TransitioningToARC/Introduction/Introduction.html
     was: https://developer.apple.com/library/prerelease/ios/releasenotes/ObjectiveC/RN-TransitioningToARC/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'The Swift Programming Language (Swift 3.0.1): Automatic Reference Counting'
     url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html
     was: https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Advanced Memory Management Programming Guide'
     url: https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/MemoryMgmt/Articles/MemoryMgmt.html
     was: https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/MemoryMgmt/Articles/MemoryMgmt.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'ARC Tutorials'
     url: http://www.raywenderlich.com/?s=arc&cof=FORID%3A10
     description: ' - Ray Wenderlich'
---

*Automatic Reference Counting* (ARC) makes memory management much easier, greatly reducing the chance that your program will have memory leaks. First, Xcode reviews your project to determine whether there are items that cannot be converted (and that you must therefore change manually). Then, Xcode rewrites your source code to use ARC.

[Swift](/Swift) uses *Automatic Reference Counting* (ARC) to track and manage your app’s memory usage. In most cases, this means that memory management “just works” in Swift, and you do not need to think about memory management yourself. ARC automatically frees up the memory used by class instances when those instances are no longer needed.

