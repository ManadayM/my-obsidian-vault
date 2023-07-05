---
template: note
aliases: [Remove Duplicates from Sorted Array]
source: https://leetcode.com/problems/remove-duplicates-from-sorted-array/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1534762867727-efa52ebe7f36?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNTczNDk0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-15) | (time:: 19:54) | (weather:: Vadodara: 🌦   +26°C ↑19km/h)

# [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)

## ✍️ Problem
Given an integer array `nums` sorted in **non-decreasing order**, remove the duplicates [**in-place**](https://en.wikipedia.org/wiki/In-place_algorithm) such that each unique element appears only **once**. The **relative order** of the elements should be kept the **same**.

Since it is impossible to change the length of the array in some languages, you must instead have the result be placed in the **first part** of the array `nums`. More formally, if there are `k` elements after removing the duplicates, then the first `k` elements of `nums` should hold the final result. It does not matter what you leave beyond the first `k` elements.

Return `k` _after placing the final result in the first_ `k` _slots of_ `nums`.

Do **not** allocate extra space for another array. You must do this by **modifying the input array [in-place](https://en.wikipedia.org/wiki/In-place_algorithm)** with O(1) extra memory.

## Solution
```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var removeDuplicates = function(nums) {
    
    let writePointer = 1;
    
    for (let readPointer = 1; readPointer < nums.length; readPointer++) {
        
        if (nums[readPointer] !== nums[readPointer - 1]) {
            nums[writePointer] = nums[readPointer];
            writePointer++;
        }   
    }
    
    return writePointer;
};
```

The key thing to notice is that the condition is such that it is _impossible_ for `writePointer` to ever get ahead of the `readPointer`. This means that we would never overwrite a value that we haven't yet read.

---
#### Internal Links
[[2022-08-15]], [[MOC/LeetCode]], [[Arrays]]