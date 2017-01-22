---
layout: kit
name: 'iAd'
iid: iad
status:
type: kit
since: iOS4
abstract: "Contains classes for displaying advertisements in your application. See iAd Framework."
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The iAd framework (iAd.framework) includes two extensions to other frameworks that make it easier to incorporate ads into your app’s content: 1) The framework introduces new methods on the MPMoviePlayerController class that let you run ads before a movie. 2) The framework extends the UIViewController class to make it easier to create ad-supported content. You can now configure your view controllers to display ads before displaying the actual content they manage."
 - update:
     ios: iOS8
     brief: "The iAd framework (iAd.framework) adds the following new features: 1) If you are using AV Kit to play a video, you can play preroll advertisements before the video is played. 2) You can look up more information about the the effectiveness of advertisements for your app."
prefixe: 'AD'
kits:
 - AdSupport
links:
 - link:
     name: 'Using iAd in Your iOS Apps'
     url: https://developer.apple.com/iad/resources/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'iAd Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/iAd_Guide/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'iAd Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Reference/iAd_ReferenceCollection/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'iAd tutorial for iOS: How To Integrate iAd into Your iPhone App'
     url: http://www.raywenderlich.com/1371/iad-tutorial-for-ios-how-to-integrate-iad-into-your-iphone-app
     description: ' - Ray Wenderlich'
     type: tutorial
 - link:
     name: 'App rejected : app uses the iOS Advertising Identifier but does not include ad functionality'
     url: https://discussions.apple.com/thread/6463462
     description: ' - Apple Support Communities'
     type: reference
---

The *iAd framework* (`iAd.framework`) lets you deliver banner-based advertisements from your app. Advertisements are incorporated into standard views that you integrate into your user interface and present when you want. The views themselves work with Apple’s iAd Service to automatically handle all the work associated with loading and presenting rich media ads and responding to taps in those ads.

iAd does not use the [AdSupport framework](/AdSupport), `ASIdentifierManager`, or the Advertising Identifier. Therefore they are not required for iAd implementations and should not be included in your app for iAd support.