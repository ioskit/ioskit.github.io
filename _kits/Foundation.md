---
layout: kit
name: 'Foundation'
iid: foundation
status: TODO
type: kit
since: iOS2
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Foundation framework (Foundation.framework) includes many enhancements: see page content."
 - update:
     ios: iOS8
     brief: "The Foundation framework (Foundation.framework) includes the following enhancements: 1) The NSFileVersion class provides access to past versions of iCloud documents. These versions are stored in iCloud, but can be downloaded on request. 2) The NSURL class supports storing document thumbnails as metadata. 3) The NSMetadataQuery class can search for external iCloud documents that your app has opened."
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'NS'
abstract: "Contains interfaces for managing strings, collections, and other low-level data types."
kits:
 - CoreFoundation
links__:
 - link:
     name: 'aaa'
     url: bbb
     description: 'ccc'
---

Contains interfaces for managing strings, collections, and other low-level data types. See Foundation Framework.


### iOS 7

The Foundation framework (Foundation.framework) includes the following enhancements:

* The NSData class adds support for Base64 encoding.
* The NSURLSession class is a new class for managing the acquisition of network-based resources. (You can use it to download content even when your app is suspended or not running.) This class serves as a replacement for the NSURLConnection class and its delegate; it also replaces the NSURLDownload class and its delegate.
* The NSURLComponents class is a new class for parsing the components of a URL. This class supports the URI standard (rfc3986/STD66) for parsing URLs.
* The NSNetService and NSNetServiceBrowser classes support peer-to-peer discovery over Bluetooth and Wi-Fi.
* The NSURLCredential and NSURLCredentialStorage classes let you create credentials with a synchronizable policy, and they provide the option of removing credentials with a synchronizable policy from iCloud.
* The NSURLCache, NSURLCredentialStorage, and NSHTTPCookieStorage classes now support the asynchronous processing of storage requests.
* The NSCalendar class supports new calendar types.
* The NSProgress class provides a general-purpose way to monitor the progress of an operation and report that progress to other parts of your app that want to use it.
