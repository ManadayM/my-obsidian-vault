---
aliases: [js:react:RootAPI,Root API]
---
![tp.web.random_picture](https://images.unsplash.com/photo-1473448912268-2022ce9509d8?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4MDg3NzU0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# React Root API
In [[React.js|ReactJS]], the "root" is a pointer to the top-level data structure. React uses it to track a tree to render. We can render a React element into the DOM with its `render` method.

![[root-api-in-react 2022-07-18 15.24.47.excalidraw|900]]

In the legacy Root API, the root was opaque to the user.
```jsx
import * as ReactDOM from 'react-dom';
import App from './App';

const container = document.getElementById('app');

// Initial render.
ReactDOM.render(<App tab="home" />, container);

// During an update, React would access
// the root of the DOM element.
ReactDOM.render(<App tab="profile" />, container);
```

In the new Root API, the caller creates a root and then calls render on it.
```jsx
import * as ReactDOM from 'react-dom/client';
import App from './App';

const container = document.getElementById('app');

// Create a root.
const root = ReactDOM.createRoot(container);

// Initial render
root.render(<App tab="home" />);

// During an update, there's no need to pass the container again.
root.render(<App tab="profile" />);
```

## Differences
1. Ergonomics of the API - In legacy API you need to pass the container for each render call, even though it never changes.
2. Hydrate - Allows removing `hydrate` method. Need to learn [[hydration-in-react|React Hydration]].

## References
- https://reactjs.org/docs/react-dom-client.html#createroot
- https://github.com/reactwg/react-18/discussions/5