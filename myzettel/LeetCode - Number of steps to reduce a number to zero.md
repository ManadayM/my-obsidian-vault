---
template: note
aliases: [Number of Steps to Reduce a Number to Zero]
source: https://leetcode.com/problems/number-of-steps-to-reduce-a-number-to-zero/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1437376576540-236661ddb41f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1ODQ5NTA0OA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [Number of Steps to Reduce a Number to Zero](https://leetcode.com/problems/number-of-steps-to-reduce-a-number-to-zero/)

## ✍️ Problem
Given an integer `num`, return _the number of steps to reduce it to zero_.

In one step, if the current number is even, you have to divide it by `2`, otherwise, you have to subtract `1` from it.

## Solution
```javascript
/**
 * @param {number} num
 * @return {number}
 */
var numberOfSteps = function(num) {
  
  let steps = 0;
  
  while (num !== 0) {
    steps += 1;
    num = num % 2 === 0 ? num / 2 : num - 1;
  }
  
  return steps;
};
```

---
#### Internal Links
[[2022-07-22]], [[MOC/LeetCode]]
