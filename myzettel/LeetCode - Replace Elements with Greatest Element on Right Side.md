---
template: note
aliases: [Replace Elements with Greatest Element on Right Side]
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1482938289607-e9573fc25ebb?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODIwNTIy&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-18) | (time:: 16:32) | (weather:: Vadodara: 🌧   +31°C ↗32km/h)

# [Replace Elements with Greatest Element on Right Side](https://leetcode.com/problems/replace-elements-with-greatest-element-on-right-side/)

Given an array `arr`, replace every element in that array with the greatest element among the elements to its right, and replace the last element with `-1`.

After doing so, return the array.

## Solution
```javascript
/**
 * @param {number[]} arr
 * @return {number[]}
 */
var replaceElements = function(arr) {
    // Logic:
    // 1) DECLARE: a variable `lastMax` that holds the greatest number
    //      found during the iteration. Set initial value to -1 as
    //      it is expected.
    // 2) LOOP: Start from the end of the array.
    //      2.1) Temp store current node's value - `curr`.
    //      2.2) Update the current node's value to `lastMax`.
    //      2.3) IF `curr` > `lastMax` then set `lastMax` to `curr`.
    // 3) RETURN: the updated `arr`.
    
    let lastMax = -1;
    
    for (let i = arr.length - 1; i >= 0; i--) {
        let curr = arr[i];
        
        arr[i] = lastMax;
        
        if(curr > lastMax) {
            lastMax = curr;
        }
    }
    
    return arr;
};
```

---
#### Internal Links
[[2022-08-18]], [[MOC/LeetCode]], [[Arrays]] 