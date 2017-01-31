---
layout: kit
iid: ApplePay
name: 'Apple Pay'
status: iOS10
since: iOS8
abstract: "Allows users to use Touch ID to easily and securely pay for physical goods and services such as groceries, clothing, tickets, and reservations in your app."
type: technology
icon: /resources/images/kits/ApplePay/apple-pay_2x.png
kits:
 - TouchID
 - PassKit
 - SiriKit
links:
 - link:
     name: 'Apple Pay'
     url: https://www.apple.com/apple-pay/
     description: ' - Your wallet. Without the wallet.'
     type: reference
 - link:
     name: 'Apple Pay for Developers'
     url: https://developer.apple.com/apple-pay/
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'ApplePay JS Framework Reference'
     url: https://developer.apple.com/reference/applepayjs
     description: ' - Apple Developer'
     type: reference
detailedUpdates:
 - update:
     ios: iOS9
     brief: "The PassKit framework (<code>PassKit.framework</code>) includes several additions that support enhancements in Apple Pay. Specifically:
             <ul><li>In <a href='/iOS9'>iOS 9</a>, Apple Pay supports Discover cards and store debit and credit cards. For more information, 
             see “Payment Networks” in <a href='https://developer.apple.com/reference/passkit/pkpaymentrequest'>PKPaymentRequest Class Reference</a>.</li>
             <li>Card issuers and payment networks can add cards to Apple Pay directly in their apps. For more information, 
             see <a href='https://developer.apple.com/reference/passkit/pkaddpaymentpassviewcontroller'>PKAddPaymentPassViewController Class Reference</a>.</li></ul>"
 - update:
     ios: iOS10
     brief: "<p>In <a href='/iOS10'>iOS 10</a>, users can make easy and secure payments using Apple Pay from websites and through interaction with 
            <a href='/Siri'>Siri</a> and Maps. For developers, <a href='/iOS10'>iOS 10</a> introduces new APIs you can use in code that runs 
            in both iOS and watchOS, the ability to support dynamic payment networks, and a new sandbox testing environment.</p>
             
             <p><a href='/iOS10'>iOS 10</a> introduces new APIs that help you incorporate Apple Pay directly into your website. When you support 
             Apple Pay in your website, users browsing with Safari in iOS or macOS can make payments using their cards in Apple Pay on their 
             iPhone or Apple Watch. To learn more, see <a href='https://developer.apple.com/reference/applepayjs'>ApplePay JS Framework Reference</a>.</p>
             
             <p>The PassKit framework (<code>PassKit.framework</code>) introduces APIs that let you support Apple Pay in places where <a href='/UIKit'>UIKit</a>
             is not available. Specifically, <code>PKPaymentAuthorizationController</code> and <code>PKPaymentAuthorizationControllerDelegate</code> 
             enable features provided by <code>PKPaymentAuthorizationViewController</code> and its delegate, but don’t require <a href='/iOS10'>iOS 10</a>. 
             Although the new API is required for supporting Apple Pay in watchOS and in certain intents, it’s recommended that you adopt it 
             in all of your code so that you can provide broad Apple Pay support with a single code base. (To learn more about intents and Siri 
             integration, see <a href='/SiriKit'>SiriKit</a>.)</p>
             
             <p>The <a href='/PassKit'>PassKit</a> framework also adds features that let card issuers present their cards from within their apps. 
             Specifically, the <code>PKPaymentButtonTypeInStore</code> button type lets you display an Apple Pay button for a card and the 
             <code>presentPaymentPass:</code> method lets you programmatically display the card (the <code>presentPaymentPass:</code> method 
             is defined in <code>PKPassLibrary</code>).</p>
             
             <p>When a new payment network becomes available, your app can automatically support the new network without requiring you to modify 
             and recompile your app. The <code>availableNetworks</code> method lets you discover the networks that are available on the user's 
             device at runtime. In addition, the <code>supportedNetworks</code> property is expanded, so that it can take some payment provider 
             names as an argument. Your app then automatically supports any networks that the payment provider supports.</p>
             
             <p><a href='/iOS10'>iOS 10</a> introduces a new testing environment that lets you provision test cards directly on the device. 
             The test environment returns encrypted test payment data. To use this environment, follow these steps:
             <ol><li>Create a testing iCloud Account at iTunes Connect.</li>
             <li>Log into that account on your device.
             <li>Set the desired region for testing.
             <li>Use test cards listed at <a href='https://developer.apple.com/apple-pay/'>https://developer.apple.com/apple-pay/</a>.</li></ol></p>
             "
---

Allows users to use [TouchID](/TouchID) to easily and securely pay for physical goods and services such as groceries, clothing, tickets, and 
reservations in your app. With a single touch, users can provide your app the payment information, billing and shipping addresses, and contact 
information to make their purchases.

The [PassKit](/PassKit) framework adds support for payment passes and payment requests. Payment requests let users securely provide you with 
their payment and contact information to pay for physical goods and services. Payment passes are added to Passbook by payment networks, 
such as credit card issuers and banks, and let the user select their account on that payment network to fund payments. For more information, 
see [PassKit](/PassKit) Framework Reference.

You can use a new class, `PKPaymentButton`, to create buttons that initiate Apple Pay purchases. These buttons are appropriately styled with 
the Apple Pay logo. 

Apple Pay now supports different shipping types, such as “shipping,” “delivery,” “pickup from store,” and “pickup from customer.” You can also 
now request the user’s name without requesting their address.

For more information on Apple Pay, see [Apple Pay Programming Guide](https://developer.apple.com/library/content/ApplePay_Guide/index.html#//apple_ref/doc/uid/TP40014764); 
to learn more about `PKPaymentButton`, see [PassKit](/PassKit) Framework Reference.
