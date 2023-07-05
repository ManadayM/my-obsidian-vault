---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1605265536104-382d8ed9f106?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYxMzIxNDQw&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-24) | (time:: 11:40) | (weather:: Vadodara: ⛅️  +28°C ↗20km/h)

# Event Bus
- Event Bus in a [[Microservice|microservice architecture]] is similar to Bus Topology in [[Networking]]. 
- The Event Bus mechanism allows different components to communicate with each other without knowing about each other.
- A component can send an event to Event Bus without knowing the end consumers.
- Components can listen to Events on an Event Bus, without knowing who sent the Events.
- Many different implementations - RabbitMQ, Kafka, NATS, etc.

![[Pasted image 20220824115628.png]]

## 📚 References
- https://dzone.com/articles/design-patterns-event-bus
- http://www.rribbit.org/eventbus.html
- https://docs.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/integration-event-based-microservice-communications

---
#### Internal Links
[[2022-08-24]], [[System Design]], [[Microservice]], [[Eventual Consistency]]