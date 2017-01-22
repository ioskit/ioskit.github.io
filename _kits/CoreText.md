---
layout: kit
name: 'Core Text'
iid: coretext
status:
type: kit
since: iOS3
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'CT'
abstract: "Contains a text layout and rendering engine."
kits:
 - TextKit
links:
 - link:
     name: 'Core Text Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/CoreText_Programming/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Text Reference Collection'
     url: https://developer.apple.com/library/ios/documentation/Carbon/Reference/CoreText_Framework_Ref/index.html
     was: https://developer.apple.com/library/ios/documentation/Carbon/Reference/CoreText_Framework_Ref/_index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Core Text Tutorial for iOS: Making a Magazine App'
     url: http://www.raywenderlich.com/4147/core-text-tutorial-for-ios-making-a-magazine-app
     description: ' - Ray Wenderlich'
     type: tutorial
---

The **Core Text** framework (`CoreText.framework`) offers a simple, high-performance C-based interface for laying out text and handling fonts. 

This framework is for apps that do not use [TextKit](/TextKit) but that still want the kind of advanced text handling capabilities found in word processor apps. The framework provides a sophisticated text layout engine, including the ability to wrap text around other content. It also supports advanced text styling using multiple fonts and rendering attributes.
