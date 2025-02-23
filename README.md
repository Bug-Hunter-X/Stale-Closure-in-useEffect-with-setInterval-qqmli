# Stale Closure Bug in React's useEffect Hook

This repository demonstrates a common issue in React applications involving stale closures within the `useEffect` hook when used with `setInterval`.  The `count` variable within the `setInterval` callback function doesn't update correctly due to closure over the initial value.

The `bug.js` file shows the problematic code. The `bugSolution.js` provides a corrected version using functional updates to resolve the stale closure issue.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the React development server.
4. Observe the incorrect count updates in the `bug.js` component.  The count might increment inconsistently or not at all.
5. Then switch to the correct example and see it works correctly.

## Solution

The key to fixing this is using a functional update with `setCount`. This ensures that the latest value of `count` is used in each interval tick.