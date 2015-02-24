---
layout: kit
name: 'CoreAudio'
id: coreaudio
status:
type: kit
since: iOS2
prefixe: 'Audio'
abstract: "Provides the data types used throughout Core Audio. See Core Audio."
kits:
 - AudioToolbox
 - AudioUnit
 - CoreMIDI
 - MediaToolbox
links:
 - link:
     name: 'Core Audio Overview'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Conceptual/CoreAudioOverview/Introduction/Introduction.html
     description: ' - Apple Developer'
 - link:
     name: 'Core Audio Overview - What Is Core Audio?'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Conceptual/CoreAudioOverview/WhatisCoreAudio/WhatisCoreAudio.html
     description: ' (OS X Core Audio architecture) - Apple Developer'
 - link:
     name: 'Core Audio Overview - Core Audio Services'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Conceptual/CoreAudioOverview/WhatsinCoreAudio/WhatsinCoreAudio.html
     description: ' - Apple Developer'
 - link:
     name: 'Audio Queue Services Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/MusicAudio/Conceptual/AudioQueueProgrammingGuide/Introduction/Introduction.html
     description: ' - Apple Developer'
 - link:
     name: 'Audio Tutorial for iOS: Playing Audio Programatically'
     url: http://www.raywenderlich.com/69369/audio-tutorial-ios-playing-audio-programatically-2014-edition
     description: ' - Ray Wenderlich (and other CoreAudio tutorials)'
---

## The family

Core Audio is a family of frameworks (listed below) that provides native support for handling audio. These frameworks support the generation, recording, mixing, and playing of audio in your apps. You can also use these interfaces to work with MIDI content and to stream audio and MIDI content to other apps.

<img src="/resources/images/kits/CoreAudio/iphone_os_audio_architecture_2x.png" width="600" alt="iOS Core Audio architecture">

* `CoreAudio.framework` - Defines the audio data types used throughout Core Audio. For more information, see below.
* `AudioToolbox.framework`- Provides playback and recording services for audio files and streams. This framework also provides support for managing audio files, playing system alert sounds, and triggering the vibrate capability on some devices. For more information, see [AudioToolbox](/AudioToolbox).
* `AudioUnit.framework` - Provides services for using the built-in audio units, which are audio processing modules. This framework also supports vending your app’s audio content as an audio component that is visible to other apps. For more information, see [AudioUnit](/AudioUnit).
* `CoreMIDI.framework` - Provides a standard way to communicate with MIDI devices, including hardware keyboards and synthesizers. You use this framework to send and receive MIDI messages and to interact with MIDI peripherals connected to an iOS-based device using the dock connector or network. For more information, see [CoreMIDI](/CoreMIDI).
* `MediaToolbox.framework` - Provides access to the audio tap interfaces. For more information, see [MediaToolbox](/MediaToolbox).

## The framework

The *Core Audio* framework (which is not an umbrella framework for the other services in Core Audio, but rather a peer) declares data types and constants used by other Core Audio interfaces. This framework also includes a handful of convenience functions.

