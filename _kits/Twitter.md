---
layout: kit
name: 'Twitter'
iid: twitter
status: 
deprecated: Social
type: kit
since: iOS5
detailedUpdates__:
 - update:
     ios: iOS8
     brief: "..."
icon__: /resources/images/kits/CoreAudio/core-audio.png
prefixe: 'TW'
abstract: "Contains interfaces for sending tweets via the Twitter service."
kits:
 - Social
 - Accounts
links:
 - link:
     name: 'Twitter Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Twitter/Reference/TwitterFrameworkReference/index.html
     description: ' - Apple Developer'
     type: reference
---

The *Twitter* framework (`Twitter.framework`) has been replaced by the [Social](/Social) framework, which supports a UI for generating tweets and support for creating URLs to access the Twitter service.

The Twitter framework provided support for sending Twitter requests on behalf of the user and for composing and sending tweets. For requests, the framework handled the user authentication part of the request for you and provided a template for creating the HTTP portion of the request. (Refer to the Twitter API for populating the content of the request.) The composition of tweets is accomplished using the `TWTweetComposeViewController` class, which is a view controller that you post with your proposed tweet content. This class gives the user a chance to edit or modify the tweet before sending it.

Users control whether an app is allowed to communicate with Twitter on their behalf using Settings. The Twitter framework also works in conjunction with the [Accounts](/Accounts) framework to access the user’s account.
