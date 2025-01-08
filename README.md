# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where long-running requests can cause the server to hang, becoming unresponsive to new connections.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The provided server uses a synchronous `while` loop to simulate a long task. This blocks the event loop, preventing the server from accepting or processing other requests.  This results in a unresponsive server.

## Solution

The solution involves using asynchronous operations, such as asynchronous functions or `setTimeout`, to handle long-running tasks. This allows the event loop to remain responsive while the task executes in the background. 