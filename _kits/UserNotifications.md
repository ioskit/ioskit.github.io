---
layout: kit
iid: UserNotifications
name: 'User Notifications'
shortName_: 'Template'
abstract: ""
language_: swift
type_: technology
xcode_: xcode6
status: iOS10
since: iOS10
icon_: /resources/images/kits/Siri/SiriKit.png
prefixe_: ''
kits:
 - UserNotificationsUI
 - AppExtensions
links_:
 - link:
     name: 'SiriKit Programming Guide'
     url: https://developer.apple.com/library/content/documentation/Intents/Conceptual/SiriIntegrationGuide/index.html#//apple_ref/doc/uid/TP40016875
     description: ' - Apple Developer'
     type: reference
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
---

[iOS 10](/iOS10) introduces the User Notifications framework (`UserNotifications.framework`), which supports the delivery and handling of local 
and remote notifications. You use the classes of this framework to schedule the delivery of local notifications based on specific conditions, 
such as time or location. Apps and [App Extensions](/AppExtensions) can use this framework to receive and potentially modify local and remote 
notifications when they are delivered to the user’s device.

Also introduced in [iOS 10](/iOS10), the [User Notifications UI](/UserNotificationsUI) framework (UserNotificationsUI.framework).

