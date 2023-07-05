---
template: note
source: https://www.youtube.com/watch?v=nogQV09YDeI
---
![tp.web.random_picture](https://images.unsplash.com/photo-1615848858306-580d88e17f57?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwMzY5MDc0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-13) | (time:: 11:07) | (weather:: Vadodara: 🌦   +30°C ↗24km/h)

# [AWS - Serverless beyond Lambda function](https://www.youtube.com/watch?v=nogQV09YDeI)

## [[AWS EventBridge]]

Event Bus - makes it easy to build event-driven apps at scale using events generated from your apps.

cron-jobs has become an event bridge.

![[Screenshot 2022-08-13 at 11.17.59.png]]

## [[AWS StepFunctions]]
- Request Response paradigm
- Can create stateful services using Step Function.
- Pararrel processing possible
- Provides retries, time waits, conditional execution
- The building of a step function is easy - JSON file.

![[Screenshot 2022-08-13 at 11.33.09.png]]

## [[AWS AppSync]]
- Managed GraphQL service.

![[Screenshot 2022-08-13 at 11.42.38.png]]

[[AWS RDS Proxy]]

![[Screenshot 2022-08-13 at 11.51.44.png]]
- Pool and share database connections

## [[AWS Aurora Serverless]]

- On-demand auto-scaling database.
- Use of Data API (v1). No problem with connection pooling.
- Cold start of 30 seconds.
- Best suited for variable workloads.

**Use cases**
- periodic jobs/reports (daily, weekly, monthly)
- Retriable workloads
- Dev Test workloads
- OLTP data stores with variable workload

---
#### Internal Links
[[2022-08-13]], [[AWS]], [[Serverless]] 