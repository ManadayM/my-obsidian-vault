---
template: note
aliases: [Move Zeroes]
source: https://leetcode.com/problems/move-zeroes/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1595250837975-aa19ae01e17e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwOTM3NTI0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-20) | (time:: 01:02) | (weather:: Vadodara: ☁️   +26°C ↗14km/h)

# [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
Given an integer array `nums`, move all `0`'s to the end of it while maintaining the relative order of the non-zero elements.

**Note** that you must do this in place without making a copy of the array.

## Solution - 1
https://leetcode.com/problems/move-zeroes/discuss/1617399/Javascript-Typescript-Really-clean-and-easy-two-pointer-solution

We use two pointers, one to track the current value being read in the array, and the other to track the position we can write in.

If we have an array without any zeroes, then the write pointer and read pointer will stay in keeping the whole time.

However, if we do encounter a zero when reading using the read pointer, we simply do not increment the write pointer.

This means the next write of a non-zero will lag behind the read pointer, overwriting the zero we found.

For simplicities sake, and to ensure trailing zeroes are maintained properly, we always assign 0 to the index we just read from.

It may be filled in at a later date with a non-zero value if one exists. If not it will remain zero, along with all subsequent indexes, satisfying the exercises' criteria.

```javascript
/**
 * @param {number[]} nums
 * @return {void} Do not return anything, modify nums in-place instead.
 */
var moveZeroes = function(nums) {
    let writePointer = 0;
	    
    for ( let readPointer = 0; readPointer < nums.length; readPointer++) {
        
        // Hold value at the current index
        const curr = nums[readPointer];
		
        // Set it to 0
        nums[readPointer] = 0;
        
        // If the original value at the current index is not 0
        // then store it at the `writePointer` index that tracks
        // the count of non-zero items.
        if(curr !== 0) {
            nums[writePointer] = curr;
            writePointer++;
        }   
    }
};
```

## Solution - 2
https://leetcode.com/problems/move-zeroes/discuss/172432/THE-EASIEST-but-UNUSUAL-snowball-JAVA-solution-BEATS-100-(O(n))-+-clear-explanation

The idea is that we go through the array and gather all zeros on our road.  

![image](https://assets.leetcode.com/users/olsh/image_1537442610.png)

Let's take our example:  
the first step - we meet 0.  
Okay, just remember that now the size of our snowball is 1. Go further. 

![image](https://assets.leetcode.com/users/olsh/image_1537442825.png)

Next step - we encounter 1. Swap the most left 0 of our snowball with element 1.

![image](https://assets.leetcode.com/users/olsh/image_1537444682.png)

Next step - we encounter 0 again!

![image](https://assets.leetcode.com/users/olsh/image_1537443824.png)

Our ball gets bigger, now its size = 2.

![image](https://assets.leetcode.com/users/olsh/image_1537443928.png)

Next step - 3. Swap again with the most left zero.

![image](https://assets.leetcode.com/users/olsh/image_1537444816.png)

Looks like our zeros roll all the time

![image](https://assets.leetcode.com/users/olsh/image_1537444189.png)

Next step - 12. Swap again:

![image](https://assets.leetcode.com/users/olsh/image_1537444465.png)

We reached finish! Congratulations!

![image](https://assets.leetcode.com/users/olsh/image_1537444540.png)

Here's the code.

```javascript
/**
 * @param {number[]} nums
 * @return {void} Do not return anything, modify nums in-place instead.
 */
var moveZeroes = function(nums) {
    let writePointer = 0;
    let snowball = 0;
    
    for (let i = 0; i < nums.length; i++) {
        
        if (nums[i] == 0) {
            snowball++;
        }
        else if(snowball > 0) {
            let curr = nums[i]
            nums[i] = 0;
            nums[i - snowball] = curr;
        }
    }
};
```

---
#### Internal Links
[[2022-08-20]], [[MOC/LeetCode]], [[Arrays]], [[Two-Pointer Technique]], [[Snowball Technique]] 