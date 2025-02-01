# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook: a missing dependency in the dependency array.  This often leads to unexpected re-renders or infinite loops. 

## The Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count. However, `count` is not included in the dependency array of `useEffect`.  This causes the effect to run after every render, even if `count` hasn't changed, which may lead to performance issues or unexpected side effects.

## The Solution
The `bugSolution.js` file shows the corrected component. By adding `count` to the dependency array, the `useEffect` hook only runs when `count` actually changes, fixing the issue.

## How to reproduce

1. Clone the repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs and the component's behavior in both the buggy and corrected versions.