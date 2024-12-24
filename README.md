# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by long-running synchronous operations that block the event loop. The `bug.js` file shows a server that hangs for 5 seconds due to busy-waiting, while `bugSolution.js` presents a solution using asynchronous programming to prevent blocking.

## Problem

In Node.js, long-running synchronous operations within the request handler can block the event loop, making the server unresponsive to new requests.  This is demonstrated in `bug.js` where a `while` loop simulates such an operation.

## Solution

The solution, demonstrated in `bugSolution.js`, involves using asynchronous techniques (e.g., `setTimeout`). Asynchronous operations do not block the event loop, allowing the server to remain responsive while performing long tasks.