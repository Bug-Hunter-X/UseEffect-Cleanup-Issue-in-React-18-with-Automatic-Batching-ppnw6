# React 18 useEffect Cleanup Bug
This repository demonstrates a subtle bug related to useEffect cleanup functions in React 18 caused by automatic batching of state updates.  The bug occurs when the cleanup function doesn't properly handle asynchronous operations or doesn't correctly prevent memory leaks.  The solution demonstrates a more robust approach to ensure correct cleanup.

## Bug Description:
In React 18, state updates are automatically batched. If you have a cleanup function in a useEffect hook, this batching can cause unexpected issues if the cleanup isn't designed to handle this behavior.

## How to Reproduce:
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the unexpected behavior. The count may not increment correctly or other issues might arise.

## Solution:
The solution file (`bugSolution.js`) demonstrates a corrected approach.  The cleanup function is carefully crafted to manage potential asynchronous operations and prevents memory leaks.