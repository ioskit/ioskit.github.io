---
layout: kit
name: 'Photos'
iid: photos
status: 
type: kit
since: iOS8
prefixe: 'PH'
icon: /resources/images/kits/Photos/photokit-icon_2x.png
abstract: "Contains interfaces for accessing and manipulating photo and videos."
kits:
 - PhotosUI
 - AssetsLibrary
links:
 - link:
     name: 'Photos Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Photos/Reference/Photos_Framework/index.html#//apple_ref/doc/uid/TP40014408
     description: ' - Apple Developer'
---

The *PhotoKit* or *Photos* framework (`Photos.framework`) provides new APIs for working with photo and video assets, including iCloud Photos assets, that are managed by the Photos app. This framework is a more capable alternative to the [AssetsLibrary](/AssetsLibrary) framework. Key features include a thread-safe architecture for fetching and caching thumbnails and full-sized assets, requesting changes to assets, observing changes made by other apps, and resumable editing of asset content.

