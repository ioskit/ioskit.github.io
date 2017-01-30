---
layout: kit
iid: addressbookui
name: 'AddressBookUI'
status: iOS8
since: iOS2
deprecated: ContactsUI
prefixe_: 'AB'
abstract: "Contains classes for displaying the system-defined people picker and editor interfaces."
kits:
 - ContactsUI
 - AddressBook
links:
 - link:
     name: 'Address Book Programming Guide for iOS'
     url: https://developer.apple.com/library/ios/documentation/ContactData/Conceptual/AddressBookProgrammingGuideforiPhone/Introduction.html#//apple_ref/doc/uid/TP40007744
     description: ' - Apple Developer'
     type: reference
---

<div class="alert alert-warning" role="alert">
    <u><a href="/iOS9">iOS 9</a></u> introduces the <u><a href="/Contacts">Contacts</a></u> and <u><a href="/ContactsUI">Contacts UI</a></u> 
    frameworks (<code>Contacts.framework</code> and <code>ContactsUI.framework</code>), which provide modern object-oriented replacements for the 
    <u><a href="/AddressBook">Address Book</a></u> and <b>Address Book UI</b> frameworks.
</div>

The *Address Book UI* framework (`AddressBookUI.framework`) is an Objective-C programming interface that you use to display standard system interfaces for creating new contacts and for editing and selecting existing contacts. This framework simplifies the work needed to display contact information in your app and also makes sure that your app uses the same interfaces as other apps, thus ensuring consistency across the platform.

For more information about the classes of the Address Book UI framework and how to use them, see Address Book Programming Guide for iOS and Address Book UI Framework Reference for iOS.

