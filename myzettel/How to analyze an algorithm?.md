---
template: note
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1639058975063-a1abba242a67?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwMjE0Njk0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-11) | (time:: 16:14) | (weather:: Vadodara: 🌧   +26°C ↗30km/h)

# [How to analyze an algorithm?](https://www.youtube.com/watch?v=xGYsEqe9Vl0&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=4)

## Analysis Criteria
An algorithm can be analyzed from different criteria as follows.
1. Time
2. Space
3. Data transfer on the network
4. Power consumption
5. CPU Registers consumed (Algorithms for Device Drivers)

## Frequency Count Method
This method is used to calculate the Time Complexity or Space Complexity of an algorithm. It is aka the Step Count method.

The method simply considers the number of times a statement is executed to calculate the complexity.

**Rules**
- For `comments` and `declarations` statements, the step count is `0`.
- For `return` and `assignment` statements, the step count is `1`.
- **Ignore constant multiplies.**
- **Ignore lower order exponents when higher order exponents are present.** For example, if the time complexity of an algorithm is 3n<sup>4</sup> + 4n<sup>3</sup> + 10n<sup>2</sup> + n + 100 then by this rule we can ignore all constants and lower order exponents. So, the time complexity is O(n<sup>4</sup>).

### Time Analysis
Time analysis means how much time our algorithm will take. Now, this time unit is not a watch/clock time unit. Every simple statement in your algorithm takes `1 unit of time`.

```javascript
function swap(a, b) {
	let temp = a; // --- time: 1, space: 1
	a = b; // ---------- time: 1, space: 1
	b = temp; // ------- time: 1, space: 1
}
```

Consider the example of the `swap` function. Each statement takes `1 unit of time`. So, the total time it requires is `3`. It is represented in the time function form as `f(n)=3`. Here, `3` is constant so in [[Big O]] notation it is represented as `O(1)`.

### Space Analysis
 List out all the variables used in your algorithm to perform the space analysis. In the `swap` example, we used `a`, `b`, and `temp` and they each consume only `1 word`. So, the total space it requires is `3 words`. it is represented in the space function form as `s(n)=3`. Here, `3` is constant so in [[Big O]] notation it is represented as `O(1)`.


## 📚 References
1. [Frequency Method by Abdul Bari](https://youtu.be/1U3Uwct45IY?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)
2. [Frequency Method by Sudhakar Atchala](https://www.youtube.com/watch?v=6cv5Quw3JGE)
3. [[Maths - Polynomials]]

---
#### Internal Links
[[2022-08-11]]