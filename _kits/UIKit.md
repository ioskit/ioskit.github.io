---
layout: kit
name: 'UIKit'
id: uikit
status: TODO
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
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
