# TypeScript: Stack Overflow in Recursive Object Comparison

This repository demonstrates a common error in TypeScript when recursively comparing objects: stack overflow due to circular references.

The `bug.ts` file contains code that attempts to compare two objects recursively. This approach fails when the objects contain circular references, causing a stack overflow error.

The `bugSolution.ts` file shows a corrected version that handles circular references, preventing stack overflow errors.  It uses a `visited` set to track objects that have already been compared, preventing infinite recursion.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `tsc bug.ts` and then `node bug.js` to observe the stack overflow error.
4. Run `tsc bugSolution.ts` and then `node bugSolution.js` to see the corrected behavior.

## Solution

The solution utilizes a `Set` to keep track of visited objects, efficiently avoiding cyclical comparisons.  This prevents infinite recursion and stack overflow errors.  This is a common approach to handle graph traversal problems involving circular references.

This example highlights the importance of considering edge cases, especially when working with recursive functions and complex data structures in TypeScript.