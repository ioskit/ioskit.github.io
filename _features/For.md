---
layout: feature
name: 'For'
iid: For
status: DOING
language: swift,objectivec
abstract: "Use for-in, for, while, and do-while to make loops."
links:
 - link:
    name: 'The Swift Programming Language: Control Flow'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID120
    description: ' - Apple Developer'
    type: reference
features:
 - While
 - Range
---

TODO.

# Swift

## For-in

This loop instruction can be used with [Range](/Range) structure:

{% highlight swift linenos %}
for index in 1...5 {
    println("\(index) times 5 is \(index * 5)")
}
{% endhighlight %}

<pre><code>let base = 3
let power = 10
var answer = 1
for _ in 1...power {
    answer *= base
}
println("\(base) to the power of \(power) is \(answer)")
</code></pre>


<pre><code>let numberOfLegs = ["spider": 8, "ant": 6, "cat": 4]
for (animalName, legCount) in numberOfLegs {
    println("\(animalName)s have \(legCount) legs")
}
// ants have 6 legs
// cats have 4 legs
// spiders have 8 legs
</code></pre>

<pre><code>for character in "Hello" {
    println(character)
}
// H
// e
// l
// l
// o
</code></pre>

## For

<pre><code>for var index = 0; index < 3; ++index {
    println("index is \(index)")
}
</code></pre>
