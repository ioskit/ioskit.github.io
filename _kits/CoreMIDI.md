---
layout: kit
name: 'Core MIDI'
iid: coremidi
status:
type: kit
since: iOS4
icon: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'MIDI'
abstract: "Contains low-level routines for handling MIDI data."
kits:
 - CoreAudio
 - AudioToolbox
 - AudioUnit
 - MediaToolbox
links:
 - link:
     name: 'Core MIDI Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Reference/CACoreMIDIRef/index.html
     was: https://developer.apple.com/library/ios/documentation/MusicAudio/Reference/CACoreMIDIRef/_index.html
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

The *Core MIDI* framework (`CoreMIDI.framework`) Provides a standard way to communicate with MIDI devices, including hardware keyboards and synthesizers. You use this framework to send and receive MIDI messages and to interact with MIDI peripherals connected to an iOS-based device using the dock connector or network.

Connect from an iOS device using the dock connector or a network. For more information about using the dock connector, see [Apple’s MFi program](http://developer.apple.com/programs/mfi/).