---
layout: kit
name: 'AudioToolbox'
iid: audiotoolbox
status: 
type: kit
since: iOS2
prefixe: 'AU,Audio'
icon: /resources/images/kits/CoreAudio/core-audio.png
abstract: "Contains the interfaces for handling audio stream data and for playing and recording audio."
kits:
 - CoreAudio
 - AudioUnit
 - CoreMIDI
 - MediaToolbox
links:
 - link:
     name: 'Audio Toolbox Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Reference/CAAudioTooboxRef/index.html
     was: https://developer.apple.com/library/ios/documentation/MusicAudio/Reference/CAAudioTooboxRef/_index.html
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


### The framework

The *Audio Toolbox* framework (`AudioToolbox.framework`) provides playback and recording services for audio files and streams. This framework also provides support for managing audio files, playing system alert sounds, and triggering the vibrate capability on some devices.

It deals with [CoreAudio](/CoreAudio) objects.
