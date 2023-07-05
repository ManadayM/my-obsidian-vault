---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1524175899813-6135c4645807?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY1NzcxNzMwNg&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# onload & onerror events in JavaScript
We can hook up with `onload` and `onerror` events in [[JavaScript|JavaScript]] to track the loading of external resources.

## onload event

```javascript
function loadScript(src, callback) {
	let script = document.createElement('script');
	script.src = src;
	
	script.onload = () => callback(null, script);
	
	document.head.append(script);
}
```

## onerror event
```javascript
function loadScript(src, callback) {
	let script = document.createElement('script');
	script.src = src;
	
	script.onload = () => callback(null, script);
	
	script.onerror = () => callback(new Error(`Error loading: ${src}`), null);
	
	document.head.append(script);
}
```

^622b3b

> [!IMPORTANT] Scope
> The errors that arose during the script processing or the script execution after its successful downloading of the script file are out of the scope for these events.

## Other Elements
These events can be used for any element that has an external `src`.

```javascript
let img = document.createElement('img');
img.src = '/path/to/image.png';

img.onload = function() {
	alert(`Image loaded, size ${img.width}x${img.height}`);
};

img.onerror = function() {
	alert(`Error loading the image.`);
};
```

---
#### Internal Links
[[2022-07-13]], [[JavaScript]]
