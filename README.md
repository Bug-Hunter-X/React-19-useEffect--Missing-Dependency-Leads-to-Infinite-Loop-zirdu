# React 19 useEffect Dependency Issue

This repository demonstrates a common error in React 19 involving the `useEffect` hook and its dependency array.  Incorrectly omitting a state variable from the dependency array can lead to unexpected behavior, such as infinite rendering loops or stale closures.  This example highlights the problem and provides a solution.

## Problem

The `bug.js` file contains a component that uses `useEffect` to log the current count to the console.  However, the `count` state variable is missing from the dependency array. This means the effect runs after every render, regardless of whether the `count` has changed.  This will lead to excessive logging. 

## Solution

The `bugSolution.js` file demonstrates the correct way to use `useEffect` by adding the `count` to the dependency array. This ensures the effect only runs when the `count` changes, improving performance and preventing unintended side effects.