---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1511489731872-324afc650052?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4NzQ5NzU4&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-25) | (time:: 17:19) | (weather:: Vadodara: 🌦   +31°C ↗20km/h)

# Java Types
There are two broad data type categories in [[Java]] - Primitive Type and Object Type.

## Java Primitive Types
| Type      | Value Range    | Size in Memory |  Sample Value   | Default | Literals | 
| --------- | -------------- | -------------- | --- | --- | --- |
| `byte`    | -128 to 128    | 1 byte         |     | `0` | `int` |
| `short`   | -32768 to 32767               | 2 bytes        |     | `0` | `int` |
| `int`     | -2147483648 to 2147483647               | 4 bytes        |  | `0`    | `int` |
| `long`    |                | 8 bytes        |  `5L`   | `0` | `L` or `l` |
| `float`   |                | 4 bytes        |  `3.14f` / `3.14F`   | `0.0f` | `F` or `f` |
| `double`  |                | 8 bytes        |   0.0d  | `0.0d` | `D` or `d` |
| `char`    |      | 2 bytes        |  a, b, c...   | `\u0000` | `''` |
| `boolean` | `true`/`false` | 1 byte         |     | `false` | `true / false` |

- For every primitive type, there is a related wrapper class implementation. Like `Integer` class for `int` primitive type.
- To store a number in a number system other than the *decimal number system*.
```java
// Standard decimal number
byte b = 10;

// Binary form of 10
byte b = 0b1010;

// Octal number starts with 0. decimal 10 = octal 12.
byte b = 012;

// Hexadecimal form of 10
byte b = 0xA;

// We can use underscore for long numbers for better readability.
long l = 999_999_999;
```

^504eed

## Java Non-primitive Types
| Type     | Sample Value |
| -------- | ------------ |
| `String` |              |


---
#### Internal Links
[[2022-07-25]], [[Java]]