---
layout: kit
name: 'Notification Center'
iid: notificationcenter
status:
type: kit
since: iOS5
detailedUpdates__:
 - update:
     ios: iOS8
     brief: ""
prefixe: 'NK'
abstract: "provides support for creating widgets that display information in Notification Center"
icon: /resources/images/kits/Notifications/notifications-hero.png
kits:
 - AppExtensions
links:
 - link:
     name: 'Local and Push Notifications for Developers'
     url: https://developer.apple.com/notifications/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Notification Center Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/NotificationCenter/Reference/NotificationCenter_Framework/index.html
     description: ' (for information about how to create notification center widgets)'
     type: reference
 - link:
     name: 'App Extension Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214
     description: ' (for information about how to create notification center widgets)'
     type: reference
 - link:
     name: 'Apple Push Notification Services in iOS 6 Tutorial'
     url: http://www.raywenderlich.com/32960/apple-push-notification-services-in-ios-6-tutorial-part-1
     description: ' - Ray Wenderlich'
     type: tutorial
---

The *Notification Center* framework (`NotificationCenter.framework`) helps you create and manage extensions—typically called widgets—in the Today view. The framework provides API you can use to specify whether a widget has content to display and to customize aspects of its appearance and behavior on both platforms.

Local and push notifications are great for keeping users informed with timely and relevant content, whether your app is running in the background or inactive. Notifications can display a message, play a distinctive sound, or update a badge on your app icon.