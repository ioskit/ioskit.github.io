---
layout: kit
name: 'NotificationCenter'
id: notificationcenter
status: TODO
type: kit
since: iOS5
detailedUpdates:
 - update:
     ios: iOS8
     brief: ""
prefixe: 'NK'
abstract: "provides support for creating widgets that display information in Notification Center"
kits:
 - AppExtensions
links:
 - link:
     name: 'App Extension Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214
     description: ' (for information about how to create notification center widgets)'
 - link:
     name: 'Notification Center Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/NotificationCenter/Reference/NotificationCenter_Framework/index.html#//apple_ref/doc/uid/TP40014443
     description: ' (for information about how to create notification center widgets)'
---

The *Notification Center* framework (`NotificationCenter.framework`) helps you create and manage extensions—typically called widgets—in the Today view. The framework provides API you can use to specify whether a widget has content to display and to customize aspects of its appearance and behavior on both platforms.
