# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running operation in the request handler causes the server to become unresponsive.  The `server.js` file shows the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The `server.js` file contains a `while` loop that simulates a long-running task.  During this time, the server cannot handle any other requests, leading to unresponsiveness.

## Solution

The `serverSolution.js` file demonstrates the correct approach.  Instead of using a blocking `while` loop, it uses asynchronous operations to handle the long-running task without blocking the main thread.  This allows the server to remain responsive even during long operations.