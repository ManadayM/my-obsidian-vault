---
template: "new-note-template"
aliases: [FizzBuzz]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1515612148533-6247582c12c7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1ODQ3NjkzMQ&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# FizzBuzz

## ✍️
Given an integer `n`, return _a string array_ `answer` _(**1-indexed**) where_:
-   `answer[i] == "FizzBuzz"` if `i` is divisible by `3` and `5`.
-   `answer[i] == "Fizz"` if `i` is divisible by `3`.
-   `answer[i] == "Buzz"` if `i` is divisible by `5`.
-   `answer[i] == i` (as a string) if none of the above conditions are true.

## Solution
```javascript
/**
 * @param {number} n
 * @return {string[]}
 */
 const fizzBuzz = (n) => {
	let answer = [];
	
	for (let i = 1; i <= n; i++) {
		let value = "";
		
		if (i % 3 === 0) value += "Fizz";
		if (i % 5 === 0) value += "Buzz";
		
		if (!value) value += i;
		
		answer.push(value);
	}
	
	return answer;
 }
```

---
#### Internal Links
[[2022-07-22]], [[MOC/LeetCode|LeetCode]]
