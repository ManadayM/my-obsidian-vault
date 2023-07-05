---
template: note
aliases: [Richest Customer Wealth]
source: https://leetcode.com/problems/richest-customer-wealth/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1501786223405-6d024d7c3b8d?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1ODQ2ODg1OA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [Richest Customer Wealth](https://leetcode.com/problems/richest-customer-wealth/)

This problem aims to find the richest customer in the town. Each customer can have multiple bank accounts. Find the richest customer who has highest total bank balance in his/her bank accounts.

The sample input `[[1,2,3][3,2,5]]`. Here, there are two customers having 3 bank accounts each. The expected output is `10` as second customer in the input is having higesth total account balance.

## Solution
```javascript
const maxWealth = function(accounts) {
	let wealthOfTheRichest = accounts[0][0];
	
	for (let i = 0; i < accounts.length; i++) {
		let thisPersonsWealth = 0;
		
		for (let j = 0; j < accounts[i].length; j++) {
			thisPersonsWealth += accounts[i][j];
		}
		
		if (thisPersonsWealth > wealthOfTheRichest) {
			wealthOfTheRichest = thisPersonsWealth;
		}
	}
	return wealthOfTheRichest;
}
```

---
#### Internal Links
[[2022-07-22]], [[MOC/LeetCode]], [[Arrays]] 