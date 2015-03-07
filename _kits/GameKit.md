---
layout: kit
name: 'GameKit'
id: gamekit
status:
type: kit
icon: /resources/images/kits/GameCenter/game-center.png
since: iOS3
updates: iOS8
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
