---
layout: kit
id: accelerate
name: 'Accelerate'
status: 
type: kit
since: iOS4
icon: /resources/images/kits/WatchKit/watchkit_2x.png
abstract: "Contains interfaces for performing digital signal processing (DSP), linear algebra, and image-processing calculations."
prefixe: 'cblas,vDSP'
kits__:
 - AddressBookUI
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Accelerate framework (Accelerate.framework) includes the following enhancements: 1) Improved support for manipulating Core Graphics data types. 2) Support for working with grayscale images of 1, 2, or 4 bits per pixel. 3) New routines for converting images between different formats and transforming image contents. 4)Support for biquad (IIR) operations"
links:
 - link:
     name: 'Accelerate Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Accelerate/Reference/AccelerateFWRef/index.html
     was: https://developer.apple.com/library/ios/documentation/Accelerate/Reference/AccelerateFWRef/_index.html
     description: ' - Apple Developer'
     type: reference
---

The *Accelerate framework* (`Accelerate.framework`) contains interfaces for performing digital signal processing (DSP), linear algebra, and image-processing calculations. The advantage of using this framework over writing your own versions of these interfaces is that they are optimized for all of the hardware configurations present in iOS devices. Therefore, you can write your code once and be assured that it runs efficiently on all devices.
