# React useEffect setInterval Memory Leak

This example demonstrates a common mistake in React: using `setInterval` within a `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

The `bug.js` file shows the incorrect implementation. The `setInterval` continues to run even after the component is unmounted, causing a memory leak. 

The `bugSolution.js` file demonstrates the correct way to implement `setInterval` within `useEffect`, using the return value of `useEffect` to clear the interval when the component unmounts.