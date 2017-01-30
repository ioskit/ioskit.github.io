---
layout: kit
iid: UserNotificationsUI
name: 'User Notifications UI'
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
 - UserNotifications
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

[iOS 10](/iOS10) intoduces the User Notifications UI framework (`UserNotificationsUI.framework`) lets you customize the appearance of local 
and remote notifications when they appear on the user’s device. You use this framework to define an [App Extensions](/AppExtensions) that 
receives the notification data and provides the corresponding visual representation. Your extension can also respond to custom actions associated 
with those notifications.

