---
template: note
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1517946546247-f092d7570cde?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNjMxNjA4&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-16) | (time:: 12:03) | (weather:: Vadodara: 🌧   +27°C ↗17km/h)

# Type Annotation
Type Annotation is a way to teach the language compilers what values we plan to store in the variable.

```typescript
// Here "Date" is called an annotation. 
// It instructs the TypeScript compiler that we will store a value of type Date in the future.
let today: Date;

// Annotation for a value of type String.
let name: string;
```

## When to use Type Annotations?
If the programming language you're working with supports [[Type Inference]] then you need to annotate your variables only in the following specific scenarios.

#### 1. A function that returns `any` type
![[Screenshot 2022-08-16 at 14.42.03.png]]

```typescript
const json = '{"x": 10, "y": 20}';
const coords = JSON.parse(json);
console.log(coords); // { x: 10, y: 20 }
```

`JSON.parse()` in [[TypeScript]] returns the type `any` as we cannot predict what value will be passed to the `JSON.parse()` function.

#### 2. When we declare on one line but initialize it later

It is self-descriptive. Isn't it? 

#### 3. When we want a variable to have a type that can't be inferred 

```typescript
let numbers = [-10, -1, 12];
// Assign number above zero otherwise false.
let numberAboveZero = false;

for (let i = 0; i < numbers.length; i++) {
	if (numbers[i] > 0) {
		numberAboveZero = numbers[i];
	}
}
```

We have assigned the `false` value to `numberAboveZero` variable. Here, [[TypeScript]] would have inferred its type as `boolean` because of that assignment.

However, inside the `for` loop we conditionally set it to a non-negative number. It will result in error.

We must annotate `numberAboveZero` as follows.

```typescript
let numberAboveZero: boolean | number = false;
```

## Destructuring with Annotations
```typescript
const todaysWeather = {
	weather: 'Sunny',
	date: new Date()
};

// In the function arguments,
// the first {} is for object destructuring and
// the second {} is to annotate the destructred object.
const logWeather = ({ weather, date }: { weather: string; date: Date}): void => {
	
	// ...
	// function body goes here...
	// ...
	
};

logWeather(todaysWeather);
```

---
#### Internal Links
[[2022-08-16]], [[Programming Language]], [[TypeScript]]