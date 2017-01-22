---
layout: kit
name: 'CloudKit'
iid: cloudkit
status: 
since: iOS8
prefixe: 'CK'
icon: /resources/images/kits/CloudKit/cloudkit-icon_2x.png
abstract: "Contains Objective-C interfaces for fetching and saving iCloud data."
kits:
 - CoreData
links:
 - link:
    name: 'iCloud for Developers'
    url: https://developer.apple.com/icloud/index.html
    description: ' - iCloud APIs enable your apps to store app data in iCloud, keeping your apps up to date automatically. Use iCloud to give your users a consistent and seamless experience across iCloud-enabled devices.'
 - link:
     name: 'iCloud - CloudKit Storage and Data Transfers'
     url: https://developer.apple.com/icloud/documentation/cloudkit-storage/
     description: ' - Apple Developer'
 - link:
     name: 'CloudKit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CloudKit/Reference/CloudKit_Framework_Reference/index.html
     description: ''
 - link:
     name: 'Beginning CloudKit Tutorial'
     url: http://www.raywenderlich.com/83116/beginning-cloudkit-tutorial
     description: ' - Ray Wenderlich'
---

*CloudKit* (`CloudKit.framework`) provides a conduit for moving data between your app and iCloud. Unlike other iCloud technologies where data transfers happen transparently, CloudKit gives you control over when transfers occur. You can use CloudKit to manage all types of data.

Apps that use CloudKit directly can store data in a repository that is shared by all users. This public repository is tied to the app itself and is available even on devices without a registered iCloud account. As the app developer, you can manage the data in this container directly and see any changes made by users through the CloudKit dashboard.

