# React setInterval Memory Leak

This repository demonstrates a common error in React components involving `setInterval` and `useEffect` that can lead to memory leaks.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

## Problem

The `setInterval` function, when used within `useEffect` without proper cleanup, continues to run even after the component unmounts.  This results in the interval accumulating and causing performance problems or memory leaks in the application.

## Solution

The solution involves using a return statement in `useEffect` to call `clearInterval`. This ensures the interval is stopped when the component is unmounted, preventing memory leaks.

## How to Run

1. Clone the repository
2. Navigate to the directory
3. Run `npm install`
4. Run `npm start`