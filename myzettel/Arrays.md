---
template: note
source: https://leetcode.com/explore/featured/card/fun-with-arrays
---
![tp.web.random_picture](https://images.unsplash.com/photo-1582149916751-c4ecb7b29adb?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4NzE2MTc3&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-25) | (time:: 07:59) | (weather:: Vadodara: 🌦   +25°C ↗10km/h)

# Arrays
![[arrays 2022-07-25 10.51.28.excalidraw|900]]
> [!INFO] Analogy
> A DVD box.
- Arrays are a simple [[Data Structure|data structure]] for storing a collection of similar items at contiguous memory locations.
- Like the size of the DVD box analogy, we need to decide how much storage space we want to allocate to an array. 
- **You reserve, what you allocate.** You cannot use these memory locations for any other purpose or type of data.
- Like a DVD box where you will only put DVDs and not your clothes, you also need to set the data type that you are planning to store in your array. You can store [[Primitive Values|primitive values]] or [[JavaScript - Objects|objects]]. **It can be anything, but it must be one.**
- We read from or write to an array through the **Indexes**. Indexes are sequential numbers given to the reserved memory blocks for our array. 
- The index always starts from `0` and ends at `N - 1`, where `N` is the array size that you have reserved at the time of array creation.

Check [[Java Arrays]] to learn array operations in [[Java]].

> [!MEMORY] Capacity vs. Size
> `Capacity` means the total size that we have reserved in memory. Whereas `size` is current items in an array.

## 3 Primary Array Operations
1. Inserting items
2. Removing items
3. Searching items

### Inserting Items

**Inserting at the end of an Array**
- To insert at the end of an array is easy. All we need to do is to assign the new element to one index past the current last element.

**Inserting at the start of an Array**
- To insert an element at the start of an array, we'll need to shift all other elements in the array to the right by one index to create space for the new element.
- **This is a very costly operation.** 
- The need to shift everything implies that it is not a constant time operation. It'll be proportional to the length of the array.
- Time complexity: `O(N)`. Where `N` is the length of an array.

**Inserting Anywhere in an Array**
- To insert at the specific index in the Array, we first need to shift all elements from that index onwards one position to the right.
- This is a special case of [[Arrays#Inserting at the start of an Array|inserting at the start of an Array]] operation.

## 📚 References
- [Glasp: Highlights on Arrays](https://glasp.co/#/ManadayM/?tag=arrays)
- https://leetcode.com/explore/featured/card/fun-with-arrays
- https://www.geeksforgeeks.org/array-data-structure

## 📚 Linked Notes
```dataview
TABLE 
	dateformat(file.cday, "yyyy-MM-dd") AS Created, 
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
FROM [[Arrays]] AND -"Calendar"
SORT file.cday ASC
```

---
#### Internal Links
[[2022-07-25]], [[Data Structure|Data Structure]]