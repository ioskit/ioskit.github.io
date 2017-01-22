---
layout: kit
name: 'Core Motion'
iid: coremotion
status:
type: kit
since: iOS4
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Core Motion framework (CoreMotion.framework) adds support for step counting and motion tracking. With step counting, the framework detects movements that correspond to user motion and uses that information to report the number of steps to your app. Because the system detects the motion, it can continue to gather step data even when your app is not running. Alongside this feature, the framework can also distinguish different types of motion, including different motions reflective of travel by walking, by running, or by automobile. Navigation apps might use that data to change the type of directions they give to users."
 - update:
     ios: iOS8
     brief: "Core Motion provides two new classes (CMAltimeter and CMAltitudeData) which allow you to access the barometer on the iPhone 6 and iPhone 6 Plus. On these two devices, you can also use a CMMotionActivity object to determine whether the user is on a bicycle."
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'CM'
abstract: "Contains interfaces for accessing accelerometer and gyro data."
kits:
 - HealthKit
links:
 - link:
     name: 'Core Motion Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CoreMotion/Reference/CoreMotion_Reference/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Motion Tracking with the Core Motion Framework'
     url: https://developer.apple.com/videos/wwdc/2014/?id=612
     description: ' - WWDC 2014'
     type: reference
 - link:
     name: 'Tutorials about Core Motion'
     url: http://www.raywenderlich.com/?s=Core+Motion&cof=FORID%3A10
     description: ' - Ray Wenderlich'
     type: tutorial
---

The **Core Motion** framework (`CoreMotion.framework`) provides a single set of interfaces for accessing all motion-based data available on a device. The framework supports accessing both raw and processed accelerometer data using a new set of block-based interfaces. For devices with a built-in gyroscope, you can retrieve the raw gyro data as well as processed data reflecting the attitude and rotation rates of the device.
You can use both the accelerometer and the gyro-based data for games or other apps that use motion as input or as a way to enhance the overall user experience. For devices with step-counting hardware, you can access that data and use it to track fitness-related activities.
