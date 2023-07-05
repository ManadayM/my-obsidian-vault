---
template: note
aliases: [Callback Hell,Nested Callbacks,Pyramid of Doom]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1534801189582-810af28d898b?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1Nzc4NDMzNg&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Nested Callbacks
Nested callbacks are aka Pyramid of Doom or Callback Hell in the [[JavaScript|JavaScript]] world. 

Let's understand it by example. Let's say, we have a `loadScript()` function as follows.

![[JavaScript - onload & onerror events#^622b3b]]

Using this, we want to **sequentially** load *script-1.js*, *script-2.js*, and *script-3.js*. 

```javascript
// Example of deeply nested callbacks aka callback hell.

loadScript('script-1.js', function(err, script) {
	if (err) {
		handleError(err);
	}
	else {
		loadScript('script-2.js', function(err, script) {
			if (err) {
				handleError(err);
			}
			else {
				loadScript('script-3.js', function(err, script) {
					if (err) {
						handleError(err);
					}
					else {
						// All scripts are loaded now.. 😅
					}
				});
			}
		});
	}
});
```

This incremental right-side indentation of function calls is known as nested callbacks or callback hell. 

We can alleviate this problem by writing standalone functions as follows.

```javascript
loadScript('script-1.js', step1);

function step1 (err, script) {
	if (!err) {
		loadScript('script-2.js', step2);
	}
	else {
		handleError(err);
	}
}

function step2 (err, script) {
	if (!err) {
		loadScript('script-3.js', step3);
	}
	else {
		handleError(err);
	}
}

function step3 (err, script) {
	if (!err) {
		// All scripts are loaded now.. 😅
	}
	else {
		handleError(err);
	}
}
```

Now, there are no deeply nested calls but this code still requires eye jumps to read between code blocks while reading it.

There is a better way to avoid this pyramid of doom. It is known as [[JavaScript - Promise|Promise]].

## References
- https://javascript.info/callbacks#pyramid-of-doom

---
#### Internal Links
[[2022-07-14]]
