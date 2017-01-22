---
layout: kit
iid: social
name: 'Social'
status:
type: kit
since: iOS6
icon__: /resources/images/kits/CoreAudio/core-audio.png
abstract: "Contains interfaces for interacting with social media accounts."
kits:
 - Twitter
links:
 - link:
     name: 'Social Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Social/Reference/Social_Framework/index.html
     description: ' - Apple Developer'
     type: reference
---

The *Social framework* (`Social.framework`) provides a simple interface for accessing the user’s social media accounts. This framework:

* supplants the [Twitter](/Twitter) framework (`TWTweetComposeViewController`) that was introduced in [iOS5](/iOS5) 
* and adds support for other social accounts, including Facebook 
* and Sina’s Weibo service. 

Apps can use this framework to post status updates and images to a user’s account. This framework works with the Accounts framework to provide a single sign-on model for the user and to ensure that access to the user’s account is approved.

* Available with [iOS6](/iOS6) and OS X
* We can share: text, image, video and files
* Benefits of this built-in API:
  * Provide a consistent user experience
  * Use of single sign-on
  * Facilitate the use
