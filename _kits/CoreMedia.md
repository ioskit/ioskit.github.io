---
layout: kit
name: 'Core Media'
iid: coremedia
status:
type: kit
since: iOS4
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'CM'
abstract: "Contains low-level routines for manipulating audio and video."
kits:
 - AVFoundation
links:
 - link:
     name: 'Core Media Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CoreMedia/Reference/CoreMediaFramework/index.html
     was: https://developer.apple.com/library/ios/documentation/CoreMedia/Reference/CoreMediaFramework/_index.html
     description: ' - Apple Developer'
     type: reference
---

The **Core Media** framework (`CoreMedia.framework`) provides the low-level media types used by the [AVFoundation](/AVFoundation) framework. Most apps never need to use this framework, but it is provided for those few developers who need more precise control over the creation and presentation of audio and video content.
