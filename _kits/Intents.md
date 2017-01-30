---
layout: kit
name: 'Intents'
iid: Intents
type: kit
status: iOS10
since: iOS10
icon_: /resources/images/kits/Siri/SiriKit.png
abstract: "Create an app extension that handles Siri-related requests for your app’s services."
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
     url: https://developer.apple.com/reference/intents
     description: ' - Apple Developer'
     type: reference
---

The Intents framework (`Intents.framework`) supports the handling of [SiriKit](/SiriKit) interactions. You use the classes of this framework to define an Intents extension, which is an app extension that processes user requests originating from Siri or Maps. When the user requests your app services through one of these conduits, the system forwards those requests to your Intents extension for handling. You use the classes of this framework to receive the data from the user and to provide an appropriate response.

For information about how to use this framework to implement an Intents extension, see [SiriKit Programming Guide](https://developer.apple.com/library/content/documentation/Intents/Conceptual/SiriIntegrationGuide/index.html#//apple_ref/doc/uid/TP40016875).