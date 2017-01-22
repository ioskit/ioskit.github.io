---
layout: kit
name: 'Game Controller'
iid: gamecontroller
status:
type: kit
icon__: /resources/images/kits/AppExtensions/app-extensions-icon_2x.png
since: iOS7
detailedUpdates:
 - update:
     ios: iOS8
     brief: "The Game Controller framework (GameController.framework) has the following changes: 1) If the controller is attached to a device, you can now receive device motion data directly from the Game Controller framework. 2) If you are working with button inputs and do not care about pressure sensitivity, a new handler can call your game only when the button’s pressed state changes."
prefixe: 'GC'
abstract: "Contains interfaces for communicating with Made-for-iPhone/iPod/iPad (MFi) game-related hardware."
kits:
 - SpriteKit
links:
 - link:
     name: 'Game Controller Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/ServicesDiscovery/Conceptual/GameControllerPG/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Game Controller Framework Reference'
     url: https://developer.apple.com/library/prerelease/ios/documentation/GameController/Reference/GameController_RefColl/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'iOS 7 Game Controller Tutorial'
     url: http://www.raywenderlich.com/66532/ios-7-game-controller-tutorial
     description: ' - Ray Wenderlich'
     type: tutorial
---

The *Game Controller* framework (`GameController.framework`) lets you discover and configure Made-for-iPhone/iPod/iPad (MFi) game controller hardware in your app. Game controllers can be devices connected physically to an iOS device or connected wirelessly over Bluetooth. The Game Controller framework notifies your app when controllers become available and lets you specify which controller inputs are relevant to your app.

Game controllers provide physical controls to trigger actions in your game. You can rely on a consistent set of high-quality controls in all game controllers because Apple has specified the look and behavior of the controls to MFi accessory manufacturers. By supporting the Game Controller framework in your game, you support all of these game controllers.

