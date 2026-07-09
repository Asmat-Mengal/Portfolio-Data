# Understanding React Hooks: A Comprehensive Guide

React Hooks revolutionized how we write React components. They allow us to use state and other React features without writing class components. Since their introduction in React 16.8, hooks have become the standard way of building React applications.

## What are React Hooks?

Hooks are functions that let you "hook into" React state and lifecycle features from function components. They provide a more direct API to the React concepts you already know: props, state, context, refs, and lifecycle.

### Why Hooks?

Before hooks, you had to use class components for state and lifecycle methods. This led to:
- **Complex components** that were hard to understand
- **Repeated logic** across components (higher-order components, render props)
- **Confusing `this` binding** in classes

Hooks solve these problems by:
- Allowing you to use state without classes
- Making it easier to reuse stateful logic
- Simplifying component structure

## The Basic Hooks

### useState: Managing Local State

The `useState` hook is the most fundamental hook. It lets you add state to function components.

```jsx
import React, { useState } from 'react';

function Counter() {
  // Declare a state variable called "count" and a function to update it
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
