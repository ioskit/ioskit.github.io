---
layout: kit
iid: ProactiveSuggestions
name: 'Proactive Suggestions'
shortName_: 'Template'
abstract: "In iOS 10 and later, you can provide information about what users do in your app, which helps the system promote your app in additional places, such as the keyboard with QuickType suggestions, Maps and CarPlay, the app switcher, Siri interactions, and (for media playing apps) the lock screen."
language_: swift
type: technology
xcode_: xcode6
status: iOS10
since: iOS10
icon_: /resources/images/kits/Siri/SiriKit.png
prefixe_: ''
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
kits:
 - SiriKit
 - UIKit
 - MapKit
 - CarPlay
links_:
 - link:
     name: 'SiriKit Programming Guide'
     url: https://developer.apple.com/library/content/documentation/Intents/Conceptual/SiriIntegrationGuide/index.html#//apple_ref/doc/uid/TP40016875
     description: ' - Apple Developer'
     type: reference
---

[iOS 10](/iOS10) introduces new ways to increase engagement with your app by helping the system suggest your app to users at appropriate times. 
If you adopted app search in your [iOS 9](/iOS9) app, you gave users access to activities and content deep within your app through Spotlight 
and Safari search results, [Handoff](/Handoff), and [Siri](/SiriKit) suggestions. In [iOS 10](/iOS10) and later, you can provide information 
about what users do in your app, which helps the system promote your app in additional places, such as the keyboard with QuickType suggestions, 
[Maps](/MapKit) and [CarPlay](/CarPlay), the app switcher, [Siri](/SiriKit) interactions, and (for media playing apps) the lock screen. 
These opportunities for enhanced integration with the system are supported by a collection of technologies, such as `NSUserActivity`, web markup 
defined by [http://Schema.org](Schema.org), and APIs defined in the Core Spotlight, [MapKit](/MapKit), [UIKit](/UIKit), and [Media Player](/MediaPlayer) 
frameworks.

In [iOS 10](/iOS10), the `NSUserActivity` object includes the `mapItem` property, which lets you provide location information that can be used 
in other contexts. For example, if your app displays hotel reviews, you can use the `mapItem` property to hold the location of the hotel the 
user is viewing so that when the user switches to a travel planning app, that hotel’s location is automatically available. And if you support 
app search, you can use the new text-based address component properties in `CSSearchableItemAttributeSet`, such as `thoroughfare` and `postalCode`, 
to fully specify locations to which the user may want to go. Note that when you use the `mapItem` property, the system automatically populates 
the `contentAttributeSet` property, too.

To share a location with the system, be sure to specify `latitude` and `longitude` values, in addition to values for the address component 
properties in `CSSearchableItemAttributeSet`. It’s also recommended that you supply a value for the `namedLocation` property, so that users 
can view the name of the `location`, and the `phoneNumbers` property, so that users can use [Siri](/SiriKit) to initiate a call to the location.

[iOS 9](/iOS9), adding markup to the structured data on your website enriched the content that users see in Spotlight and Safari search results. 
In [iOS 10](/iOS10), you can use location-related vocabulary defined at [http://Schema.org](Schema.org), such as `PostalAddress`, to further 
enhance the user’s experience. For example, if users view a location described on your website, the system can suggest the same location when 
users switch to Maps. Note that Safari supports both JSON-LD and Microdata encodings of [http://Schema.org](Schema.org) vocabularies.

[UIKit](/UIKit) introduces the `textContentType` property in the `UITextInputTraits` protocol so that you can specify the semantic meaning 
of the content you expect users to enter in a text area. When you provide this information, the system can in some cases automatically select 
an appropriate keyboard and improve keyboard corrections and proactive integration with information supplied from other apps and websites. 
For example, if you use `UITextContentTypeFullStreetAddress` to tell the system that you expect users to enter a complete address in a text field, 
the system can suggest the address of a location the user was recently viewing.

If your app plays media and you use the `MPPlayableContentManager` APIs, [iOS 10](/iOS10) helps you let users view album art and play media 
through your app on the lock screen.

If your ride-sharing app uses the `MKDirectionsRequest` API, [iOS 10](/iOS10) can display it in the app switcher when the user is likely to 
want a ride. To register as a ride-share provider, specify the `MKDirectionsModeRideShare` value for the `MKDirectionsApplicationSupportedModes` 
key in your `Info.plist` file. If your app supports only ride sharing, the system suggests your app with text that begins “Get a ride to...”; 
if your app supports both ride sharing and another routing type (such as Automobile or Bike), the system uses the text “Get directions to...”. 
Note that the `MKMapItem` object you receive may not include latitude and longitude information and would require geocoding.
