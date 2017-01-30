---
layout: kit
iid: addressbook 
name: 'Address Book'
status: iOS8
since: iOS2
deprecated: Contacts
abstract: "The Address Book technology for iOS provides a way to store people’s contact information and other personal information in a centralized database, and to share this information between applications."
kits:
 - Contacts
 - AddressBookUI
links:
 - link:
     name: 'Address Book Programming Guide for iOS'
     url: https://developer.apple.com/library/ios/documentation/ContactData/Conceptual/AddressBookProgrammingGuideforiPhone/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Address Book Framework'
     url: https://developer.apple.com/library/ios/documentation/Miscellaneous/Conceptual/iPhoneOSTechOverview/CoreServicesLayer/CoreServicesLayer.html#//apple_ref/doc/uid/TP40007898-CH10-SW13
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Address Book Tutorial in iOS (Ray Wenderlich)'
     url: https://developer.apple.com/library/ios/documentation/ContactData/Conceptual/AddressBookProgrammingGuideforiPhone/Introduction.html
     description: ' - Ray Wenderlich'
     type: tutorial
---

<div class="alert alert-warning" role="alert">
    <u><a href="/iOS9">iOS 9</a></u> introduces the <u><a href="/Contacts">Contacts</a></u> and <u><a href="/ContactsUI">Contacts UI</a></u> 
    frameworks (<code>Contacts.framework</code> and <code>ContactsUI.framework</code>), which provide modern object-oriented replacements for the 
    <b>Address Book</b>  and <u><a href="/AddressBookUI">Address Book UI</a></u> frameworks.
</div>

* The **Address Book** framework provides access to the contact information.
* The **Address Book UI** framework provides the user interface to display the information.
* The **Address Book** database stores the information.
* The **Contacts** application provides a way for users to access their contact information.

[iOS 9](/iOS9) introduces the [Contacts](/Contacts) and [Contacts UI](/ContactsUI) frameworks (`Contacts.framework` and `ContactsUI.framework`), 
which provide modern object-oriented replacements for the **Address Book** and [Address Book UI](/AddressBookUI) frameworks.