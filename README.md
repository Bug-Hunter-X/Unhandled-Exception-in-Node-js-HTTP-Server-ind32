# Unhandled Exception in Node.js HTTP Server

This repository demonstrates an uncommon error in Node.js where an unhandled exception crashes the HTTP server.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

The issue arises from the lack of proper error handling within the HTTP server's request handler.  An exception thrown within the handler is not caught, leading to server termination.

**How to reproduce:**
1. Clone this repository.
2. Run `node bug.js`.
3. Navigate to `http://localhost:3000/error` in your browser.  You will observe the server crashing.
4. Run `node bugSolution.js`.  The server will now handle the error gracefully and will not crash.

**Solution:**
The solution involves using a `try...catch` block to handle potential exceptions within the request handler. This prevents the server from crashing and allows for more robust error management.