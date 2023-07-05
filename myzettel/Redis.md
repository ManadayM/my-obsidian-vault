---
template: note
source: https://www.youtube.com/watch?v=OqCK95AS-YE
---
![tp.web.random_picture](https://images.unsplash.com/photo-1514480924801-4eb7a65d3ed3?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU5OTQxMjAw&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-08) | (time:: 12:16) | (weather:: Vadodara: 🌦   +26°C ↑10km/h)

# Redis
- Redis stands for **Re**mote **Di**ctionary **S**erver is an **In-Memory database**. 
- It is often used as **Cache** to improve performance.
- However, Redis **can be used as a fully-fledged primary database** to store and persist multiple data formats.
- The **Redis Core** is a basic building block that is a key-value store.
- Use **Redis Modules** to **extend** the Redis for different data types and different purposes. For example, *RediSearch* for search functionality like *Elastic Search*.
- It is **schemaless**.

## Persistence
There are multiple ways to persist data in Redis DB.

### Snapshotting (RDB)
- Produces single-file point-in-time snapshots of your dataset - (`dump.rdb`).
- Configure based on time or number of writes passed, etc.
- ✅  Great for backups & disaster recovery.
- ❌  You may lose the latest minutes of data.

### Append Only File (AOF)
- Logs every write operation continuously - `appendonly.aof`.
- Upon restarting Redis, it will re-play the AOF to rebuild the state.
- ✅  More durable.
- ❌  Slower than snapshotting.

> [!INFO] Persistent Storage Location
> **Separate** Persistent Storage from Data Service. For example, if your app is running on an AWS EC2 instance then you should use Elastic Block Storage (EBS) to persist your data.

## Scaling

### Clustering
- Primary Client: Read & Write.
- Replica Clients: Read.

Here, replicas hold complete copies of the Primary instance's data.

### Sharding
Redis also supports [[Database Sharding|sharding]].


---
#### Internal Links
[[2022-08-08]], [[Database]]