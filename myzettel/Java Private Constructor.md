---
template: note
parent: [[Java]]
tags: 
aliases: []
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1515365872443-112d89414bea?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4ODQ5MTE4&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-26) | (time:: 20:55) | (weather:: Vadodara: 🌦   +27°C →9km/h)

# Java Private Contstructor
The following code snippet grabbed my attention from [this page](https://algs4.cs.princeton.edu/11model/Knuth.java.html) from Princeton University.

```java
public class Knuth {
	
	// this class should not be instantiated.
	private class Knuth { }
}

// Source:
// https://algs4.cs.princeton.edu/11model/Knuth.java.html
```

It is a private constructor that restricts object creation in [[Java]].



---
#### Internal Links
[[2022-07-26]], [[Java]]