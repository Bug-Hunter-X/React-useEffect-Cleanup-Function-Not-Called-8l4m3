# React useEffect Cleanup Function Not Called

This repository demonstrates a common error in React involving the useEffect hook's cleanup function not being called.  The issue arises from a missing or incorrect dependency array within the useEffect hook, which can lead to unexpected behavior and performance problems.  The solution provides a corrected version of the code. 

## Problem
The provided `bug.js` file contains a `MyComponent` which uses the `useEffect` hook. The effect is designed to log the current count and clean up resources. However, due to a missing dependency, the cleanup function is not called as expected when the component unmounts.

## Solution
The `bugSolution.js` provides a corrected version of the code with the appropriate dependency array added. This ensures the cleanup function is called when the component unmounts or when the count changes, preventing memory leaks or other issues. This is particularly important when working with asynchronous operations, timers or subscriptions, in which case, the cleanup function ensures these actions are properly disposed of.