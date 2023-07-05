---
template: note
aliases: [JS:hasOwn,JS:hasOwnProperty]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1433086966358-54859d0ed716?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1NzUyMTYzMg&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# JavaScript Object.hasOwn() method
The `Object.hasOwn()` method in [[JavaScript|JavaScript]] will return `true` for direct properties of the object. If the property is inherited or doesn't exist, the method will return `false`.

> [!NOTE]
> `Object.hasOwn()` is recommended replacement for `Object.prototype.hasOwnProperty()`.

```javascript
const user = { name: 'Manaday Mavani' };

// ✅
Object.hasOwn(user, 'name'); // returns true
Object.hasOwn(user, 'toString'); // returns false

// 👋 
user.hasOwnProperty('name'); // returns true
user.hasOwnProperty('toString'); // returns false

// ✋
'name' in user; // returns true
'toString' in user; // returns true
```

## References
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwn
2. https://www.instagram.com/p/Cf1ZWa5L0sx/
---
#### Internal Links
[[2022-07-11]], [[JavaScript]]
