---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1533583135452-3e1300f8c597?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYyNDAxMzMy&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-05) | (time:: 23:51) | (weather:: Vadodara: ☀️   +29°C ↑13km/h)

# Singly Linked List
- A singly linked list is a unidirectional type of [[Linked List]].
- Each node in a singly linked list contains a value and a reference field to link to the next node in a chain or list.
- It can be traversed in one direction only i.e. from `head` to `tail` node.
![[Singly Linked List 2022-07-27 07.22.30.excalidraw|900]]

## Typical Node Structure
```TypeScript
export class SinglyListNode {
	next: SinglyListNode | null = null;
	
	constructor(public value: number) {}
}
```

## Time Complexity & Performance Rating
| | Access | Search | Insertion | Deletion |
| ------ | ------ | ------ | --------- | -------- |
|**Complexity**| `O(n)` | `O(n)` | `O(1)`    | `O(1)`   |
|**Rating** | Fair       |  Fair      |     Excellent      |    Excellent      |
Source: https://www.bigocheatsheet.com/

## Add Operation
If we want to add a new value after a given node `prev`, we should: 
1. Initialize a new node `cur` with the given value.
   ![[Singly Linked List - Init new node.png|500]]
2. Link the "next" field of `cur` to prev's next node `next`.
   ![[Singly Linked List - Link cur next to prev next.png|500]]
3. Link the "next" field in `prev` to `cur`.
   ![[Singly Linked List - Link prev next to current node.png|500]]
### Add a node at the beginning
1. Initialize a new node `cur`.
2. Link the new node to our original head node `head`.
3. Assign `cur` to `head`.

## Delete Operation
If we want to delete an existing node `cur` from the singly linked list, we can do it in two steps:
1. Find `cur`'s previous node `prev` and its next node `next`.
2. Link `prev` to `cur`'s next node `next`.

### Delete the first node
If we want to delete the first node, we can simply `assign the head's next node to the head`.

## Resources
1. [Intro to LinkedList - Apna College](https://www.youtube.com/watch?v=oAja8-Ulz6o)
2. [Singly Linked List - Educative.io](https://www.educative.io/answers/what-is-a-singly-linked-list)
---
## Internal Links
[[2022-09-05]], [[Linked List]], [[Common Data Structure Operations]]