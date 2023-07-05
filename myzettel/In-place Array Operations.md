---
template: note
source: https://leetcode.com/explore/learn/card/fun-with-arrays/511/in-place-operations/3257/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1506361797048-46a149213205?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODIyMjM2&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-18) | (time:: 17:00) | (weather:: Vadodara: 🌧   +31°C ↗32km/h)

# [In-place Array Operations](https://leetcode.com/explore/learn/card/fun-with-arrays/511/in-place-operations/3257/)

"In-place array operations" is a technique to perform array operations without creating a copy of the array in question. This way, instead of requiring `O(N)` space, we can reduce it down to `O(1)`.

An important difference between in-place and not in-place is that in-place _modifies the input Array_. This means that other functions *can no longer access the original data* because it has been overwritten.

## When not to use it?
Do not use [[In-place Array Operations|in-place array operations]] in the following circumstances.
1. If we will need the original values again later. In such a case, it's best to create a copy to work with or anything else but in-place operation.
2. If somebody else has written the code and tread carefully. If another code is depending on the original array then an in-place operation will completely break the program.

## Also, check
1. [[LeetCode - Remove Duplicates from Sorted Array]] - In-place Array Operations in action

---
#### Internal Links
[[2022-08-18]], [[Arrays]] 