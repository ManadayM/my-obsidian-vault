---
template: note
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1543169108-32ac15a21e05?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNjMyMTY1&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-16) | (time:: 12:12) | (weather:: Vadodara: 🌧   +27°C ↗17km/h)

# Type Inference
When a language compiler tries to figure out what type of value a variable refers to.

In [[TypeScript]] it happens when you declare and initialize the variable simultaneously.

**If you just declare a variable but don't assign any value to it then that variable will be considered of type `any`.**

## Effective Type Inference (TypeScript)
```typescript
// Declaration + Initialization
// TypeScript will infer its type as Date.
const today = new Date();
```

![[Screenshot 2022-08-16 at 12.21.40.png]]

## Generic Type Inference (TypeScript)
```typescript
// Only declaration without annotation
// Here, type inference won't happen.
let today;
today = new Date();
```

![[Screenshot 2022-08-16 at 12.20.38.png|100%]]

## Type Inference and functions
With `functions`, Type Inference will figure out what type of value a function will return. It cannot happen for the function arguments.

**It is recommended to always annotate a function with its return type.** If you don't return from a function by mistake then the TypeScript compiler will infer its return type as `void` which is not desirable.

```typescript
// Return type will be void which is not desirable
const subtract = (a: number, b: number) => {
	a - b; // notice the missing 'return' keyword
}
```

---
#### Internal Links
[2022-08-16](app://obsidian.md/2022-08-16), [Programming Language](app://obsidian.md/Programming%20Language), [TypeScript](app://obsidian.md/TypeScript)