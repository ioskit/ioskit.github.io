---
layout: kit
name: 'GameKit'
iid: gamekit
status:
type: kit
icon: /resources/images/kits/GameCenter/game-center.png
since: iOS3
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Game Kit framework (GameKit.framework) includes numerous changes: see page content."
 - update:
     ios: iOS8
     brief: "The GameKit framework has many changes: 1) The new GKSavedGame class and new methods in GKLocalPlayer make it easy to save and restore a user’s progress (iCloud). 2) Methods and properties that use player identifier strings are now deprecated. Instead, use GKPlayer objects to identify players. See the page for more details."
prefixe: 'GK'
abstract: "Contains interfaces for managing peer-to-peer connectivity."
kits:
 - GameCenter
links__:
 - link:
     name: 'GameKit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/GameKit/Reference/GameKit_Collection/index.html
     description: 'ccc'
---

Game Kit offers features that you can use to create great social games.

Game Kit provides three separate pieces of functionality:

* [GameCenter](/GameCenter) offers a centralized game service that connects players to each other. Game Center implements many different features: Friends, Multiplayer, Turn-Based Gaming, Leaderboards, Achievements, Challenges.
* **Peer-to-peer connectivity** allows your game to create an ad hoc Bluetooth or wireless network between multiple iPhones in the same local area. Although designed with games in mind, this network is useful for any type of data exchange among users of your app. For example, an app could use peer-to-peer connectivity to share electronic business cards or other data. This functionality is only available on iOS. You can also get the same functionality using Game Center.
* **In-game voice chat** allows your game to provide voice communication between two iPhones. In-game voice relies on your game’s network connection to another user to create its own network connection to transmit voice data. This functionality is only available on iOS. You can also get the same functionality using Game Center.


### iOS 8

The GameKit framework has the following changes:

* Features that were added in iOS 7 are available on OS X 10.10, making it easier to use these features in a cross-platform game.
* The new `GKSavedGame` class and new methods in `GKLocalPlayer` make it easy to save and restore a user’s progress. The data is stored on iCloud; GameKit does the necessary work to synchronize the files between the device and iCloud.
* Methods and properties that use player identifier strings are now deprecated. Instead, use GKPlayer objects to identify players. Replacement properties and methods have been added that take `GKPlayer` objects.


### iOS 7

Game Center includes the following improvements:

* Turn-based matches now support a new feature known as exchanges. Exchanges let players initiate actions with other players, even when it is not their turn. You can use this feature to implement simultaneous turns, player chats, and trading between players.
* The limit on per-app leaderboards has been raised from 25 to 100. You can also organize your leaderboards using a GKLeaderboardSet object, which increases the limit to 500.
* You can add conditions to challenges that define when the challenge has been met. For example, a challenge to beat a time in a driving game might stipulate that other players must use the same vehicle.
* The framework has improved its authentication support and added other features to prevent cheating.
