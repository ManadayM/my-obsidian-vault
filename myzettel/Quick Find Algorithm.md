---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1463693396721-8ca0cfa2b3b5?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU5NDMyNDIz&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-02) | (time:: 14:57) | (weather:: Vadodara: ☁️   +33°C →16km/h)

# Quick Find Algorithm
- It's an eager algorithm.
- It uses a simple [[Arrays|array]] data structure to solve the problem.
- Interpretation: `p` and `q` are connected if and only if they have the same id.

![[Screenshot 2022-08-02 at 15.04.35.png]]

- The `find` operation is easy - if the two objects have the same id then they're connected.
- The `union` operation is costly - it requires all connected components to update their values. To merge components containing `p` and `q`, change all entries whose id equals `id[p]` to `id[q]`.

## Example of Union Operation

**Initial State**
![[Screenshot 2022-08-02 at 15.23.28.png]]

**Union 4 and 3**
![[Screenshot 2022-08-02 at 15.24.39.png]]

**Union 3 and 8**

![[Screenshot 2022-08-02 at 15.26.00.png]]

**Union 2 and 1**

![[Screenshot 2022-08-02 at 15.28.36.png]]

**Connected query for 8 and 9**
This will return `true` since they're already connected.

![[Screenshot 2022-08-02 at 15.29.43.png]]

## Implementation
> [!NOTE] Princeton Implementation
> https://algs4.cs.princeton.edu/code/edu/princeton/cs/algs4/QuickFindUF.java.html

```java
public class QuickFindUF {
	
	private int[] id;
	
	// Constructor
	public QuickFindUF(int N) {
		id = new int[N];
		
		// Set the id of each object to itself.
		// N array accesses.
		for (int i = 0; i < N; i++) {
			id[i] = i;
		}
	}
	
	/**
	 * Check whether p and q are in the same component.
	 * 2 array accesses.
	 */	
	public boolean connected(int p, int q) {
		return id[p] == id[q];
	}
	
	/**
	 * union (2, 1)
	 * Connect 1 and 2. Use 1 as the connection value.
	 * 2N + 2 array accesses.
	 */
	public void union(int p, int q) {
		
		// Fetch current values stored at p and q
		int pid = id[p];
		int qid = id[q];
		
		// Replace all values where id[x] = pid with id[x] = qid
		for (int i = 0; i < this.id.length; i++) {
			if (id[i] == pid) {
				id[i] = qid;
			}
		}
	}
}
```

## Algorithm Efficiency

**Number of array accesses - read and write**

1. `initialize`: N
2. `union`: N
3. `find`: 1


![[algorithms-part-1_05-union-find-slides.pdf]]


---
#### Internal Links
[[2022-08-02]]