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

Calling Effects

If we want to only call our effect after the first render, we pass an empty array to useEffect() as the second argument. This second argument is called the dependency array.

```
```

If we want to call our effect when a specific value changes.

```
useEffect(() => {
  document.title = `You clicked ${count} times`;
}, [count]); // Only re-run the effect if the value stored by count changes
```

Hook Gotchas

There are two main rules to keep in mind when using Hooks:
- Only call Hooks at the top level.
- Only call Hooks from React functions.

Custom Hooks

Container vs Presentational Components

The pattern we’ll learn about focuses on splitting complex components into stateful (container) and stateless (presentational) components, where stateful components manage complex state or logic and stateless components only render JSX.

React Styles

Inline Styles

```
```

Style Object Variables

```
```

StyleSheet Per Component

```
```

className attribute

React Forms

Controlled vs Uncontrolled

There are two terms that will probably come up when you talk about React forms: controlled component and uncontrolled component.

An uncontrolled component is a component that maintains its own internal state. A controlled component is a component that does not maintain any internal state. Since a controlled component has no state, it must be controlled by someone else.

Other Hooks

useCallback

useContext

```
import { createContext, useContext } from 'react';

const ThemeContext = createContext(null);

export default function MyApp() {
  return (
    <ThemeContext.Provider value="dark">
      <Form />
    </ThemeContext.Provider>
  )
}

function Form() {
  return (
    <Panel title="Welcome">
      <Button>Sign up</Button>
      <Button>Log in</Button>
    </Panel>
  );
}

function Panel({ title, children }) {
  const theme = useContext(ThemeContext);
  const className = 'panel-' + theme;
  return (
    <section className={className}>
      <h1>{title}</h1>
      {children}
    </section>
  )
}

function Button({ children }) {
  const theme = useContext(ThemeContext);
  const className = 'button-' + theme;
  return (
    <button className={className}>
      {children}
    </button>
  );
}
```

useMemo

useMemo is a React Hook that lets you cache the result of a calculation between re-renders.

```
const cachedValue = useMemo(calculateValue, dependencies)
```

useReducer

Call useReducer at the top level of your component to manage its state with a reducer.

```
import { useReducer } from 'react';

function reducer(state, action) {
  // ...
}

function MyComponent() {
  const [state, dispatch] = useReducer(reducer, { age: 42 });
  // ...
```

Parameters

- reducer: The reducer function that specifies how the state gets updated. It must be pure, should take the state and action as arguments, and should return the next state. State and action can be of any types.

useRef

useRef is a React Hook that lets you reference a value that’s not needed for rendering.

```
const ref = useRef(initialValue)
```

Official Documentation

Courses

Last Updated 9/19/24
