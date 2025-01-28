# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook. The bug causes an infinite loop due to improper dependency management within the `useEffect` function. The solution showcases a proper way to handle state changes within `useEffect` to prevent this issue.

## Bug Description

The provided `MyComponent` uses `useEffect` to log the current count to the console after every render. However, this creates an infinite loop because the effect itself causes the component to re-render, triggering the effect again, and so on. This leads to continuous logging and potential performance problems.

## Solution

The solution involves correctly specifying the dependency array for the `useEffect` hook.  By only including `count` in the dependency array, the effect will only run when the value of `count` changes.