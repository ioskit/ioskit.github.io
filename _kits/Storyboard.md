---
layout: kit
name: 'Storyboard'
iid: storyboard
kind: technology
status:
type: kit
since: iOS5
detailedUpdates__:
 - update:
     ios: iOS7
     brief: "The Core Foundation framework (CoreFoundation.framework) now lets you schedule stream objects on dispatch queues."
icon__: /resources/images/kits/AppExtensions/app-extensions-icon_2x.png
xcode: xcode42
prefixe:
abstract: "enables you to use Interface Builder to specify all the screens in your application, including the transitions between them and the controls used to trigger the transitions"
kits:
 - UIKit
links:
 - link:
     name: 'Cocoa Application Competencies for iOS - Storyboard'
     url: https://developer.apple.com/library/ios/documentation/General/Conceptual/Devpedia-CocoaApp/Storyboard.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Start Developing iOS Apps Today: Tutorial: Storyboards'
     url: https://developer.apple.com/library/prerelease/ios/referencelibrary/GettingStarted/RoadMapiOS/SecondTutorial.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'About Storyboards'
     url: https://developer.apple.com/library/ios/recipes/xcode_help-IB_storyboard/chapters/AboutStoryboards.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Xcode Overview'
     url: https://developer.apple.com/library/ios/documentation/ToolsLanguages/Conceptual/Xcode_Overview/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'UIStoryboard Class Reference'
     url: https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIStoryboard_Class/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Storyboards Tutorials'
     url: http://www.raywenderlich.com/tag/storyboard
     description: ' - Ray Wenderlich'
     type: tutorial
---

In [Xcode 4.2](/Xcode42), the Interface Builder user interface for iOS app UI design is based on using storyboards, that is, images of view controllers populated with user interface objects and connected together with segues. Storyboards enable you to use Interface Builder to specify all the screens in your application, including the transitions between them and the controls used to trigger the transitions. With storyboards, you can lay out every possible path through your application graphically, greatly reducing the amount of code you need to write for a complex multiscreen application.

Storyboards are the recommended way to design your app’s user interface. Storyboards let you design your entire user interface in one place so that you can see all of your views and view controllers and understand how they work together. An important part of storyboards is the ability to define **segues**, which are transitions from one view controller to another. These transitions allow you to capture the flow of your user interface in addition to the content. You can define these transitions visually, in Xcode, or initiate them programmatically.

You can use a single storyboard file to store all of your app’s view controllers and views, or you can use multiple view storyboards to organize portions of your interface. At build time, Xcode takes the contents of the storyboard file and divides it into discrete pieces that can be loaded individually for better performance. Your app never needs to manipulate these pieces directly. The [UIKit](/UIKit) framework provides convenience classes for accessing the contents of a storyboard from your code.

