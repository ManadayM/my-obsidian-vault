---
template: note
aliases: []
source: [[Graph Databases - Neo4j by Oreilly.pdf]]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1534953356485-3b0fa4742c8f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwOTA1NjI0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-19) | (time:: 16:10) | (weather:: Vadodara: 🌦   +32°C ↗19km/h)

# Graph Database
- A *graph database* is an online database management system with CRUD methods that expose a graph data model.
- Graph databases are generally built for use with transactional ([[OLTP]]) systems.
- A graph database stores nodes and relationships instead of tables, or documents.
- Data is stored without restricting it to a pre-defined model.

## Use cases
Source:: https://youtu.be/-dCeFEqDkUI?list=PL9Hl4pk2FsvWM9GWaguRhlCQ-pa-ERd4U
- Real-Time Recommendations
- Master Data Management
- Fraud Detection
- Graph Base Search
- Network & IT Operations
- Identity & Access Management

## Drawbacks
Source:: [[The Graph Traversal Pattern.pdf]]
- The primary drawback is that it is difficult to shard a graph. This is also possible with a [[Relational Database]] if it maintains [[Referential Integrity]].

---
#### Internal Links
[[2022-08-19]], [[Database]]