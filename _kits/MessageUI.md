---
layout: kit
name: 'Message UI'
iid: messageui
status:
type: kit
since: iOS3
detailedUpdates:
 - update:
     ios: iOS7
     brief: "In the Message UI framework, the MFMessageComposeViewController class adds support for attaching files to messages."
prefixe: 'MF'
icon: /resources/images/kits/Messages/icon_messages_large.png
abstract: "Contains interfaces for composing and queuing email messages."
kits:
 - Messages
links:
 - link:
     name: 'Message UI Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/MessageUI/Reference/MessageUI_Framework_Reference/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'System Messaging Programming Topics for iOS'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/SystemMessaging_TopicsForIOS/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
---

The *Message UI* framework (`MessageUI.framework`) provides support for composing email or SMS messages from your app. The composition support consists of a view controller interface that you present in your app. You can populate the fields of this view controller to set the recipients, subject, body content, and any attachments you want to include with the message. After presenting the view controller, the user then has the option of editing the message before sending it.

