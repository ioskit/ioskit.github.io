---
layout: kit
name: 'CFNetwork'
iid: cfnetwork
status: 
type: kit
since: iOS2
prefixe: 'CF'
abstract: "Contains interfaces for accessing the network via Wi-Fi and cellular radios."
links:
 - link:
     name: 'CFNetwork Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/Networking/Conceptual/CFNetwork/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'CFNetwork Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/CFNetwork/Reference/CFNetwork_Framework/index.html
     was: https://developer.apple.com/library/ios/documentation/CFNetwork/Reference/CFNetwork_Framework/_index.html
     description: ' - Apple Developer'
     type: reference
---

The *CFNetwork* framework (`CFNetwork.framework`) is a set of high-performance C-based interfaces that use object-oriented abstractions for working with network protocols. These abstractions give you detailed control over the protocol stack and make it easy to use lower-level constructs such as BSD sockets. You can use this framework to simplify tasks such as communicating with FTP and HTTP servers or resolving DNS hosts. With the CFNetwork framework, you can:

* Use BSD sockets
* Create encrypted connections using SSL or TLS
* Resolve DNS hosts
* Work with HTTP servers, authenticating HTTP servers, and HTTPS servers
* Work with FTP servers
* Publish, resolve, and browse Bonjour services

CFNetwork is based, both physically and theoretically, on BSD sockets. 

