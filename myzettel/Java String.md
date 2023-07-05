---
template: note
parent: [[Java]]
tags: 
aliases: []
source: https://jenkov.com/tutorials/java/strings.html
---
![tp.web.random_picture](https://images.unsplash.com/photo-1509728628963-c39e0e38d32d?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4NzUyMjgx&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-25) | (time:: 18:01) | (weather:: Vadodara: 🌦   +31°C ↗20km/h)

# Java String
In [[Java]], `String` is a reference type that can contain multiple characters (`chars`).

## Create a string in Java
Since `String` in Java is an object. We need to use the `new` operator to create a new String object.

```java
String name = new String("Manaday");
```

**Shorthand** approach.

```java
String name = "Manaday";
```

### String Literals as Constants or Singletons
The [[Java Virtual Machine (JVM)|JVM]] manages a string pool for string literals. If you create two string objects using the shorthand method, and if they contain the same string value then JVM may only create a single `String` instance in memory.

Consider the following two `String` objects - `msg1` and `msg2`.

```java
// With the shorthand syntax and the same string literal values,
// JVM may create only a single string instance in its string pool.

String msg1 = "Hello world";
String msg2 = "Hello world";
```

Since both `msg1` and `msg2` contain the same string literals, JVM may create only a single `String` instance in memory. For the subsequent initializations, JVM would return the same object reference.

**Initialize `String` objects using the `new` operator to ensure JVM creates separate copies for each string literal.**

```java
// With the new keyword JVM will create separate copies in its string pool.

String msg1 = new String("Hello world");
String msg2 = new String("Hello world");
```

## String concatenation



---
#### Internal Links
[[2022-07-25]], [[Java]], [[Java Types]]
