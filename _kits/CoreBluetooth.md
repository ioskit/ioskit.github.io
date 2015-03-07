---
layout: kit
name: 'Core Bluetooth'
id: corebluetooth
status: 
type: kit
since: iOS5
updates: iOS7
prefixe: 'CB'
abstract: "Provides access to low-power Bluetooth hardware."
kits:
 - iBeacon
 - CoreLocation
links:
 - link:
     name: 'Bluetooth for Developers'
     url: https://developer.apple.com/bluetooth/
     description: ' - Apple Developer'
 - link:
     name: 'Core Bluetooth Programming Guide'
     url: https://developer.apple.com/library/prerelease/ios/documentation/NetworkingInternetWeb/Conceptual/CoreBluetooth_concepts/AboutCoreBluetooth/Introduction.html
     description: ' - Apple Developer'
 - link:
     name: 'Core Bluetooth Framework Reference'
     url: https://developer.apple.com/library/mac/documentation/CoreBluetooth/Reference/CoreBluetooth_Framework/
     description: ' - Apple Developer'
 - link:
     name: 'Introduction to Core Bluetooth: Building a Heart Rate Monitor'
     url: http://www.raywenderlich.com/52080/introduction-core-bluetooth-building-heart-rate-monitor
     description: ' - Ray Wenderlich (other tutorials about Core Bluetooth)'
---

The *Core Bluetooth* framework (`CoreBluetooth.framework`) allows developers to interact specifically with **Bluetooth low energy** (LE) accessories. The Objective-C interfaces of this framework allow you to do the following:

* Scan for Bluetooth accessories and connect and disconnect to ones you find
* Vend services from your app, turning the iOS device into a peripheral for other Bluetooth devices
* Broadcast iBeacon information from the iOS device
* Preserve the state of your Bluetooth connections and restore those connections when your app is subsequently launched
* Be notified of changes to the availability of Bluetooth peripherals


##Details

-   Bluetooth protocol:
    -   Devices
    -   Services
    -   Characteristics
-   Since [iOS2](/iOS2), and Bluetooth Low Energy since [iOS5](/iOS5)
-   Since iPhone 4s and iPad 3rd generation (since iPad 2)
-   Slow speed (100k bytes / minute)
-   See also [iBeacon](/iBeacon)
-   GATT Profiles
-   Central
    -   `CBCentralManager`
    -   `CBCentralDelegate`
-   and Peripherical
    -   `CBPeriphericalManager`
    -   `CBPeriphericalDelegate`
    -   `CBPeripherical`
    -   `CBService`
    -   `CBCharacteristic`
-   Particle Detector app
