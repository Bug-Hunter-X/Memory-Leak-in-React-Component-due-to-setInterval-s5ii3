# React Memory Leak: setInterval in useEffect
This repository demonstrates a common mistake in React applications: using setInterval inside a useEffect hook without proper cleanup.  This leads to a memory leak because the interval continues to run even after the component unmounts.

The `bug.js` file contains the faulty code. The `bugSolution.js` provides a corrected version that prevents the memory leak.

## How to Reproduce
1. Clone the repository
2. Navigate to the directory
3. Run `npm install`
4. Run `npm start`
5. Observe the behavior (count will continue to increase even after unmounting the component in the corrected version).

## Solution
The solution involves using the return value of useEffect to clear the interval when the component unmounts, preventing the memory leak.