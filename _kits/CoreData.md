---
layout: kit
name: 'CoreData'
iid: coredata
status: 
since: iOS3
prefixe: 'NS'
link: https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/CoreData/cdProgrammingGuide.html
abstract: "Contains interfaces for managing your application’s data model. See Core Data Framework."
kits:
 - CloudKit
links:
 - link:
     name: 'Core Data Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Cocoa/Reference/CoreData_ObjC/index.html#//apple_ref/doc/uid/TP40001181
     description: ''
 - link:
     name: 'Introduction to Core Data Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/CoreData/cdProgrammingGuide.html
     description: ' - Apple Developer'
 - link:
     name: 'Core Data Tutorial for iOS: Getting Started'
     url: http://www.raywenderlich.com/934/core-data-tutorial-for-ios-getting-started
     description: ' - Ray Wenderlich'
---

The *Core Data framework* (`CoreData.framework`) is a technology for managing the data model of a Model-View-Controller app. Core Data is intended for use in apps in which the data model is already highly structured. Instead of defining data structures programmatically, you use the graphical tools in Xcode to build a schema representing your data model. At runtime, instances of your data-model entities are created, managed, and made available through the Core Data framework.

By managing your app’s data model for you, Core Data significantly reduces the amount of code you have to write for your app. Core Data also provides the following features:

* Storage of object data in a SQLite database for optimal performance
* An `NSFetchedResultsController` class to manage results for table views
* Management of undo/redo beyond basic text editing
* Support for the validation of property values
* Support for propagating changes and ensuring that the relationships between objects remain consistent
* Support for grouping, filtering, and organizing data in memory

If you are starting to develop a new app or are planning a significant update to an existing app, you should consider using Core Data. For an example of how to use Core Data in an iOS app, see Core Data Tutorial for iOS.
