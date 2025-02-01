# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Express.js applications:  unhandled promise rejections within route handlers.  Asynchronous operations (like database queries, API calls, or file I/O) often use promises.  If these promises reject and the error isn't caught, the application might crash without clear error messages.

The `bug.js` file showcases this issue.  The `someAsyncOperation` function simulates an asynchronous task that can fail. However, the route handler lacks proper error handling, leading to an unhandled rejection.

The solution, provided in `bugSolution.js`, demonstrates how to correctly handle promise rejections using `.catch()` within the route handler.  This prevents the application from crashing and allows for more graceful error management (logging, sending error responses to the client, etc.).