---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1502943693086-33b5b1cfdf2f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU5MDA3NDA3&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-28) | (time:: 16:53) | (weather:: Vadodara: ⛅️  +34°C →18km/h)

# Maths - Sets
> [!NOTE] Definition
> Collection of well-defined and distinct objects are called Sets.

The objects that form a set are called `Elements`. Set is a collection of **related** elements. For example, the set of things we **can see** can include a *tree, table, man, puppy, mobile, etc.* while the set of things we **cannot see** can include *air, heat, oxygen, etc*.

Another important characteristic of a set is that its `elements` should be `well-defined`. We cannot make a set of **good teachers** or **intelligent students** as the words good and intelligent are subjective and not well-defined.

We use the `curly brackets` to mark the start and end of the sets.

### Example
A set of 1st 3 natural numbers can be represented in the following ways.

1. **Listing Method** - `{ 1, 2, 3 }`
2. **Set-builder Method** - `{ 𝒙: 𝒙 < 4, 𝒙 ∈ N }`
3. **Venn Diagram** - The entire set is represented within a circle.

Here,
- 𝒙 is a variable, we can use anything. It reads as `All 𝒙`.
- **:** reads as `such that`.
- ∈ means belongs to.
- N means natural numbers.

The whole expression can be read as `The set of all 𝒙 such that 𝒙 is less than 4 and 𝒙 belongs to natural numbers`.

## Types
![[Screenshot 2022-07-28 at 17.03.08.png]]

![[Screenshot 2022-07-28 at 17.46.24.png]]

### Cardinal Numbers
> [!NOTE] Cardinality
> The word Cardinality in [[Maths]] means size. 

`A = { 1, 2, 3 }` here `number of elements` are `3`. It can be represented as `n(A) = 3`.

`B = { 1, 2, 3, 4}`. Here `n(B) = 4`.

We can say that `The cardinality of Set A is less than the cardinality of Set B`.

### Equivalent Sets
> [!NOTE]
> Equivalent = Same Cardinal Number

The sets are called equivalent sets if they have the same cardinal number.

Let's say we have the following sets.

`A = { 1, 2, 3 }`, `B = { 2, 3, 4, 5 }`, `C = { 3, 5, 6 }`, and `D = { 2, 5, 9, 1 }`.

Here, `n(A)=3, n(B)=4, n(C)=3, n(D)=4`.

Here,
1. `A` is `equivalent` to `C`.
2. `B` is `equivalent` to `D`.

## Subsets
![[Screenshot 2022-07-29 at 13.15.43.png]]

Let's say you have 3 ice cream choices - Chocolate (c), Vanilla (v), and Butterscotch (b). In this regard, our primary or main set is `{ c, b, v }`.

You can have the following choices. 
- **Any one ice cream:** `{c}, {b}, {v}`.
- **Any two ice creams:** `{c,b}, {c,v}, {b,v}`.
- **All three ice creams:** `{c, b, v}`.
- **None (if you're ill):** `{}`.

These choices from the primary set of choices are called the Subsets. They are represented using `⊆`. 

#### Every set is a subset of itself

Let's say we have these sets `P = { 1, 2, 3 }`, `Q = { 1, 2, 3, 4, 5 }`, `C = { 4, 5, 6 }`, and `D = { 5, 4, 6 }`.

Here, `P ⊆ Q` as all elements of `P` are present in `Q`. We can also say that `P ⊆ P` and `Q ⊆ Q`.

#### Proper Subset & Superset
Check the sets `P` and `Q` in the above examples. Every element of `P` is part of `Q`. **However, there is at least one element in `Q` which is not present in set `P`.**

In this case, we say `P ⊂ Q` (`P` is a proper subset of `Q`). The sign `⊂` is used to denote a proper subset.

We can also say that `Q` is a superset of `P` - `Q ⊃ P`.

#### Null set
A set having no elements is called a `null set`. It can be represented using `{}` or `∅`.

**A null set is a subset of every set or null set.** So, we can say `∅ ⊆ P` or `∅ ⊆ Q` or `∅ ⊆ ∅`.


## 📚 References
1. [Middle School Math - Sets - Youtube Playlist](https://www.youtube.com/playlist?list=PLmdFyQYShrjfi7EeDyHxr0jhoPXEOlFX0)
2. [Natural Numbers vs. Whole Numbers](https://www.cuemath.com/numbers/natural-numbers/) 
---
#### Internal Links
[[2022-07-28]]