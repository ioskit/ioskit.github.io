---
layout: kit
iid: HapticFeedback
name: 'Haptic Feedback'
shortName_: 'Template'
status: iOS10
since: iOS10
abstract: "On supported devices, haptics provide a way to physically engage users with tactile feedback that gets attention and reinforces actions."
language: swift
type: technology
xcode_: xcode6
deprecated_: Contacts
icon_: /resources/images/kits/Siri/SiriKit.png
prefixe_: ''
kits:
 - UIKit
links:
 - link:
     name: "What's New in iOS 10.0: Providing Haptic Feedback"
     url: https://developer.apple.com/library/content/releasenotes/General/WhatsNewIniOS/Articles/iOS10.html#//apple_ref/doc/uid/TP40017084-DontLinkElementID_1
     description: ' - Apple Developer'
     type: reference
 - link:
     name: "iOS Human Interface Guidelines: Haptic Feedback"
     url: https://developer.apple.com/ios/human-interface-guidelines/interaction/feedback/
     description: ' - Apple Developer'
     type: reference
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
---

On [iPhone 7](/iPhone7) and [iPhone 7 Plus](/iPhone7Plus), haptics provide additional ways to physically engage users with tactile feedback 
that gets attention and reinforces actions. Some system-provided interface elements, such as pickers, switches, and sliders, automatically 
provide haptic feedback as users interact with them.

To give you the ability to generate haptics in an app that targets [iOS 10](/iOS10), [UIKit](/UIKit) introduces the new `UIFeedbackGenerator` 
class and three concrete subclasses, each of which enables haptics that are appropriate for a specific scenario, as shown in Table below:

<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th>Class name</th>
      <th>Example usage</th>
    </tr>
  </thead>
  <tbody>
    <tr><th><code>UIImpactFeedbackGenerator</code></th><td>Provides a physical experience that complements the visual feedback for an action or task. For example, the user might feel a thud when a view slides into place or two objects collide.</td></tr>
    <tr><th><code>UINotificationFeedbackGenerator</code></th><td>Indicates that a task or action, such as depositing a check or unlocking a vehicle, has completed, failed, or produced a warning of some kind.</td></tr>
    <tr><th><code>UISelectionFeedbackGenerator</code></th><td>Indicates that the selection is actively changing. For example, the user feels light taps while scrolling a picker wheel.</td></tr>
  </tbody>
</table>

Using one of the concrete subclasses, you ask the system to generate haptics for a specific scenario and iOS manages the strength and behavior 
of the feedback based on the scenario you choose. In addition, you can call the `prepare` method of `UIFeedbackGenerator` to inform the system 
that haptic feedback is about to be required and to minimize latency. To learn how to use haptics to provide the best user experience in your 
app, see “Haptic Feedback” in [iOS Human Interface Guidelines](https://developer.apple.com/ios/human-interface-guidelines/).