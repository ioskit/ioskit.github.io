---
layout: kit
name: 'AVKit'
iid: avkit
status:
type: kit
since: iOS8
updates:
icon___: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
prefixe: 'AV'
abstract: "The AVKit framework (AVKit.framework) previously introduced on OS X is available on iOS. Use it instead of Media Player framework when you need to display a video."
kits:
 - MediaPlayer
 - AVFoundation
links:
 - link:
     name: 'Mastering Modern Media Playback'
     url: https://developer.apple.com/videos/wwdc/2014/?id=503
     description: ' - WWDC 2014'
     type: reference
---

The *AVKit framework* (`AVKit.framework`) previously introduced on OS X is available on iOS. It leverages existing objects in AV Foundation to manage the presentation of video on a device. It is intended as a replacement for the [Media Player](/MediaPlayer) framework when you need to display video content.
