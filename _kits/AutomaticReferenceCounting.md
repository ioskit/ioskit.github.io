---
layout: kit
name: 'Automatic Reference Counting (ARC)'
shortName: ARC
id: arc
kind: technology
status: TODO
since: iOS4
xcode: xcode42
prefixe:
abstract: "automates memory management for Objective-C objects."
links:
 - link:
     name: 'Transitioning to ARC Release Notes'
     url: https://developer.apple.com/library/prerelease/ios/releasenotes/ObjectiveC/RN-TransitioningToARC/Introduction/Introduction.html
     description: ' - Apple Developer'
---

*Automatic Reference Counting* (ARC) makes memory management much easier, greatly reducing the chance that your program will have memory leaks. First, Xcode reviews your project to determine whether there are items that cannot be converted (and that you must therefore change manually). Then, Xcode rewrites your source code to use ARC.

