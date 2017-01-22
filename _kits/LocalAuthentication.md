---
layout: kit
name: 'LocalAuthentication'
iid: localauthentication
status: 
since: iOS8
prefixe: 'LA'
link: 
abstract: "Provides support for authenticating the user via Touch ID."
kits:
 - TouchID
links:
 - link:
     name: 'Local Authentication Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/LocalAuthentication/Reference/LocalAuthentication_Framework/index.html
     description: ''
---

The *Local Authentication Framework* (`LocalAuthentication.framework`) lets you use [Touch ID](/TouchID) to authenticate the user. Some apps may need to secure access to all of their content, while others might need to secure certain pieces of information or options. In either case, you can require the user to authenticate before proceeding. Use this framework to display an alert to the user with an application-specified reason for why the user is authenticating. When your app gets a reply, it can react based on whether the user was able to successfully authenticate.
