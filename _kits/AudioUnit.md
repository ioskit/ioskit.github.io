---
layout: kit
name: 'AudioUnit'
id: audiounit
status: 
type: kit
since: iOS2
prefixe: 'AU,Audio'
abstract: "Contains the interfaces for loading and using audio units and support for Inter-App Audio."
kits:
 - CoreAudio
links:
 - link:
     name: 'Audio Unit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/AudioUnit/Reference/AudioUnit_Framework/_index.html
     description: ' - Apple Developer'
 - link:
     name: 'Audio Unit Processing Graph Services Reference'
     url: https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AUGraphServicesReference/index.html#//apple_ref/doc/uid/TP40007289
     description: ' - Apple Developer'
 - link:
     name: 'Audio Unit Hosting Guide for iOS'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Conceptual/AudioUnitHostingGuide_iOS/Introduction/Introduction.html
     description: ' - Apple Developer'
---

### Inter-App Audio

The *Audio Unit* framework (`AudioUnit.framework`) adds support for **Inter-App Audio**, which enables the ability to send MIDI commands and stream audio between apps on the same device. For example, you might use this feature to record music from an app acting as an instrument or use it to send audio to another app for processing. To vend your app’s audio data, publish a I/O audio unit (`AURemoteIO`) that is visible to other processes. To use audio features from another app, use the audio component discovery interfaces in [iOS7](/iOS7).
For information about the new interfaces, see the framework header files. For general information about the interfaces of this framework, see Audio Unit Framework Reference.
