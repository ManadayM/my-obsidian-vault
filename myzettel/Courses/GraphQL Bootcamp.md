---
template: course
progress: 0%
priority: 1.0
url: https://www.udemy.com/course/graphql-bootcamp
---
![tp.web.random_picture](https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2NTYzODA2MA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [GraphQL Bootcamp](https://www.udemy.com/course/graphql-bootcamp)

## Section 1: Course Overview
[[2022-10-13]]

### What and why GraphQL?
- GraphQL stands for *Graph Query Language*.
- Operates over HTTP.
- GraphQL creates fast and flexible APIs, giving clients complete control to ask for just the data they need.
- Fewer HTTP requests, flexible data querying, and less code to manage.

## Section 2: GraphQL Basics: Schemas and Queries
[[2022-10-13]]
- The term "Graph" in GraphQL refers to all of the application data and how they relate to each other.
- In a blogging app *User*, *Post*, and *Comment* are data types.
- GraphQL Playground - https://graphql-demo.mead.io/
- There are **3 major operations** in GraphQL APIs - **Query**, **Mutation**, and **Subscription**.
- **All GraphQL APIs are self-documenting in contrast to REST APIs.**
- GraphQL is a specification, not an implementation.
- GraphQL Yoga is an implementation for Node.js.
- Install GraphQL Yoga - ```npm install graphql-yoga```.
- 
```

### Query
```graphql
query {
	hello
	courseInstructor
}
```

The above query returns the following result.
```json
{
	"data": {
		"hello": "Hello world",
		"courseInstructor": "Andrew"
	}
}
```


## 📚 Linked Notes
```dataview
TABLE file.cday AS Created 
FROM [[GraphQL Bootcamp]]
WHERE contains(template, "note") 
SORT file.cday ASC
```

---
#### Internal Links
[[Courses]]
