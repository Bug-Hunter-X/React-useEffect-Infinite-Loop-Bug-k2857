# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## The Bug
The `bug.js` file contains a `MyComponent` that uses the `useState` and `useEffect` hooks. The `useEffect` hook logs the current `count` to the console.  However, because `count` is not included in the dependency array, the effect runs on every render, causing an infinite loop and the console to flood with messages.

## The Solution
The `bugSolution.js` file fixes the issue by adding `count` to the dependency array. Now, the effect only runs when the `count` changes.