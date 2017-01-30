---
layout: kit
name: 'SiriKit'
iid: SiriKit
type: kit
status: iOS10
since: iOS10
icon: /resources/images/kits/Siri/SiriKit.png
abstract: "SiriKit lets you integrate your app’s content and services with the system. As its name implies, SiriKit is used most prominently to support Siri, giving users the ability to control your app’s behavior using their voice. "
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
prefixe: ''
kits:
 - Intents
 - IntentsUI
 - CarPlay
links:
 - link:
     name: 'SiriKit Programming Guide'
     url: https://developer.apple.com/library/content/documentation/Intents/Conceptual/SiriIntegrationGuide/index.html#//apple_ref/doc/uid/TP40016875
     description: ' - Apple Developer'
     type: reference
---

SiriKit lets you integrate your app’s content and services with the system. As its name implies, SiriKit is used most prominently to support Siri, 
giving users the ability to control your app’s behavior using their voice. However, Maps also uses SiriKit to integrate data from specific 
types of apps into the overall Maps experience. In both cases, the process for adding SiriKit support to your app is the same.

SiriKit is comprised of two frameworks, which you use to implement app extensions. 

* The [Intents](/Intents) framework supports the fundamental communication between your app and the system. You use that 
framework to define the types of tasks  you can perform and to handle those tasks when asked to do so. 
* The [Intents UI](/IntentsUI) framework provides optional support for presenting a custom interface when one of your tasks is performed.

SiriKit support is divided into domains, each of which defines one or more tasks that can be performed. In order to support SiriKit, 
apps must support one of the following domains:

- VoIP calling
- Messaging
- Payments
- Photo
- Workouts
- Ride booking
- [CarPlay](/CarPlay) (automotive vendors only)
- Restaurant reservations (requires additional support from Apple)
- Each domain defines one or more tasks that an app can perform. These tasks are known as intents because they represent the intentions of the user, and each intent is represented by a custom class whose properties contain information related to the task. For example, intents in the Payments domain contain properties with the amount of money to transfer and the users involved in the transaction. When the user makes a request through Siri or Maps, the system fills an intent object with the details of the request and delivers that object to your app extension. You use the intent object to validate the request data and perform the associated task.

For a list of intents contained in each domain, see [Intents Domains](https://developer.apple.com/library/content/documentation/Intents/Conceptual/SiriIntegrationGuide/SiriDomains.html#//apple_ref/doc/uid/TP40016875-CH9-SW2). 
For a list of classes in the Intents framework, see [Intents Framework Reference](https://developer.apple.com/reference/intents).
