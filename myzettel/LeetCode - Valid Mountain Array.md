---
template: note
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1513803302974-44bd99bcf333?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNzMwNDYz&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-17) | (time:: 15:31) | (weather:: Vadodara: 🌦   +29°C ↗37km/h)

# LeetCode - Valid Mountain Array
Given an array of integers `arr`, return _`true` if and only if it is a valid mountain array_.

Recall that arr is a mountain array if and only if:
-   `arr.length >= 3`
-   There exists some `i` with `0 < i < arr.length - 1` such that:
    -   `arr[0] < arr[1] < ... < arr[i - 1] < arr[i]`
    -   `arr[i] > arr[i + 1] > ... > arr[arr.length - 1]`

![](https://assets.leetcode.com/uploads/2019/10/20/hint_valid_mountain_array.png)

## Solution
```javascript
/**
 * @param {number[]} arr
 * @return {boolean}
 */
var validMountainArray = function(arr) {
    
    if (arr.length < 3) {
        return false;
    }
    
    let isClimbing = true;
    
    for (let i = 0; i < arr.length; i++) {
        let prev = arr[i - 1];
        let curr = arr[i];
        let next = arr[i + 1];
        
        // When all elements are in decreasing order
        // E.g. [9,8,7,6,5,4,3,2,1,0]
        if (i === 1 && curr < prev) {
            return false;
        }
                
        // Two adjacent elements should not be same
        // Return if we find such a pair anywhere.
        if(prev === curr) {
            return false;
        }
        
        // Mark a beginning of the downward slope.
        if (isClimbing && curr < prev) {
            isClimbing = false;
        }
        
        // Downward slope...
        // Now, next element must be smaller than current element.
        if (!isClimbing && curr < next) {
            return false;
        }
    }
    
    // By this point, isClimbing must be false for valid mountain array.
    // For example, for [0,3,4,5] it keeps increasing so at the end of loop
    // isClimbing will still be `true`. Since, mountain array can only be formed
    // when it goes up on left and goes down on the right.
    return !isClimbing;
};
```

---
#### Internal Links
[[2022-08-17]], [[MOC/LeetCode]], [[Arrays]] 