---
template: note
parent: [[LeetCode]]
aliases: [Running sum of 1D array]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1512847179643-f1794c3e0ac8?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1ODM5MjMyNQ&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Running sum of 1D array
https://leetcode.com/problems/running-sum-of-1d-array/

## ✍️
The running sum of the 1D array is a simple exercise where we do running additions of the numbers we come across as we traverse.

Let's say we have `[1, 2, 3, 4]` array as input then its running sum of the array is `[1, 1+2, 1+2+3, 1+2+3+4]`.

### Solution
1. The 0th value will remain as is in any case. Start from index 1.
2. Do in-place addition as we don't require original value as we progress.
3. Return the updated array at the end.

```javascript
function runningSum(nums) {
	for (let i = 1; i < nums.length; i++) {
		nums[i] += nums[i - 1];
	}
	return nums;
}
```

---
#### Internal Links
[[2022-07-21]], [[MOC/LeetCode|LeetCode]]