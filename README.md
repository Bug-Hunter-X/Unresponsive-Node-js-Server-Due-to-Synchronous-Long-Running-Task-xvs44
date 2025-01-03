# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler blocks the event loop, making the server unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` shows how to fix it using asynchronous operations.

**Problem:** The server performs a 5-second CPU-bound task synchronously, preventing it from handling other requests during that time.

**Solution:** Refactor the code to use asynchronous operations (e.g., using `setTimeout` or promises), allowing the event loop to continue processing other tasks while the long operation runs in the background.