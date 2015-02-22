---
layout: kit
name: 'AVFoundation'
id: avfoundation
status:
since: iOS2
prefixe: 'AV'
link: https://developer.apple.com/library/ios/documentation/AudioVideo/Conceptual/AVFoundationPG/Articles/00_Introduction.html
abstract: "AV Foundation framework provides essential services for working with time-based audiovisual media on iOS and OS X. Through a modern Objective-C interface, you can easily play, capture, edit, or encode media formats such as QuickTime movies and MPEG-4 files."
links:
 - link:
     name: 'AV Foundation for iOS and OS X'
     url: https://developer.apple.com/av-foundation/
     description: ' - Apple Developer'
 - link:
     name: 'AV Foundation Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/AudioVideo/Conceptual/AVFoundationPG/Articles/00_Introduction.html
     description: ' - For more information about how to use AV Foundation'
 - link:
     name: 'AV Foundation Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVFoundationFramework/index.html
     description: ' - For information about the classes of the AV Foundation framework'
 - link:
     name: 'Moving to AV Kit and AV Foundation'
     url: https://developer.apple.com/videos/wwdc/2013/#606
     description: ' - WWDC 2013'
---

The **AV Foundation framework** (`AVFoundation.framework`) provides a set of Objective-C classes for playing, recording, and managing audio and video content. Use this framework when you want to integrate media capabilities seamlessly into your app’s user interface. You can also use it for more advanced media handling. For example, you use this framework to play multiple sounds simultaneously and control numerous aspects of the playback and recording process.

The services offered by this framework include:

* Audio session management, including support for declaring your app’s audio capabilities to the system
* Management of your app’s media assets
* Support for editing media content
* The ability to capture audio and video
* The ability to play back audio and video
* Track management
* Metadata management for media items
* Stereophonic panning
* Precise synchronization between sounds
* An Objective-C interface for determining details about sound files, such as the data format, sample rate, and number of channels
* Support for streaming content over AirPlay
