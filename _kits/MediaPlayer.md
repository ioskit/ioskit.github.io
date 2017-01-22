---
layout: kit
name: 'Media Player'
iid: mediaplayer
status:
type: kit
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "In the Media Player framework, the MPVolumeView class provides support for determining whether wireless routes such as AirPlay and Bluetooth are available for the user to select. You can also determine whether one of these wireless routes is currently active. For information about the new interfaces, see the framework header files."
 - update:
     ios: iOS8
     brief: "Two Media Player framework (MediaPlayer.framework) classes are extended with new metadata information."
icon: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
prefixe: 'MP'
abstract: "Contains interfaces for playing full-screen video."
kits:
 - AVKit
links:
 - link:
     name: 'Media Player Framework Reference'
     url: https://developer.apple.com/library/prerelease/ios/documentation/MediaPlayer/Reference/MediaPlayer_Framework/index.html
     description: ' - Apple Developer'
     type: reference
---

The *Media Player* framework provides facilities for playing movie, music, audio podcast, and audio book files. This framework also gives your application access to the iPod library, letting you find and play audio-based media items synced from iTunes on the desktop. iPod library access is read-only.
