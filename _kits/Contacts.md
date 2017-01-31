---
layout: kit
iid: Contacts 
name: 'Contacts'
status: iOS10
since: iOS9
abstract: "Provides modern object-oriented replacements for the Address Book and Address Book UI frameworks."
icon: /resources/images/kits/Contacts/swift-2-contacts-framework.png
language: swift,objectivec
type_: technology
xcode_: xcode6
deprecated_: Contacts
prefixe_: ''
kits:
 - ContactsUI
 - AddressBook
links:
 - link:
     name: 'Contacts'
     url: https://developer.apple.com/reference/contacts
     description: ' - Apple Developer'
     type: reference
---

[iOS 9](/iOS9) introduces the **Contacts** and [Contacts UI](/ContactsUI) frameworks (`Contacts.framework` and `ContactsUI.framework`), 
which provide modern object-oriented replacements for the [Address Book](/AddressBook) and [Address Book UI](/AddressBookUI) frameworks.

The Contacts framework provides [Swift](/Swift) and [Objective-C](/ObjectiveC) API to access the user’s contact information. Because most apps 
read contact information without making any changes, this framework is optimized for thread-safe, read-only usage.
