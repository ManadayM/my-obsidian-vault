---
template: note
aliases: []
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1471815497777-a3cec075d826?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxNDQ4OTQw&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-25) | (time:: 23:05) | (weather:: Vadodara: 🌦   +29°C ↑16km/h)

# [Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)
Given an integer array `nums` sorted in **non-decreasing** order, return _an array of **the squares of each number** sorted in non-decreasing order_.

**Example 1:**

**Input:** nums = [-4,-1,0,3,10]
**Output:** [0,1,9,16,100]
**Explanation:** After squaring, the array becomes [16,1,0,9,100].
After sorting, it becomes [0,1,9,16,100].

**Example 2:**

**Input:** nums = [-7,-3,2,3,11]
**Output:** [4,9,9,49,121]

**Constraints:**
-   `1 <= nums.length <= 104`
-   `-104 <= nums[i] <= 104`
-   `nums` is sorted in **non-decreasing** order.

**Follow up:** Squaring each element and sorting the new array is very trivial, could you find an `O(n)` solution using a different approach?

## Solution
```typescript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var sortedSquares = function(nums) {
    let leftPointer = 0;
    let rightPointer = nums.length - 1;
    let squareNums = new Array(nums.length);
	
    for (let i = nums.length - 1; i >= 0; i--) {
        let leftAbs = Math.abs(nums[leftPointer]);
        let rightAbs = Math.abs(nums[rightPointer]);
		
        if(leftAbs > rightAbs) {
            squareNums[i] = leftAbs * leftAbs;
            leftPointer++;
        }
        else {
            squareNums[i] = rightAbs * rightAbs;
            rightPointer--;
        }
    }
	
    return squareNums;
};
```

---
#### Internal Links
[[2022-08-25]], [[LeetCode]], [[Arrays]], [[Two-Pointer Technique]]