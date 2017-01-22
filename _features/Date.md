---
layout: feature
name: 'Date'
iid: Date
status: DOING
language: swift
abstract: ""
links:
 - link:
    name: 'Swiftly getting a human-readable date with NSDateFormatter'
    url: http://www.codingexplorer.com/swiftly-getting-human-readable-date-nsdateformatter/
    description: ' - Coding Explorer Blog'
    type: tutorial
features_:
 - Variable
---

TODO.

##Create stringFromDate

<pre><code>let dateFormatter = NSDateFormatter()
dateFormatter.dateFormat = "yyyy-MM-dd 'at' h:mm a" // superset of OP's format
let str = dateFormatter.stringFromDate(NSDate())
</code></pre>
