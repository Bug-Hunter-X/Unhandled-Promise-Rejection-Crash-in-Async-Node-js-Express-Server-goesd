# Unhandled Promise Rejection in Async Node.js Express Server

This repository demonstrates a common error in Node.js applications: unhandled promise rejections leading to server crashes.  The `bug.js` file showcases a scenario where an asynchronous operation within an Express.js route handler can throw an uncaught error, resulting in the server's termination.  The solution, provided in `bugSolution.js`, illustrates how to gracefully handle these errors using appropriate error handling mechanisms.

## Problem

The provided `bug.js` code simulates an asynchronous operation (using `setTimeout`) that randomly throws an error.  Since this error is not caught, it results in an unhandled promise rejection, causing the Node.js process to crash.

## Solution

The `bugSolution.js` file corrects this by implementing a `try...catch` block within the asynchronous operation to catch and handle potential errors.  This prevents the application from crashing and allows for more robust error management.  Proper logging also enhances debugging capabilities.