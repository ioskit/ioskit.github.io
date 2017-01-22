---
layout: kit
name: 'NewsstandKit'
iid: newsstandkit
status:
type: kit
since: iOS5
icon: /resources/images/kits/Newsstand/newsstand.png
prefixe: 'NK'
abstract: "Provides interfaces for downloading magazine and newspaper content in the background."
kits__:
 - Foo
links:
 - link:
     name: 'Newsstand for Developers'
     url: https://developer.apple.com/newsstand/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'NewsstandKit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/StoreKit/Reference/NewsstandKit_Framework/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Local and Remote Notification Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Introduction.html
     description: ' - Apple Developer'
     type: reference
---

The Newsstand app provides a central place for users to read magazines and newspapers. Publishers who want to deliver their magazine and newspaper content through Newsstand can create their own iOS apps using the *NewsstandKit* framework (`NewsstandKit.framework`), which lets you initiate background downloads of new magazine and newspaper issues. After you start a download, the system handles the download operation and notifies your app when the new content is available.
