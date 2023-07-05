---
template: note
aliases: [Check If N and Its Double Exist]
source: https://leetcode.com/problems/check-if-n-and-its-double-exist/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1464852045489-bccb7d17fe39?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNjQ3NTc1&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-16) | (time:: 16:29) | (weather:: Vadodara: 🌧   +26°C ↑17km/h)

# [Check If N and Its Double Exist](https://leetcode.com/problems/check-if-n-and-its-double-exist/)

## ✍️ Problem 
Given an array `arr` of integers, check if there exist two integers `N` and `M` such that `N` is the double of `M` ( i.e. `N = 2 * M`).

More formally check if there exist two indices `i` and `j` such that :
-   `i != j`
-   `0 <= i, j < arr.length`
-   `arr[i] == 2 * arr[j]`

## Solution
```javascript
/**
 * @param {number[]} arr
 * @return {boolean}
 */
var checkIfExist = function(arr) {
    
    for (let i = 0; i < arr.length; i++) {
	        
        for (let j = arr.length - 1; j > i; j--) {
				
            const isJDouble = arr[j] * 2 === arr[i];
            const isJHalf = arr[j] / 2 === arr[i];
	            
            if (isJDouble || isJHalf) {
                return true;
            }
        }
    }
    
    return false;
};
```

---
#### Internal Links
[[2022-08-16]], [[MOC/LeetCode]], [[Arrays]], [[Linear Search]] 