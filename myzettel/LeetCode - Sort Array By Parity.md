---
template: note
aliases: [Sort Array By Parity]
source: https://leetcode.com/problems/sort-array-by-parity/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1470043201067-764120126eb4?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMDIwODQ0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-21) | (time:: 00:10) | (weather:: Vadodara: ☁️   +28°C ↗15km/h)

# [Sort Array By Parity](https://leetcode.com/problems/sort-array-by-parity/)
Given an integer array `nums`, move all the even integers at the beginning of the array followed by all the odd integers.

Return _**any array** that satisfies this condition_.

**Example 1:**
**Input:** nums = [3,1,2,4]
**Output:** [2,4,3,1]
**Explanation:** The outputs [4,2,3,1], [2,4,1,3], and [4,2,1,3] would also be accepted.

**Example 2:**
**Input:** nums = [0]
**Output:** [0]

## Solution
```javascript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var sortArrayByParity = function(nums) {
    
    let snowball = 0;
    
    for (let i = 0; i < nums.length; i++) {
			
        if (nums[i] % 2 !== 0) {
            snowball++;
        }
        else if (snowball > 0) {
            let oddNum = nums[i - snowball];
            nums[i - snowball] = nums[i];
            nums[i] = oddNum;
        }
    }
    
    return nums;
};
```

---
#### Internal Links
[[2022-08-21]], [[MOC/LeetCode]], [[Arrays]], [[Snowball Technique]] 