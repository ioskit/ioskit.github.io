---
layout: kit
iid: AppThinning
name: 'App Thinning'
shortName_: 'Template'
status: iOS10
since: iOS9
abstract: "App thinning helps you develop apps for diverse platforms and deliver an optimized installation automatically."
language_: swift
type: technology
xcode_: xcode6
deprecated_: Contacts
icon_: /resources/images/kits/Siri/SiriKit.png
prefixe_: ''
kits_:
 - Intents
links:
 - link:
     name: 'App Thinning (iOS, watchOS)'
     url: https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppDistributionGuide/AppThinning/AppThinning.html#//apple_ref/doc/uid/TP40012582-CH35
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'On-Demand Resources Guide'
     url: https://developer.apple.com/library/content/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/index.html#//apple_ref/doc/uid/TP40015083
     description: ' - Apple Developer'
     type: reference
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
---

App thinning helps you develop apps for diverse platforms and deliver an optimized installation automatically. App thinning includes the following elements:

* **Slicing**. Artwork incorporated into the Asset Catalog and tagged for a platform allows the App Store to deliver only what is needed for installation.
* **On-Demand Resources**. Host additional content for your app in the iTunes App Store repository, allowing it to fetch resources as needed 
using asynchronous download and installation. To learn more about this technology, see [On-Demand Resources Guide](https://developer.apple.com/library/content/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/index.html#//apple_ref/doc/uid/TP40015083).
* **Bitcode**. Archive your app for submission to the App Store in an intermediate representation, which is compiled into 64- or 32-bit executables 
for the target devices when delivered.

To learn more about app thinning, see [App Thinning (iOS, watchOS)](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppDistributionGuide/AppThinning/AppThinning.html#//apple_ref/doc/uid/TP40012582-CH35).

