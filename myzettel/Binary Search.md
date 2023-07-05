---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1514897859680-373d0d5f380b?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU5ODkzMTQ4&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-07) | (time:: 22:44) | (weather:: Vadodara: 🌦   +29°C ↗16km/h)

# Binary Search
- A search algorithm takes a **sorted list** of elements as input.
- If the element you're looking for is in that list, the binary search **returns the position** where it is located. Otherwise, it **returns null**.
- With binary search, you **guess the middle number and eliminate the remaining half** elements every time.
- In general, for any list of `n`, **binary search will take log<sub><b>2</b></sub>n steps to run in the worst case**, whereas simple search will always take `n` steps.
- **You are not searching every element, but a rapidly reducing subset. The search is not linear but logarithmic. And, because it is "either this half or that half"** it is base 2.

## Implementation
```javascript
function binarySearch(sortedArray = [], searchItem) {
	const len = sortedArray.length;
	
	let min = 0;
	let max = len - 1;
	
	while (min < max) {
		let mid = Math.ceil( (min + max) / 2 );
		const guess = sortedArray[mid];
		
		if (guess === searchItem) {
			return guess;
		}
		
		if (guess < searchItem) {
			min = mid + 1;
		}
		
		if (guess > searchItem) {
			max = mid - 1;
		}
	}
	
	return null;
}
```

## Running Time
- For a simple/linear search, a list of 100 items, requires 100 guesses. If it’s a list of 4 billion numbers, it takes up to 4 billion guesses. So maximum number of guesses is the same as the size of the list. This is called **linear time**.
- For Binary search, if the list is 100 items long, it takes at most 7 guesses. If it is 4 billion items, it takes at most 32 guesses. This is called **logarithmic time - O (log n)**.

---
#### Internal Links
[[2022-08-07]], [[Algorithms]]