---
layout: kit
name: 'iAd'
id: iad
status:
since: iOS4
detailedUpdates:
 - update:
     ios: iOS7
 - update:
     ios: iOS8
     brief: "The iAd framework (iAd.framework) adds the following new features: 1) If you are using AV Kit to play a video, you can play preroll advertisements before the video is played. 2) You can look up more information about the the effectiveness of advertisements for your app."
prefixe: 'AD'
link: https://developer.apple.com/iad/resources/
abstract: "Contains classes for displaying advertisements in your application. See iAd Framework."
kits:
 - AdSupport
links:
 - link:
     name: 'Using iAd in Your iOS Apps'
     url: https://developer.apple.com/iad/resources/
     description: ' - Apple Developer'
 - link:
     name: 'iAd Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/iAd_Guide/Introduction/Introduction.html
     description: ''
 - link:
     name: 'iAd Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Reference/iAd_ReferenceCollection/index.html
     description: ''
 - link:
     name: 'iAd tutorial for iOS: How To Integrate iAd into Your iPhone App'
     url: http://www.raywenderlich.com/1371/iad-tutorial-for-ios-how-to-integrate-iad-into-your-iphone-app
     description: ' - Ray Wenderlich'
 - link:
     name: 'App rejected : app uses the iOS Advertising Identifier but does not include ad functionality'
     url: https://discussions.apple.com/thread/6463462
     description: ' - Apple Support Communities'
---

The *iAd framework* (`iAd.framework`) lets you deliver banner-based advertisements from your app. Advertisements are incorporated into standard views that you integrate into your user interface and present when you want. The views themselves work with Apple’s iAd Service to automatically handle all the work associated with loading and presenting rich media ads and responding to taps in those ads.

iAd does not use the [AdSupport framework](/AdSupport), `ASIdentifierManager`, or the Advertising Identifier. Therefore they are not required for iAd implementations and should not be included in your app for iAd support.