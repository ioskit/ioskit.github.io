---
layout: kit
name: 'Multipeer Connectivity'
iid: multipeerconnectivity
status:
type: kit
since: iOS7
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'MC'
abstract: "Provides interfaces for implementing peer-to-peer networking between devices."
kits:
 - AirDrop
links:
 - link:
     name: 'Multipeer Connectivity Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/MultipeerConnectivity/Reference/MultipeerConnectivityFramework/index.html
     description: ' - Apple Developer'
---

The *Multipeer Connectivity* framework (`MultipeerConnectivity.framework`) supports the discovery of nearby devices and the direct communication with those devices without requiring Internet connectivity. This framework makes it possible to create multipeer sessions easily and to support reliable in-order data transmission and real-time data transmission. With this framework, your app can communicate with nearby devices and seamlessly exchange data.

The framework provides programmatic and UI-based options for discovering and managing network services. Apps can integrate the `MCBrowserViewController` class into their user interface to display a list of peer devices for the user to choose from. Alternatively, you can use the `MCNearbyServiceBrowser` class to look for and manage peer devices programmatically.
