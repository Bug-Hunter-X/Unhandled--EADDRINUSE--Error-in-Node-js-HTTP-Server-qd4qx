# Unhandled 'EADDRINUSE' Error in Node.js HTTP Server

This repository demonstrates a common error in Node.js when creating an HTTP server: the 'EADDRINUSE' error. This error occurs when the server attempts to bind to a port that is already in use.  The example shows how to improve error handling to gracefully manage this scenario.

## Bug

The `bug.js` file contains a simple HTTP server that attempts to listen on port 8080. If this port is already in use (e.g., by another instance of the server or a different application), the server will crash without proper error handling.

## Solution

The `bugSolution.js` file demonstrates a more robust approach.  It includes an 'error' event listener on the server to catch the 'EADDRINUSE' error and handle it appropriately (e.g., logging the error, trying a different port, or exiting gracefully).