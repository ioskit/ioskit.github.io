---
layout: kit
name: 'Intents UI'
iid: IntentsUI
type: kit
status: iOS10
since: iOS10
icon_: /resources/images/kits/Siri/SiriKit.png
abstract: "Create an app extension that injects custom content into the Siri and Maps interfaces"
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
prefixe: ''
kits:
 - IntentsUI
 - SiriKit
links:
 - link:
     name: 'API reference: IntentsUI'
     url: https://developer.apple.com/reference/intentsui
     description: ' - Apple Developer'
     type: reference
---

The Intents UI framework (`IntentsUI.framework`) supports the creation of an Intents UI extension, 
which is an optional app extension that displays custom content in the Siri or Maps interfaces. 
An Intents UI extension requires a corresponding Intents extension, which handles intents and provides an appropriate response. 
The Intents UI extension provides only the interface elements needed to display that response to the user.
