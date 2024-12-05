# Node.js Server Hang: Blocking Event Loop

This repository demonstrates a common Node.js issue where a long-running synchronous operation in a request handler blocks the event loop, causing the server to hang and become unresponsive. The `bug.js` file contains the problematic code.  The solution, provided in `bugSolution.js`, illustrates how to use asynchronous operations to prevent this issue. 

## How to reproduce the bug:

1. Clone this repository.
2. Run `node bug.js`.
3. Try to access `http://localhost:3000` in your browser.  You'll notice the server becomes unresponsive.

## Solution:

The solution involves refactoring the code to use asynchronous operations and prevent blocking the event loop. The `bugSolution.js` shows the corrected implementation.

## Key takeaway:

Always use asynchronous operations for I/O-bound tasks (like network requests, file system operations, etc.) in Node.js to prevent blocking the event loop and maintain server responsiveness.