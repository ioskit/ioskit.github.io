---
layout: feature
name: 'Array'
iid: Array
status: DOING
language: swift,objectivec
abstract: "Create arrays and dictionaries using brackets ([]), and access their elements by writing the index or key in brackets."
links:
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features_:
 - Variable
---

# Swift

Create arrays and dictionaries using brackets (`[]`), and access their elements by writing the index or key in brackets.

<pre><code>var shoppingList = ["catfish", "water", "tulips", "blue paint"]
shoppingList[1] = "bottle of water"
 
var occupations = [
    "Malcolm": "Captain",
    "Kaylee": "Mechanic",
]
occupations["Jayne"] = "Public Relations"
</code></pre>

To create an empty array or dictionary, use the initializer syntax.

<pre><code>let emptyArray = [String]()
let emptyDictionary = [String: Float]()
</code></pre>

If type information can be inferred, you can write an empty array as [] and an empty dictionary as [:]—for example, when you set a new value for a variable or pass an argument to a function.

<pre><code>shoppingList = []
occupations = [:]
</code></pre>


# Objective-C

TODO.
