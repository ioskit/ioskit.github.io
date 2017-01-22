---
layout: kit
name: 'Accounts'
iid: accounts
status: 
since: iOS5
prefixe: 'AC'
link: https://developer.apple.com/library/ios/documentation/ContactData/Conceptual/AddressBookProgrammingGuideforiPhone/Introduction.html
abstract: "Contains interfaces for managing access to a user’s system accounts."
links:
 - link:
     name: 'Address Book Programming Guide for iOS'
     url: https://developer.apple.com/library/ios/documentation/ContactData/Conceptual/AddressBookProgrammingGuideforiPhone/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Address Book Framework Reference for iOS'
     url: https://developer.apple.com/library/ios/documentation/AddressBook/Reference/AddressBook_iPhoneOS_Framework/index.html
     was: https://developer.apple.com/library/ios/documentation/AddressBook/Reference/AddressBook_iPhoneOS_Framework/_index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Address Book Tutorial in iOS'
     url: http://www.raywenderlich.com/63885/address-book-tutorial-in-ios
     description: ' - Ray Wenderlich'
     type: tutorial
---

The *Address Book framework* (`AddressBook.framework`) provides programmatic access to a user’s contacts database. If your app uses contact information, you can use this framework to access and modify that information. 

For example, a chat program might use this framework to retrieve the list of possible contacts with which to initiate a chat session and display those contacts in a custom view.

**Important**: Access to a user’s contacts data requires explicit permission from the user. Apps must therefore be prepared for the user to deny that access. Apps are also encouraged to provide `Info.plist` keys describing the reason for needing access.
