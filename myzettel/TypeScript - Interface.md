---
template: note
aliases: []
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1472195870936-d88b0d4c1b41?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMTQ2ODIx&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-22) | (time:: 11:10) | (weather:: Vadodara: 🌦   +26°C →20km/h)

# TypeScript - Interface
[[Type Annotation]] can be long and hard to read. You cannot reuse it in multiple places.

 The interface lets you create a new custom type, describing the property names and value types of an object.

An interface can act as a gatekeeper to our functions. The objects/classes that want to use those functions **must** satisfy the interface requirements.

![[TypeScript - Interface 2022-08-22 13.16.36.excalidraw|100%]]

```typescript
interface Reportable {
	summary(): string;
}

function printReport(item: Reportable): void {
	console.log(item.summary());
}

// The following objects want to use the "printReport" method.
// Since, its argument is annotated with the type Reportable 
// the object must satisfy the interface requirements.
const civic = {
	name: 'Civic',
	year: 2000,
	broken: true,
	summary(): string {
		return `Name: ${this.name}`;
	}
};

const drink = {
	name: 'Pepsi',
	color: 'Brown',
	sugar: 40,
	summary(): string {
		return `My drink ${this.name} has ${this.sugar}gms of sugar.`
	}
};

printReport(civic);
printReport(drink);
```

---
#### Internal Links
[[2022-08-22]], [[TypeScript]]