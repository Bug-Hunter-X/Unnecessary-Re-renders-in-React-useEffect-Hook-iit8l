# Unnecessary Re-renders in React useEffect Hook
This repository demonstrates a common React bug involving inefficient use of the `useEffect` hook. The `useEffect` hook, while powerful, can lead to unnecessary re-renders if not used correctly. This example showcases how to identify and fix this issue.

## Problem:
The provided `MyComponent` re-renders every time due to the `useEffect` hook. The `useEffect` hook is missing its dependency array so React believes it should run every render. This can lead to performance issues, especially in complex components.

## Solution:
The solution includes adding a dependency array to the `useEffect` hook. This ensures that the effect runs only when the value(s) in the dependency array change. In this case, only when the `count` changes.