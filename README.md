# React useEffect Hook Stale Closure Bug

This repository demonstrates a common error in React's `useEffect` hook: a stale closure caused by an incomplete dependency array.  The `fetch` call inside the `useEffect` hook only runs once on mount because the dependency array is empty (`[]`).  This means that even if the `count` state changes, the `fetch` request is never re-triggered, resulting in unexpected behavior.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the behavior of the counter and note how the data from the API only fetches once.