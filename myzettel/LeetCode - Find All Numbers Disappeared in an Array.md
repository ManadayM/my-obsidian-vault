---
template: note
aliases: [Find All Numbers Disappeared in an Array]
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1501446393885-828292b7670a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMzQ5MTEz&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-24) | (time:: 19:21) | (weather:: Vadodara: 🌦   +29°C ↑19km/h)

# [Find All Numbers Disappeared in an Array](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
Given an array `nums` of `n` integers where `nums[i]` is in the range `[1, n]`, return _an array of all the integers in the range_ `[1, n]` _that do not appear in_ `nums`.

**Example 1:**

**Input:** nums = [4,3,2,7,8,2,3,1]
**Output:** [5,6]

**Example 2:**

**Input:** nums = [1,1]
**Output:** [2]

**Constraints:**
-   `n == nums.length`
-   `1 <= n <= 105`
-   `1 <= nums[i] <= n`

**Follow up:** Could you do it without extra space and in `O(n)` runtime? You may assume the returned list does not count as extra space.

## Solution - 1
The following solution is **not optimal from either time or space complexity**.

```javascript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var findDisappearedNumbers = function(nums) {
    
    let numMap = new Map();
    
    for (let i = 0; i < nums.length; i++) {
        if(!numMap.get(i + 1))
            numMap.set(i + 1, false);
        
        numMap.set(nums[i], true);
    }
    
    let result = [];
    
    for (const [key, value] of numMap) {
        if (value === false) {
            result.push(key);
        }
    }
    
    return result;
};
```

## Solution - 2
Found the following optimal solution. Source [YouTube Video](https://www.youtube.com/watch?v=8i-f24YFWC4).

```javascript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var findDisappearedNumbers = function(nums) {
        
    for (let i = 0; i < nums.length; i++) {
        let index = Math.abs(nums[i]) - 1;
        nums[index] = -1 * Math.abs(nums[index]);
    }
    
    let result = []
    for (let i = 0; i < nums.length; i++) {
        if (nums[i] > 0) {
            result.push(i + 1);
        }
    }
    
    return result;
};
```

---
#### Internal Links
[[2022-08-24]], [[LeetCode]], [[Arrays]] 