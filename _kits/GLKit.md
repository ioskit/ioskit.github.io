---
layout: kit
name: 'GLKit'
iid: glkit
status:
type: kit
since: iOS5
updates:
icon___: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
prefixe: 'GLK'
abstract: "Contains Objective-C utility classes for building complex OpenGL ES applications."
kits:
 - OpenGLES
links:
 - link:
     name: 'GLKit Framework Reference'
     url: https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/CoreImaging/ci_intro/ci_intro.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'OpenGL ES 1.1 specification'
     url: http://www.khronos.org/opengles/sdk/1.1/docs/man/
     description: ''
     type: resource
---

The **GLKit** framework (`GLKit.framework`) contains a set of Objective-C based utility classes that simplify the effort required to create an OpenGL ES app. GLKit supports four key areas of app development:

* The `GLKView` and `GLKViewController` classes provide a standard implementation of an OpenGL ES–enabled view and associated rendering loop. The view manages the underlying framebuffer object on behalf of the app; your app just draws to it.
* The `GLKTextureLoader` class provides image conversion and loading routines to your app, allowing it to automatically load texture images into your context. It can load textures synchronously or asynchronously. When loading textures asynchronously, your app provides a completion handler block to be called when the texture is loaded into your context.
* The GLKit framework provides implementations of vectors, matrices, and quaternions, as well as a matrix stack operation that provides the same functionality found in OpenGL ES 1.1.
* The `GLKBaseEffect`, `GLKSkyboxEffect`, and `GLKReflectionMapEffect` classes provide existing, configurable graphics shaders that implement commonly used graphics operations. In particular, the `GLKBaseEffect` class implements the lighting and material model found in the [OpenGL ES 1.1 specification](http://www.khronos.org/opengles/sdk/1.1/docs/man/), simplifying the effort required to migrate an app from OpenGL ES 1.1 to later versions of OpenGL ES.
