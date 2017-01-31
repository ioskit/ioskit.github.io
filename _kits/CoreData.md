---
layout: kit
type: kit
iid: coredata
name: 'CoreData'
status: iOS10
since: iOS3
deprecated_: Contacts
prefixe: 'NS'
abstract: "Contains interfaces for managing your application’s data model. See Core Data Framework."
icon: /resources/images/kits/CoreData/core-data-icon.png
language_: swift
xcode_: xcode6
kits:
 - CloudKit
links:
 - link:
     name: 'Core Data Framework Reference'
     url: https://developer.apple.com/reference/coredata#//apple_ref/doc/uid/TP40001181
     was: https://developer.apple.com/library/ios/documentation/Cocoa/Reference/CoreData_ObjC/index.html#//apple_ref/doc/uid/TP40001181
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Data Programming Guide'
     url: https://developer.apple.com/library/prerelease/content/documentation/Cocoa/Conceptual/CoreData/
     was: https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/CoreData/cdProgrammingGuide.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Data Tutorial for iOS: Getting Started'
     url: http://www.raywenderlich.com/934/core-data-tutorial-for-ios-getting-started
     description: ' - Ray Wenderlich'
     type: tutorial
detailedUpdates:
 - update:
     ios: iOS10
     brief: "<p>The Core Data framework (<code>CoreData.framework</code>) includes the following enhancements:</p>
             <ul><li><code>NSPersistentStoreCoordinator</code> now maintains a connection pool for SQLite stores. Root <code>NSManagedObjectContext</code> 
             objects (those without parent MOCs) transparently support concurrent fetching and faulting without serializing against each other.</li>
             <li><code>NSManagedObjectContext</code> objects with SQLite stores in WAL journal_mode support a new feature called query generations. 
             These allow a MOC to be pinned to a version of the database at a point in time and perform all future fetching and faulting against 
             that version of the database. Pinned MOCs are moved to the most recent transaction with any save, and query generations do not 
             survive the process's life time.</li>
             <li>The new <code>NSPersistentContainer</code> class provides your app with a high-level integration point that maintains references 
             to your <code>NSPersistentStoreCoordinator</code>, <code>NSManagedObjectModel</code>, and other configuration resources.</li>
             <li>Core Data now has tighter integration with Xcode and automatically generates and updates your <code>NSManagedObject</code> subclasses.</li>
             <li><code>NSManagedObject</code> includes several additional convenience methods, making it easier to fetch and create subclasses. 
             <code>NSManagedObject</code> subclasses that have a 1:1 relationship with an entity now support entity.</li>
             <li>Core Data introduces several API adjustments that provide better integration with Swift, including parameterized <code>NSFetchRequest</code> objects.</li></ul>
             <p>For more information, see <a href='https://developer.apple.com/reference/coredata'>Core Data Framework Reference</a>.</p>"
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
