# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook that can lead to an infinite rendering loop.  The issue arises from an improper dependency array, causing the effect to run repeatedly without a change in state. The solution showcases how to properly define dependencies to avoid this problem.

## Bug Description

The `bug.js` file contains a React component that uses the `useEffect` hook.  The effect logs the current count but lacks the `count` variable in the dependency array. This leads to the effect triggering on every render, causing an infinite loop as `setCount` is called within the effect (directly or indirectly).