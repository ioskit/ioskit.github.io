---
layout: kit
name: 'WebKit'
iid: webkit
type: kit
status:
icon:
xcode:
since: iOS8
detailedUpdates__:
 - update:
     ios: iOS8
     brief: "A number of new classes have been added to make it easier to create high-performance native apps that utilize web content."
prefixe: 'WK'
abstract: "Provides support for integrating web content into your apps"
links:
 - link:
     name: 'WebKit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Cocoa/Reference/WebKit/ObjC_classic/index.html
     description: ' - Apple Developer'
 - link:
     name: 'WebKit Objective-C Programming Guide'
     url: https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/DisplayWebContent/DisplayWebContent.html
     description: ' - Apple Developer'
---

Apple has finally replaced `UIWebView`. 

The *WebKit* framework (`WebKit.framework`) lets you display HTML content in your app. In addition to displaying HTML, you can provide basic editing support so that users can replace text and manipulate document text and attributes, including CSS properties. WebKit also supports creating and editing content at the DOM level of an HTML document. For example, you could extract the list of links on a page, modify them, and replace them prior to displaying the document in a web view.

