---
layout: kit
name: 'PushKit'
iid: pushkit
status: 
type: kit
icon:
since: iOS8
prefixe: 'PK'
link: 
abstract: "Provides a way for VoIP apps to register with a device."
links:
 - link:
     name: 'PushKit Framework Reference - Introduction to PushKit'
     url: https://developer.apple.com/library/prerelease/ios/documentation/NetworkingInternet/Reference/PushKit_Framework/index.html
     description: ' (This is a preliminary document for an API or technology in development)'
---

The *PushKit* framework (`PushKit.framework`) provides registration support for VoIP apps. This framework replaces the previous APIs for registering VoIP apps. Instead of keeping a persistent connection open, and thus draining the device’s battery, an app can use this framework to receive push notifications when there is an incoming call.

