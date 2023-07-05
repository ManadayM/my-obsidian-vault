---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1506953823976-52e1fdc0149a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMTAzOTk2&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-21) | (time:: 23:16) | (weather:: Vadodara: ⛅️  +28°C ↗15km/h)

# [Height Checker](https://leetcode.com/problems/height-checker/)
A school is trying to take an annual photo of all the students. The students are asked to stand in a single file line in **non-decreasing order** by height. Let this ordering be represented by the integer array `expected` where `expected[i]` is the expected height of the `ith` student in line.

You are given an integer array `heights` representing the **current order** that the students are standing in. Each `heights[i]` is the height of the `ith` student in line (**0-indexed**).

Return _the **number of indices** where_ `heights[i] != expected[i]`.

**Example 1:**

**Input:** heights = [1,1,4,2,1,3]
**Output:** 3
**Explanation:** 
heights:  [1,1,4,2,1,3]
expected: [1,1,1,2,3,4]
Indices 2, 4, and 5 do not match.

**Example 2:**

**Input:** heights = [5,1,2,3,4]
**Output:** 5
**Explanation:**
heights:  [5,1,2,3,4]
expected: [1,2,3,4,5]
All indices do not match.

**Example 3:**

**Input:** heights = [1,2,3,4,5]
**Output:** 0
**Explanation:**
heights:  [1,2,3,4,5]
expected: [1,2,3,4,5]
All indices match.

**Constraints:**
-   `1 <= heights.length <= 100`
-   `1 <= heights[i] <= 100`

## Solution
```javascript
/**
 * @param {number[]} heights
 * @return {number}
 */
var heightChecker = function(heights) {
    let sortedHeights = [...heights].sort((a, b) => a - b);
    
    let notExpectedCounter = 0;
    
    for (let i = 0; i < heights.length; i++) {
        if (heights[i] !== sortedHeights[i]) {
            notExpectedCounter++;
        }
    }
    
    return notExpectedCounter;
};
```

---
#### Internal Links
[[2022-08-21]], [[LeetCode]], [[Arrays]]