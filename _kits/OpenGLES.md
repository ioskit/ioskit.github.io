---
layout: kit
name: 'OpenGL ES'
iid: opengles
status:
type: kit
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "iOS 7 adds support for OpenGL ES 3.0 and adds new features to OpenGL ES 2.0."
icon: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
prefixe: 'EAGL, GL'
abstract: "Contains the interfaces for OpenGL ES, which is an embedded version of the OpenGL cross-platform 2D and 3D graphics rendering library."
kits:
 - GLKit
links:
 - link:
     name: 'OpenGL ES Programming Guide for iOS'
     url: https://developer.apple.com/library/ios/documentation/3DDrawing/Conceptual/OpenGLES_ProgrammingGuide/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'OpenGL ES Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/OpenGLES/Reference/OpenGLES_Framework/index.html
     description: ' - Apple Developer'
     type: reference
---

The **OpenGL ES** framework (`OpenGLES.framework`) provides tools for drawing 2D and 3D content. It is a C-based framework that works closely with the device hardware to provide fine-grained graphics control and high frame rates for full-screen immersive apps such as games. You use the OpenGL framework in conjunction with the EAGL interfaces, which provide the interface between your OpenGL ES drawing calls and the native window objects in UIKit.

The framework supports OpenGL ES 1.1, 2.0, and 3.0. The 2.0 specification added support for fragment and vertex shaders and the 3.0 specification added support for many more features, including multiple render targets and transform feedback.
