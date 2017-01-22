---
layout: kit
name: 'Generic Security Services (GSS)'
shortName: GSS
iid: gss
status:
type: kit
since: iOS5
prefixe: 'gss'
abstract: "Provides a standard set of security-related services."
detailedUpdates__:
 - update:
     ios: iOS8
     brief: "..."
icon___: /resources/images/kits/CoreAnimation/graphics_coreanimation.png
kits__:
 - Foo
links__:
 - link:
     name: 'Core Image Programming Guide'
     url: https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/CoreImaging/ci_intro/ci_intro.html
     description: ' - Apple Developer'
     type: reference
---

The *Generic Security Services* framework (`GSS.framework`) provides a standard set of security-related services to iOS apps. The basic interfaces of this framework are specified in IETF [RFC 2743](http://www.ietf.org/rfc/rfc2743.txt) and [RFC 4401](http://tools.ietf.org/html/rfc4401). In addition to offering the standard interfaces, iOS includes some additions for managing credentials that are not specified by the standard but that are required by many apps.

