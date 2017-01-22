---
layout: kit
iid: corelocation
name: 'Core Location'
status:
type: kit
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Core Location framework (CoreLocation.framework) supports region monitoring and ranging using Bluetooth devices. Region monitoring lets you determine whether the iOS device enters a specific area, and ranging lets you determine the relative range of nearby Bluetooth devices. For example, an art museum might use region monitoring to determine whether a person is inside a particular gallery, and then place iBeacons near each painting. When the person is standing by a painting, the app would display information about it."
 - update:
     ios: iOS8
     brief: "The Core Location framework (CoreLocation.framework) has the following changes: 1) You can determine which floor the device is on, if the device is in a multistory building. 2) The visit service provides an alternative to the significant location change service for apps that need location information about interesting places visited by the user."
icon__: /resources/images/kits/CoreAudio/core-audio.png
abstract: "lets you determine the current location or heading associated with a device. "
kits:
 - iBeacon
 - MapKit
 - CoreBluetooth
links:
 - link:
     name: 'Location and Maps Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/LocationAwarenessPG/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Location Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CoreLocation/Reference/CoreLocation_Framework/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'How To Make an App Like RunKeeper'
     url: http://www.raywenderlich.com/73984/make-app-like-runkeeper-part-1
     description: ' - Ray Wenderlich'
     type: tutorial
---

The *Core Location* framework (`CoreLocation.framework`) provides location and heading information to apps. For location information, the framework uses the onboard GPS, cell, or Wi-Fi radios to find the user’s current longitude and latitude. You can incorporate this technology into your own apps to provide position-based information to the user. For example, you might have a service that searches for nearby restaurants, shops, or facilities, and base that search on the user’s current location. Core Location also provides the following capabilities:

* Access to compass-based heading information on iOS devices that include a magnetometer
* Support for region monitoring based on a geographic location or [CoreBluetooth](/CoreBluetooth) [iBeacon](/iBeacon)
* Support for low-power location-monitoring using cell towers
* Collaboration with [MapKit](/MapKit) to improve the quality of location data in specific situations, such as when driving
