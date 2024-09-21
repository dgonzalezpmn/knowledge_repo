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

Official Documentation

Courses

Last Updated 9/19/24
