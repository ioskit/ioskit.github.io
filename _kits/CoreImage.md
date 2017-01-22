---
layout: kit
iid: coreimage
name: 'Core Image'
status:
type: kit
since: iOS5
detailedUpdates:
 - update:
     ios: iOS8
     brief: "The Core Image framework (CoreImage.framework) has the following changes: 1) You can create custom image kernels in iOS. 2) Core image detectors can detect rectangles and QR codes in an image."
icon: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
prefixe: 'CI'
abstract: "Contains interfaces for manipulating video and still images."
kits__:
 - Foo
links:
 - link:
     name: 'Core Image Programming Guide'
     url: https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/CoreImaging/ci_intro/ci_intro.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Image Reference Collection'
     url: https://developer.apple.com/library/ios/documentation/GraphicsImaging/Reference/CoreImagingRef/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Beginning Core Image in iOS 6'
     url: http://www.raywenderlich.com/22167/beginning-core-image-in-ios-6
     description: ' - Ray Wenderlich'
     type: tutorial
---

The *Core Image* framework (`CoreImage.framework`) provides a powerful set of built-in filters for manipulating video and still images. You can use the built-in filters for everything from simple operations (like touching up and correcting photos) to more advanced operations (like face and feature detection). The advantage of using these filters is that they operate in a nondestructive manner so that your original images are never changed directly. In addition, Core Image takes advantage of the available CPU and GPU processing power to ensure that operations are fast and efficient.
