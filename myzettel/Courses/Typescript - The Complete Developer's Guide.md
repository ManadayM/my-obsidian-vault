---
template: course
progress: 25%
priority: 0.8
url: https://www.udemy.com/course/typescript-the-complete-developers-guide
aliases: [TypeScript with Design Patterns]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1513634917318-5c1a1a678d51?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNTgyNDAw&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [Typescript - The Complete Developer's Guide](https://www.udemy.com/course/typescript-the-complete-developers-guide)

repo_url:: https://github.com/ManadayM/TypeScript-Udemy

## Section 1: Getting Started
[[2022-08-15]]
- [[TypeScript|Introduction to TypeScript]]
- Environment Setup
	- [[TypeScript Installation]]
	- [[VSCode|VSCode Installation]]
	- [[VSCode - Add code to PATH]]
	- [[Prettier|Prettier Installation]]
- **First App** - Built a small TS app that fetches a single Todo entry from a mock todo API. The purpose of this exercise was not to learn any TS stuff but it was to showcase how TS can be helpful during development to catch errors early.

## Section 2: What is a Type System?
[[2022-08-16]]

##### Introduction to Types
When we say types, we imply a value having some properties and methods. For example, the `string` is a type that has methods like `charAt()`, `charCodeAt()`, `endsWith()`, etc. Hence, a `Type` is a label given to a specific type of value.

##### Different Types and examples of Types
Like other programming languages, TypeScript also has [[Primitive Values|Primitive Type]] and Non-primitive Types (Class, Objects, Functions, Date, and Arrays).

Created a features project to demonstrate how TypeScript infers different types when we assign a value to our variables.

## Section 3: Type annotations in action
[[2022-08-16]]
- [[Type Annotation|Introduction to Type Annotation]]
- [[Type Inference|Introduction to Type Inference]]
- Explored type annotation on variables, arrays, and classes.
- [[Type Annotation#When to use Type Annotations|Understood when we have to use Type Annotation and when we can rely upon Type Inference]].

## Section 4: Annotations with functions and objects
[[2022-08-17]]
- [[Type Inference#Type Inference and functions|Type Inference with functions]]
- [[TypeScript - Never Type]]
- [[Type Annotation#Destructuring with Annotations|Destructuring with Annotations]]
- Annotation around objects - Check `udemy-ts/features/annotations/objects.ts` for examples.

## Section 5: Mastering Typed Arrays
[[2022-08-17]] | Examples: `udemy-ts/features/annotations/arrays.ts`
- Arrays in TypeScript
- Typed Arrays
- Why typed arrays?
- Multiple Types in an array.

## Section 6: Tuples in TypeScript
[[2022-08-17]] | Examples: `udemy-ts/features/annotations/tuples.ts`
- [[TypeScript - Tuples]]

## Section 7: The All-Important Interface
[[2022-08-22]] | Examples: `udemy-ts/features/interfaces.ts`
- [[TypeScript - Interface]]

## Section 8: Building functionality with classes
[[2022-08-22]] | Examples: `udemy-ts/features/classes.ts`
- Basics of Classes
- Inheritance basics
	- Method override example
- Instance method modifiers - `public`, `private`, `protected`
	- Difference b/w ES6 classes and TypeScript classes
	- By default, all methods are `public`
- Class in TypeScript has a dual nature. We can use it to create objects from it. We can also use it as a type.

## Section 9: Design Patterns with TypeScript
[[2022-08-26]]
> [!MEMORY] Key Learnings
> Limit the API surface by wrapping a library. Invert dependencies using `interfaces` - check `CustomMap` implementation. It enforces other classes to adhere to the `Mappable` interface.
- Set up [[Parcel]] bundler globally.
- Identified and created basic classes - `User` and `Company`.
- Generated a [Google Maps API key](https://console.cloud.google.com/apis/credentials?project=total-byte-277218).
- Installed [Type Definition files for Google maps](https://developers.google.com/maps/documentation/javascript/using-typescript) `npm i -D @types/google.maps`.
- Wrapped Google Maps object creation inside a `CustomMap` class to limit the feature usage. Wrapping and only exposing what is required is a good practice as it reduces the issue curve. It only exposes a single method named `addMarkter` that adds a marker layer through the Google Maps library.
- The [current implementation](https://github.com/ManadayM/TypeScript-Udemy/blob/883a5bcb53ea4c1fab2db1c246b6cc940e32a0e3/maps/src/CustomMap.ts) of `CustomMap` is suboptimal. It has two implementations for adding a marker - `addUserMarker` to add a marker for `User` type and `addCompanyMarker` to add a marker for `Company` type.
- [Refactored](https://github.com/ManadayM/TypeScript-Udemy/commit/9fb26030a852a2c6b9ccbaef3bd67998f417e37c) the initial implementation using the `Mappable` interface and a generic method `addMarker` to add a marker on the map. This way we made the `CustomMap` class a standalone class i.e. we don't need external references for the `User` and `Company` class. The `CustomMap` class has become an independent and reusable class that can be used in any project.

## Section 10: More on Design Patterns
- Generated a [[TypeScript Config]] file. 
- Understood two compiler options of `tsconfig.json` file.
- Understood how to invoke the TypeScript compiler and use *watch* mode to detect changes.
- Generated `package.json` file. Installed `nodemon` and `concurrently` node modules.
- Started implementing a simple `Sorter` class that can sort `number[]`, `string`, or `linked list`.
- The initial implementation only covered the support for numbers array.
- Later, we indicated that `collection` can be initialized for `string` values as well. 
```TypeScript
class Sorter {
	constructor(public collection: number[] | string) {}
}
```
- Now, the compiler started showing errors for the initially implemented logic to access number values from the array. It is happening because the `string` values can be accessed using the `index` method but we cannot assign/update any character at a particular index.
- We introduced [TypeScript Type Guard](https://blog.logrocket.com/how-to-use-type-guards-typescript/) to temporarily handle this issue.
```TypeScript
if (this.collection instanceof Array) {
	if (this.collection[j] > this.collection[j + 1]) {
		const leftHand = this.collection[j];
		this.collection[j] = this.collection[j + 1];
		this.collection[j + 1] = leftHand;
	}
}
```


## 📚 Linked Notes
```dataview
TABLE file.cday AS Created 
FROM [[Typescript - The Complete Developer's Guide]] AND -"Calendar" AND -"People"
SORT file.cday ASC
```

---
#### Internal Links
[[Courses]], [[TypeScript]]