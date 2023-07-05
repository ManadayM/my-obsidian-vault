---
template: course
progress: 5%
priority: 0.9
url: https://www.udemy.com/course/microservices-with-node-js-and-react/
---
![tp.web.random_picture](https://images.unsplash.com/photo-1448518340475-e3c680e9b4be?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MDc0OTk2OA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [Microservices with Node.js](https://www.udemy.com/course/microservices-with-node-js-and-react/)

## Section 1: Microservices Fundamentals
Lecture 1 - 6: [[2022-08-17]], Lecture 7 - 10: [[2022-08-23]]
- [[Monolith Service|What is a monolith service?]]
- [[Microservice|What is a microservice?]]
- Challenges with Microservices
	- Data management between services is the biggest problem with microservices.
- Communication Strategies - Sync vs. Async
	- The sync strategy makes **direct requests**.
	- The async strategy makes use of **events**.
- A high-level overview of the async communication strategy. This lecture presented a use case of a service that **shows orders made by a particular user**. 
- Pros and Cons of Async communication
	- Data duplication - Not a big issue in present times as storage is cheap now.
	- Hard to understand.

![[Pasted image 20220823121040.png|600]]

## Section 2: A Mini-Microservices App
Lecture 11 - 27: [[2022-08-23]], Lecture 28 - 39: [[2022-08-24]], Lecture 40 - 53: [[2022-08-25]]
[Github Repo](https://github.com/ManadayM/microservices-blog-udemy)
- In this section, we built tiny blogging react app on the front end. It allows creating a post, adding a comment, and viewing a list of comments. We built two small Microservice apps on the back-end - Posts and Comments.
- Understood issues with the initial setup where each Post makes its own request to the Comments service.
- Discussed request minimizing strategies using Sync and Async approaches.
- Explored the Async approach as the Sync approach has many drawbacks and doesn't fit in the definition of Microservice architecture. With the Sync approach, services create interdependencies for their data needs.
- The Async approach introduces an Event Bus and a new Query Service that will listen to events like **PostCreated** and **CommentCreated**.
![[Screenshot 2022-08-24 at 11.29.05.png|500]]
- Understood [[Event Bus]]. We will build our own tiny Event Bus system in the coming lectures using Express.js. It'd look something like this.
![[Screenshot 2022-08-24 at 12.01.37.png|500]]
- Implemented Event Bus service. 
- Modified Comments and Posts Services to send events to the Events Bus service.
- Event Bus service delivers events to all services on the `events` endpoint of each service with a payload as shown in the diagram below.
![[Screenshot 2022-08-24 at 13.22.52.png|500]]
- Implemented Query Service that listens to the `PostCreated` and `CommentCreated` events. It will store the posts with comments in its data store.
- Changed implementation in the client app to request the new `Query Service` instead of making multiple requests to `posts` and `comments` endpoints.
![[Screenshot 2022-08-24 at 14.40.07.png|500]]
- We will introduce a new feature of comment moderation in the next lectures.
![[Screenshot 2022-08-24 at 14.54.59.png|500]]
- Explored 3 different ways to introduce the Comment Moderation feature.
  
	- **Approach - 1:** Waits for Comment Moderation service to moderate the comment content first. However, this approach isn't viable as users won't see anything on the application. If the moderation service is slow due to human intervention or for any other reasons then the delay to moderate a comment can reach unacceptable levels.
	  
	- **Approach - 2:** The other approach could be to show the comment as `Waiting for moderation` when the `Query Service` gets the `CommentCreated` event. This way user gets the immediate feedback that his/her comment has been recorded by the system. 

	  When the `Moderation Service` service *moderates* (approve or reject) the comment, it raises the `CommentModerated` event with a `status` flag. The `Query Service` will update the `status` accordingly.
	  
	  The problem with this approach is `Query Service` requires the domain knowledge of `Comment Service`. If we introduce more features like `CommentUpvoted`, `CommentDownvoted`, `CommentPromoted`, `CommentAnonymized`, etc. then the `Query Service` has to implement those features. 
	  
	  The real purpose of the `Query Service` is to combine different sources to reduce the total number of requests for individual services.
	  
	- **Approach - 3:** The 3<sup>rd</sup> approach is to handle all the domain-specific operations in the `Comment Service` itself. The `Query Service` only listens to the `CommentUpdated` event raised by the `CommentService`. The `Query Service` will just update the existing comment data with the latest one.
	  
- Created a new `Moderation Service` that listens to the `CommentCreated` events. It simply filters the comment for the `orange` word in the comment. It then adds a conditional `status` flag with possible values of `approved` or `rejected`.
- The `Comment Service` listens to the `CommentModerated` event from the Event Bus. It updates the comment with the latest moderation `status`. The `Comment Service` further raises the `CommentUpdated` event intended for the `Query Service`.
- The `Query Service` only subscribes to `CommentUpdated` events from the Event Bus. It finds the comment in question and updates its latest `status` and `content`.
- Updated the `React App` to handle comment moderation states. The app now shows `Awaiting for moderation` for `pending` moderation, `Rejected comment` for `rejected`. We terminated the `Moderation Service` to reproduce the delayed moderation scenario.
- With that test, Stephen introduced a new problem of **Sync Events**. **How do we sync all the events that have happened while the `Moderation Service` was offline?** 
- [Lecture 50] We understood different ways to deal with missing events. The only practical and industry-standard approach is to store all events in an event data store in the order they were generated.
- [Lecture 52] Implemented a simple events data store using an array in the `Event Bus` service. It simply pushes the newly generated event into an array.
- [Lecture 53] Implemented a mechanism to request missing events from the `Event Bus` service when the service starts listening on some port.
  
  To test, we turned off the query service initially. We still were able to create posts but couldn't see them on the app as the `Query Service` was offline. It fetched all the missing events from the `Event Bus Service`.
  
  I implemented similar logic in the `Moderation Service` to handle the scenario of the missing events.

![[Pasted image 20220827110213.png]]
The current state of the app.

Section 2 concludes. 🎉

## Section 3: Running Microservices with Docker


## 📚 Linked Notes
```dataview
TABLE file.cday AS Created 
FROM [[Microservices with Node.js]] AND -"Calendar" AND -"People"
SORT file.cday ASC
```

---
#### Internal Links
[[Courses]], [[Node.js]]
