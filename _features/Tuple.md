---
layout: feature
name: 'Tuple'
iid: Tuple
status: DOING
language: swift
abstract: "Tuples group multiple values into a single compound value. The values within a tuple can be of any type and do not have to be of the same type as each other."
links:
 - link:
    name: 'The Swift Programming Language: The Basics, Tuples'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID329
    description: ' - Apple Developer'
    type: reference
features:
- Constant
- Variable
---

TODO.

<pre><code>let http404Error = (404, "Not Found")
</code></pre>

<pre><code>let (justTheStatusCode, _) = http404Error
println("The status code is \(justTheStatusCode)")
</code></pre>
