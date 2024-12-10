# React Native Silent Crash on Network Request Failure

This repository demonstrates a common error in React Native applications where network request failures lead to silent crashes due to improper error handling within the `useEffect` hook. The application uses `fetch` to retrieve data and displays it in a `FlatList`. If the network request fails, the application crashes without providing any feedback to the user.

## Problem

The original `DataList.js` component lacks robust error handling. When the `fetch` call fails, the promise rejects, causing the application to crash silently.

## Solution

The solution, implemented in `DataListSolution.js`, properly handles potential errors using a `try...catch` block within the `useEffect` hook.  It sets an `error` state to display a user-friendly error message when the network request fails.