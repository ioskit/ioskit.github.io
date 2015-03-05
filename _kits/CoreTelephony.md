---
layout: kit
name: 'Core Telephony'
id: coretelephony
status:
type: kit
since: iOS4
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'CT'
abstract: "Contains routines for accessing telephony-related information."
kits__:
 - Foo
links:
 - link:
     name: 'Core Telephony Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/NetworkingInternet/Reference/CoreTelephonyFrameworkReference/index.html
     description: ' - Apple Developer'
     type: reference
---

The **Core Telephony** framework (`CoreTelephony.framework`) provides interfaces for interacting with phone-based information on devices that have a cellular radio. Apps can use this framework to get information about a user’s cellular service provider. Apps interested in cellular call events (such as VoIP apps) can also be notified when those events occur.