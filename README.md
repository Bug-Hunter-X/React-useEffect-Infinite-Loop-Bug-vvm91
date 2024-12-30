# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite rendering loop. The bug arises from the omission of dependencies in the `useEffect` hook, leading to the effect running after every render, thereby creating a continuous cycle.

## Bug Description
The `useEffect` hook is used to perform side effects, such as data fetching or DOM manipulation. However, if no dependency array is provided, the effect runs after every render, which can cause an infinite loop if the effect itself triggers a state update. This is exactly what's happening in the `bug.js` file.

## Bug Solution
The solution involves adding a dependency array to the `useEffect` hook. This dependency array specifies the values the effect depends on. The effect only runs when one of these values changes. In this case, the effect only needs to run when the `count` changes.

## How to Reproduce
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the infinite loop in the browser's console.