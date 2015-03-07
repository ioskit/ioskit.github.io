---
layout: kit
name: 'PassKit - Passbook'
id: passkit
status:
type: kit
since: iOS6
updates: iOS7
icon: /resources/images/kits/Passbook/passbook.png
prefixe: 'PK'
abstract: "Contains interfaces for creating digital passes to replace things like tickets, boarding passes, member cards, and more."
kits:
 - ApplePay
links:
 - link:
     name: 'Passbook Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/PassKit_PG/Chapters/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Passbook for Developers'
     url: https://developer.apple.com/passbook/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Beginning Passbook in iOS 6'
     url: http://www.raywenderlich.com/tag/passbook
     description: ' - Ray Wenderlich'
     type: tutorial
---

The Passbook app provides users with a place to store coupons, boarding passes, event tickets, and discount cards for businesses. Instead of carrying a physical representation of these items, users can now store them on their iOS device and use them the same way as before. The **PassKit** framework (`PassKit.framework`) provides the Objective-C interfaces you need to integrate support for these items into your apps. You use this framework in combination with web interfaces and file format information to create and manage the passes your company offers.

Passes are created by your company’s web service and delivered to the user’s device via email, Safari, or your custom app. The pass itself, using a special file format, is cryptographically signed before being delivered. The file format identifies relevant information about the service being offered so that the user knows what the service is for. It might also contain a bar code or other information that you can then use to validate the card so that it can be redeemed or used.
