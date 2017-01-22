---
layout: kit
name: 'UIKit'
iid: uikit
status: TODO
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The UIKit framework (UIKit.framework) includes many enhancements: see the content of the page."
 - update:
     ios: iOS8
     brief: "The UIKit framework (UIKit.framework) includes many enhancements: see the content of the page."
prefixe: 'UI'
link: 
abstract: "Contains classes and methods for the iOS application user interface layer. See UIKit Framework."
kits:
 - TextKit
links:
 - link:
     name: 'Unified Storyboards for Universal Apps'
     url: https://developer.apple.com/library/prerelease/ios/releasenotes/General/WhatsNewIniOS/Articles/iOS8.html#//apple_ref/doc/uid/TP40014205-SW30
     description: ' - Apple Developer'
     type: reference
---

Contains classes and methods for the iOS application user interface layer. See UIKit Framework.

### iOS 8

The UIKit framework (UIKit.framework) includes the following enhancements:

* Apps that use local or push notifications must explicitly register the types of alerts that they display to users by using a `UIUserNotificationSettings` object. This registration process is separate from the process for registering remote notifications, and users must grant permission to deliver notifications through the requested options.
* Local and push notifications can include custom actions as part of an alert. Custom actions appear as buttons in the alert. When tapped, your app is notified and asked to perform the corresponding action. Local notifications can also be triggered by interactions with Core Location regions.
* Collection views support dynamically changing the size of cells. Typically, you use this support to accommodate changes to the preferred text size, but you can adapt it for other scenarios too. Collection views also support more options for invalidating different portions of the layout and thereby improving performance.
* The `UISearchController` class replaces the `UISearchDisplayController` class for managing the display of search-related interfaces.
* The `UIViewController` class adopts traits and the new sizing techniques for adjusting the view controller’s content, as described in [Unified Storyboards for Universal Apps](https://developer.apple.com/library/prerelease/ios/releasenotes/General/WhatsNewIniOS/Articles/iOS8.html#//apple_ref/doc/uid/TP40014205-SW30).
* The `UISplitViewController` class is now supported on iPhone as well as iPad. The class adjusts its presented interface to adapt to the available space. The class also changes the way it shows and hides the primary view controller, giving you more control over how to display the split view interface.
* The `UINavigationController` class has new options for changing the size of the navigation bar or hiding it altogether.
* The new `UIVisualEffect` class enables you to integrate custom blur effects into your view hierarchies.
* The new `UIPresentationController` class lets you separate the content of your view controllers from the chrome used to display them.
* The new `UIPopoverPresentationController` class handles the presentation of content in a popover. The existing `UIPopoverController` class uses the popover presentation controller to show popovers on the screen.
* The new `UIAlertController` class replaces the `UIActionSheet` and `UIAlertView` classes as the preferred way to display alerts in your app.
* The new `UIPrinterPickerController` class offers a view controller-based way to display a list of printers and to select one to use during printing. Printers are represented by instances of the new `UIPrinter` class.
* You can take the user directly to your app-related settings in the Settings app. Pass the `UIApplicationOpenSettingsURLString` constant to the `openURL:` method of the `UIApplication` class.


### iOS 7

The UIKit framework (UIKit.framework) includes the following enhancements:

* All UI elements have been updated to present the new look associated with iOS 7.
* UIKit Dynamics lets you mimic real-world effects such as gravity in your animations; see Dynamic Behaviors for Views.
* Text Kit provides sophisticated text editing and display capabilities; see Text Kit.
* The UIView class defines the following additions:
  * The tintColor property applies a tint color to both the view and its subviews. For information on how to apply tint colors, see iOS 7 UI Transition Guide.
  * You can create keyframe-based animations using views. You can also make changes to your views and specifically prevent any animations from being performed.
* The UIViewController class defines the following additions:
  * View controller transitions can be customized, driven interactively, or replaced altogether with ones you designate.
  * View controllers can now specify their preferred status bar style and visibility. The system uses the provided information to manage the status bar style as new view controllers appear. You can also control how this behavior is applied using the UIViewControllerBasedStatusBarAppearance key in your app’s Info.plist file.
* The UIMotionEffect class defines the basic behavior for motion effects, which are objects that define how a view responds to device-based motion.
* Collection views add support for intermediate layout transitions and invalidation contexts (invalidation contexts help you improve the performance of your custom layout code). You can also apply UIKit Dynamics to collection view layout attributes to animate the items in the collection.
* The imageNamed: method of UIImage supports retrieving images stored in asset catalogs, which are a way to manage and optimize assets that have multiple sizes and resolutions. You create asset catalogs in Xcode.
* There are methods on UIView and UIScreen for creating a snapshot of their contents. Generating snapshots using these new interfaces is significantly faster than rendering the view or screen contents yourself.
* Gesture recognizers can specify dependencies dynamically to ensure that one gesture recognizer fails before another is considered.
* The UIKeyCommand class wraps keyboard events received from an external hardware keyboard. These events are delivered to the app’s responder chain for processing.
* A UIFontDescriptor object describes a font using a dictionary of attributes. Use font descriptors to interoperate with other platforms.
* The UIFont and UIFontDescriptor classes support dynamic text sizing, which improves legibility for text in apps. With this feature, the user controls the desired font size that all apps in the system should use.
* The UIActivity class now supports new activity types, including activities for sending items via AirDrop, adding items to a Safari reading list, and posting content to Flickr, Tencent Weibo, and Vimeo.
* The UIApplicationDelegate protocol adds methods for handling background fetch behaviors.
The UIScreenEdgePanGestureRecognizer class is a new gesture recognizer that tracks pan gestures that originate near an edge of the screen.
* UIKit adds support for running in a guided-access mode, which allows an app to lock itself to prevent modification by the user. This mode is intended for institutions such as schools, where users bring their own devices but need to run apps provided by the institution.
* State restoration now allows the saving and restoration of any object. Objects adopting the UIStateRestoring protocol can write out state information when the app moves to the background and have that state restored during subsequent launches.
* Table views now support estimating the height of rows and other elements, which improves scrolling performance.
* You can now more easily configure a UISearchDisplayController object to work with a UINavigationBar object.
