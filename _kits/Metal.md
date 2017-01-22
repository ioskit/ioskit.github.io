---
layout: kit
name: 'Metal'
iid: metal
status: 
type: kit
since: iOS8
prefixe: 'MTL'
icon: /resources/images/kits/Metal/metal-icon_2x.png
abstract: "Provides a low-overhead graphics rendering engine for apps."
links:
 - link:
     name: 'Metal Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/Miscellaneous/Conceptual/MetalProgrammingGuide/Introduction/Introduction.html
     description: ''
 - link:
     name: 'Metal Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Metal/Reference/MetalFrameworkReference/index.html
     description: ''
 - link:
     name: 'Metal Shading Language Guide'
     url: https://developer.apple.com/library/ios/documentation/Metal/Reference/MetalShadingLanguageGuide/Introduction/Introduction.html
     description: ''
---

Metal provides extremely low-overhead access to the A7 GPU enabling incredibly high performance for your sophisticated graphics rendering and computational tasks. 

* Metal eliminates many performance bottlenecks—such as costly state validation—that are found in traditional graphics APIs. 
* Metal is explicitly designed to move all expensive state translation and compilation operations out of the critical path of your most performance sensitive rendering code. 
* Metal provides precompiled shaders, state objects, and explicit command scheduling to ensure your application achieves the highest possible performance and efficiency for your GPU graphics and compute tasks. 

This design philosophy extends to the tools used to build your app. When your app is built, Xcode compiles Metal shaders in the project into a default library, eliminating most of the runtime cost of preparing those shaders.

Graphics, compute, and blit commands are designed to be used together seamlessly and efficiently. Metal is specifically designed to exploit modern architectural considerations, such as multiprocessing and shared memory, to make it easy to parallelize the creation of GPU commands.

With Metal, you have a streamlined API, a unified graphics and compute shading language, and Xcode-based tools, so you don’t need to learn multiple frameworks, languages and tools to take full advantage of the GPU in your game or app.
