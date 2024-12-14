# React useEffect Hook: Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: missing dependencies in the dependency array.  This can lead to unexpected behavior and subtle bugs that are difficult to track down. 

The `bug.js` file showcases the problem: an `useEffect` hook that should run after the `count` variable changes. However, because `count` is missing from the dependency array, the effect only runs on the initial render.  This will cause the console log to only execute once. 

The `bugSolution.js` file shows the correct implementation.  By including `count` in the dependency array, the effect is now correctly triggered whenever `count` changes. 

This example highlights the importance of carefully considering which variables to include in the `useEffect` hook's dependency array.  Omitting necessary dependencies is a frequent source of errors in React applications.