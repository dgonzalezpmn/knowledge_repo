React

JSX

JSX is a syntax for writing React components.

JSX files must be translated into plain Javascript before they can run in the browser.

Attributes

```
<a href="www.example.com"></a>
```

Rendering

createRoot and render

```
import React from 'react';
import { createRoot } from 'react-dom/client';

<TODO createRoot example>
```

Virtual DOM

Differences between JSX and HTML

class vs className

Curly Braces

Event Listeners

onClick

JSX Conditionals

Keys

React without JSX

React Components

React Dom Library

Function Components

Props

Passing event handlers as props

props.children

```
<TODO add props.children example>
```

Default props

```
function Component(props) {
  return (<div>{props.foobar}</div>);
}

Component.defaultProps = {
  foobar: '123';
};

or

function Component({ foobar = '123' }) {
  return (<div>{foobar}</div>);
}

```

React Developer Tools

Hooks

"React Hooks, plainly put, are functions that let us manage the internal state of components and handle post-rendering side effects directly from our function components. Using Hooks, we can determine what we want to show the users by declaring how our user interface should look based on the state."

Example hooks
- useState()
- useEffect()
- useContext()
- useReducer()
- useRef()

State Hook

```
import React, { useState } from 'react';
```

Returns an array. First item is the current state. Second item is the function to update the state.

```
const [currentState, setCurrentState] = useState();
```

Use callbacks with the set state functions to update state.

```
  setCurrentState((prev) => {

  });
```

Effect Hook

Effect hook sample use cases
- fetch data from a back-end service
- subscribe to a stream of data
- manage timers and intervals
- read from and make changes to the DOM

Effect hook runs in the following scenarios
- When the component is first added, or mounted, to the DOM and renders.
- When the state or props change, causing the component to re-render.
- When the component is removed, or unmounted, from the DOM.

Clean Up Effects

For example, remove event listeners.

```
<Todo: Example of how to clean up effects>
```

Official Documentation

Courses

Last Updated 9/19/24
