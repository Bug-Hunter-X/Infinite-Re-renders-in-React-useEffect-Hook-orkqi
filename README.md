# Infinite Re-renders in React useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook: infinite re-renders caused by missing dependencies.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

The issue arises when the `useEffect` hook lacks a dependency array, causing it to run after every render, creating an endless loop.  The solution involves correctly specifying the dependencies that trigger the effect.

## How to Reproduce

1. Clone the repository.
2. Navigate to the directory.
3. Run `npm install` or `yarn install` to install dependencies (if any).
4. Run the application (method depends on your setup). You'll observe the console log message repeatedly. 

## Solution

The solution involves adding the `count` variable to the dependency array. This ensures the `useEffect` hook only runs when the `count` changes, preventing the infinite loop.