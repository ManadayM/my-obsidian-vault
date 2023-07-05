---
template: note
aliases: [Relational Database,RDBMS]
source: https://arxiv.org/pdf/1004.1001.pdf
---
![tp.web.random_picture](https://images.unsplash.com/photo-1534762867727-efa52ebe7f36?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwOTA5MDk1&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-19) | (time:: 17:08) | (weather:: Vadodara: 🌦   +31°C ↗25km/h)

# Relational Database
- Relational databases maintain a collection of tables.
- Each table can be defined by a set of rows and a set of columns.
- Semantically, rows denote objects and columns denote properties/attributes.
- Thus, the datum at a particular row/column-entry is the value of the column property for that row object.
- Usually, a problem domain is modeled over multiple tables in order to avoid data duplication. This process is known as data normalization.
- In order to unify data in disparate tables, a “join” is used. A join combines two tables when columns of one table refer to columns of another table.
- Maintaining these references in a consistent state is known as [[Referential Integrity]].

---
#### Internal Links
[[2022-08-19]], [[Database]]