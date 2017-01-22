---
layout: kit
iid: ibeacon
name: 'iBeacon'
status:
type: technology
since: iOS7
icon: /resources/images/kits/iBeacon/ibeacon-logo-300x300.png
abstract: "Give your iOS apps the ability to determine its proximity to iBeacon-enabled hardware with Core Location APIs."
kits:
 - CoreLocation
 - CoreBluetooth
links:
 - link:
     name: 'iBeacon for Developers'
     url: https://developer.apple.com/ibeacon/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Getting Started with iBeacon'
     url: https://developer.apple.com/ibeacon/Getting-Started-with-iBeacon.pdf
     description: ' (PDF, 11 pages)'
     type: reference
 - link:
     name: 'Taking Core Location Indoors'
     url: https://developer.apple.com/videos/wwdc/2014/#708
     description: ' - WWDC 2014'
     type: reference
 - link:
     name: 'Developing iOS 7 Applications with iBeacons Tutorial'
     url: http://www.raywenderlich.com/66584/ios7-ibeacons-tutorial
     description: ' - Ray Wenderlich'
     type: tutorial
 - link:
     name: 'Buying an iBeacon: Guide to Bluetooth LE Devices'
     url: http://beekn.net/guide-to-ibeacons/
     description: ' - [beekn] Beacons, brands and culture on the Internet of Things'
     type: tutorial
---

From welcoming people as they arrive at a sporting event to providing information about a nearby museum exhibit, iBeacon opens a new world of possibilities for location awareness, and countless opportunities for interactivity between iOS devices and iBeacon hardware.

A few simple definitions from [beekn](http://beekn.net/guide-to-ibeacons/):

- **Beacons**: A beacon is any device that transmits a signal which allows another device to determine its proximity to the broadcaster. In a store, a beacon lets a customer’s app determine that it’s close to the candy aisle. The beacon doesn’t transmit content, it simply transmits a signal that lets a user’s phone or tablet figure out what its proximity to the beacon. The content (a coupon, for example) is delivered separately to the user’s app.
- **Bluetooth Low Energy** (BLE): This is the specification for one type of signal that beacons transmit. There are other types of signals that power beacons (e.g. audio signals) but Bluetooth LE has the advantage that it is low energy and is ‘native’ to most modern phones and tablets. See [CoreBluetooth](/CoreBluetooth)
- **iBeacon**: The term iBeacon and beacon are often used interchangeably. But iBeacon is a trademarked term by Apple that refers to the protocols, devices and uses of Bluetooth LE to create user experiences. Apple is vague about what it specifically means by an iBeacon. We take the definition to include the software protocols inside a user’s app, the use cases and user experiences, and the specifications that Apple requires of any beacon that can be called an iBeacon. They have not yet released those specifications [12.24.2013].
- **Devices**: *[The list below](http://beekn.net/guide-to-ibeacons/)* includes all devices that are capable of Bluetooth LE broadcasting. But a device can include other functionality. An iPhone, for example, can be programmed to act as a beacon. But it obviously does a whole lot more. Similarly, a beacon in a store can transmit Bluetooth LE signals, but they can also detect humidity, temperature, acceleration, or include modules for WiFi.

