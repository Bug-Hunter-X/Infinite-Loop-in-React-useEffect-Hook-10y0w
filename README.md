# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: omitting a necessary dependency from the dependency array. This leads to an infinite loop, as the effect runs repeatedly without a proper condition to stop it.

## Bug Description

The `useEffect` hook in `bug.js` is missing `count` in its dependency array.  Every time the component renders, the effect runs causing another render, and so on.

## Solution

The corrected code in `bugSolution.js` includes `count` in the dependency array. Now the effect only runs when `count` changes, resolving the infinite loop.

## How to reproduce:
1. Clone the repository.
2. Navigate to the directory containing bug.js.
3. Run `npm install`
4. Run `npm start`.
5.Observe the infinite loop in the console and the erratic component behavior.
6.Examine the fix in bugSolution.js.