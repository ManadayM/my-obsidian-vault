---
template: note
source: [[Graph Databases Neo4j]]
last_reviewed: "2022-12-31"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1499354271251-d2c2cf66568a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwOTAwNjc2&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# What is Graph?
A graph is a set of *nodes* and the *relationships* that connect them. It represents entities as *nodes* and the ways in which those entities relate to the world as *relationships*.

Let's represent Twitter's data in a form of a graph.

![[What is Graph? 2022-08-19 14.55.26.excalidraw|100%]]

Each node is labeled User, indicating its role in the network. These nodes are then connected with relationships, which help further establish the semantic context: namely, that Bob follows Shawn, and that Shawn, in turn, follows Bob. Alice and Shaun likewise follow each other, but sadly, although Alice follows Bob, Bob hasn’t (yet) reciprocated.

---
#### Internal Links
[[Graph Database]]