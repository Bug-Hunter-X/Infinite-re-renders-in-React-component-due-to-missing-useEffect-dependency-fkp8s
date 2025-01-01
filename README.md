# Infinite Re-renders in React Component

This repository demonstrates a common React bug: infinite re-renders caused by a missing dependency in the `useEffect` hook.  The `MyComponent` component renders infinitely because the `useEffect` hook is missing the `count` dependency.  This means the effect runs on every render, causing a continuous update cycle.

The solution involves adding `count` to the dependency array, limiting the effect to only run when the value of `count` changes. 

## How to reproduce
1. Clone the repository.
2. Run `npm install`
3. Run `npm start`

Observe the infinite logging in your console.