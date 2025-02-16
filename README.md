# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and its dependency array.  The improper use of the `useEffect` hook without a dependency array leads to an infinite rendering loop.

## Problem
The provided `MyComponent` uses `useEffect` without a dependency array.  This means that the effect runs after every render, causing the component to constantly update and re-render itself, resulting in an infinite loop.

## Solution
The solution involves adding a dependency array to the `useEffect` hook.  This array specifies the values that the effect should depend on. If none of the values in the dependency array change between renders, the effect will not re-run.  In this case, the dependency array should contain `count`, as the effect only needs to run when `count` changes.