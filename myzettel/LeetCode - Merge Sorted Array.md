---
template: note
aliases: [Merge Sorted Array]
source: https://leetcode.com/problems/merge-sorted-array/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1632402514303-0c59dd152b7f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwMzA2NzIx&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-12) | (time:: 17:48) | (weather:: Vadodara: 🌦   +29°C ↗35km/h)

# [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)

## ✍️ Problem
You are given two integer arrays `nums1` and `nums2`, sorted in **non-decreasing order**, and two integers `m` and `n`, representing the number of elements in `nums1` and `nums2` respectively.

**Merge** `nums1` and `nums2` into a single array sorted in **non-decreasing order**.

The final sorted array should not be returned by the function, but instead, be _stored inside the array_ `nums1`. To accommodate this, `nums1` has a length of `m + n`, where the first `m` elements denote the elements that should be merged, and the last `n` elements are set to `0` and should be ignored. `nums2` has a length of `n`.

## Solution
```javascript
/**
 * @param {number[]} nums1
 * @param {number} m
 * @param {number[]} nums2
 * @param {number} n
 * @return {void} Do not return anything, modify nums1 in-place instead.
 */
var merge = function(nums1, m, nums2, n) {

  let p1 = m - 1;
  let p2 = n - 1;
  
  for (let i = nums1.length - 1; i >= 0; i--) {
    
    if (p1 >= 0 && nums1[p1] > nums2[p2]) {
      nums1[i] = nums1[p1];
      p1--;
    }
    else if (p2 >= 0) {
      nums1[i] = nums2[p2];
      p2--;
    }
  }
};
```

---
#### Internal Links
[[2022-08-12]], [[MOC/LeetCode]], [[Arrays]] 