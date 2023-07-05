---
template: note
aliases: []
source: https://leetcode.com/problems/contains-duplicate/
summary: "Solved using a hash table."
---
![tp.web.random_picture](https://images.unsplash.com/photo-1578583515301-b9d69416871e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYyMzgwODc4&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-05) | (time:: 17:57) | (weather:: Vadodara: ⛅️  +32°C →14km/h)

# [LeetCode - Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)

## Problem
Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

**Example 1:**
**Input:** nums = [1,2,3,1]
**Output:** true

**Example 2:**
**Input:** nums = [1,2,3,4]
**Output:** false

**Example 3:**
**Input:** nums = [1,1,1,3,3,4,3,2,4,2]
**Output:** true

## Solution
I knew two solutions initially
1. Sort and then just iterate over the array
2. Use a hash table.

Found this [community implementation](https://leetcode.com/problems/contains-duplicate/discuss/60858/Possible-solutions) cleaner than my initial solution.

```javascript
/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
    let numMap = new Map();
    
    for (let i = 0; i < nums.length; i++) {
        if(numMap.get(nums[i])) {
            return true;
        }
        numMap.set(nums[i], true);
    }
    
    return false;
};
```

---
## Internal Links
[[2022-09-05]], [[LeetCode]], [[Arrays]] 