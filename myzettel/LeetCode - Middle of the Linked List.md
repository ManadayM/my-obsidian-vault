---
template: note
aliases: [Middle of the Linked List]
source: https://leetcode.com/problems/middle-of-the-linked-list/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1437502920657-db9708bfe2ef?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4OTM1ODM5&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-27) | (time:: 21:00) | (weather:: Vadodara: 🌦   +27°C ↗14km/h)

# [Middle of the Linked List Problem](https://leetcode.com/problems/middle-of-the-linked-list/)

## ✍️ Problem
Given the `head` of a [[Linked List]], return _the middle node of the linked list_.

If there are two middle nodes, return **the second middle** node.

## Solution
```javascript
/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
const middleNode = function(head) {
	
	const arr = [head];
	
	// iterate till the head is not null
	// Remember: tail node always contains `null` value.
	while(head) {
		// push the current head into the array.
		arr.push(head);
		
		// Update head to the next node
		head = head.next;
	}
	
	// We have an array with a linked list of nodes
	// at each position, starting from the respective 
	// index during the iteration.
	
	// To find the middle, we'll divide it by 2.
	// To cover the case of multiple middles we need to 
	// pick the second middle node. Hence, we will use
	// Math.ceil function.
	return arr[Math.ceil(arr.length / 2)];
};
```

---
#### Internal Links
[[2022-07-27]], [[MOC/LeetCode]], [[Linked List]]