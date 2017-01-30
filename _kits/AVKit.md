---
layout: kit
name: 'AVKit'
iid: avkit
type: kit
status: iOS10
since: iOS8
detailedUpdates:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
 - update:
     ios: iOS10
     brief: "The AVKit framework (AVKit.framework) includes the `updatesNowPlayingInfoCenter` property, which indicates when the Now Playing Info Center should be updated."
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

The *AVKit framework* (`AVKit.framework`) previously introduced on OS X is available on iOS. 
It leverages existing objects in AV Foundation to manage the presentation of video on a device. 
It is intended as a replacement for the [Media Player](/MediaPlayer) framework when you need to display video content.
