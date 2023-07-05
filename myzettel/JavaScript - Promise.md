---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1503049555010-f8616ee8f0f3?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1NzgwNjkwNg&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# JavaScript - Promise
![[promises-in-javascript 2022-07-14 19.26.34.excalidraw|900]] ^ca08d7

This beautiful famous singer has a huge fan following. The fans constantly ask her for her next album. To get some relief, she promised to update her fans in the future through a subscription list. ^eda582

Now, she can focus on her next album without disappointing her fans. Fans are also happy as they're promised that she'll send them an email update in the future.

Let's apply this analogy in our [[JavaScript|JavaScript]] world.

Here,
- Beautiful Singer is our Producing Code. It needs time to produce something (network calls).
- Fans are our Consuming Code that wants to consume results from the Producing Code as soon as it is ready.
- The subscription list is a promise.

A *promise* is a special JavaScript object that bridges the "Producing code" and "Consumer code". It notifies the subscribers when results are available. ^3d5781

![[promises-in-javascript 2022-07-15 12.26.32.excalidraw|900]]

Let's see two examples.

```javascript
// fulfilled promise example.
let promise = new Promise(function (resolve, reject) {

	// After 1 second, we signal that the job is "done".
	setTimeout( () => resolve('done') , 1000 );
	
	// Promise state: { state: 'fulfilled', value: 'done' }
});
```

```javascript
// rejected promise example.
let promise = new Promise(function (resolve, reject) {

	// After 1 second, we signal that the job has failed.
	setTimeout( () => reject(new Error('Error!')), 1000 );
	
	// Promise state: { state: 'rejected', value: error }
});
```

## Consumers: then, catch

If we go by our singer analogy then the `promise` object acts as a link between the `singer(producer)` and `fans(consumers)`. The `executor` function in the above examples is a producing function. Now, let's see the consuming functions.

### then
```javascript
promise.then(	
	function onResolve(result) { },
	function onError(error) { }
);
```

Here, we can skip the `onError(error)` callback function if we're only interested in the successful completions.

### catch
If we're only interested in intercepting errors, then we have the following two options.

```javascript
promise.then(
	null,
	function onError(error) { }
);
```

```javascript
// catch is a shorthand for promise.then(null, errFunc)
promise.catch(error => alert(error));
```

### finally
The `finally` in promises is used for performing any cleanup. Its callback function has no arguments so we cannot know whether the promise was `fulfilled` or `rejected`.

```javascript
promise
	// runs when the promise is settled doesn't matter successful or not.
	.finally( () => { /* E.g. code to stop loading indicator. */ } )
	.then(
		function onFulfilled(result) { },
		function onError(error) { }
	);
```

## loadScript with Promises

Remember this function with callbacks?

![[JavaScript - onload & onerror events#^622b3b]]

Let's rewrite it using promise.

```javascript
function loadScript(src) {
	return new Promise(function(resolve, reject) {
		
		let script = document.createElement('script');
		script.src = src;
		
		script.onload = () => resolve(script);
		script.onerror = () => reject(new Error(`Error loading: ${src}`));
		
		document.head.append(script);
	});
}

// Usage
let promise = loadScript("https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js");

promise.then(
	function onFulfilled(script) { },
	function onRejected(error) { }
);

// Another handler... In the singer-fan analogy,
// another fan subscribing to receive an update.
// This is called "Promise Chaining".
promise.then((script) => { });
```

We can call `.then` on a Promise as many times as we want. Each time, we’re adding a new “fan”, a new subscribing function, to the “subscription list”. 

## Practice
Write a `delay` function using a promise.

```javascript
function delay(ms) {
	return new Promise(
		(resolve, reject) => setTimeout( () => resolve('done'), ms)
	);
}

// Usage
delay(3000).then(() => alert('Time up!'));
```


## References
- https://javascript.info/promise-basics

---
#### Internal Links
[[2022-07-14]], [[JavaScript]]