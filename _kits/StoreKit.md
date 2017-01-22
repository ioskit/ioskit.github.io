---
layout: kit
name: 'StoreKit'
iid: storekit
status:
since: iOS3
type: kit
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Store Kit framework (StoreKit.framework) has migrated to a new receipt system that developers can use to verify in-app purchases on the device itself. You can also use it to verify the app purchase receipt on the server."
prefixe: 'SK'
abstract: "Contains interfaces for handling the financial transactions associated with in-app purchases."
kits:
 - InAppPurchase
links:
 - link:
     name: 'About In-App Purchase'
     url: https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/StoreKitGuide/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'StoreKit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/StoreKit/Reference/StoreKit_Collection/index.html
     description: ' - Apple Developer'
     type: reference
---

The *StoreKit framework* (`StoreKit.framework`) provides support for the purchasing of content and services from within your iOS apps, a feature known as [In-App Purchase](/InAppPurchase). For example, you can use this feature to allow the user to unlock additional app features. Or if you are a game developer, you can use it to offer additional game levels. In both cases, the StoreKit framework handles the financial aspects of the transaction, processing payment requests through the user’s iTunes Store account and providing your app with information about the purchase.

StoreKit focuses on the financial aspects of a transaction, ensuring that transactions occur securely and correctly. Your app handles the other aspects of the transaction, including the presentation of a purchasing interface and the downloading (or unlocking) of the appropriate content. This division of labor gives you control over the user experience for purchasing content. You decide what kind of purchasing interface you want to present to the user and when to do so. You also decide on the delivery mechanism that works best for your app.

