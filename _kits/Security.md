---
layout: kit
iid: security
name: 'Security'
since: iOS2
status: TODO
links:
 - link:
     name: 'Security Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Security/Reference/SecurityFrameworkReference/index.html
     was: https://developer.apple.com/library/ios/documentation/Security/Reference/SecurityFrameworkReference/_index.html
     description: ' - Apple Developer'
     type: reference
abstract: "In addition to its built-in security features, iOS also provides an explicit Security framework (Security.framework) that you can use to guarantee the security of the data your app manages. This framework provides interfaces for managing certificates, public and private keys, and trust policies. It supports the generation of cryptographically secure pseudorandom numbers. It also supports the storage of certificates and cryptographic keys in the keychain, which is a secure repository for sensitive user data."
---

In addition to its built-in security features, iOS also provides an explicit Security framework (Security.framework) that you can use to guarantee the security of the data your app manages. This framework provides interfaces for managing certificates, public and private keys, and trust policies. It supports the generation of cryptographically secure pseudorandom numbers. It also supports the storage of certificates and cryptographic keys in the keychain, which is a secure repository for sensitive user data.

The Common Crypto library provides additional support for symmetric encryption, hash-based message authentication codes (HMACs), and digests. The digests feature provides functions that are essentially compatible with those in the OpenSSL library, which is not available in iOS.

It is possible for you to share keychain items among multiple apps that you create. Sharing items makes it easier for apps in the same suite to interoperate smoothly. For example, you could use this feature to share user passwords or other elements that might otherwise require you to prompt the user from each app separately. To share data between apps, you must configure the Xcode project of each app with the proper entitlements.

* For information about the functions and features associated with the Security framework, see [Security Framework Reference](https://developer.apple.com/library/ios/documentation/Security/Reference/SecurityFrameworkReference/index.html) ([PDF](https://developer.apple.com/library/ios/documentation/Security/Reference/SecurityFrameworkReference/SecurityFrameworkReference.pdf)). 
* For information about how to access the keychain, see [Keychain Services Programming Guide](https://developer.apple.com/library/ios/documentation/Security/Conceptual/keychainServConcepts/01introduction/introduction.html#//apple_ref/doc/uid/TP30000897). 
* For information about setting up entitlements in your Xcode projects, see [Adding Capabilities](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html#//apple_ref/doc/uid/TP40012582-CH26) in [App Distribution Guide](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40012582). 
* For information about the entitlements you can configure, see the description for the [SecItemAdd](https://developer.apple.com/library/ios/documentation/Security/Reference/keychainservices/index.html#//apple_ref/c/func/SecItemAdd) function in [Keychain Services Reference](https://developer.apple.com/library/ios/documentation/Security/Reference/keychainservices/index.html#//apple_ref/doc/uid/TP30000898).
