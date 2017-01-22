---
layout: kit
name: 'CoreFoundation'
iid: corefoundation
status:
type: kit
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Core Foundation framework (CoreFoundation.framework) now lets you schedule stream objects on dispatch queues."
icon__: /resources/images/kits/AppExtensions/app-extensions-icon_2x.png
prefixe: 'CF'
abstract: "Provides fundamental software services, including abstractions for common data types, string utilities, collection utilities, resource management, and preferences."
kits:
 - Foundation
links:
 - link:
     name: 'Core Foundation Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CoreFoundation/Reference/CoreFoundation_Collection/index.html
     was: https://developer.apple.com/library/ios/documentation/CoreFoundation/Reference/CoreFoundation_Collection/_index.html
     description: ' - Apple Developer'
     type: reference
---

The *Core Foundation* framework (`CoreFoundation.framework`) is a set of C-based interfaces that provide basic data management and service features for iOS apps. This framework includes support for the following:

* Collection data types (arrays, sets, and so on)
* Bundles
* String management
* Date and time management
* Raw data block management
* Preferences management
* URL and stream manipulation
* Threads and run loops
* Port and socket communication

The Core Foundation framework is closely related to the [Foundation](/Foundation) framework, which provides Objective-C interfaces for the same basic features. When you need to mix Foundation objects and Core Foundation types, you can take advantage of the “toll-free bridging” that exists between the two frameworks. Toll-free bridging means that you can use some Core Foundation and Foundation types interchangeably in the methods and functions of either framework. This support is available for many of the data types, including the collection and string data types. The class and type descriptions for each framework state whether an object is toll-free bridged and, if so, what object it is connected to.

