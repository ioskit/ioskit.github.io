---
layout: kit
iid: airdrop
name: 'AirDrop'
status: 
type: technology
since: iOS7
icon: /resources/images/kits/AirDrop/AirDrop_Icon.png
abstract: "With AirDrop, you can share photos, videos, websites, locations, and more with people nearby with an Apple device."
kits:
 - MultipeerConnectivity
links:
 - link:
     name: 'AirDrop Examples'
     url: https://developer.apple.com/library/prerelease/ios/samplecode/sc2273/Introduction/Intro.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Share content with AirDrop from your iPhone, iPad, or iPod touch'
     url: https://support.apple.com/en-us/HT204144
     description: ' - Apple Support'
     type: reference
 - link:
     name: 'Mac Basics: AirDrop lets you send files from your Mac to nearby Macs and iOS devices'
     url: https://support.apple.com/en-us/HT203106
     description: ' - Apple Store'
     type: reference
---

AirDrop lets users share photos, documents, URLs, and other kinds of data with nearby devices. AirDrop support is now built in to the existing UIActivityViewController class. This class displays different options for sharing the content that you specify. If you are not yet using this class, you should consider adding it to your interface.

To receive files sent via AirDrop, do the following:

* In Xcode, declare support for the document types your app supports. (Xcode adds the appropriate keys to your app’s Info.plist file.) The system uses this information to determine whether your app can open a given file.
* Implement the application:openURL:sourceApplication:annotation: method in your app delegate. (The system calls this method when a new file is received.)
Files sent to your app are placed in the Documents/Inbox directory of your app’s home directory. If you plan to modify the file, you must move it out of this directory before doing so. (The system allows your app to read and delete files in this directory only.) Files stored in this directory are encrypted using data protection, so you must be prepared for the file to be inaccessible if the device is currently locked.

