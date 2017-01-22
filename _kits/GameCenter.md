---
layout: kit
name: 'Game Center'
iid: gamecenter
status:
type: technology
icon: /resources/images/kits/GameCenter/game-center.png
since: iOS3
updates: iOS7
prefixe:
abstract: "Enables your users to track their best scores on a leaderboard, compare their achievements, invite friends to play a game, and start a multiplayer game through auto-matching."
kits:
 - GameKit
links:
 - link:
     name: 'Game Center for Developers'
     url: https://developer.apple.com/game-center/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Using Game Center on your Mac or iOS device'
     url: https://support.apple.com/en-us/HT202097
     description: ' - Apple Support'
     type: reference
---

Games on iOS and OS X can take advantage of Game Center, Apple’s social gaming network. Game Center enables your users to track their best scores on a leaderboard, compare their achievements, invite friends to play a game, and start a multiplayer game through auto-matching.

Game Center offers a centralized game service that connects players to each other. Game Center implements many different features:

* **Friends** allow players to create anonymous online personas. Users connect to Game Center and interact with other players through an alias. Players can set status messages as well as mark other players as friends.
* **Multiplayer** allows your game to create network matches that connect players through Game Center. Players can invite their friends or be connected to anonymous players. Most importantly, players can receive invitations to join a match even when your game is not running. Your game is running on each device and the instances of your game exchange match and voice data with each other.
* **Turn-Based Gaming** provides store-and-forward network match infrastructure where the match is played out over a series of discrete turns. This kind of match can be played without requiring all of the players to be connected to Game Center simultaneously.
* **Leaderboards** allow your game to store and fetch player scores from Game Center.
* **Achievements** provide the ability to track a player’s accomplishments in your game.
* **Challenges** allow a player to challenge other players to complete an achievement or to beat a leaderboard score.
