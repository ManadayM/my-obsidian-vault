---
template: note
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1498855926480-d98e83099315?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNzE2NzA4&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-17) | (time:: 11:41) | (weather:: Vadodara: 🌦   +27°C ↑28km/h)

# [Never Type](https://www.typescriptlang.org/docs/handbook/2/functions.html#never)

Some functions never return a value. The `never` type represents values that are *never* observed. In a return type, this means that function throws an exception or terminates the execution of the program.

```typescript
const throwError = (msg: string): never => {
	throw new Error(msg);
}
```

---
#### Internal Links
[[2022-08-17]], [[TypeScript]]