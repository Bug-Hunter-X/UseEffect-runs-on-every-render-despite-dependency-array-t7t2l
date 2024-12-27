# React useEffect Bug: Unexpected Rerenders

This repository demonstrates a common issue in React applications where the `useEffect` hook rerenders unexpectedly, even when a dependency array is provided. The bug is related to missing optimization of the dependency array, causing an infinite loop or unexpected behavior.

## Bug Description

The `useEffect` hook is designed to perform side effects after a component renders. It takes a second argument, a dependency array, to specify when the effect should run. However, the following demonstrates a scenario where it runs on every render, even when using a dependency array.

## How to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Observe the console logs, which show the effect running on each render.

## Solution

The solution is to properly handle the dependency array which, in the scenario, correctly using the dependency array to prevent unnecessary re-renders.