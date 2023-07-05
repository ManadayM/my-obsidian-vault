---
template: note
aliases: []
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1455156218388-5e61b526818b?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMTc3MjUx&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-22) | (time:: 19:37) | (weather:: Vadodara: ⛅️  +27°C →14km/h)

# [Third Maximum Number](https://leetcode.com/problems/third-maximum-number/)
Given an integer array `nums`, return _the **third distinct maximum** number in this array. If the third maximum does not exist, return the **maximum** number_.

**Example 1:**

**Input:** nums = [3,2,1]
**Output:** 1
**Explanation:**
The first distinct maximum is 3.
The second distinct maximum is 2.
The third distinct maximum is 1.

**Example 2:**

**Input:** nums = [1,2]
**Output:** 2
**Explanation:**
The first distinct maximum is 2.
The second distinct maximum is 1.
The third distinct maximum does not exist, so the maximum (2) is returned instead.

**Example 3:**

**Input:** nums = [2,2,3,1]
**Output:** 1
**Explanation:**
The first distinct maximum is 3.
The second distinct maximum is 2 (both 2's are counted together since they have the same value).
The third distinct maximum is 1.

**Constraints:**
-   `1 <= nums.length <= 104`
-   `-231 <= nums[i] <= 231 - 1`

**Follow up:** Can you find an `O(n)` solution?

## Solution - 1
```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var thirdMax = function(nums) {
    let max = -Infinity;
    let secondMax = -Infinity;
    let thirdMax = -Infinity;
    
    for (let i = 0; i < nums.length; i++) {
        let curr = nums[i];
        
        if (max === curr || secondMax === curr || thirdMax === curr) {
            continue;
        }
        
        if (curr > max) {
            thirdMax = secondMax;
            secondMax = max;
            max = curr;
        }
        else if (curr > secondMax) {
            thirdMax = secondMax;
            secondMax = curr;
        }
        else if (curr > thirdMax) {
            thirdMax = curr;
        }
        // console.log(`curr: ${curr} => max: ${max}, max2: ${secondMax}, max3: ${thirdMax}`);
    }
    
    return thirdMax > -Infinity ? thirdMax : max;
};
```

## Solution - 2
```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var thirdMax = function(nums) {
    let max = -Infinity;
    let secondMax = -Infinity;
    let thirdMax = -Infinity;
    
    for (let i = 0; i < nums.length; i++) {
        let curr = nums[i];
        if (max === curr || secondMax === curr || thirdMax === curr) {
            continue;
        }
        
        thirdMax = Math.min(Math.max(curr, thirdMax), secondMax);
        secondMax = Math.min(Math.max(curr, secondMax), max);
        max = Math.max(curr, max);
        
        // let _max = max;
        // let _secondMax = secondMax;
        
        // max = Math.max(curr, max);
        // secondMax = Math.min(Math.max(curr, secondMax), _max);
        // thirdMax = Math.min(Math.max(curr, thirdMax), _secondMax);
        console.log(`curr: ${curr} => max: ${max}, max2: ${secondMax}, max3: ${thirdMax}`);
    }
    
    return thirdMax > -Infinity ? thirdMax : max;
};
```

---
#### Internal Links
[[2022-08-22]]