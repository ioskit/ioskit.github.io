---
layout: kit
name: 'AVFoundation'
iid: avfoundation
status:
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The AV Foundation framework (AVFoundation.framework) includes many enhancements: see page content."
 - update:
     ios: iOS8
     brief: "Arbitrary types of metadata can be embedded with a video recording at various points in time. For example, you might record the current physical location in a video created by a moving camera device."
prefixe: 'AV'
abstract: "AV Foundation framework provides essential services for working with time-based audiovisual media on iOS and OS X."
kits:
 - CoreMedia
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


### iOS 7

The AV Foundation framework (AVFoundation.framework) includes the following enhancements:

* The AVAudioSession class supports the following new behaviors:
  * Selecting the preferred audio input, including audio from built-in microphones
  * Multichannel input and output
* The AVVideoCompositing protocol and related classes let you support custom video compositors.
* The AVSpeechSynthesizer class and related classes provide speech synthesis capabilities.
* The capture classes add support and interfaces for the following features:
  * Discovery of a camera’s supported formats and frame rates
  * High fps recording
  * Still image stabilization
  * Video zoom (true and digital) in recordings and video preview, including custom ramping
  * Real-time discovery of machine-readable metadata (barcodes)
  * Autofocus range restriction
  * Smooth autofocus for capture
  * Sharing your app’s audio session during capture
  * Access to the clocks used during capture
  * Access to capture device authorization status (user must now grant access to the microphone and camera)
  * Recommended settings for use with data outputs and asset writer
* There are new metadata key spaces for supported ISO formats such as MPEG-4 and 3GPP, and improved support for filtering metadata items when copying those items from source assets to output files using the AVAssetExportSession class.
* The AVAssetWriter class provides assistance in formulating output settings, and there are new level constants for H.264 encoding.
* The AVPlayerLayer class adds the videoRect property, which you can use to get the size and position of the video image.
* The AVPlayerItem class supports the following changes:
  * Asset properties can be loaded automatically when AVPlayerItem objects are prepared for playback.
  * When you link your app against iOS 7 SDK, the behavior when getting the values of player item properties—such as the duration, tracks, or presentationSize properties—is different from the behaviors in previous versions of iOS. The properties of this class now return a default value and no longer block your app if the AVPlayerItem object is not yet ready to play. As soon as the player item’s status changes to AVPlayerItemStatusReadyToPlay, the getters reflect the actual values of the underlying media resource. If you use key-value observing to monitor changes to the properties, your observers are notified as soon as changes are available.
* The AVPlayerItemLegibleOutput class can process timed text from media files.
* The AVAssetResourceLoaderDelegate protocol now supports loading of arbitrary ranges of bytes from a media resource.
