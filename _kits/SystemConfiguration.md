---
layout: kit
name: 'SystemConfiguration'
iid: systemconfiguration
status: 
type: kit
since: iOS2
prefixe: 'SC'
icon__: /resources/images/kits/AppExtensions/app-extensions-icon_2x.png
abstract: "Contains interfaces for determining the network configuration of a device."
kits__:
 - Foo
links:
 - link:
     name: 'System Configuration Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/Networking/Reference/SysConfig/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'Reachability sample code project'
     url: https://developer.apple.com/library/ios/samplecode/Reachability/Introduction/Intro.html#//apple_ref/doc/uid/DTS40007324
     description: ' - For an example of how to use this framework to obtain network information'
     type: sample
detailedUpdates__:
 - update:
     ios: iOS7
     brief: "TODO"
---

The *System Configuration* framework (`SystemConfiguration.framework`) provides the reachability interfaces, which you can use to determine the network configuration of a device. You can use this framework to determine whether a Wi-Fi or cellular connection is in use and whether a particular host server can be accessed.

For more information about the interfaces of this framework, see System Configuration Framework Reference. For an example of how to use this framework to obtain network information, see the Reachability sample code project.

