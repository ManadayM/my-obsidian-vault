---
template: note
aliases: [JS:Callback]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1508766229-1a45d4127740?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1NzcwNjk1Ng&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Callbacks in JavaScript
> [!INFO] TL;DR
> The callback is a function (generally IIFE) passed as an argument to the async function. This is a way to be notified when async action is completed.

^7f6cf0

There are certain actions that we initiate now but they finish later. We call them *asynchronous* actions. For example, `setTimeout()` is one such function in [[JavaScript|JavaScript]].

Let's say, we have a function called `loadScript()` as follows that allows us to dynamically download any JavaScript files.

```javascript
function loadScript(src) {
	let script = document.createElement('script');
	script.src = src;
	
	document.head.append(script);
}
```

The browser will immediately start downloading the script when we invoke this function as follows. It will execute the script only after its download gets completed.

```javascript
loadScript('/path/to/myscript.js');
```

Let's say, we want to call the `newFunction()` from this dynamically loaded script file.

```javascript
newFunction();
```

This immediate call to the `newFunction()` after we called the `loadScript()` function would result in an error. We don't have any mechanisms in place that track the download progress and notify us when the browser has downloaded and executed the script in its environment.

We want to be notified when the browser has finished loading the script to safely and confidently use `newFunction()` and other variables from that script. This is where a **callback** function comes into the picture.

Let's add a simple callback function to our `loadScript()` function.

```javascript
function loadScript(src, callback) {
	let script = document.createElement('script');
	script.src = src;
	
	script.onload = () => callback(null, script);
	
	document.head.append(script);
}
```

^72c333

The [[JavaScript - onload & onerror events|JS:onload]] event is a browser event that is called by a browser when it completes the script download and its execution.

Now, we need to pass an anonymous function as a callback function to call the `newFunction()` from the downloaded script.

```javascript
loadScript('/path/to/myscript.js', function() {
	newFunction(); // it works here! 🎉
});
```

The second argument is a callback function that runs when the async action is completed. That's a *callback-based* style of async programming.

The above example only covers the case for successful script loading as here focus was on the callback functions. Check [[JavaScript - onload & onerror events|JS:onerror]] event to handle the script loading errors.

## References
- https://javascript.info/callbacks

---
#### Internal Links
[[2022-07-13]], [[JavaScript - onload & onerror events|JS:onerror]]