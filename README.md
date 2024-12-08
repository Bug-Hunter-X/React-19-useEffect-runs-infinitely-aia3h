# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common bug in React 19 applications where the `useEffect` hook runs after every render, leading to performance problems and unexpected behavior.  The issue stems from missing dependencies in the `useEffect` hook's dependency array.

## Bug Description

The `useEffect` hook in the provided `MyComponent` is intended to log the current count to the console. However, because it lacks a dependency array, it runs on every render. This can cause a performance bottleneck, especially in more complex components, and lead to inaccurate state updates.

## Solution

The solution involves adding the `count` variable to the dependency array of `useEffect` ensuring it runs only when the value of `count` changes.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs and the frequent re-renders.

## How to fix

View the corrected code in `bugSolution.js` for the solution. 
