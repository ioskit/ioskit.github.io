---
layout: kit
name: 'CoreGraphics'
iid: coregraphics
status:
type: kit
since: iOS2
icon__: /resources/images/kits/AppExtensions/app-extensions-icon_2x.png
prefixe: 'CG'
abstract: "Contains the interfaces for Quartz 2D"
kits:
 - ImageIO
links:
 - link:
     name: 'Quartz 2D Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/GraphicsImaging/Conceptual/drawingwithquartz2d/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Graphics Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CoreGraphics/Reference/CoreGraphics_Framework/index.html
     was: https://developer.apple.com/library/ios/documentation/CoreGraphics/Reference/CoreGraphics_Framework/_index.html
     description: ' - Apple Developer'
     type: reference
---

The *Core Graphics* framework (`CoreGraphics.framework`) contains the interfaces for the Quartz 2D drawing API. Quartz is the same advanced, vector-based drawing engine that is used in OS X. It supports path-based drawing, antialiased rendering, gradients, images, colors, coordinate-space transformations, and PDF document creation, display, and parsing. Although the API is C based, it uses object-based abstractions to represent fundamental drawing objects, making it easy to store and reuse your graphics content.
