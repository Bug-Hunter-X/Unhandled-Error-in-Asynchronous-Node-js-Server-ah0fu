# Unhandled Error in Asynchronous Node.js Server

This example demonstrates a common error in Node.js: an unhandled error within an asynchronous callback function.  The server crashes without providing any useful information about the error, making debugging difficult. The solution shows how to properly handle errors using try...catch blocks or error listeners for asynchronous operations.

## Bug
The `bug.js` file contains a simple HTTP server that simulates an asynchronous operation.  Half the time, the operation simulates an error, but the error isn't caught, causing the server to crash.

## Solution
The `bugSolution.js` file demonstrates how to correctly handle errors in this scenario.  It uses a try...catch block to handle synchronous errors and adds an error listener to the server to handle asynchronous errors.