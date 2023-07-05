---
template: course
progress: 0%
priority: 0
url: https://app.pluralsight.com/library/courses/rxjs-angular-reactive-development/table-of-contents
---
![tp.web.random_picture](https://images.unsplash.com/photo-1598859409649-e261d6af8d2b?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY3NzQ2MzAwNA&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# [RxJS in Angular - Reactive Development](https://app.pluralsight.com/library/courses/rxjs-angular-reactive-development/table-of-contents)

> [!NOTE] RxJS
> RxJS is a library for composing asynchronous and event-based programs by using observable sequences.

> [!NOTE] RxJS
> RxJS is a library for **observing** and **reacting to** data and events by using observable sequences.
> 
> *Deborah Kurata*

## Section 2: Introduction

### 2.1: What is RxJS?
- RxJS stands for **Reactive Extensions for JavaScript** originally developed by Microsoft as Rx.NET.
- RxJS helps us to leverage patterns to collect data from multiple sources, combine data for display, cache data to improve performance, and react to user actions and state changes.
- RxJS is designed to work with asynchronous actions and events though it works with synchronous items.

### 2.2: Why RxJS?
There are other techniques for managing async and event-based data like callbacks.
- It can be difficult to manage async and event-based data with **callbacks** when working with nested async operations.
- A **promise** is an object that may produce a single value sometime in the future. It can handle only single emission and is not cancelable.
- **async/await** is another approach for writing an async code that looks synchronous. It can only handle a single emission and is not cancelable.

Using RxJS has several advantages as follows:
- **One technique to rule them all** - We can use the same techniques for any type of data source like Events from the Keyboard or mouse, and routes and data from arrays, files, databases, or third-party APIs.
- **Compositional** - We can easily compose data for our views using RxJS.
- **Watchful** - RxJS can produce multiple values over time and uses a push model to notify our code when specific actions occur.
- **Lazy** - Evaluation doesn't start until we subscribe.
- **Handle errors** - RxJS has built-in error handling for graceful error handling.
- **Cancellable** - We can cancel async actions with RxJS.

## Section 3: Terms and Syntax
- **Data Streams**: They can be visualized as discreet items on a conveyor belt. They are not continuous like the water in actual streams.
- **Observable**: Observable emits some sort of value over time.
- **Observer**: An observer is a collection of **callbacks** i.e. `next()`, `error()`, `complete()` that knows how to listen to values delivered by the Observable.
- **Subscriber**: A subscriber is basically an observer with additional features to unsubscribe from an observable. Note that subscriber is rarely used except within RxJS. In our code, we normally work with an observer.





## 📚 Linked Notes
```dataview
TABLE file.cday AS Created 
FROM [[RxJS in Angular - Reactive Development]]
WHERE contains(template, "note") 
SORT file.cday ASC
```

---
#### Internal Links
[[Courses]]
