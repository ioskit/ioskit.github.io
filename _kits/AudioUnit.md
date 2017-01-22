---
layout: kit
name: 'AudioUnit'
iid: audiounit
status: 
type: kit
since: iOS2
prefixe: 'AU,Audio'
icon: /resources/images/kits/CoreAudio/core-audio.png
abstract: "Contains the interfaces for loading and using audio units and support for Inter-App Audio."
kits:
 - CoreAudio
 - AudioToolbox
 - CoreMIDI
 - MediaToolbox
links:
 - link:
     name: 'Audio Unit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/AudioUnit/Reference/AudioUnit_Framework/index.html
     was: https://developer.apple.com/library/ios/documentation/AudioUnit/Reference/AudioUnit_Framework/_index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Audio Unit Processing Graph Services Reference'
     url: https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AUGraphServicesReference/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Audio Unit Hosting Guide for iOS'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Conceptual/AudioUnitHostingGuide_iOS/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
---

## The family

Core Audio is a family of frameworks that provides native support for handling audio. These frameworks support the generation, recording, mixing, and playing of audio in your apps. You can also use these interfaces to work with MIDI content and to stream audio and MIDI content to other apps.

* [CoreAudio](/CoreAudio)
* [AudioToolbox](/AudioToolbox)
* [AudioUnit](/AudioUnit)
* [CoreMIDI](/CoreMIDI)
* [MediaToolbox](/MediaToolbox)


### Inter-App Audio

The *Audio Unit* framework (`AudioUnit.framework`) adds support for **Inter-App Audio**, which enables the ability to send MIDI commands and stream audio between apps on the same device. For example, you might use this feature to record music from an app acting as an instrument or use it to send audio to another app for processing. To vend your app’s audio data, publish a I/O audio unit (`AURemoteIO`) that is visible to other processes. To use audio features from another app, use the audio component discovery interfaces in [iOS7](/iOS7).
For information about the new interfaces, see the framework header files. For general information about the interfaces of this framework, see Audio Unit Framework Reference.
