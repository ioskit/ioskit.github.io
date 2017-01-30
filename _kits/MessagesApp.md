---
layout: kit
iid: MessagesApp
name: 'Integrating with the Messages App'
shortName: 'Messages App'
abstract: "In iOS 10, you can create app extensions that interact with the Messages app and let users send text, stickers, media files, and interactive messages, including interactive messages that update as each recipient responds to the message."
language_: swift
type: technology
xcode_: xcode6
status: iOS10
since: iOS10
icon: /resources/images/kits/Messages/icon_messages_large.png
prefixe_: ''
kits:
 - Messages
 - AppExtensions
links_:
 - link:
     name: 'SiriKit Programming Guide'
     url: https://developer.apple.com/library/content/documentation/Intents/Conceptual/SiriIntegrationGuide/index.html#//apple_ref/doc/uid/TP40016875
     description: ' - Apple Developer'
     type: reference
detailedUpdates_:
 - update:
     ios: iOS9
     brief: "The AVKit framework (AVKit.framework) includes the AVPictureInPictureController and AVPlayerViewController classes, 
     which help you participate in Picture in Picture. For more information about Picture in Picture, see 'Multitasking Enhancements for iPad'."
---

In [iOS 10](/iOS10), you can create [App Extensions](/AppExtensions) that interact with the Messages app and let users send text, stickers, 
media files, and interactive messages, including interactive messages that update as each recipient responds to the message. You can also make 
your publicly accessible images available to the #images app in Messages.

You can create two types of [App Extensions](/AppExtensions):

* A Sticker pack provides a set of stickers that users can add to their Messages content.
* An iMessage app lets you present a custom user interface within the Messages app, create a sticker browser, include text, stickers, and media 
files within a conversation, and create, send, and update interactive messages.
* An iMessage app can also help users search images that you host on your app’s related website while they’re in the Messages app.

You can create a Sticker pack without writing any code: Simply drag images into the Sticker Pack folder inside the Stickers asset catalog in Xcode.

To develop an iMessage app, you use the APIs in the [Messages](/Messages) framework (`Messages.framework`). To learn about the [Messages](/Messages) 
framework, see [Messages Framework Reference](https://developer.apple.com/reference/messages). For general information about creating app extensions, 
see [App Extension Programming Guide](https://developer.apple.com/library/content/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214).

The #images app in Messages shows people popular images from public websites. Your publicly accessible images can be included in #images search 
results after Apple's web crawler, known as Applebot, has scanned your website. To make your public images available in #images, follow these steps:

* Implement an iMessage app.
* Add the `com.apple.developer.associated-domains` key to your app’s entitlements. Include a list of the web domains that host the images you 
want to make searchable. For each domain, specify the `spotlight-image-search` service in an entry such as `spotlight-image-search:yourdomain.com`.
* Add an `apple-app-site-association` file to your website. Add a dictionary for the `spotlight-image-search` service and include your app ID, 
which is the team ID or app ID prefix, followed by the bundle ID. You can specify up to 500 paths and patterns that should be included for 
indexing for #images (for some examples of website paths, see the universal links examples in 
[Creating and Uploading the Association File](https://developer.apple.com/library/content/documentation/General/Conceptual/AppSearch/UniversalLinks.html#//apple_ref/doc/uid/TP40016308-CH12-SW4)).
* Allow crawling by Applebot (to learn more, see [About Applebot](https://support.apple.com/en-us/HT204683)).
