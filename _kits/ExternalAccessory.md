---
layout: kit
name: 'External Accessory'
iid: externalaccessory
status:
type: kit
since: iOS3
icon__: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
prefixe: 'EA'
abstract: "Contains interfaces for communicating with attached hardware accessories."
links:
 - link:
     name: 'External Accessory Programming Topics'
     url: https://developer.apple.com/library/ios/featuredarticles/ExternalAccessoryPT/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
---

The *External Accessory* framework (`ExternalAccessory.framework`) provides support for communicating with hardware accessories attached to an iOS-based device. Accessories can be connected through the 30-pin dock connector of a device or wirelessly using Bluetooth. The External Accessory framework provides a way for you to get information about each available accessory and to initiate communications sessions. After that, you are free to manipulate the accessory directly using any commands it supports.
