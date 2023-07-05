---
template: note
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1529198792282-ca6752042aa2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwNjQzMDky&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-16) | (time:: 15:14) | (weather:: Vadodara: 🌧   +26°C ↑17km/h)

# Linear Search
In [[Arrays|Array Data Structure]] we can check every element if the index is not known for the element we are searching for. We continue checking elements until we find the element we're looking for or reach the Array's end. This technique for finding an element by checking every element one by one is known as the linear search algorithm.

In the worst case, a linear search ends up checking the entire Array. Therefore, the time complexity for a linear search is `O(N)`.

It's better to use [[Binary Search]] if the dataset you're dealing with is sorted. Sorting and searching on the dataset is only recommended if you intend to perform multiple searches on the same dataset. Otherwise, sorting an array is an expensive operation.

## Edge cases
It is important to handle all edge cases during the implementation of your linear search algorithm. Check the list of example edge cases as follows.
1. Search element doesn't exist.
2. Array doesn't contain any element, or it is `null`.

## Implementation
```java
public static boolean linearSearch(int[] array, int length, int element) {
    // Check for edge cases. Is the array null or empty?
    // If it is, then we return false because the element we're
    // searching for couldn't possibly be in it.
    if (array == null || length == 0) {
        return false;
    }

    // Carry out the linear search by checking each element,
    // starting from the first one.
    for (int i = 0; i < length; i++) {
        // We found the element at index i.
        // So we return true to say it exists.
        if (array[i] == element) {
            return true;
        }
    }

    // We didn't find the element in the array.
    return false;
}
```

---
#### Internal Links
[[2022-08-16]], [[Arrays]], [[Algorithms]], [[Search Algorithm]] 