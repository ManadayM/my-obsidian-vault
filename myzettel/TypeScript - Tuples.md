---
template: note
last_reviewed: "2022-11-04"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNzI4Mjc2&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-17) | (time:: 14:54) | (weather:: Vadodara: 🌦   +29°C ↗37km/h)

# Tuples
Tuples are an `array-like` structure where each element represents some property of a record.

```typescript
type OHLC = [string, number, number, number, number];

const historyData: OHLC[] = [
	
	["2022-08-10", 20, 23, 19, 22],
	["2022-08-11", 20, 23, 19, 22],
	["2022-08-12", 20, 23, 19, 22]
];

// Type alias
type Drink = [string, boolean, number];

const pepsi: Drink = ["brown", true, 40];
const sprite: Drink = ["clear", true, 40];
const tea: Drink = ["brown", false, 0];
```

---
#### Internal Links
[[2022-08-17]], [[TypeScript]], [[Arrays]]